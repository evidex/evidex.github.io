---
layout: post
title: "Getting to Philosophy"
description: ""
category: coding
tags: [python, projects]
---
{% include JB/setup %}

For quite a while, I've loved playing the Wikipedia Philosophy game, which I first learned about over at [XKCD](http://xkcd.com/903/). Essentially, from a pretty much any Wikipedia page, you can eventually return to Philosophy, by clicking the first non-italicized link which isn't in parentheses.

[According to Wikipedia](http://en.wikipedia.org/wiki/Wikipedia:Getting_to_Philosophy) this works for about 95% of Wikipedia pages. For the fun, I decided to write a Python script, which would select a bunch of random pages, and attempt to travel to Philosophy. 

The script uses the fantastic [Python Requests](http://docs.python-requests.org/en/latest/) module, along with [BeautifulSoup4](http://www.crummy.com/software/BeautifulSoup/) to request and parse Wikipedia pages. The project is a fork of [David Muller's getting_to_philosophy](https://github.com/DavidMuller/getting_to_philsophy), allowing me to re-use his code for correctly parsing the first non-italicized link from the raw HTML.

Once the script has played the game a number of times, it generates a nice tree of the Wikipedia pages it's visited, along with some basic statistics. Below is an example for 5 random pages, and [here]({{ site.url }}/assets/images/get_to_philosophy/random_to_philosophy_100.png)(~4Mb PNG) you can see the massive tree for 100 pages.

Naturally, the code for all of this can be found on [Github](https://github.com/evidex/getting_to_philsophy).

![Random 5]({{ site.url  }}/assets/images/get_to_philosophy/random_5.png)
