---
title: "REST API Development Best Practices"
layout: post
date: 2018-07-06 15:21:00 -0400
image: /assets/images/markdown.jpg
headerImage: false
tag:
category: blog
author: cherylbrown
description: REST API Best Practices
# jemoji: '<img class="emoji" title=":ramen:" alt=":ramen:" src="https://assets.github.com/images/icons/emoji/unicode/1f35c.png" height="20" width="20" align="absmiddle">'
---
My team is responsible for developing and maintaining two REST API services, one of which handles 7 million API requests per day and has an average response time of 15 milliseconds. The other service averages about 200,000 requests per day and has a 35 millisecond average response time.

We have created a few different iterations of these services while attempting to continually improve them, and along the way I learned a few best practices.

## 0. Get the fundamentals down

There are many fundamentals of REST API development such as using SSL, using HTTP methods properly, using appropriate error codes, and so on, that should always be your top priority. There are many articles that cover these in [greater](https://www.vinaysahni.com/best-practices-for-a-pragmatic-restful-api#restful) [detail](https://hackernoon.com/restful-api-designing-guidelines-the-best-practices-60e1d954e7c9).

But, as your development continues, I find these practices to be particularly helpful...

## 1. Version from the start

If we know one thing about life (and software), it is that *it changes*. New things come along, and old things go away. The "old things go away" part is tricky when it comes to REST APIs. If a consumer is using your API, and you need to remove or rename a critical field they depend upon, you will break them.

The best way to handle this situation is to create the next version of your API, remove or rename the field in the new version, deprecate the previous one, and give your consumers a time frame to migrate.

Versioning an API simply means putting a version number before the endpoint. For example, let's say I am building an API for a film website:

{% highlight javascript %}
GET https://www.hostname.com/api/films // No version :(

GET https://www.hostname.com/api/v1/films // Fixed :)
{% endhighlight %}

## 2. Paginate from the start

Ok, so you just started developing your REST API and you have a way to bulk dump all the data, but you told everyone to please just query for a subset of data at a time, so you're good, right?

Wrong! The best way to kill the performance of your API is to assume that consumers will be nice and play by the rules. If they can get the data in one shot, they will.

Unfortunately, this means you will be dealing with a lot of performance issues that essentially can not be solved, because sending all the data at once is never a performant solution. Not that I have seen in practice, that is!

You can include an object with the paging information in each response, as shown below, or you can use the [Link header](https://tools.ietf.org/html/rfc5988).

{% highlight javascript %}
GET https://www.hostname.com/api/v1/films
Authorization: Basic asdf
Accept: application/json

Response:

{
    pages: {
        current: https://www.hostname.com/api/v1/films?page=1,
        first: https://www.hostname.com/api/v1/films?page=1,
        next: https://www.hostname.com/api/v1/films?page=2,
        last: https://www.hostname.com/api/v1/films?page=10
    },
    data: [
        // array of films here
    ]
}
{% endhighlight %}

## 3. Only expose the data that is needed

If you expose every field in your database right from the start, consumers will find ways to become reliant on all that data. As time goes on and your database grows, this is another sure way to kill the performance of your API. In general, the bigger the response body, the slower your response time will be.

To solve this, be very selective about which fields to expose and only send back that absolute minimum amount of fields that are needed. Going back to #1 above, remember that it's easy to add more fields if needed, but it is very hard to remove them.

## 4. Continually monitor and improve performance

We assess the performance of our APIs every day and monitor for blips in performance, higher than usual error rates, unauthorized use, thread crashes, and anything else that might be outside of the norm. We are also on call should the API go down or performance degrades to an unacceptable level. This way, we are always in a proactive state and can often fix performance issues before they ever become noticeable to our consumers. This has been critical in our effort to keep our API highly avaialable and performant.
