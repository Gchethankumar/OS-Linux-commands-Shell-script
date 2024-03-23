# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
## OUTPUT

![Screenshot from 2024-03-23 08-24-57](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/b83a11d4-dde5-4d6b-b7ae-ec5d323e00f5)


### Display the content of the files
cat < file1

## OUTPUT

![Screenshot from 2024-03-23 08-25-09](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/9926312a-d1b9-49e9-8169-cd8975698119)


cat < file2

## OUTPUT

![Screenshot from 2024-03-23 08-25-20](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/10514701-12c6-41a8-83ce-67db53e0ea02)


# Comparing Files
cmp file1 file2
## OUTPUT

 ![Screenshot from 2024-03-23 08-27-23](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/916dfb12-b2ca-4f6f-8438-b3511720830a)

comm file1 file2
 ## OUTPUT
![Screenshot from 2024-03-23 08-27-57](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/2a237cdb-88ad-4bae-9831-f375d4790ddb)

 
diff file1 file2
## OUTPUT
![Screenshot from 2024-03-23 08-28-37](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/bed7ba59-d785-4cf1-8b7e-fecd743fbccd)


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```
## OUTPUT

![Screenshot from 2024-03-23 08-30-10](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/501e6492-c5b4-41df-b05f-c8c89d89ef0c)


cut -c1-3 file11
## OUTPUT

![Screenshot from 2024-03-23 08-34-05](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/b3eb2c3d-85ac-483f-8f69-bdb1f7f64946)

cut -d "|" -f 1 file22
## OUTPUT

![Screenshot from 2024-03-23 08-34-19](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/ef49f4f3-c899-4959-9300-017efb45fde6)


cut -d "|" -f 2 file22
## OUTPUT

![Screenshot from 2024-03-23 08-34-27](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/f7e72c10-4216-478b-9514-a8ec5efbc728)

cat > newfile 
```
Hello world
hello world
^d
````
## OUTPUT
![Screenshot from 2024-03-23 08-34-36](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/d666e058-3b78-4505-98db-5269d3660d3f)

cat < newfile 

## OUTPUT

![Screenshot from 2024-03-23 08-37-47](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/8c71256b-573e-4095-aa42-bad49c30a4f9)

 
grep Hello newfile 
## OUTPUT

![Screenshot from 2024-03-23 08-38-26](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/ae76bdad-f2ad-4f9a-82b3-256e4b30018b)


grep hello newfile 
## OUTPUT

![Screenshot from 2024-03-23 08-38-34](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/2b428b5b-6484-4dd1-bac6-03bb7f3eb72a)



grep -v hello newfile 
## OUTPUT

![Screenshot from 2024-03-23 08-38-44](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/e3ab7ed4-bfc0-48b4-bf02-0aa9ffb680fc)


cat newfile | grep -i "hello"
## OUTPUT

![Screenshot from 2024-03-23 08-39-00](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/71549128-f5fd-478e-822d-2a31210f4740)


cat newfile | grep -i -c "hello"
## OUTPUT

![Screenshot from 2024-03-23 08-42-37](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/2464e2c8-ffa2-497c-ac0e-84fda899b5d9)

grep -R ubuntu /etc
## OUTPUT
![Screenshot from 2024-03-23 08-43-14](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/adb70c16-e7d3-42cd-8f88-a742a8126667)
![Screenshot from 2024-03-23 08-43-41](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/e0b8b5ff-33de-4fcc-8f74-81d02c36a8c6)



grep -w -n world newfile   
## OUTPUT
![Screenshot from 2024-03-23 08-44-05](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/3cc1193a-10a8-42c6-bb25-3faf8b5f43eb)


cat > newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```
## OUTPUT

![Screenshot from 2024-03-23 08-45-19](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/7660b4a9-f18f-4193-9bef-cd53290c1881)

cat < newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
## OUTPUT

![Screenshot from 2024-03-23 08-45-25](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/4d07e3b6-97cc-4de7-9b47-9ba7d00191f7)

egrep -w 'Hello|hello' newfile 
## OUTPUT

![Screenshot from 2024-03-23 08-51-10](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/8bfff398-9682-4f6f-9921-909b7b9cd760)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![Screenshot from 2024-03-23 08-51-22](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/982102f5-7177-4383-9a5c-cfddeb347b98)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


![Screenshot from 2024-03-23 08-51-36](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/7a4915e1-c1a1-4876-b2e6-6d7360791b25)


egrep '(^hello)' newfile 
## OUTPUT

![Screenshot from 2024-03-23 08-51-52](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/c2cac1ff-c608-487a-b262-912bcf84d43f)


egrep '(world$)' newfile 
## OUTPUT

![Screenshot from 2024-03-23 08-52-43](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/44c6bfa9-7842-4f25-bfaa-b75c1821ffb1)


egrep '(World$)' newfile 
## OUTPUT
![Screenshot from 2024-03-23 08-52-55](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/91dd99e0-0382-4655-bfbb-c9c69430c769)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![Screenshot from 2024-03-23 08-53-07](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/0b9bdbca-a3a5-4559-9c72-3c12ddcd5beb)


egrep '[1-9]' newfile 
## OUTPUT

![Screenshot from 2024-03-23 08-53-16](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/8cabb5ed-792d-4084-9d05-7d53fbca4e8b)


egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot from 2024-03-23 08-54-04](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/a607faa9-8071-4620-8f77-7fda6b92e0d1)


egrep 'Linux.*World' newfile 
## OUTPUT

![Screenshot from 2024-03-23 08-54-11](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/d38031c8-18e7-4331-9084-f111bb2f56a8)

egrep l{2} newfile
## OUTPUT

![Screenshot from 2024-03-23 08-54-40](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/073654a5-dd66-494f-8882-310b99577e9e)


egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot from 2024-03-23 08-54-54](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/74922d61-fb38-4d0e-8b33-c93485569e94)


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```
## OUTPUT
![Screenshot from 2024-03-23 09-04-38](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/250364a6-908f-4252-b964-bfc8701fb8d7)


