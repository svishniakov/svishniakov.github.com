---
layout: post
title: "How to run simple PHP server on your PC"
tags: [development, tips]
---
PHP 5.4 has a built-in web-server. Command to launch it:

{% highlight php %}
php [options] -S <addr>:<port> [-t docroot]
{% endhighlight %}

# Example to launch it from the project root folder:

{% highlight php %}
php -S localhost:8000 -t .
{% endhighlight %}

{% include JB/setup %}