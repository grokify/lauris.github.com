---
layout: post
title: "Glip Inbound Webhook SDKs"
category: software
permalink: /glip-inbound-webhook-sdks
---

I recently put together two SDKs to wrap [Glip](https://glip.com)'s inbound webhooks when there's a desire to have data from other sites integrated into Glip alerts. The SDKs are in Ruby and Swift. I originally built the library in Ruby since this is one of go to languages for quick prototyping, however, after learning that many chat users may not be developers with the means to run their own servers, I looked into rewriting this as a Google App and a Swift iOS app. After a security issue using another library with the Google App, I settled on Swift and pushed that out as well.

<!-- more -->

## Ruby SDK - Overview

The Ruby SDK, [`Glip::Poster`](https://github.com/grokify/glip-poster-ruby) is designed to have the same interface as other `*::Poster` chat SDKs making them interchangeable. It provides an easy to use interface supporting webhook options on a per-message basis and as part of the defaults.

{% highlight bash %}
require 'glip_poster'

poster = Glip::Poster.new(YOUR_WEBHOOK_URL)
poster.options[:icon] = 'http://example.com/icon.png'
poster.send_message('Hi there!')
{% endhighlight %}

As mentioned above, while Ruby is nice and used by many people, setting up a service to transform event data to Glip's inbound webhook format requires standing up a server permanently which may not be attractive or possible given the circumstances.

## Swift SDK - Overview

When thinking of alternative approaches, the thought of creating a Chrome App and an iOS App both came up. When the iOS app was the only viable choice, the [Glip Swift SDK](https://github.com/grokify/glip-sdk-swift) was born.

{% highlight ruby %}
glip = Poster(YOUR_WEBHOOK_URL, icon: "http://example.com/icon.png")
glip.sendMessage("Hi there!")
{% endhighlight %}

## SMS to Glip Webhook Example

In addition to the SDK libraries themselves, the Ruby SDK includes a sample script)[] which runs and demonstrates this in action. As part of the solution, the script subscribes to all inbound extensions and will send an alert to the chat system of choice for new alerts.

## Summary ##

Although the Glip Inbound Webhook format is simple, create an easy to use SDK is still very helpful. If you have an interest in using Glip, please try out these SDKs and provide more shelter.
