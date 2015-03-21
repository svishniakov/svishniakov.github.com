---
layout: post
title: "Bootstrap flash messages"
tags: [rails, bootstrap]
---
First of all ApplicationHelper should be modified

{% highlight ruby linenos %}

module ApplicationHelper

  def bootstrap_class_for flash_type
    { success: "alert-success", error: "alert-danger", alert: "alert-warning", notice: "alert-info" }[flash_type.to_sym] || flash_type.to_s
  end

  def flash_messages(opts = {})
    flash.each do |msg_type, message|
      concat(content_tag(:div, message, class: "alert #{bootstrap_class_for(msg_type)} fade in") do
               concat content_tag(:button, 'x', class: "close", data: { dismiss: 'alert' })
               concat message
             end)
    end
    nil
  end
end
{% endhighlight %}

Application layout

{% highlight ruby %}
<%= flash_messages %>
{% endhighlight %}

{% include JB/setup %}
