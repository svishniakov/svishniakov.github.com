---
layout: post
title: "Useful RegExp tricks"
tags: [regexp, tips]
---

Trivial approach to find all the HTML tags using RegExp:

<pre>
<[^>]*>
</pre>

======

The **dot** matches all except newlines (\r\n). We need to use \s\S, which will match ALL characters.

{% include JB/setup %}