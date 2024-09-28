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
### Display the content of the files
cat < file1
## OUTPUT
<img width="1581" alt="cat file1" src="https://github.com/user-attachments/assets/362131f4-0b93-42db-8de3-4b46dd9e0329">

cat < file2
## OUTPUT
<img width="1581" alt="cat file2" src="https://github.com/user-attachments/assets/254fda0b-f3fe-4ab1-850b-0e1b1d6c86b0">


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="1593" alt="comp" src="https://github.com/user-attachments/assets/afdc404b-074f-4f1f-9a5c-15822cdf0358">

comm file1 file2
 ## OUTPUT
<img width="1581" alt="comm" src="https://github.com/user-attachments/assets/451e643f-dc7c-4f5a-b338-8621c4d61c9d">


 
diff file1 file2
## OUTPUT
<img width="1581" alt="diff" src="https://github.com/user-attachments/assets/2dfe00e8-e5f6-494a-93ff-b2cddd614f38">



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


cut -c1-3 file11
## OUTPUT

<img width="1581" alt="cut-c1-c3file11" src="https://github.com/user-attachments/assets/dba1108f-63e8-4146-8081-62d31a620e89">


cut -d "|" -f 1 file22
## OUTPUT

<img width="1669" alt="cut-d-f1file22" src="https://github.com/user-attachments/assets/158d0e7d-5731-4e07-b66a-7568a2010a1d">


cut -d "|" -f 2 file22
## OUTPUT
<img width="1669" alt="cut-d-f2file22" src="https://github.com/user-attachments/assets/e488706e-cc75-4eb5-8be1-4fde14b4e688">



cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT

<img width="1669" alt="grepHello" src="https://github.com/user-attachments/assets/13284407-a195-4d2a-9510-a3f52189e5e7">


grep hello newfile 
## OUTPUT

<img width="1669" alt="grep_hello" src="https://github.com/user-attachments/assets/6e551e6a-289f-4b65-8aa7-9cd1467925cf">



grep -v hello newfile 
## OUTPUT
<img width="1669" alt="grep-v" src="https://github.com/user-attachments/assets/05407dad-4679-44a4-9b9a-2fb0f2519ca2">


cat newfile | grep -i "hello"
## OUTPUT

<img width="1781" alt="catgrepi" src="https://github.com/user-attachments/assets/662af053-3840-4f96-b609-e62f82f9ed10">


cat newfile | grep -i -c "hello"
## OUTPUT
<img width="1827" alt="catgrepic" src="https://github.com/user-attachments/assets/d61a0aab-6e3c-42b6-aabf-0a6c02e05d0f">

grep -R ubuntu /etc
## OUTPUT

<img width="1039" alt="grep -r ubuntu" src="https://github.com/user-attachments/assets/92c114c3-d85a-4f22-bee6-54c9bfbb49a2">


grep -w -n world newfile   
## OUTPUT
<img width="1108" alt="grep newworld" src="https://github.com/user-attachments/assets/f048bb7b-cae8-4d77-9ce3-5a916bc57b24">


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT
<img width="1172" alt="egrep1" src="https://github.com/user-attachments/assets/259a843b-891b-4074-8fe4-6fdeb726813d">


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="1172" alt="egrep2" src="https://github.com/user-attachments/assets/e5f13d6c-c86a-4d9e-a7b4-65c6088f0f83">


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="1191" alt="egrep3" src="https://github.com/user-attachments/assets/47892540-3744-4ff4-93de-b95095295206">


egrep '(^hello)' newfile 
## OUTPUT

<img width="1191" alt="egrep4" src="https://github.com/user-attachments/assets/0969740b-d365-4155-8576-8836813ff08c">


egrep '(world$)' newfile 
## OUTPUT
<img width="1191" alt="egrep5" src="https://github.com/user-attachments/assets/5cd35cd0-8a63-45c9-9948-6d85a8e50cfe">



