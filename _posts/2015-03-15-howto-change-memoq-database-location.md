---
layout: post
title: "How to move memoQ base to another place"
tags: [localization, memoQ, tips]
---
1. Download and install MS SQL Management Studio 2008 using this [tutorial](http://blogs.msdn.com/b/bethmassi/archive/2011/02/18/step-by-step-installing-sql-server-management-studio-2008-express-after-visual-studio-2010.aspx){:target="_blank"}
1. Detach DB using MS SQL Management Studio
1. Move data folder to another place
1. Attach DB using MS SQL Management Studio
1. Edit **Configuration.xml** located at C:\ProgramData\memoQ Server\
1. Start memoQ server

{% include JB/setup %}