---
layout: default
title: "A new friend - github."
---
# A new friend - github.

So of the new technologies that I'm learning at bootcamp, github has to be the coolest. So far at least. Well technically it's "git" thats the actual software, but github is the place I keep going to. So heres how I understand it: git is what is called version control and it helps programmers to keep track of collaborative work. Theres a central repository (github) that all the collaboraters work from, and there are a whole set of rules that regulate what people can and can't do to the code. The rules keep the code safe. So people can't just put whatever craziness in there and ruin other people's work. 

Mostly it's cool because it makes it way easier to keep track of files. If you mess up your files locally, you can just pull down a fresh copy of code and go nuts. It's a bit daunting - mostly cause it's all CLI (command line interface), but it's something I have been using pretty much 8 hours a day every day so I'm getting the hang of it. Almost like learning a new Point of sale at a new job. It's going to click and I'll stop worrying as much about the details. 

{% for post in site.posts %}
      
        <a href="{{ post.url }}">{{ post.title }}</a>
        |
      
    {% endfor %}