egrep '(World$)' newfile 
## OUTPUT
<img width="1191" alt="egrep6" src="https://github.com/user-attachments/assets/743bc49f-8390-445a-9741-97dceec28e41">



egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="1191" alt="egrep7" src="https://github.com/user-attachments/assets/f486e498-8a1a-45c5-bb93-9d8aea159948">



egrep '[1-9]' newfile 
## OUTPUT
<img width="1191" alt="egrep8" src="https://github.com/user-attachments/assets/b00d240e-fa77-44ba-8c56-e411bdd7a94e">



egrep 'Linux.*world' newfile 
## OUTPUT

<img width="1191" alt="egrep9" src="https://github.com/user-attachments/assets/39f1fd9d-f26e-40e8-a3f0-ca3224fc3ef6">


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="1191" alt="egrep10" src="https://github.com/user-attachments/assets/83b153ef-c2c8-4f97-8e57-0aa1a8ad937a">



egrep l{2} newfile
## OUTPUT
<img width="1191" alt="egrep11" src="https://github.com/user-attachments/assets/07d13f82-acfe-45e0-b431-506f13f0b4f1">


egrep 's{1,2}' newfile
## OUTPUT 

<img width="1191" alt="egrep12" src="https://github.com/user-attachments/assets/32b0399a-5bdb-45c9-a04b-f52f75ac9e29">


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


sed -n -e '3p' file23
## OUTPUT

<img width="1191" alt="sed1" src="https://github.com/user-attachments/assets/9a47732f-ebe2-4bd7-8b18-c7cefc80060f">


sed -n -e '$p' file23
## OUTPUT
<img width="1191" alt="sed2" src="https://github.com/user-attachments/assets/34f22580-ff64-44c6-957d-1028bf0e8a6c">


sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="1191" alt="sed3" src="https://github.com/user-attachments/assets/4b06e822-0183-4a75-b555-dfb53d351199">


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="1191" alt="sed4" src="https://github.com/user-attachments/assets/2f01eb43-aab1-4c22-bd9f-c8a50983f33d">



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="1191" alt="sed5" src="https://github.com/user-attachments/assets/d2dabd6f-6228-45c7-81c9-1c6a129ca4b0">


sed -n -e '1,5p' file23
## OUTPUT

<img width="1191" alt="sed6" src="https://github.com/user-attachments/assets/e022d25d-d4a1-494c-a6e3-a2503fceebb9">


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="1191" alt="sed7" src="https://github.com/user-attachments/assets/d8822e9e-1578-4fd0-8eb2-2cd6954f09ac">



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="1191" alt="sed8" src="https://github.com/user-attachments/assets/73f2cb2d-bf9c-45b5-8ce5-109076e77be6">


seq 10 
## OUTPUT
<img width="1191" alt="seq1" src="https://github.com/user-attachments/assets/6cf006d7-b2ec-4e6a-bba6-e4fe00300428">


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="1191" alt="seq2" src="https://github.com/user-attachments/assets/991bdffa-ae22-42f8-80a4-b69241ae0483">


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="1191" alt="seq3" src="https://github.com/user-attachments/assets/f228db37-4be0-408f-8600-b0325cfbba35">


seq 3 | sed '2a hello'
## OUTPUT
<img width="1191" alt="seq4" src="https://github.com/user-attachments/assets/090b3a6d-b7a1-4237-b5ce-4c12f198f171">


seq 2 | sed '2i hello'
## OUTPUT
<img width="1191" alt="seq5" src="https://github.com/user-attachments/assets/14acbecc-22bd-418e-abf0-e8aa7b68340a">

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="1191" alt="seq6" src="https://github.com/user-attachments/assets/03683764-349e-4aa5-836c-d8c3cb3e5424">



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="1191" alt="seq7" src="https://github.com/user-attachments/assets/61098294-89f6-4dcc-a12f-9d1cd157024c">


sed -n '2,4{s/$/*/;p}' file23


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT

