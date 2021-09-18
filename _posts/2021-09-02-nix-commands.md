---
name: nix commands
layout: post
title: nix command cheatsheet
---

```
cat contacts.csv | awk -F',' '{print $1}' | awk '{print substr($0,0,1);}' | awk '{for (i=1; i<=NF; i++){a[$i]++}}END{for (i in a){print i, a[i]}}' | sort -nr -k 2
```

```
sort -nr -k
```