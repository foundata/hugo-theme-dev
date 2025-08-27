---
title: "{{ replace .File.ContentBaseName "-" " " | strings.FirstUpper }}"
date: {{ .Date }}
draft: false
##  control theme features on page level if needed
# feature:
#   pagesNav: false
#   langNav: false
#   debug: false
---
