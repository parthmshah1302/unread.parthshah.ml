---
id: sX5HCJQCQctqtxtSOOdo6
title: 'Lab 3'
desc: ''
updated: 1631709723620
created: 1631178674787
---

![](/assets/images/2021-09-09-14-45-25.png)

# Q1
```bash
#!/usr/bin/env bash
# Parth Shah AU1940065
cat << "EOF"

██████╗  █████╗ ██████╗ ████████╗██╗  ██╗    ███████╗██╗  ██╗ █████╗ ██╗  ██╗    
██╔══██╗██╔══██╗██╔══██╗╚══██╔══╝██║  ██║    ██╔════╝██║  ██║██╔══██╗██║  ██║    
██████╔╝███████║██████╔╝   ██║   ███████║    ███████╗███████║███████║███████║    
██╔═══╝ ██╔══██║██╔══██╗   ██║   ██╔══██║    ╚════██║██╔══██║██╔══██║██╔══██║    
██║     ██║  ██║██║  ██║   ██║   ██║  ██║    ███████║██║  ██║██║  ██║██║  ██║    
╚═╝     ╚═╝  ╚═╝╚═╝  ╚═╝   ╚═╝   ╚═╝  ╚═╝    ╚══════╝╚═╝  ╚═╝╚═╝  ╚═╝╚═╝  ╚═╝    
                                                                                 
 █████╗ ██╗   ██╗ ██╗ █████╗ ██╗  ██╗ ██████╗  ██████╗  ██████╗ ███████╗         
██╔══██╗██║   ██║███║██╔══██╗██║  ██║██╔═████╗██╔═████╗██╔════╝ ██╔════╝         
███████║██║   ██║╚██║╚██████║███████║██║██╔██║██║██╔██║███████╗ ███████╗         
██╔══██║██║   ██║ ██║ ╚═══██║╚════██║████╔╝██║████╔╝██║██╔═══██╗╚════██║         
██║  ██║╚██████╔╝ ██║ █████╔╝     ██║╚██████╔╝╚██████╔╝╚██████╔╝███████║         
╚═╝  ╚═╝ ╚═════╝  ╚═╝ ╚════╝      ╚═╝ ╚═════╝  ╚═════╝  ╚═════╝ ╚══════╝         
                                                                                 

EOF
DIR="/home/parth/Desktop/Code/OS-Labs/Lab3/"
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
cat << "EOF"

██████╗  █████╗ ██████╗ ████████╗██╗  ██╗    ███████╗██╗  ██╗ █████╗ ██╗  ██╗    
██╔══██╗██╔══██╗██╔══██╗╚══██╔══╝██║  ██║    ██╔════╝██║  ██║██╔══██╗██║  ██║    
██████╔╝███████║██████╔╝   ██║   ███████║    ███████╗███████║███████║███████║    
██╔═══╝ ██╔══██║██╔══██╗   ██║   ██╔══██║    ╚════██║██╔══██║██╔══██║██╔══██║    
██║     ██║  ██║██║  ██║   ██║   ██║  ██║    ███████║██║  ██║██║  ██║██║  ██║    
╚═╝     ╚═╝  ╚═╝╚═╝  ╚═╝   ╚═╝   ╚═╝  ╚═╝    ╚══════╝╚═╝  ╚═╝╚═╝  ╚═╝╚═╝  ╚═╝    
                                                                                 
 █████╗ ██╗   ██╗ ██╗ █████╗ ██╗  ██╗ ██████╗  ██████╗  ██████╗ ███████╗         
██╔══██╗██║   ██║███║██╔══██╗██║  ██║██╔═████╗██╔═████╗██╔════╝ ██╔════╝         
███████║██║   ██║╚██║╚██████║███████║██║██╔██║██║██╔██║███████╗ ███████╗         
██╔══██║██║   ██║ ██║ ╚═══██║╚════██║████╔╝██║████╔╝██║██╔═══██╗╚════██║         
██║  ██║╚██████╔╝ ██║ █████╔╝     ██║╚██████╔╝╚██████╔╝╚██████╔╝███████║         
╚═╝  ╚═╝ ╚═════╝  ╚═╝ ╚════╝      ╚═╝ ╚═════╝  ╚═════╝  ╚═════╝ ╚══════╝         
                                                                                 

EOF
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
cat << "EOF"

██████╗  █████╗ ██████╗ ████████╗██╗  ██╗    ███████╗██╗  ██╗ █████╗ ██╗  ██╗    
██╔══██╗██╔══██╗██╔══██╗╚══██╔══╝██║  ██║    ██╔════╝██║  ██║██╔══██╗██║  ██║    
██████╔╝███████║██████╔╝   ██║   ███████║    ███████╗███████║███████║███████║    
██╔═══╝ ██╔══██║██╔══██╗   ██║   ██╔══██║    ╚════██║██╔══██║██╔══██║██╔══██║    
██║     ██║  ██║██║  ██║   ██║   ██║  ██║    ███████║██║  ██║██║  ██║██║  ██║    
╚═╝     ╚═╝  ╚═╝╚═╝  ╚═╝   ╚═╝   ╚═╝  ╚═╝    ╚══════╝╚═╝  ╚═╝╚═╝  ╚═╝╚═╝  ╚═╝    
                                                                                 
 █████╗ ██╗   ██╗ ██╗ █████╗ ██╗  ██╗ ██████╗  ██████╗  ██████╗ ███████╗         
██╔══██╗██║   ██║███║██╔══██╗██║  ██║██╔═████╗██╔═████╗██╔════╝ ██╔════╝         
███████║██║   ██║╚██║╚██████║███████║██║██╔██║██║██╔██║███████╗ ███████╗         
██╔══██║██║   ██║ ██║ ╚═══██║╚════██║████╔╝██║████╔╝██║██╔═══██╗╚════██║         
██║  ██║╚██████╔╝ ██║ █████╔╝     ██║╚██████╔╝╚██████╔╝╚██████╔╝███████║         
╚═╝  ╚═╝ ╚═════╝  ╚═╝ ╚════╝      ╚═╝ ╚═════╝  ╚═════╝  ╚═════╝ ╚══════╝         
                                                                                 

EOF
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
cat << "EOF"

██████╗  █████╗ ██████╗ ████████╗██╗  ██╗    ███████╗██╗  ██╗ █████╗ ██╗  ██╗    
██╔══██╗██╔══██╗██╔══██╗╚══██╔══╝██║  ██║    ██╔════╝██║  ██║██╔══██╗██║  ██║    
██████╔╝███████║██████╔╝   ██║   ███████║    ███████╗███████║███████║███████║    
██╔═══╝ ██╔══██║██╔══██╗   ██║   ██╔══██║    ╚════██║██╔══██║██╔══██║██╔══██║    
██║     ██║  ██║██║  ██║   ██║   ██║  ██║    ███████║██║  ██║██║  ██║██║  ██║    
╚═╝     ╚═╝  ╚═╝╚═╝  ╚═╝   ╚═╝   ╚═╝  ╚═╝    ╚══════╝╚═╝  ╚═╝╚═╝  ╚═╝╚═╝  ╚═╝    
                                                                                 
 █████╗ ██╗   ██╗ ██╗ █████╗ ██╗  ██╗ ██████╗  ██████╗  ██████╗ ███████╗         
██╔══██╗██║   ██║███║██╔══██╗██║  ██║██╔═████╗██╔═████╗██╔════╝ ██╔════╝         
███████║██║   ██║╚██║╚██████║███████║██║██╔██║██║██╔██║███████╗ ███████╗         
██╔══██║██║   ██║ ██║ ╚═══██║╚════██║████╔╝██║████╔╝██║██╔═══██╗╚════██║         
██║  ██║╚██████╔╝ ██║ █████╔╝     ██║╚██████╔╝╚██████╔╝╚██████╔╝███████║         
╚═╝  ╚═╝ ╚═════╝  ╚═╝ ╚════╝      ╚═╝ ╚═════╝  ╚═════╝  ╚═════╝ ╚══════╝         
                                                                                 

EOF

read -p "Enter the directory name: " dirname
# dirname="/home/parth/Desktop/Code/OS-Labs/Lab3"
# dirname="/home/parth/Desktop/Code/stepwell-spotdl"
cd $dirname

cat << "EOF" 

   ___                                     __     ___
  / _ |  ___   ___   ____ ___  ___ _ ____ / /    <  /
 / __ | / _ \ / _ \ / __// _ \/ _ `// __// _ \   / / 
