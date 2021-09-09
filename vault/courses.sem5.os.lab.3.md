---
id: sX5HCJQCQctqtxtSOOdo6
title: 'Lab 3'
desc: ''
updated: 1631186746900
created: 1631178674787
---

![](/assets/images/2021-09-09-14-45-25.png)

# Q1
```bash
#!/usr/bin/env bash
# Parth Shah AU1940065
DIR="/home/parth/Desktop/Codee"
if [ -d "$DIR" ]; then 
    echo "The directory is found"
    cd $DIR
    ls -R
else 
    echo "No directory found"
fi
``` 
# Q2
```bash
#!/usr/bin/env bash
# Parth Shah AU1940065
read -p "enter value of dir1: " dir1
read -p "enter value of dir2: " dir2
if [[ -d "$dir1" ]] && [[ -d "$dir2" ]]; then
    mergedir="q2_merged"
    mkdir $mergedir
    cp -r $dir1/* $mergedir && cp -r $dir2/* $mergedir
    echo "$mergedir"    
else
    echo "Either directory does not exist"
fi
``` 
# Q3
```bash
#!/usr/bin/env bash
# Parth Shah AU1940065
read -p "enter time interval: " interval
read -p "enter number of times: " howmany
gcc q3_hello.c
for ((i=1; i<=$howmany; i++))  
    do gcc q3_hello.c && ./a.out;
    sleep $interval; 
done

``` 
# Q4
```bash
#!/usr/bin/env bash 
# Parth Shah AU1940065
read -p "Enter the directory name: " dirname
for entry in $dirname
do  
    echo $entry
done
``` 