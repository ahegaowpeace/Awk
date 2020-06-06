## data1
```
cat data1
hoge 2
moge 3
hoge 5
moge 7
hoge 11
hoge 13
```
```
$ cat data1 | awk '{d[$1]=d[$1]" "$2}END{for(i in d){print i d[i]}}'
hoge 2 5 11 13
moge 3 7
```
