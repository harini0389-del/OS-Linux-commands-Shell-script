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
cat > op1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d


```
cat > op2
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
<img width="481" height="123" alt="image" src="https://github.com/user-attachments/assets/613f9c6e-1573-4707-a684-7e53a9392231" />





cat < file2
## OUTPUT
<img width="590" height="168" alt="image" src="https://github.com/user-attachments/assets/d94734b0-d6ec-43d4-8ed4-e7c4d52970c7" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="372" height="43" alt="image" src="https://github.com/user-attachments/assets/44a0d243-e2d5-4c01-852a-7a67a9fbed8b" />


comm file1 file2
 ## OUTPUT
<img width="447" height="317" alt="image" src="https://github.com/user-attachments/assets/da9227ef-d6e7-4b69-a56d-28ccb68bcaad" />


 
diff file1 file2
## OUTPUT
<img width="430" height="280" alt="image" src="https://github.com/user-attachments/assets/73b85418-ab0d-46fa-adf4-4ef75e8af2cf" />


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
<img width="547" height="442" alt="image" src="https://github.com/user-attachments/assets/327cba51-fdea-42db-9961-7f1268d677aa" />




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
<img width="453" height="36" alt="image" src="https://github.com/user-attachments/assets/0335db48-3fd3-46e6-9db3-e04faaf5697a" />



grep hello newfile 
## OUTPUT
<img width="432" height="37" alt="image" src="https://github.com/user-attachments/assets/ff8ab732-e3a3-44a1-b6ed-21e861992a63" />




grep -v hello newfile 
## OUTPUT
<img width="470" height="40" alt="image" src="https://github.com/user-attachments/assets/843ef410-2473-45a5-b11a-e7babe80b996" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="577" height="92" alt="image" src="https://github.com/user-attachments/assets/333270c6-eb33-4851-bef4-12198115242c" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="576" height="33" alt="image" src="https://github.com/user-attachments/assets/3786ad48-e1ab-4a61-8c15-4f3794f431a5" />




grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
<img width="940" height="36" alt="image" src="https://github.com/user-attachments/assets/8bdb3e84-19a1-4bf2-9aed-28082a205da9" />


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
<img width="518" height="56" alt="image" src="https://github.com/user-attachments/assets/c81ebe3e-3c54-4265-9b60-a04dab699892" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="513" height="52" alt="image" src="https://github.com/user-attachments/assets/fcdea6ea-9657-4732-aa6e-a9737c419fd4" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="557" height="52" alt="image" src="https://github.com/user-attachments/assets/5d174282-3bc5-44ed-a17e-239c0379357c" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="480" height="40" alt="image" src="https://github.com/user-attachments/assets/8182946d-59e9-4ddf-9351-54367f9a6ac0" />



egrep '(world$)' newfile 
## OUTPUT
<img width="325" height="57" alt="image" src="https://github.com/user-attachments/assets/fde3c1c7-8305-4e11-b10a-f618780b2136" />



egrep '(World$)' newfile 
## OUTPUT
<img width="542" height="48" alt="image" src="https://github.com/user-attachments/assets/d87b4673-3ef1-4fb1-97e2-97177d1f5531" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="357" height="57" alt="image" src="https://github.com/user-attachments/assets/8f7189e7-7688-4671-b1c3-8941dc115223" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="452" height="40" alt="image" src="https://github.com/user-attachments/assets/e879cdf7-e818-4b6a-8911-e67d97f1d199" />



egrep 'Linux.*world' newfile 
## OUTPUT

<img width="532" height="52" alt="image" src="https://github.com/user-attachments/assets/9b53a3b7-2033-45a9-bdd1-3d79554603bd" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="496" height="45" alt="image" src="https://github.com/user-attachments/assets/0b72165e-8e33-4cde-8a00-08875beb8820" />


egrep l{2} newfile
## OUTPUT

<img width="940" height="35" alt="image" src="https://github.com/user-attachments/assets/a36793a6-c4d5-4575-82e5-142657c379d0" />



egrep 's{1,2}' newfile
## OUTPUT 

<img width="940" height="46" alt="image" src="https://github.com/user-attachments/assets/3d318ce9-bfff-4531-8b9d-104baff8540f" />


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

<img width="481" height="42" alt="image" src="https://github.com/user-attachments/assets/e1b95a2d-7672-4fec-b5a6-4fb83e38a189" />



sed -n -e '$p' file23
## OUTPUT



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="507" height="187" alt="image" src="https://github.com/user-attachments/assets/c4e52118-afab-4990-9e59-fb02420b73ca" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="515" height="187" alt="image" src="https://github.com/user-attachments/assets/49fade3f-ccec-4997-aef2-dadd457ee814" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="595" height="187" alt="image" src="https://github.com/user-attachments/assets/6cc7765f-f86b-4905-9537-13ef2822b2c8" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="505" height="127" alt="image" src="https://github.com/user-attachments/assets/ded7184d-99de-4eaf-8ac0-e454e7c99c4a" />




sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="577" height="76" alt="image" src="https://github.com/user-attachments/assets/3a451e14-8a57-4e08-8f76-8fa74b72403d" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="537" height="66" alt="image" src="https://github.com/user-attachments/assets/e36dc479-6322-4efd-b186-81bc106e1928" />



seq 10 
## OUTPUT

<img width="431" height="217" alt="image" src="https://github.com/user-attachments/assets/b011736e-4cdc-4e86-8590-5a849f5f9a92" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="482" height="70" alt="image" src="https://github.com/user-attachments/assets/f2d2f959-49b2-4809-b567-0cfe25fcfeb7" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="512" height="76" alt="image" src="https://github.com/user-attachments/assets/e83dbec6-ab45-4a3a-b61a-5e10d175a41e" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="526" height="102" alt="image" src="https://github.com/user-attachments/assets/980e495b-4150-4342-8832-5a822037f1f6" />



seq 2 | sed '2i hello'
## OUTPUT

<img width="485" height="78" alt="image" src="https://github.com/user-attachments/assets/99f51d0b-a30e-4fbc-b092-9e436f6e35f3" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="487" height="78" alt="image" src="https://github.com/user-attachments/assets/3576a43d-60c2-4a3a-9ca6-8ed10774ff90" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

 <img width="550" height="71" alt="image" src="https://github.com/user-attachments/assets/5daf727b-c577-41cd-8b2b-d2f5b66c4225" />



sed -n '2,4{s/$/*/;p}' file23
## Output
<img width="551" height="86" alt="image" src="https://github.com/user-attachments/assets/98d44fbe-03c5-4e7c-b141-136b118509b8" />

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



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="645" height="173" alt="image" src="https://github.com/user-attachments/assets/b03a10be-d9c3-4fec-abdd-e1cffbec81c3" />

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

<img width="542" height="77" alt="image" src="https://github.com/user-attachments/assets/e2d6216e-adfb-4f1b-8078-9f98bae59670" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="655" height="73" alt="image" src="https://github.com/user-attachments/assets/6b81c927-9a83-4067-aad1-1f06392fce63" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT


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

<img width="713" height="42" alt="image" src="https://github.com/user-attachments/assets/103dcdd1-4c7b-4fd5-9938-e6ab80738b45" />



 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="482" height="176" alt="image" src="https://github.com/user-attachments/assets/c10904c0-aceb-4bac-a6ac-4befc15c9d9f" />


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

 
ls op1
## OUTPUT

<img width="940" height="25" alt="image" src="https://github.com/user-attachments/assets/9fc7ce67-fe3c-4660-ab63-51aa222fc719" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied

 <img width="940" height="25" alt="image" src="https://github.com/user-attachments/assets/88468e7b-c47b-4392-af4a-1ab3b9305943" />

echo $?
## OUTPUT 
 <img width="940" height="25" alt="image" src="https://github.com/user-attachments/assets/ad8752b9-b0dd-4b99-b979-d345c4ae34a1" />
 
abcd
 
echo $?
 ## OUTPUT
<img width="940" height="112" alt="image" src="https://github.com/user-attachments/assets/8d1daca9-4cb2-4e57-bd11-15ea8d8a493a" />


 
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
<img width="940" height="26" alt="image" src="https://github.com/user-attachments/assets/a08e41ff-dda4-4ef6-8065-21392e848fe3" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="940" height="117" alt="image" src="https://github.com/user-attachments/assets/df75856a-7ab9-487a-ba13-50afdb7449e5" />


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
<img width="496" height="245" alt="image" src="https://github.com/user-attachments/assets/aa33610a-789f-4708-88b0-fa447af1cb16" />

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
<img width="492" height="310" alt="image" src="https://github.com/user-attachments/assets/2d146244-2949-4fc2-bd27-b5d289f0f9ea" />

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
<img width="542" height="223" alt="image" src="https://github.com/user-attachments/assets/09680f7d-b91b-4404-b072-faf3e77e1342" />

 
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
<img width="761" height="276" alt="image" src="https://github.com/user-attachments/assets/9ae34e59-7657-4c2a-872d-d3f0002ba338" />

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
<img width="877" height="172" alt="image" src="https://github.com/user-attachments/assets/657cf566-8424-421b-91f5-d5b825196613" />


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
<img width="613" height="391" alt="image" src="https://github.com/user-attachments/assets/891f812a-a1dd-40f6-b966-d02eef980671" />

 
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
 <img width="940" height="48" alt="image" src="https://github.com/user-attachments/assets/5878717a-d76d-48a6-85a5-d2a2c36c8c2a" />

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
 
<img width="940" height="148" alt="image" src="https://github.com/user-attachments/assets/adce6900-83b6-4456-beeb-73ac4583fbb3" />

 
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
<img width="531" height="267" alt="image" src="https://github.com/user-attachments/assets/b81506e1-12b9-48c4-8dfd-b76b93308c88" />

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
<img width="738" height="501" alt="image" src="https://github.com/user-attachments/assets/a767a2b2-3be3-4429-9cfc-199331ff33e6" />


# RESULT:
The Commands are executed successfully.
