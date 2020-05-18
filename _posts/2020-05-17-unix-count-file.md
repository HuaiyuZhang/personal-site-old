---
layout: post
title: Unix How To--Count the number of files
---

## Count the files with specific patterned names

John has a folder called `results` within which are the simulation results returned from the computation on the cluster. He'd like to know how many of them start with letter `GroupA`.

Easy job. 

```
ls -l GroupA* | wc -l
```

## Count the files with certain time criteria

Shawn is facing a folder with 1000 trasaction record files. The file time shows the transaction day. He'd like to know the number of transactions in the most recent 30 days.

Not that hard.

```
find . -type f -ctime -30 -print | wc -l
```

`-type f` is for regular file.

`-ctime -30` File's status was last changed less than 30*24 hours ago.
