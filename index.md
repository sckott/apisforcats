---
title: "Home"
layout: default
---





## An intro to APIs for R users

This is an introduction to working with APIs in R. We promise this will be fun. 

This introduction assumes basic knowledge of the R language. If you need to get that
check out <https://rforcats.net>.

## Table of contents

* [Let's get our paws dirty first](#dirty)
* [Definitions](#definitions)
* [Server-Client](#serverclient)
* [URLs](#urls)
* [Install things](#install)
* [Your first GET request](#get)
* [Status codes](#statuscodes)
* [Reading](#reading)
* [Want this page to be better?](#makeitbetter)

## <a href="#dirty" name="dirty">#</a> Get dirty

Here, we'll just use a web browser - since you're reading this in a browser, this
should be doable for every cat!  

First, let's have some fun with cat pics. Head over to <https://http.cat/> in your 
favorite browser. This API give back a different cat image for each of the HTTP 
status codes (you may not be familiar with this, [read below](#statuscodes)). 

Try <https://http.cat/200>

That's for a `200` HTTP status code, which means a successful request!

Now try <https://http.cat/500>

The `500` HTTP status code means something went wrong on the server. Oh no!

-----

Next, let's try an API that gives back text. 

<https://catfact.ninja/fact>

Click on the above link or paste it into another tab. You should be back something like:

```json
{
    "fact": "Cat's urine glows under a black light.",
    "length": 38
}
```

That text based data is called JSON. Read about it in the next section.


## <a href="#definitions" name="definitions">#</a> Definitions

* API: 
* URL: 
* HTTP: 
* JSON: 
* Server:
* Client: 


## <a href="#serverclient" name="serverclient">#</a> Server-Client

With any API you work with you there is an interaction between a server
and a client.

A server is most often running on the cloud (e.g. [Amazon][aws], [DigitalOcean][do]) and 
has a set of code for handling how to react to requests. 

A client is any entity making requests to the server. A client can be a 
browser (desktop or mobile), a command line utility like [curl][], or a 
R program.


## <a href="#urls" name="urls">#</a> URLs

URLs are the most fundamental part of working with APIs. Every API you'll work with is 
found at some URL. 

Let's go over the structure of a URL. A URL is made up of the following parts:

- scheme: `http` or `https`
- base: includes domain e.g. "cats.com"
- path: any number of paths after the base, separated by `/`, e.g., `/cat/kitty`
- query parameters: key-value pairs after a `?`, e.g., `?query=tilapia`

The former two are mandatory: You need a scheme and base. The latter two - path and 
query parameters - are optional. 

To put it all together:

```
URL = scheme + base + path + query parameters
```

For example:

```
https://http.cat/404 = scheme (https) + base (http.cat) + path (404)
```

The neat thing about URLs is that you can often pop them into your favorite web 
browser and test them out.


## <a href="#install" name="install">#</a> Install


```r
install.packages("crul")
```

## <a href="#get" name="get">#</a> Your first GET request


```r
connection <- crul::HttpClient$new(url = "https://catfact.ninja")
result <- connection$get('fact')
result$parse("UTF-8")
```

```
#> [1] "{\"fact\":\"The biggest wildcat today is the Siberian Tiger. It can be more than 12 feet (3.6 m) long (about the size of a small car) and weigh up to 700 pounds (317 kg).\",\"length\":158}"
```

## <a href="#statuscodes" name="statuscodes">#</a> Status codes

xxx

## <a href="#reading" name="reading">#</a> Reading

xxxx

## <a href="#makeitbetter" name="makeitbetter">#</a> Make it better

Contribute by following [these instructions](/Contribute).

## <a href="#license" name="license">#</a> License

[aws]: https://aws.amazon.com/
[do]: https://www.digitalocean.com/
[curl]: https://curl.haxx.se/
