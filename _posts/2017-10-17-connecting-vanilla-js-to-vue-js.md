---
layout: default
title: "Connecting Vue and JS"
excerpt_separator: <!--more-->
---

<div class="card">
  <div class="card-block">
    Connecting two technologies
  </div>
</div>

<!--more-->


<p class="blog-text">Today we revisited some of the more fundamental aspects of vue js by comparing them to their vanilla js counterpart. Specifically we worked together as a class to recreate tic-tac-toe which we previously did in regular javascript as the same app but this time using vue. Not only did we work through it as a class but... I got to type the dang thing in front of the class. So yeah it was hands on.</p> 

<p class="blog-text">But despite being nerve-wracking it was actually very helpful. Like... super helpful. Heres some things I got from the session:</p>

<p class="blog-text"> * in vue components, 'data' is treated like a function and has to have a return statement.</p> 

```
data: function(){
	return // all your stuff
}
```


```
<div v-if="statement" ...>
```

<p class="blog-text">this will show or not show an element (like a div) if the "statement" is not true


the $emit statement ---> this.$emit('new'); is a way that vue can let the "child" component tell the parent something, but the parent also has to listen with an on: statement ---> v-on:new="newClick"
<br>

so it looks something like this:
<br>

child:
```
this.$emit('new');
```
parent:</p>
```
<div v-on:new="newClick" // where the "newClick" is a function that is called
```

