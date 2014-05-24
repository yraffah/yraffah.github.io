---
  title: Varnishing
  category: technology
  tags:
    - tech
    - development
    - mac os x
    - nginx
    - varnish
  layout: post
  description: I managed to install and configure **nginx** for the first time ever on my home computer. What is nginx and why not **Apache** is a long story but Apache is resource hungry and I do have limited resources on this machine. On the other hand, **nginx** is resource friendly, i.e. it uses much less resources than Apache does. Plus, I wanted to learn something new :).
---

### nginx ###

I managed to install and configure **[nginx](http://nginx.net/ "nginx website")** for the first time ever on my home computer. What is nginx and why not **[Apache](http://httpd.apache.org "Apache's website")** is a long story but Apache is resource hungry and I do have limite resources on this machine. On the other hand, nginx is resource friendly, i.e. it uses much less resources than Apache does. Plus, I wanted to learn something new :).
***

### Varnish ###

Since I don't have enough resources on this machine, I decided to reduce the webserver load even further by utilizing and using a cache. A cache engine basically stores the static content of your webserver in order to reduce the load on the backend (your webserver) and have faster loads for visitors since the content is served from the memory or disk (depending on the used cache).
***

#### So what is Varnish? ####

[Varnish](https://www.varnish-cache.org/ "Varnish Cache") is the caching engine I used on this machine. Yes, it was something new to me and I wanted to learn it. Installing and configuring it was straight forward and simple especially with [Macports](http://www.macports.org "Macports"), which is how I installed it.
***

### Writing a tutorial ###
I might share with you later how I did my setup and what kind of configuration I used for it, so lookout for something here later down the line.
