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
<img width="252" height="130" alt="Screenshot 2026-10-29 082233" src="https://github.com/user-attachments/assets/3b811565-e07c-4d28-8718-4dbab7a2fb08" />



cat < file2
## OUTPUT
<img width="282" height="147" alt="Screenshot 2026-10-29 082350" src="https://github.com/user-attachments/assets/0aed3c68-35f5-48bb-8d07-f09bd5964917" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="297" height="75" alt="Screenshot 2026-10-29 082422" src="https://github.com/user-attachments/assets/f7765510-7763-4413-9672-76967c65af00" />

diff file1 file2
## OUTPUT
<img width="296" height="255" alt="Screenshot 2026-10-29 082456" src="https://github.com/user-attachments/assets/ef062fde-fe84-4c25-af08-553098fdfdb7" />


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
<img width="235" height="103" alt="Screenshot 2026-10-29 082616" src="https://github.com/user-attachments/assets/7293ab2c-8bf0-4c02-93e8-b861124a3201" />




cut -d "|" -f 1 file22
## OUTPUT



cut -d "|" -f 2 file22
## OUTPUT


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
<img width="227" height="71" alt="Screenshot 2026-10-29 082738" src="https://github.com/user-attachments/assets/50271af4-0f10-496a-b0ad-28758e43215c" />



grep hello newfile 
## OUTPUT
<img width="257" height="82" alt="Screenshot 2026-10-29 082759" src="https://github.com/user-attachments/assets/56608238-05a2-49ec-a753-a5833bc736c9" />




grep -v hello newfile 
## OUTPUT

<img width="257" height="82" alt="Screenshot 2026-10-29 082759" src="https://github.com/user-attachments/assets/0ec4679f-fd2c-4eaa-a76e-25f9ed47e2af" />


cat newfile | grep -i "hello"
## OUTPUT
<img width="305" height="85" alt="Screenshot 2026-10-29 082824" src="https://github.com/user-attachments/assets/da3b9ba2-94d8-4bd7-8b58-f8233481d113" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="340" height="65" alt="Screenshot 2026-10-29 082845" src="https://github.com/user-attachments/assets/7b2e24ec-d0e3-4ee3-ba79-36fa71152d17" />



grep -R ubuntu /etc
## OUTPUT

<img width="612" height="413" alt="Screenshot 2026-10-29 082957" src="https://github.com/user-attachments/assets/a45b72eb-c766-4728-bd73-6d7752764c71" />


grep -w -n world newfile   
## OUTPUT
<img width="245" height="82" alt="Screenshot 2026-10-29 083441" src="https://github.com/user-attachments/assets/2c5763d7-5104-4ce1-8ed0-22e9aa4ff03f" />


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

<img width="308" height="82" alt="Screenshot 2026-10-29 083608" src="https://github.com/user-attachments/assets/c5baf93f-97d9-4be5-b7b7-266f123d62f4" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="317" height="77" alt="Screenshot 2026-10-29 083649" src="https://github.com/user-attachments/assets/e3756f9c-e9f2-4298-9b4c-71ece3c5fbc2" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="317" height="77" alt="Screenshot 2026-10-29 083649" src="https://github.com/user-attachments/assets/c0719a4e-c488-4eb1-ab0a-71bf99d936b5" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="246" height="65" alt="Screenshot 2026-10-29 083704" src="https://github.com/user-attachments/assets/541635ca-bb9a-42b8-812b-92fcc16869cc" />


egrep '(world$)' newfile 
## OUTPUT
<img width="252" height="63" alt="Screenshot 2026-10-29 083747" src="https://github.com/user-attachments/assets/f0709897-07c1-403e-8448-7e0fcd99fafa" />



egrep '(World$)' newfile 
## OUTPUT
<img width="302" height="101" alt="Screenshot 2026-10-29 083814" src="https://github.com/user-attachments/assets/84123b2b-10af-4369-aa31-64a3e63d53a1" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="302" height="101" alt="Screenshot 2026-10-29 083814" src="https://github.com/user-attachments/assets/6ffa2993-1d56-4825-9e6a-ec9d2445425f" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="247" height="70" alt="Screenshot 2026-10-29 083831" src="https://github.com/user-attachments/assets/c4ed25f9-e18b-4098-9064-2999aaf88a5c" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="288" height="63" alt="Screenshot 2026-10-29 083847" src="https://github.com/user-attachments/assets/99cc4dbf-da02-496e-a5a5-7295ce526cc1" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="288" height="72" alt="Screenshot 2026-10-29 083914" src="https://github.com/user-attachments/assets/f892d1dc-6b61-4e47-925e-53090491af8b" />


egrep l{2} newfile
## OUTPUT