<img width="1191" alt="sort" src="https://github.com/user-attachments/assets/98850437-9560-465d-8de0-9d51935b384f">


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT

<img width="1191" alt="uniq" src="https://github.com/user-attachments/assets/655cf439-9d1e-4100-b8e3-37a94d19534f">


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="1220" alt="catfile23" src="https://github.com/user-attachments/assets/27262b34-1988-49e8-9cab-550d6a5e2cbd">


cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT

<img width="1150" alt="caturl1" src="https://github.com/user-attachments/assets/c65e8b1d-bdfb-4840-832e-cd9a57cfeb46">

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="1262" alt="caturl2" src="https://github.com/user-attachments/assets/9b0e82ff-1682-43f7-a11b-8fdd47363153">


#Backup commands tar -cvf backup.tar *
## OUTPUT
<img width="983" alt="tar1" src="https://github.com/user-attachments/assets/2c2c2bca-3ec2-44a4-a0d0-d7c5750909fb">


 mkdir backupdir

mv backup.tar backupdir
## OUTPUT

<img width="983" alt="mv1" src="https://github.com/user-attachments/assets/837f99e9-1eb2-45d7-ad72-3b833e8a1efa">


tar -xvf backup.tar
## OUTPUT


gzip backup.tar
ls .gz
## OUTPUT
 <img width="983" alt="ls1" src="https://github.com/user-attachments/assets/a0f09165-6de4-4ea9-acf3-80e6c095a16c">

gunzip backup.tar.gz
## OUTPUT
<img width="1112" alt="ls2" src="https://github.com/user-attachments/assets/0fa1d3c0-dfae-47b0-875a-c6ad177332ad">

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="1303" alt="echo1" src="https://github.com/user-attachments/assets/d6db7198-40e4-4f0f-a455-22faa141a41b">

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="1303" alt="catherecheck" src="https://github.com/user-attachments/assets/f4c8241d-c755-4e9f-ad51-96aeed2ff674">


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

 <img width="1303" alt="catscriptcheck" src="https://github.com/user-attachments/assets/24708a63-63cb-4acb-9d3e-208c852fe7af">

ls file1
## OUTPUT
<img width="1303" alt="ls_1" src="https://github.com/user-attachments/assets/a9dd98af-3e09-4389-a8a9-38f57850fe33">



echo $?
## OUTPUT 
<img width="1303" alt="echo_1" src="https://github.com/user-attachments/assets/4fde8e05-bffd-4757-93ee-1733374fbb2b">


./one bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="1303" alt="echo_3" src="https://github.com/user-attachments/assets/d1124941-5575-457b-a14d-be06daaf85d5">

abcd
 
echo $?
 ## OUTPUT

<img width="1303" alt="echo_2" src="https://github.com/user-attachments/assets/b8614af6-82ea-4f13-ab27-5125da2d7e96">

 
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

<img width="1303" alt="cat_Strcmp" src="https://github.com/user-attachments/assets/40d70a1e-399f-40f1-a65b-75818cfcb7c9">


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="1303" alt="strcmp" src="https://github.com/user-attachments/assets/99917387-e43d-4a36-bdb8-74ced954617c">


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

<img width="1303" alt="psswdperm" src="https://github.com/user-attachments/assets/a93791d2-f3b6-4e20-9d10-b47ae97c3fc8">


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