sed -n -e '3p' file23
## OUTPUT

![Screenshot from 2024-03-23 09-05-09](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/7e965151-5e47-40b8-9b16-9034e2bf5a4b)


sed -n -e '$p' file23
## OUTPUT

![Screenshot from 2024-03-23 09-05-17](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/5013e9de-d40b-4d2d-9a69-d87a3047114e)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2024-03-23 09-05-36](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/49382d1b-ace6-4fb1-898e-9d7856efd9ab)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2024-03-23 09-05-51](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/c5b5bb8e-71e0-40f8-aa3c-c9feab894971)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![Screenshot from 2024-03-23 09-06-05](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/18a0445d-89d6-440e-8c15-d7daa530db49)


sed -n -e '1,5p' file23
## OUTPUT

![Screenshot from 2024-03-23 09-06-14](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/9f13aa69-61d5-4e44-b2ae-04070d81cceb)


sed -n -e '2,/Joe/p' file23
## OUTPUT


![Screenshot from 2024-03-23 09-06-24](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/311463d4-81fa-46b1-acf6-43f298e957c1)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


![Screenshot from 2024-03-23 09-06-35](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/7dc2140f-659f-4108-8c40-9fa5203ba51b)

seq 10 
## OUTPUT

![Screenshot from 2024-03-23 09-06-55](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/4e535872-6b15-42aa-83a0-d90826849a77)


seq 10 | sed -n '4,6p'
## OUTPUT

![Screenshot from 2024-03-23 09-07-07](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/44062eda-143c-47d2-af53-84622a32a731)


seq 10 | sed -n '2,~4p'
## OUTPUT

![Screenshot from 2024-03-23 09-07-15](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/fc19d53a-5e5e-42d9-bcfc-a70acf54118d)


seq 3 | sed '2a hello'
## OUTPUT

![Screenshot from 2024-03-23 09-07-58](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/0a99a276-0a71-4d83-a6eb-bd994180c2c6)


seq 2 | sed '2i hello'
## OUTPUT

![Screenshot from 2024-03-23 09-08-13](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/cceef5f7-2707-4e9d-a5a2-03d67a4f537e)


seq 10 | sed '2,9c hello'
## OUTPUT

![Screenshot from 2024-03-23 09-08-29](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/b6967350-495b-4c53-8812-046d654bdd46)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![Screenshot from 2024-03-23 09-08-40](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/79036177-9c82-4520-901f-6b81bb62fbe5)


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

![Screenshot from 2024-03-23 09-08-52](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/1e72a9e3-c5fb-40cf-890f-1f4e60ac8fee)

#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
```
## OUTPUT

![Screenshot from 2024-03-23 09-21-55](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/048c500e-c787-4907-b533-ee5ea4445e73)

sort file21
## OUTPUT
![Screenshot from 2024-03-23 09-22-02](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/3e8f196f-6212-4ec7-be32-224a84473e9c)

cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
```
## OUTPUT
![Screenshot from 2024-03-23 09-22-09](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/5b515738-d969-4a82-aa1f-9a658104f574)

uniq file22
## OUTPUT

![Screenshot from 2024-03-23 09-22-19](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/6d420a67-2b8b-43ac-b2f5-62380630208a)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Screenshot from 2024-03-23 09-22-33](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/9867ff63-80ba-42fb-83ef-fb7aef8cd40b)

cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
## OUTPUT
![Screenshot from 2024-03-23 09-22-48](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/cda8027e-75dc-42aa-a8e3-83f9bb1bbf1a)

cat < urllist.txt
## OUTPUT
![Screenshot from 2024-03-23 09-22-55](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/34acb606-e0ab-4be0-8dbd-76e399ec1a20)

cat urllist.txt | tr -d ' '
 ## OUTPUT

![Screenshot from 2024-03-23 09-23-03](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/d882dcc5-5e52-45ff-96d9-e81ad4729e67)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![Screenshot from 2024-03-23 09-23-23](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/748f4d0c-5afa-445e-9c43-2f5d2b7a116a)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
![Screenshot from 2024-03-23 09-23-34](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/2a8bb54e-8436-4cde-b522-45cbc03124f7)


mkdir backupdir
 
mv backup.tar backupdir
 ## OUTPUT
 ![Screenshot from 2024-03-23 09-42-28](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/9931dce5-53c1-4529-afa8-30be564abc72)

tar -tvf backup.tar
## OUTPUT
![Screenshot from 2024-03-23 09-42-49](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/a841f4bc-dcbf-4a44-b800-7a1f83d4b668)


tar -xvf backup.tar
## OUTPUT
![Screenshot from 2024-03-23 09-43-07](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/1d90e3fd-d7e6-4a3d-a8d3-4c6e1e590938)

gzip backup.tar

ls .gz
## OUTPUT
 ![Screenshot from 2024-03-23 09-43-26](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/e2e94645-0b25-4e3a-af7f-f6f9f2717274)

gunzip backup.tar.gz
## OUTPUT

![Screenshot from 2024-03-23 09-43-39](https://github.com/Gchethankumar/OS-Linux-commands-Shell-script/assets/118348224/e8fa7cf3-5d9d-43ad-aa15-1f76184bb9d1)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT

# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT



# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT


# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 
 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 
 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 
cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 

 
 ./funcex.sh 1 2

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
 
 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
 
cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 


# RESULT:
The Commands are executed successfully.