<img width="223" height="87" alt="Screenshot 2026-10-29 083931" src="https://github.com/user-attachments/assets/a4e40640-f897-49a6-92aa-858e7aa3a26e" />


egrep 's{1,2}' newfile
## OUTPUT 


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

<img width="240" height="71" alt="Screenshot 2026-10-29 084022" src="https://github.com/user-attachments/assets/9e4024fe-1bb7-4f9f-865a-885cd981b582" />


sed -n -e '$p' file23
## OUTPUT

<img width="262" height="67" alt="Screenshot 2026-10-29 084041" src="https://github.com/user-attachments/assets/51943da3-bf86-40b7-8422-04b57841b24a" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="317" height="190" alt="Screenshot 2026-10-29 084055" src="https://github.com/user-attachments/assets/9babb96e-3bb3-441d-a5ee-e35bf3767a2d" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="281" height="188" alt="Screenshot 2026-10-29 084110" src="https://github.com/user-attachments/assets/bc299854-e8b4-43c7-9dd9-aeb1b42721b1" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="332" height="193" alt="Screenshot 2026-10-29 084125" src="https://github.com/user-attachments/assets/f607f9d1-5c65-4e92-8fd6-173a56c4c5c4" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="265" height="137" alt="Screenshot 2026-10-29 084139" src="https://github.com/user-attachments/assets/6ebf6a95-efa1-463c-8dcb-2b4b6271d3e8" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="277" height="102" alt="Screenshot 2026-10-29 084154" src="https://github.com/user-attachments/assets/72cea315-62d3-4c59-87d7-351787aa8a0b" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


<img width="311" height="87" alt="Screenshot 2026-10-29 084211" src="https://github.com/user-attachments/assets/d9b7179c-bbe6-4dbc-b09c-db5d244a43f8" />


seq 10 
## OUTPUT

<img width="252" height="212" alt="Screenshot 2026-10-29 084226" src="https://github.com/user-attachments/assets/0a482306-2f55-436d-b235-961c21aa167d" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="231" height="102" alt="Screenshot 2026-10-29 084238" src="https://github.com/user-attachments/assets/2b3bfa3c-611a-479c-9420-4e18fa625465" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="237" height="100" alt="Screenshot 2026-10-29 084254" src="https://github.com/user-attachments/assets/6b844f03-576e-4c8d-90df-b6a21f6087ce" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="241" height="111" alt="Screenshot 2026-10-29 084309" src="https://github.com/user-attachments/assets/43fa2c7a-3a36-4ca2-84d5-78ac70b00915" />



seq 2 | sed '2i hello'
## OUTPUT

<img width="228" height="93" alt="Screenshot 2026-10-29 084328" src="https://github.com/user-attachments/assets/60750b0c-1d1e-4efb-958a-db19ef302b9f" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="260" height="96" alt="Screenshot 2026-10-29 084358" src="https://github.com/user-attachments/assets/875f50e0-7fe7-4db4-8e7a-373b27b83315" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="321" height="108" alt="Screenshot 2026-10-29 084413" src="https://github.com/user-attachments/assets/09e10df6-4955-409e-bfaa-a3d3dbaa6700" />



sed -n '2,4{s/$/*/;p}' file23
<img width="305" height="105" alt="Screenshot 2026-10-29 084429" src="https://github.com/user-attachments/assets/9c72a673-86eb-4316-afe1-1a4c63138c4f" />


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
<img width="265" height="127" alt="Screenshot 2026-10-29 084507" src="https://github.com/user-attachments/assets/773fa4ad-db5d-489b-a41c-3f37c75dfd48" />


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

<img width="258" height="132" alt="Screenshot 2026-10-29 084545" src="https://github.com/user-attachments/assets/191899bb-e4d8-4cfe-acfe-91d5f67bde7a" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="336" height="183" alt="Screenshot 2026-10-29 084608" src="https://github.com/user-attachments/assets/8b78eb41-2a36-4353-86a4-3bb2335a0c5b" />

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
<img width="310" height="95" alt="Screenshot 2026-10-29 084703" src="https://github.com/user-attachments/assets/447dceb1-2e46-4665-a4cf-6fd38abbee4b" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="367" height="97" alt="Screenshot 2026-10-29 084722" src="https://github.com/user-attachments/assets/09863871-ca10-4736-9d6d-080319025f6a" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="458" height="86" alt="Screenshot 2026-10-29 084803" src="https://github.com/user-attachments/assets/111dc889-5457-4ea0-8876-9a0c28358740" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 
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

<img width="250" height="92" alt="Screenshot 2026-10-29 212737" src="https://github.com/user-attachments/assets/ea9c04b3-5ea9-4d18-9010-f92ab1f9c860" />

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

 <img width="328" height="240" alt="Screenshot 2026-10-29 212854" src="https://github.com/user-attachments/assets/74990b29-474e-4d49-82eb-f0c7a3afe3b4" />

