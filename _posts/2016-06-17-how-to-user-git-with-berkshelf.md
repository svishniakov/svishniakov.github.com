---
layout: post
title: "Proper Rails project start"
tags: [chef, tips, deployment, berkshelf]
---

1. If you need to use custom git URL(to your private repo) with Berkshelf the following syntax needs to be used:
   <pre>
   cookbook 'thing', git: 'git@github.com:company/cookbook.git'
   </pre>

{% include JB/setup %}