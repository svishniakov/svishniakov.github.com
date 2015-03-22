---
layout: post
title: "How to migrate databases in production environment"
tags: [rails, tips, deploy, production]
---
{% highlight ruby %}
rake db:migrate RAILS_ENV="production"
{% endhighlight %}

{% include JB/setup %}