/_/ |_|/ .__// .__//_/   \___/\_,_/ \__//_//_/  /_/  
      /_/   /_/                                      

EOF
name=$(ls -lh $dirname | awk '{print  $9}')
size=$(ls -lh $dirname | awk '{print  $5}')
datemonth=$(ls -lh $dirname | awk '{print  $6}')
datenum=$(ls -lh $dirname | awk '{print  $7}')
protection=$(ls -lh $dirname | awk '{print  $1}')
owner=$(ls -lh $dirname | awk '{print  $3}')
paste <(printf %s "$name") <(printf %s "$size") <(printf %s "$datemonth") <(printf %s "$datenum") <(printf %s "$protection") <(printf %s "$owner")

cat << "EOF" 

   ___                                     __     ___ 
  / _ |  ___   ___   ____ ___  ___ _ ____ / /    |_  |
 / __ | / _ \ / _ \ / __// _ \/ _ `// __// _ \  / __/ 
/_/ |_|/ .__// .__//_/   \___/\_,_/ \__//_//_/ /____/ 
      /_/   /_/                                       

EOF
shopt -s dotglob
name=$(stat --printf="%n\n" $dirname/*)
size=$(stat --printf="%s\n" $dirname/*)
date=$(stat --printf="%.10y\n" $dirname/*)
protection=$(stat --printf="%A\n" $dirname/*)
owner=$(stat --printf="%U\n" $dirname/*)
paste <(printf %s "$name") <(printf %s "$size") <(printf %s "$date") <(printf %s "$protection") <(printf %s "$owner") | column -t

totalFiles=$(ls $dirname | wc -l)
totalSpace=$(du $dirname -sh)

printf "\nTotal files in a directory is: "
printf $totalFiles

printf "\n"

printf "\nTotal space of a directory is: "
printf $totalSpace

printf "\n"
``` 
## Q5
```bash
#!/usr/bin/env bash
# Parth Shah AU1940065
cat << "EOF"

██████╗  █████╗ ██████╗ ████████╗██╗  ██╗    ███████╗██╗  ██╗ █████╗ ██╗  ██╗    
██╔══██╗██╔══██╗██╔══██╗╚══██╔══╝██║  ██║    ██╔════╝██║  ██║██╔══██╗██║  ██║    
██████╔╝███████║██████╔╝   ██║   ███████║    ███████╗███████║███████║███████║    
██╔═══╝ ██╔══██║██╔══██╗   ██║   ██╔══██║    ╚════██║██╔══██║██╔══██║██╔══██║    
██║     ██║  ██║██║  ██║   ██║   ██║  ██║    ███████║██║  ██║██║  ██║██║  ██║    
╚═╝     ╚═╝  ╚═╝╚═╝  ╚═╝   ╚═╝   ╚═╝  ╚═╝    ╚══════╝╚═╝  ╚═╝╚═╝  ╚═╝╚═╝  ╚═╝    
                                                                                 
 █████╗ ██╗   ██╗ ██╗ █████╗ ██╗  ██╗ ██████╗  ██████╗  ██████╗ ███████╗         
██╔══██╗██║   ██║███║██╔══██╗██║  ██║██╔═████╗██╔═████╗██╔════╝ ██╔════╝         
███████║██║   ██║╚██║╚██████║███████║██║██╔██║██║██╔██║███████╗ ███████╗         
██╔══██║██║   ██║ ██║ ╚═══██║╚════██║████╔╝██║████╔╝██║██╔═══██╗╚════██║         
██║  ██║╚██████╔╝ ██║ █████╔╝     ██║╚██████╔╝╚██████╔╝╚██████╔╝███████║         
╚═╝  ╚═╝ ╚═════╝  ╚═╝ ╚════╝      ╚═╝ ╚═════╝  ╚═════╝  ╚═════╝ ╚══════╝         
                                                                                 
EOF

declare -i flag=1

read -r -d '' menu << EOM
\n a. Display Current Directory\n
b. List Directory\n
c. Make a new directory\n
d. Change directory\n
e. Copy File\n
f. Rename File\n
g. Delete File\n
h. Edit content of File\n
i. Exit\n
EOM



while [ $flag -eq 1 ]
do
    echo -e $menu 
    echo -e "\e[1mEnter your command: \e[0m"
    read inpcommand 
    if [ "$inpcommand" = "a" ]
    then 
        echo -e "\e[3m\n Only those who wander find new paths. Here is yours\n\e[0m"
        pwd
    elif [ "$inpcommand" = "b" ]
    then
        ls 
    elif [ "$inpcommand" = "c" ]
    then
        echo -e "What would you like to name it, Joe?"
        read dirName 
        mkdir $dirName 
        echo -e "\n$dirName was succesfully incanted." 
    elif [ "$inpcommand" = "d" ]
    then
        declare -i cdFlag=1
        while [ $cdFlag -eq 1 ]
        do 
            echo -e "Where does thy wish to go?"
            read changeDir
            if [ -d "$changeDir" ] 
            then
                cd $changeDir
                echo -e "Hope you had a horrible journey. "
                cdFlag=0
            else 
                echo -e "No such thing exists. Get sober and try again!"
            fi
        done    
    elif [ "$inpcommand" = "e" ]
    then
        declare -i sourceFilePathFlag=1
        while [ $sourceFilePathFlag -eq 1 ]
        do 
            echo -e "Enter the source file path."
            read sourceFilePath 
            if [ -f $sourceFilePath ] 
            then 
                echo -e "Enter the destination directory"
                read destinationFilePath
                if [ -d $destinationFilePath ]
                then
                    cp -p $sourceFilePath $destinationFilePath/
                    echo -e "\nIt's known as Originality. You should try it sometime."
                    destinationFileFlag=0
                else 
                    echo -e "Enter a valid destination directory."
                fi
                sourceFilePathFlag=0
            else
                echo -e "Enter a valid source file path."
            fi
        done
    elif [ "$inpcommand" = "f" ]
    then
        declare -i sourceFilePathFlag=1
        while [ $sourceFilePathFlag -eq 1 ]
        do 
            echo -e "Enter the source file path."
            read sourceFilePath 
            if [ -f $sourceFilePath ] 
            then 
                echo -e "Enter the new name that you would like"
                read newName
                mv $sourceFilePath $newName
                sourceFilePathFlag=0
            else
                echo -e "Enter a valid source file path."
            fi
        done
    elif [ "$inpcommand" = "g" ]
    then
        declare -i deleteFileFlag=1
        while [ $deleteFileFlag -eq 1 ]
        do
            echo -e "Enter the path of file that you want to delete"
            read deleteFilePath
            if [ -f $deleteFilePath ]
            then
                rm $deleteFilePath
                echo -e "The file has been deleted!"
                deleteFileFlag=0
            else 
                echo -e "No such file exists"
            fi
        done
    elif [ "$inpcommand" = "h" ]
    then
        declare -i editFileFlag=1
        while [ $editFileFlag -eq 1 ]
        do
            echo -e "Enter the path of file that you want to edit"
            read deleteFilePath
            if [ -f $deleteFilePath ]
            then
                nano $deleteFilePath
                echo -e "The file has been edited!"
                editFileFlag=0
            else 
                echo -e "No such file exists"
            fi
        done
    elif [ "$inpcommand" = "i" ]
    then 
        flag=0
        echo -e "See you later, alligator!"
    else 
        echo -e "Enter something from the list, you jack!"
    fi
done
```

## Q7 
```bash 
#!/usr/bin/env bash
# Parth Shah AU1940065
cat << "EOF"

██████╗  █████╗ ██████╗ ████████╗██╗  ██╗    ███████╗██╗  ██╗ █████╗ ██╗  ██╗    
██╔══██╗██╔══██╗██╔══██╗╚══██╔══╝██║  ██║    ██╔════╝██║  ██║██╔══██╗██║  ██║    
██████╔╝███████║██████╔╝   ██║   ███████║    ███████╗███████║███████║███████║    
██╔═══╝ ██╔══██║██╔══██╗   ██║   ██╔══██║    ╚════██║██╔══██║██╔══██║██╔══██║    
██║     ██║  ██║██║  ██║   ██║   ██║  ██║    ███████║██║  ██║██║  ██║██║  ██║    
╚═╝     ╚═╝  ╚═╝╚═╝  ╚═╝   ╚═╝   ╚═╝  ╚═╝    ╚══════╝╚═╝  ╚═╝╚═╝  ╚═╝╚═╝  ╚═╝    
                                                                                 
 █████╗ ██╗   ██╗ ██╗ █████╗ ██╗  ██╗ ██████╗  ██████╗  ██████╗ ███████╗         
██╔══██╗██║   ██║███║██╔══██╗██║  ██║██╔═████╗██╔═████╗██╔════╝ ██╔════╝         
███████║██║   ██║╚██║╚██████║███████║██║██╔██║██║██╔██║███████╗ ███████╗         
██╔══██║██║   ██║ ██║ ╚═══██║╚════██║████╔╝██║████╔╝██║██╔═══██╗╚════██║         
██║  ██║╚██████╔╝ ██║ █████╔╝     ██║╚██████╔╝╚██████╔╝╚██████╔╝███████║         
╚═╝  ╚═╝ ╚═════╝  ╚═╝ ╚════╝      ╚═╝ ╚═════╝  ╚═════╝  ╚═════╝ ╚══════╝         
                                                                                 

EOF

alias la='ls -a'

read -r -d '' menu << EOM
\n a. Find files newer than a particular date\n
b. Find files older than a particular date\n
c. Exit\n

EOM

declare -i directoryNameFlag=1
while [ $directoryNameFlag -eq 1 ]
do 
    echo -e "Enter the name of directory"
    read directoryName
    if [ -d $directoryName ]
    then
        cd $directoryName
        declare -i menuFlag=1
        while [ $menuFlag -eq 1 ]
        do 
            echo -e $menu 
            echo -e "Enter your command: " 
            read menuCommand 
            if [ "$menuCommand" == "a" ]
            then
                echo -e "Enter date to find files newer than this date (eg: sept 13, 2021):  "
                read newerDate 
                find . -type f -newermt "$newerDate" -iname ".*" -ls
            elif [ "$menuCommand" == "b" ]
            then 
                echo -e "Enter date to find files older than this date (eg: sept 13, 2021): "
                read olderDate 
                find . -type f -not -newermt "$olderDate" -iname ".*" -ls
            else 
                echo -e "See you later, alligator!"
                menuFlag=0
            fi  
        done 
        directoryNameFlag=0
    else 
        echo -e "It does not exist. Try some other directory!"
    fi
done
````