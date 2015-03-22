---
layout: post
title: ".gitignore_global"
tags: [git, development, tips]
---
You can create a global .gitignore file, which is a list of rules for ignoring files in every Git repositories on your computer. For example, you might create the file at ~/.gitignore_global and add some rules to it.

Run the following command in your terminal:

<pre>
git config --global core.excludesfile ~/.gitignore_global
</pre>

### Some common .gitignore configurations

<pre>
# Compiled source
####################
*.com
*.class
*.dll
*.exe
*.o
*.so

# Packages
#############
# it's better to unpack these files and commit the raw source
# git has its own built in compression methods
*.7z
*.dmg
*.gz
*.iso
*.jar
*.rar
*.tar
*.zip

# Logs and databases
#######################
*.log
*.sql
*.sqlite

# IDE generated files
#######################
.idea

# OS generated files
#######################
.DS_Store
.DS_Store?
._*
.Spotlight-V100
.Trashes
ehthumbs.db
Thumbs.db

</pre>

{% include JB/setup%}