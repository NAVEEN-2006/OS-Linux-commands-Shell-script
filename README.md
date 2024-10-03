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
```
cat > file1
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
```
```
cat > file2
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
```
### Display the content of the files
```cat < file1```
## OUTPUT
![image](https://github.com/user-attachments/assets/a485e6f1-ab9f-4cb2-bc3c-1e2b6eec135f)


```cat < file2```
## OUTPUT
![image](https://github.com/user-attachments/assets/2313bfc8-8cb2-4760-b218-4211a7c33eff)


# Comparing Files
```cmp file1 file2```
## OUTPUT
![image](https://github.com/user-attachments/assets/a8134b84-72e4-4ff7-8ce7-1f01ddca37fd)


```comm file1 file2```
## OUTPUT
![image](https://github.com/user-attachments/assets/e3a457b0-1cf9-4ebf-ae20-c69daac4bb35)


```diff file1 file2```
## OUTPUT
![image](https://github.com/user-attachments/assets/63987257-18c3-4e9a-8a52-5c8cd75e0b35)


# Filters

### Create the following files file11, file22 as follows:
```
cat > file11
Hello world
This is my world
```
```
cat > file22
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
```
```
cut -c1-3 file11
```
## OUTPUT
![image](https://github.com/user-attachments/assets/0b282f01-01b7-4ae5-9f8d-7708e8e577a8)


```
cut -d "|" -f 1 file22
```
## OUTPUT

![image](https://github.com/user-attachments/assets/4f819925-a3c1-4bbe-8dbd-d9c80f789e3f)


```
cut -d "|" -f 2 file22
```
## OUTPUT
![image](https://github.com/user-attachments/assets/7a89e702-15c4-42fb-9d34-0a4832fc8ca0)

```
cat < newfile 
Hello world
hello world
```
```
cat > newfile 
Hello world
hello world
```
```
grep Hello newfile 
```
## OUTPUT
![image](https://github.com/user-attachments/assets/41306ef2-752a-4faf-ae22-215095d43b6c)


```
grep hello newfile 
```
## OUTPUT
![image](https://github.com/user-attachments/assets/0853a614-08e6-4085-b053-2ac80ceb4eb5)

```
grep -v hello newfile 
```
## OUTPUT
![image](https://github.com/user-attachments/assets/62cedb50-6160-4d0e-b37f-17f964398665)


```
cat newfile | grep -i "hello"
```
## OUTPUT

![image](https://github.com/user-attachments/assets/1ce8134f-e399-4ad5-92fe-2779f2099cbe)


```
cat newfile | grep -i -c "hello"
```
## OUTPUT

![image](https://github.com/user-attachments/assets/029a759a-eda2-49ba-ba9b-bac32aa75f24)


```
grep -R ubuntu /etc
```
## OUTPUT
![image](https://github.com/user-attachments/assets/f2448db8-cf58-46dd-acb8-508f15d84e35)
![image](https://github.com/user-attachments/assets/13fbafaa-81c9-48da-8a2b-9b65676d272d)
![image](https://github.com/user-attachments/assets/232644fc-593f-4380-bab8-f485d3306a73)
![image](https://github.com/user-attachments/assets/67421b5b-3765-4f52-8e85-2ab149acc7c4)
![image](https://github.com/user-attachments/assets/e62d533e-4809-432d-b8a4-9cf3c41557ee)
![image](https://github.com/user-attachments/assets/218ffb5b-2e34-474e-8f8d-0c2095da75f5)
```
grep -w -n world newfile  
```
## OUTPUT
![image](https://github.com/user-attachments/assets/5010a7ea-5c81-4845-8fb6-a5ce500b8348)


```
cat < newfile 
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
```
```
cat > newfile
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
```

```
egrep -w 'Hello|hello' newfile 
```
## OUTPUT
![image](https://github.com/user-attachments/assets/ed2c117d-1d01-4e4b-971b-fd5f058a1d3d)

```
egrep -w '(H|h)ello' newfile 
```
## OUTPUT
![image](https://github.com/user-attachments/assets/6694f4b4-4b49-42e1-8f00-7a2448112c18)


```
egrep -w '(H|h)ell[a-z]' newfile 
```
## OUTPUT
![image](https://github.com/user-attachments/assets/5fecd84b-4f8a-4c21-ab97-844523c120b8)


```
egrep '(^hello)' newfile 
```
## OUTPUT
![image](https://github.com/user-attachments/assets/31d9bac1-4e59-43d4-961e-35cdcc1325b0)


```
egrep '(world$)' newfile 
```
## OUTPUT
![image](https://github.com/user-attachments/assets/f7e0c75f-6847-4573-9480-a19d3350cde7)



```
egrep '(World$)' newfile 
```
## OUTPUT

![image](https://github.com/user-attachments/assets/91694069-e814-4457-93e7-1b437514ba19)

```
egrep '((W|w)orld$)' newfile 
```
## OUTPUT

![image](https://github.com/user-attachments/assets/a4386282-9909-490f-857b-4391165fe106)

```
egrep '[1-9]' newfile 
```
## OUTPUT

![image](https://github.com/user-attachments/assets/924ce43b-bef3-4a1d-b814-a91f20225eb7)


```
egrep 'Linux.*world' newfile 
```
## OUTPUT
![image](https://github.com/user-attachments/assets/e254ba37-a86d-44d2-89df-bff3b206b815)

```
egrep l{2} newfile
```
## OUTPUT
![image](https://github.com/user-attachments/assets/1cedc514-ed7e-4d42-8469-daf08953c31d)


```
egrep 's{1,2}' newfile
```
## OUTPUT 
![image](https://github.com/user-attachments/assets/aa74440c-8e0a-48fc-b98a-83015f48c6d9)


```
cat > file23
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
```

```
sed -n -e '3p' file23
```
## OUTPUT
![image](https://github.com/user-attachments/assets/77f82aad-48ff-4a9f-a7c7-e8fd969393a3)

```
sed -n -e '$p' file23
```
## OUTPUT

![image](https://github.com/user-attachments/assets/796cba7a-829f-49c4-81df-d6deab5f73e9)

```
sed  -e 's/Ram/Sita/' file23
```
## OUTPUT

![image](https://github.com/user-attachments/assets/79765753-4c42-403f-99a4-c97f01eb2574)

```
sed  -e '2s/Ram/Sita/' file23
```

## OUTPUT

![image](https://github.com/user-attachments/assets/9a0f26ea-d1de-4bdc-8d06-3adae732aeb7)

```
sed  '/tom/s/5000/6000/' file23
```
## OUTPUT
![image](https://github.com/user-attachments/assets/0664c558-1287-4bcc-a8b4-2caf9d9d0c87)


```
sed -n -e '1,5p' file23
```
## OUTPUT
![image](https://github.com/user-attachments/assets/222e7d4a-0ec4-41be-9bd6-2018fe840fa4)

```
sed -n -e '2,/Joe/p' file23
```
## OUTPUT
![image](https://github.com/user-attachments/assets/623b6ade-0251-4529-b8da-3a3384a73f6f)


```
sed -n -e '/tom/,/Joe/p' file23
```
## OUTPUT
![image](https://github.com/user-attachments/assets/2e3b4da9-d29f-4b7e-b79b-cc348e63fd83)

```
seq 10 
```
## OUTPUT
![image](https://github.com/user-attachments/assets/f1087051-b922-4c89-bdbd-1cfcf9c132b8)



```
seq 10 | sed -n '4,6p'
```
## OUTPUT

![image](https://github.com/user-attachments/assets/d58956fc-d3e8-4673-92bc-208c8bc0f477)


```
seq 10 | sed -n '2,~4p'
```
## OUTPUT
![image](https://github.com/user-attachments/assets/a0f4ba28-abd8-4999-9d74-6b28686e5e16)


```
seq 3 | sed '2a hello'
```
## OUTPUT
![image](https://github.com/user-attachments/assets/84138a8a-7013-4eef-ac86-213a96174794)


```
seq 2 | sed '2i hello'
```
## OUTPUT
![image](https://github.com/user-attachments/assets/72cceb2b-e3cd-4463-8e5c-cdaac4bb7676)


```
seq 10 | sed '2,9c hello'
```
## OUTPUT
![image](https://github.com/user-attachments/assets/fd105c00-7d29-4feb-af11-15bb39dae049)


```
sed -n '2,4{s/^/$/;p}' file23
```
## OUTPUT

![image](https://github.com/user-attachments/assets/3ca61fee-26cc-4a54-a678-dba7d4a410cf)


```
sed -n '2,4{s/$/*/;p}' file23
```
## OUTPUT
![image](https://github.com/user-attachments/assets/9520a3ad-d3e0-4b80-b4bf-1c6c9fafe480)


# Sorting File content

```
cat > file21
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
```
sort file21
```
## OUTPUT
![image](https://github.com/user-attachments/assets/538910cd-e2b8-4c63-a62d-11a9fae80d1c)



```
cat > file22
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
```
uniq file22
```
## OUTPUT
![image](https://github.com/user-attachments/assets/84775504-1fe8-4892-aac1-2e7d2f38abc6)


# Using tr command
```
cat file23 | tr [:lower:] [:upper:]
```
## OUTPUT
![image](https://github.com/user-attachments/assets/a4278783-0fe7-4b26-99b9-7c09b47b256d)



```
cat < urllist.txt
www. yahoo. com
www. google. com
www. mrcet.... com
```

```
cat > urllist.txt
www. yahoo. com
www. google. com
www. mrcet.... com
```
```
cat urllist.txt | tr -d ' '
```
 ## OUTPUT
![image](https://github.com/user-attachments/assets/5e864f78-18cb-4f24-a2b0-52d99911e6e2)


```
cat urllist.txt | tr -d ' ' | tr -s '.'
```
## OUTPUT
![image](https://github.com/user-attachments/assets/eae0adca-5f4c-48b2-b2cf-b147cbf0fd4c)


# Backup commands
```
tar -cvf backup.tar *
```
## OUTPUT
![image](https://github.com/user-attachments/assets/f2ad5aa8-5a83-4f15-bc1b-1609f375e104)

![image](https://github.com/user-attachments/assets/eca3216c-9324-4887-a4e4-09a802e970b4)

```
mkdir backupdir
mv backup.tar backupdir 
tar -tvf backup.tar
```
## OUTPUT
![image](https://github.com/user-attachments/assets/dc0c5696-37d3-4a61-9311-58f4eb7cbabf)


```
tar -xvf backup.tar
```
## OUTPUT
![image](https://github.com/user-attachments/assets/521ad861-17c7-43c9-b097-dede6841d67f)


```
gzip backup.tar
ls *.gz
```

## OUTPUT
 ![image](https://github.com/user-attachments/assets/7d169f8f-c5ac-4819-8cb9-55ad9cb122ec)


```
gunzip backup.tar.gz
ls *.tar
```
## OUTPUT 
![com](<Screenshot from 2024-09-04 09-44-03.png>)
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
```
chmod 755 my-script.sh
./my-script.sh
```
## OUTPUT
![image](https://github.com/user-attachments/assets/2e5bc2b2-3761-482b-8bde-e7ab1cd7cd5d)

```
cat << stop > herecheck.txt
```
```
hello in this world
i cant stop
for this non stop movement
stop
cat herecheck.txt
```
## OUTPUT
![image](https://github.com/user-attachments/assets/9dc4f63f-bb93-49bc-b804-7703317c37a3)

```
cat < scriptest.sh 
```
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
```
![image](https://github.com/user-attachments/assets/f6543dac-6a72-43ec-a5f5-6d80db12c5e1)

```
cat scriptest.sh 
```
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
```
chmod 777 scriptest.sh
./scriptest.sh 1 2 3
```
## OUTPUT
![image](https://github.com/user-attachments/assets/e60aeef6-fa3b-4264-915f-d8ee75d1115e)

 
```
ls file1
```
## OUTPUT
![image](https://github.com/user-attachments/assets/9d5797bf-39e9-4054-bca9-e67ccb2c7346)

```
echo $?
```
## OUTPUT 
![image](https://github.com/user-attachments/assets/53e2629b-4a1f-4353-8d25-fc9035328fd1)

```
./one bash: ./one: Permission denied
echo $?
```
## OUTPUT 
![image](https://github.com/user-attachments/assets/77210088-86d4-4749-9f23-b30dc7fc6fd0)

```
abcd
echo $?
```
## OUTPUT
![image](https://github.com/user-attachments/assets/a8a393e5-b184-4f0d-b1ce-7cc664a483e9)


# mis-using string comparisons

```
cat > strcomp.sh 
```
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
```
cat strcomp.sh 
```
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
## OUTPUT
![image](https://github.com/user-attachments/assets/36b8ea8d-25ba-4cf1-b34e-9b53a7f6130b)



```
chmod 755 strcomp.sh
./strcomp.sh 
```
## OUTPUT
![image](https://github.com/user-attachments/assets/dfaa3d5b-9518-47fa-aabf-f95364ae2b5a)


# check file ownership
```
cat > psswdperm.sh 
```
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
```
```
cat psswdperm.sh 
```
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
```
```
./psswdperm.sh
```
## OUTPUT
![image](https://github.com/user-attachments/assets/8c2f034c-5870-485e-9571-b073f22612c0)


# check if with file location

```
cat>ifnested.sh 
```
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
```
cat ifnested.sh 
```
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
```
./ifnested.sh 
```
## OUTPUT
![image](https://github.com/user-attachments/assets/7f7fcc16-44c7-450a-b5eb-1e6bd6df8e2f)


# using numeric test comparisons
```
cat > iftest.sh 
```
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
```
cat iftest.sh 
```
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
```
$ chmod 755 iftest.sh
$ ./iftest.sh 
```
## OUTPUT
![image](https://github.com/user-attachments/assets/697c438e-5c7d-4e54-9e94-5ae750c4e756)


# check if a file
```
cat > ifnested.sh
``` 
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
```
cat ifnested.sh 
```
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
```
$ chmod 755 ifnested.sh
$ ./ifnested.sh 
```
## OUTPUT
![image](https://github.com/user-attachments/assets/fb4a860d-0c9f-4c55-906f-885f51a10bbf)


# looking for a possible value using elif
```
cat elifcheck.sh 
```
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
```
$ chmod 755 elifcheck.sh
$ ./elifcheck.sh 
```
## OUTPUT
![image](https://github.com/user-attachments/assets/9b7ccd83-2583-4c13-87a6-ad174b7026db)


# testing compound comparisons
```
cat> ifcompound.sh 
```
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
```
## OUTPUT
![image](https://github.com/user-attachments/assets/b30c6c10-14cf-418c-a036-a9aaf6a0e15b)


# using the case command
```
cat >casecheck.sh 
```
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
```
$ chmod 755 casecheck.sh 
$ ./casecheck.sh 
```
## OUTPUT
![image](https://github.com/user-attachments/assets/2754cd51-4dd5-405f-9123-c7cad7d75fc7)

```
cat > whiletest
```
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
```
$ chmod 755 whiletest.sh
$ ./whiletest.sh
```
## OUTPUT
![image](https://github.com/user-attachments/assets/609f105d-48a0-4284-b8ad-dd5431b3ea84)

```
cat > untiltest.sh 
```
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
```
$ chmod 755 untiltest.sh
$ ./untiltest.sh
```
![image](https://github.com/user-attachments/assets/fb973bb0-bca8-4dc3-8f51-1ad4f05afd0b)

```
cat > forin1.sh 
```
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
```
$ chmod 755 forin1.sh
$ ./forin1.sh
```
![image](https://github.com/user-attachments/assets/79eee1a3-fd98-4ff2-873d-ef268f49a8e7)

```
cat > forin2.sh 
```
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
```
$ chmod 755 forin2.sh
$ ./forin2.sh 
```
## OUTPUT
![image](https://github.com/user-attachments/assets/e0d3839e-7ed4-4db5-b001-76f35874c85f)

```
cat > forin3.sh 
```
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
```
$ ./forin3.sh 
```
## OUTPUT
![image](https://github.com/user-attachments/assets/2546d83f-9f7a-4fce-9f2a-276d00ad2f65)

```
cat > forin1.sh 
```
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
```
$ chmod 755 forin1.sh
$ ./forin1.sh
```
## OUTPUT
![image](https://github.com/user-attachments/assets/952ad5df-4808-4ff4-89fd-6153db23b725)

```
cat > forinfile.sh 
```
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file"
done
```
```
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam
```
```
$ chmod 777 forinfile.sh
$ ./forinfile.sh
```
## OUTPUT
![image](https://github.com/user-attachments/assets/793b9f77-83ab-4c5d-b709-4df7c7a6ce14)

```
cat > forctype.sh 
```
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
```
```
$ chmod 755 forctype.sh
$ ./forctype.sh 
```
## OUTPUT
![image](https://github.com/user-attachments/assets/70a87df4-efda-4021-8c98-c2da6552430e)

```
cat > forctype1.sh 
```
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
```
$ chmod 755 forctype1.sh
$ ./forctype1.sh 
```
## OUTPUT
![image](https://github.com/user-attachments/assets/4e1f7685-5ed4-472c-81bd-2b20b3f34067)

```
cat > fornested1.sh 
```
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
```
$ chmod 755 fornested1.sh
$ ./fornested1.sh 
```
 ## OUTPUT
![image](https://github.com/user-attachments/assets/ebd6be2b-2d26-4d33-b36b-6028ae7c3667)

```
cat > forbreak.sh 
```
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
echo "The for loop is completed"
```
```
$ chmod 755 forbreak.sh
$ ./forbreak.sh
```
## OUTPUT
![image](https://github.com/user-attachments/assets/c0090daf-7676-4392-946a-842bcaaee4d5)

```
cat > forcontinue.sh 
```
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
echo "The for loop is completed"
```
```
$ chmod 755 forcontinue.sh
$ ./forcontinue.sh 
```
## OUTPUT
![image](https://github.com/user-attachments/assets/ec6d252d-4bb1-4d55-9b3a-63320dec3629)

```
cat > exread.sh 
```
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
```
```
$ chmod 755 exread.sh 
$ ./exread.sh 
```
## OUTPUT
![image](https://github.com/user-attachments/assets/467609d8-2f4d-4013-ab26-c56779cd66b5)

```
cat > exread1.sh
```
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. "
``` 
```
$ chmod 755 exread1.sh 
$ ./exread1.sh
```
## OUTPUT
![image](https://github.com/user-attachments/assets/63318ff9-3094-4b4f-9707-7be7435e4c3b)


```
cat > funcex.sh
```
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
```
./funcex.sh 
./funcex.sh 1 2
```
## OUTPUT
![image](https://github.com/user-attachments/assets/e5cf2454-79cf-499a-a29a-fc218eb47c94)


``` 
cat > argshift.sh
```
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
```
$ chmod 777 argshift.sh
$ ./argshift.sh 1 2 3
```
## OUTPUT
![image](https://github.com/user-attachments/assets/e1827cf1-9986-4771-8cf5-f68ad9a64989)


```
cat > argshift1.sh
```
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
```
$ chmod 777 argshift1.sh
$ ./argshift1.sh 1 2 3
```
## OUTPUT
![image](https://github.com/user-attachments/assets/b55ed68f-27d3-40c5-9c61-39e78b824c50)

```
cat > argshift.sh
```
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
```
chmod 777 argshift.sh
./argshift.sh 1 2 3
```
## OUTPUT
![image](https://github.com/user-attachments/assets/c174acbe-d73b-4868-b4fe-2407d0f46bed)

```
cat > nc.awk
```
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
```
cat>data.dat
```
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
```
awk -f nc.awk data.dat
```
## OUTPUT 
![image](https://github.com/user-attachments/assets/4c7ff8ca-321d-4f68-9c1a-bd69ca99f427)


```
cat > palindrome.sh
```
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
```
bash palindrome.sh
```
## OUTPUT 
![image](https://github.com/user-attachments/assets/d12b02da-dc1f-4fbb-be19-6c9fe324f560)


# RESULT:
The Commands are executed successfully.
