---
layout: post
title: "Delayed Jobs restart"
tags: [rails, tips, production]
---
To restart multiple delayed_job workers:

<pre>
RAILS_ENV=production script/delayed_job -n4 restart
</pre>

{% include JB/setup %}