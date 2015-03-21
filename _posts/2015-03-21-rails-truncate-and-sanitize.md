---
layout: post
published: true
tags: rails
---
Dealing with sanitize helpers and truncation can be tricky. There are a lot of different sanitize helpers: h, CGI::escapeHTML, sanitize, strip_tags, html_safe, etc. Sanitization and truncation do not work well together if a string is truncated between an opening and a closing tag or right in the middle of a special HTML character.The following statement seems to work

<code>
  sanitize(text, :tags=>[]).truncate(30, :separator => " ").html_safe
</code>

The trick is to a pass a :separator option to truncate text at a natural break.