ls file1
## OUTPUT
<img width="235" height="63" alt="Screenshot 2026-10-29 212955" src="https://github.com/user-attachments/assets/ccfd9f28-ac00-4ec8-96c7-d8a744f3de6c" />

echo $?
## OUTPUT 
<img width="245" height="67" alt="Screenshot 2026-10-29 213010" src="https://github.com/user-attachments/assets/dc0ede5c-bb13-4187-a7fc-001b1c6d12f3" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="207" height="58" alt="Screenshot 2026-10-29 213050" src="https://github.com/user-attachments/assets/950c7e53-8beb-4a6c-b801-c773247baec2" />

abcd
 
echo $?
 ## OUTPUT
<img width="207" height="58" alt="Screenshot 2026-10-29 213050" src="https://github.com/user-attachments/assets/c302f532-8e4b-492e-ae72-c7e5a0ca1284" />


 
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
<img width="317" height="206" alt="Screenshot 2026-10-29 213157" src="https://github.com/user-attachments/assets/e9e10c82-b7ed-4fa7-83a7-21c02cd10bab" />



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
<img width="862" height="283" alt="image" src="https://github.com/user-attachments/assets/c9397d5e-2e0f-4d66-9176-9885954cf420" />

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

<img width="766" height="698" alt="image" src="https://github.com/user-attachments/assets/9e19b428-b4ec-4666-b25d-3f19b367120f" />


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
<img width="726" height="501" alt="image" src="https://github.com/user-attachments/assets/2446b932-ae82-4e36-9b9f-8c83b4bc34a9" />

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

<img width="725" height="236" alt="image" src="https://github.com/user-attachments/assets/b33a77ac-2a1a-4f5a-998a-4ee23ace152f" />

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
<img width="775" height="240" alt="image" src="https://github.com/user-attachments/assets/8118b329-1d43-4cf1-90c3-03686707358a" />

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
 <img width="655" height="587" alt="image" src="https://github.com/user-attachments/assets/be5727ea-fa7f-4a54-99b6-3cad52292f35" />

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
 
 <img width="758" height="381" alt="image" src="https://github.com/user-attachments/assets/5676134c-cefc-4ccc-99af-0aa609532df8" />

 
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
 <img width="757" height="456" alt="image" src="https://github.com/user-attachments/assets/d2e8dc58-ade4-4212-a45d-13e11bd08c87" />

 
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
 <img width="770" height="347" alt="image" src="https://github.com/user-attachments/assets/7c833e85-e3c8-479d-9a8b-918627166834" />

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
 <img width="350" height="123" alt="image" src="https://github.com/user-attachments/assets/56d13ac4-e9fa-4035-b552-7e1218009bb3" />

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
 <img width="307" height="66" alt="image" src="https://github.com/user-attachments/assets/7a3907bc-dddb-4be2-bafe-42399d2644d9" />

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

<img width="636" height="181" alt="image" src="https://github.com/user-attachments/assets/9225bc8b-5c5b-448b-9874-ad4252d50f40" />

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
<img width="197" height="132" alt="image" src="https://github.com/user-attachments/assets/b178b35c-0fe0-4233-ad5c-b10bb39ca29a" />

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

 <img width="255" height="238" alt="image" src="https://github.com/user-attachments/assets/481db769-3344-4637-906e-4d807deafc09" />

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
 <img width="592" height="97" alt="image" src="https://github.com/user-attachments/assets/764492f9-5f61-4ec1-9ec0-dd7483e7a9c1" />

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
 <img width="597" height="130" alt="image" src="https://github.com/user-attachments/assets/81706515-8ba5-4887-9c0d-9b7c493917d5" />

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

<img width="315" height="83" alt="image" src="https://github.com/user-attachments/assets/4c66f0d5-7299-4dd7-a45a-298c6a74a8e7" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="315" height="83" alt="image" src="https://github.com/user-attachments/assets/a9651698-3379-4eb2-bc8e-66b0286c195c" />



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
 <img width="225" height="95" alt="image" src="https://github.com/user-attachments/assets/69b5a361-baeb-4b46-9f15-dfe1a6ed7bf8" />

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
 <img width="225" height="95" alt="image" src="https://github.com/user-attachments/assets/8ea77437-a229-495a-8c03-b80911ffa5c3" />

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
 <img width="327" height="252" alt="image" src="https://github.com/user-attachments/assets/94d32fdc-66ff-405e-9486-1bf013bd0771" />

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
<img width="237" height="100" alt="image" src="https://github.com/user-attachments/assets/7177ba7b-0a0e-424b-85bc-9d5e73ea4d91" />


# RESULT:
The Commands are executed successfully.
