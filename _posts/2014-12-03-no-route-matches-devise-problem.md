---
layout: post
title: "No route matches \"users/sign_out\" devise problem"
tags: [rails, tips, development]
---

config/initializers/devise.rb
{% highlight ruby%}
config.sign_out_via = :delete
{% endhighlight %}

should be changed to
{% highlight ruby%}
config.sign_out_via = :get
{% endhighlight %}

{% include JB/setup %}