---
layout: post
title: "Proper Rails project start"
tags: [rails, tips, development]
---

1. Switch to Ruby version you want to use
   <pre>
   rvm use 2.1.2
   </pre>
1. Gemset creation and use
   <pre>
   rvm gemset create gemsetname
   rvm use 2.1.2@gemsetname # 2.1.2 - Ruby version
   </pre>
1. Proper Rails version installation
   <pre>
   gem install rails
   </pre>
   or
   <pre>
   gem install rails -v 4.0.1 # 4.0.1 - specific Rails version
   </pre>
1. New project creation with particular database type
   <pre>
   rails new projectname -d postgresql
   </pre>
1. Fixing ruby version in the project folder
   <pre>
   rvm --ruby-version use 2.1.2@gemsetname
   </pre>

### Create and use gemset using one-line command
<pre>
rvm --ruby-version use 2.1.2@gemsetname
</pre>

{% include JB/setup %}