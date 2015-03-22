---
layout: post
title: "Postgres + Netzke case sensitive search issue"
tags: [netzke, rails, postgres, tips]
---
In case you need to provide case sensitive search feature in your Netzke application using LiveSearch plugin.

Columns has to be defined within component using **LIKE** operand. Netzke is using ILIKE by default

{% include JB/setup %}