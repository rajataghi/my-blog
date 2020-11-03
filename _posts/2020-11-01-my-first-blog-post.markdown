---
layout: post
title:  "My First Blog Post"
date:   2020-11-01 23:09:18 -0500
categories: No Code
---

This is my first blog post. Today, I found a subreddit which has deals on various parts [required to build a pc][reddit-buildapcsales]. Surprisingly, it also has deals on pc-setup peripherals like chairs and tables. All post titles seem to have a title in their category name (ssd, mouse, chair etc.). I'll try to build a parser that can segregate the posts by category, making it easier for myself to keep track of things I am interested in. I plan to keep this blog as a live document, updating it along the way as a way to track my progress and keep me motivated to do this. Excited to get started tomorrow!

### Day 1
I started looking into the reddit API to see how I can parse through all of the submissions on a subreddit. Found the official documentation to be very underwhelming. I did find this  wrapper on the API, [pushshift][push-shift-api], which can help me get what I need. Seems like I need to make a single GET request to this wrapper and it will return a list of json objects that I can then parse.

#### Deciding what framework and language to use
I've been using Java spring boot at work recently, so I am most fluent in that at the moment but that seems like a bit of overkill for this app. I think I will use react for this though. I learnt that recently but never really built anything with it(except for the demo application in the [coursework][scrimba-react]). If I do only front-end though, I will have query and parse the api on every page load. I don't think this subreddit gets that many submissions to warrant such frequent updates. I could make a small backend in python that pre-processes new posts everyday and then my front-end can just query this backend without having to parse and pre-packaged data. Maybe there is a way to do this pre-packaging in react for at least distinct user sessions? Not sure, but for now, I'll let it be only front-end. 

If its too slow, I can think about having a backend. So **react** it is!

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
[reddit-buildapcsales]: https://www.reddit.com/r/buildapcsales
[push-shift-api]: https://github.com/pushshift/api
[scrimba-react]: https://scrimba.com/learn/learnreact