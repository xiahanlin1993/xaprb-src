---
title: Maatkit version 1314 released
date: "2007-11-26"
url: /blog/2007/11/26/maatkit-version-1314-released/
categories:
  - Databases
  - Open Source
---

[Maatkit](http://code.google.com/p/maatkit/) (formerly MySQL Toolkit) contains essential command-line utilities for MySQL, such as a table checksum tool and query profiler. It provides missing features such as checking replicas for data consistency, with emphasis on quality and scriptability.

This release fixes several minor bugs. It also renames all the tools to avoid trademark violation, completing the project rename. (Let me know if I missed anything.)

```
Changelog for mk-find:

2007-11-25: version 0.9.7

   * Added --sid option.

Changelog for mk-show-grants:

2007-11-25: version 1.0.5

  * --askpass ignored the entered password (bug #1838131).

Changelog for mk-table-checksum:

2007-11-25: version 1.1.20

   * --replcheck didn't recurse; it should recurse one level (to replicas).
```


