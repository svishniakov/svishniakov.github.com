---
layout: post
title: "How to delete particular Model name with migration"
tags: [rails, tips, development]
---
1. Create model with
   <pre>
   rails g ModelName
   </pre>
1. Migrate with
   <pre>
   rake db:migrate
   </pre>
1. Run rake task
   <pre>
   rake db:migrate:down VERSION=20130417185845 # where 20130417185845 is migration version
   </pre>
1. Delete model with
   <pre>
   rails d model ModelName
   </pre>

{% include JB/setup %}