---
layout: post
title: "Blog post #2"
date: 2013-10-09 18:50
comments: true
categories: 
---
my second blog post

To make this post using octopress, I first loaded my octopress directory.
```
cd ~/workspace/octopress
```

Then I created a new post with the command
```
rake new_post["Blog post #2"]
```
I opened the blog post in RubyMine with iterm by giving the command
```
mine .
```
I then ran the rake commands to generate and preview the post:
```
rake generate
rake watch
rake preview
```
This allowed me to load and preview my post on my local server with the address
"http:\\localhost:4000"

The next step was to rerun rake generate (I don't know if this step is necessary)

```
rake generate
```
Finally, I ran rake deploy to load this post to my github repository.

```
rake deploy
```
