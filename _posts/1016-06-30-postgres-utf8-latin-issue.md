---
layout: post
title: "When struggling with postgresql and utf8/latin"
tags: [postgres, development, tips]
---
<pre>
sudo su postgres
psql
</pre>

<pre>
update pg_database set datistemplate=false where datname='template1';
drop database Template1;
create database template1 with owner=postgres encoding='UTF-8' lc_collate='en_US.utf8' lc_ctype='en_US.utf8' template template0;
update pg_database set datistemplate=true where datname='template1';
</pre>

{% include JB/setup %}