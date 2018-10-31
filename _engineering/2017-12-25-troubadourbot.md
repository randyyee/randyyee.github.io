---
layout: post
title: "Troubadour (Poetry Twitter Bot)"
---
A little code to make a Twitter bot that tweets lines of William Wordsworth's <i>Lyrical Ballads</i>).

Info:
This project is written in Python 3 and makes use of the Tweepy (a python library for accessing the Twitter api). It seems that everyone is using this handy library for there own Twitter projects. More information can be found [here](www.tweepy.org).

Setup was relatively simple:
1. Make a Twitter account
2. Go to https://apps.twitter.com/apps to notify Twitter that I intended to create an app. Follow the steps (should only take a minute or so), and get your consumer key and secret code as well as you access key and secret code.
3. Find a body of text to tweet - <i>Lyrical Ballads</i> from Project Gutenberg.
4. Customize code below.

{% highlight python %}
# -*- coding: utf-8 -*-
import tweepy, time

#Twitter credentials
CONSUMER_KEY = 'xxxxx' #replace
CONSUMER_SECRET = 'xxxxx' #replace
ACCESS_KEY = 'xxxxx' #replace
ACCESS_SECRET = 'xxxxx' #replace
auth = tweepy.OAuthHandler(CONSUMER_KEY, CONSUMER_SECRET)
auth.set_access_token(ACCESS_KEY, ACCESS_SECRET)
api = tweepy.API(auth)

filename = open('lyricalballads.txt','r')
content = filename.readlines()
filename.close()

for line in content:
    if line=="\n": #don't tweet an empty line
        continue
    else:
        try:
            api.update_status(line)
            print(line)
            time.sleep(10)
        except:
            continue
{% endhighlight %}

On second thought, tweeting line-by-line might not have been the best idea as longer poems got more and more confusing. However, this would be a great bot for a shorter poetry such as koans or haikus - in which case the code can even be modified to get the entire poem with an appropriate loop.
