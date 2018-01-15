---
layout: posts
title: "LAMP stack"
---

Jan - 15, 2018


Recently I was lucky enough to get a call back from a job I applied for and a request for an interview. The company is a large online retailer that is seeking junior level developers and uses a technology stack called LAMP. As of about a week ago I had no idea even what LAMP was - but I was sure I could at least gain a cursory understanding for the interview. So this blog post is to document my findings over the past week of research into this new technology. 

So let’s start with a definition. LAMP stands is an acronym for Linux-Apache-MySQL-PHP. These are four technologies that work in conert to create what is called a “stack” or development environment. 

----

#### L - _Linux_
Linux is the operating system that it is built upon. This is honestly the least important technology for me at the moment because there are identical stacks available on Mac Os and Windows (WAMP, XAMP). But I’ll also take it as a boon that I exclusively use UBUNTU (Linux) for development as it is. So… go me. 

#### A - _Apache Web Server_
Apache is a server technology for local development. This works hand in hand with PHP (the P in LAMP), since PHP is a server side language and requires a server to operate. In my prior experience with PHP I used the built in server that came equipped with Laravel (PHP Artisan Serve). Apache (I think) comes from an era when you actually had to go FIND a server to run your PHP on. Current versions of PHP (I use 5.6 but it goes up to 7.1 for bleeding edge) come with a super convenient server built in. But, earlier days of PHP did not have such conveniences. Anyhow Apache is a convenient local development server for the PHP language. 

#### M - _MySQL_
MySQL is the database technology utilized in the LAMP stack. Turns out that MySQL is the most widely used relational database management system (RDBMS) utilized on the internet. The syntax is very similar to the technology I have used previously, PostgreSQL, so the learning curve was pretty fast. I’ve mostly used the terminal with MySQL but there also exists a handy GUI called PHPmyAdmin. 

#### P - _PHP_
PHP is the serverside scripting language used in this stack. Again an incredibly popular language used by some of the web giants - Facebook, Wikipedia, Flikr, Tumblr. This language is most well suited for programatically running your MySQL code, allowing for the user to manipulate the database without having to write any code. That’s good, because I can’t imagine any normal person wanting to write out MySQL inserts to save their name and email address. 

One of the most interesting discoveries I’ve made in this past week of research on the LAMP stack was finding c9 or Cloud 9. Cloud 9 is a company that hosts prepackaged development environments available in “the cloud.” In other words, you sign up for an account and just tell them what stack you would like to use and then… boom. You have an IDE (integrated development environment), and then in my case I was given access to an emulated: Linux terminal, MySQL database, Apache web server and PHP… and heres the kicker - It’s all preconfigured and works. What!!! The first two days of this research project were spent on me trying to make all these technologies play nice together on my current dev environment on my Ubuntu laptop. With c9 - I was up and running in less than 15 minutes. That was a real game changer. 

So the takeaway from this experiment is that a LAMP stack (or XAMP or WAMP) is essentially the precursor to more modern (and more complete) technologies such as Laravel and Django. However, as a junior level developer it’s important for me to understand things without all the bells and whistles of modern prepackaged environments. This is a great technology for me to develop in - especially since I am new. I have to configure all the database connections manually, which is a huge pain in the butt since Laravel did that for you, but that’s why I am here - to learn. 

References:

[LAMP Wikipedia](https://en.wikipedia.org/wiki/LAMP_(software_bundle))
['<img src="https://www.unixmen.com/wp-content/uploads/2017/05/lamp_stack.jpg">'](https://en.wikipedia.org/wiki/LAMP_(software_bundle))