<img width="1303" alt="ifnested" src="https://github.com/user-attachments/assets/8da1519f-d41b-4c56-97ad-78d74c8fd9f4">



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
``
##OUTPUT
<img width="1303" alt="iftest" src="https://github.com/user-attachments/assets/fdca87ff-3ac6-4924-9057-47e953c40410">

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
<img width="1303" alt="ifnested" src="https://github.com/user-attachments/assets/fbe2e3f3-1b26-43b2-bf9d-12a138dc6e41">

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
<img width="1303" alt="elifcheck" src="https://github.com/user-attachments/assets/8f28379b-44bb-49d4-8427-60fd5acc92b0">


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
<img width="1303" alt="ifcompound" src="https://github.com/user-attachments/assets/716a871e-cd58-43aa-903e-b151937b237f">

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
##output
<img width="1303" alt="casecheck" src="https://github.com/user-attachments/assets/26dc5f67-e6e8-4898-8591-a271c6a0f23d">

 
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
##output 
 <img width="1303" alt="whiletest" src="https://github.com/user-attachments/assets/a9ed6b65-6b2b-44eb-9c95-9f92bbff7c26">

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
 
## output 
 <img width="1303" alt="untiltest" src="https://github.com/user-attachments/assets/34dcad28-5fe9-40ea-b0fb-037c009a02fc">

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
## output  
<img width="1303" alt="forin1" src="https://github.com/user-attachments/assets/7cd47d88-bf44-4f4f-a514-211b4338e6bc">

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
 ## output 
 <img width="1303" alt="forin1" src="https://github.com/user-attachments/assets/2aff6d3a-2a19-433a-870d-e4d0c7e1661e">

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
 ## output 
 <img width="1303" alt="forin2" src="https://github.com/user-attachments/assets/6f19fdce-bc6c-412c-a497-515c6e97eb84">

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
 ## output 
 <img width="1303" alt="forin3" src="https://github.com/user-attachments/assets/9f82e18a-9863-4e32-80d7-1e921cddccf5">

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
<img width="1303" alt="forin3" src="https://github.com/user-attachments/assets/b74b3dd3-f810-4596-bdf6-96d68e7e40c4">


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
cat cities Hyderabad Alampur Basara Warangal Adilabad Bhadrachalam Khammam

$ chmod 777 forinfile.sh $./forinfile.sh

## OUTPUT
<img width="1303" alt="forinfile" src="https://github.com/user-attachments/assets/696a6e45-567d-43ed-b7af-32108a22a050">


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
<img width="1303" alt="forctype" src="https://github.com/user-attachments/assets/ac6f6213-b389-4a34-a2ca-13d0c80e8aee">

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
<img width="1303" alt="forctype1" src="https://github.com/user-attachments/assets/4c62fd9b-e001-422a-860d-39653f712012">

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

 <img width="1303" alt="forneseted1" src="https://github.com/user-attachments/assets/77d025c5-ce5a-434c-9307-21aafd195f13">

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
<img width="1303" alt="forbreak" src="https://github.com/user-attachments/assets/4356502c-5264-4ee3-a70f-9983adf9b12c">

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
 <img width="1303" alt="forcontinue" src="https://github.com/user-attachments/assets/714a922c-ab3b-4b42-b5e8-b3669e50ee8e">

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
<img width="1303" alt="funcex" src="https://github.com/user-attachments/assets/4406d770-3d0f-4cdc-8882-559ef6e0fd68">

 
 ./funcex.sh 1 2
<img width="1303" alt="funcex123" src="https://github.com/user-attachments/assets/cc204900-22a4-487e-bd24-7d750cf30e49">

 
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
 <img width="1303" alt="argshift" src="https://github.com/user-attachments/assets/b9f0b025-27b2-4d27-8f66-a1fd40b4207e">

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
 <img width="1303" alt="argshift1" src="https://github.com/user-attachments/assets/7ce626c6-c517-4129-88b0-53b78c630d69">

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
 <img width="1303" alt="argshift3" src="https://github.com/user-attachments/assets/194ae932-867f-4139-8764-48171f1ae2cc">

 
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
 <img width="1303" alt="awk" src="https://github.com/user-attachments/assets/1daedabe-ef36-4be7-8dc1-d03d283376a5">

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
<img width="1303" alt="pallindrome" src="https://github.com/user-attachments/assets/b2528df6-bd6c-4fd8-b3e1-07995a055e6a">


# RESULT:
The Commands are executed successfully.
