---
layout: post
title: "Using netzkeGetComponent"
tags: [netzke, rails, tips, development, extjs]
---
You can find any netzke component in DOM using Chrome console and netzkeGetComponent command.

Example:
{% highlight js%}
Netzke.page.application.netzkeGetComponent("sandboxes").netzkeGetComponent("import_window").netzkeGetComponent("edit_form").getForm().findField("pack__name").getValue();
{% endhighlight %}

{% include JB/setup %}