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
<img width="341" height="155" alt="Screenshot 2026-07-29 180337" src="https://github.com/user-attachments/assets/0654875e-7b76-4ef2-b6a0-ba4c020a40d9" />




cat < file2
## OUTPUT
<img width="282" height="182" alt="Screenshot 2026-07-29 180353" src="https://github.com/user-attachments/assets/c4b1bc40-ccce-4e33-90df-58a30a5402d8" />



# Comparing Files
cmp file1 file2
## OUTPUT

<img width="392" height="98" alt="Screenshot 2026-07-29 180415" src="https://github.com/user-attachments/assets/727d1266-3483-4cf1-bfc6-e699f45438c4" />

comm file1 file2
 ## OUTPUT

<img width="392" height="280" alt="Screenshot 2026-07-29 180426" src="https://github.com/user-attachments/assets/01b1b5eb-128b-4d8e-957c-0a8283eb18b3" />

 
diff file1 file2
## OUTPUT
<img width="392" height="280" alt="Screenshot 2026-07-29 180426" src="https://github.com/user-attachments/assets/cc28be10-0f27-48fd-97c4-1871a1827042" />



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

<img width="332" height="132" alt="Screenshot 2026-07-29 183157" src="https://github.com/user-attachments/assets/94112514-87de-4a75-b48d-286ce96e770a" />





cut -d "|" -f 1 file22
## OUTPUT

<img width="406" height="155" alt="Screenshot 2026-07-29 183211" src="https://github.com/user-attachments/assets/cb622ddc-d809-4e84-aef9-089c47401bcd" />



cut -d "|" -f 2 file22
## OUTPUT

<img width="432" height="160" alt="Screenshot 2026-07-29 183218" src="https://github.com/user-attachments/assets/27b65306-5fe0-445c-aabb-d9b036ce8976" />



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
<img width="307" height="82" alt="Screenshot 2026-07-29 183514" src="https://github.com/user-attachments/assets/22d8d80e-b1c6-474e-82be-cf1cfcd63eb2" />





grep hello newfile 
## OUTPUT

<img width="300" height="82" alt="Screenshot 2026-07-29 183522" src="https://github.com/user-attachments/assets/cb5da2cd-aa1c-456c-aa74-884ce5f20b71" />





grep -v hello newfile 
## OUTPUT

<img width="405" height="100" alt="Screenshot 2026-07-29 183528" src="https://github.com/user-attachments/assets/9f3b3df3-c903-401a-8a5d-fdf4625e86a5" />




cat newfile | grep -i "hello"
## OUTPUT


<img width="415" height="101" alt="Screenshot 2026-07-29 183535" src="https://github.com/user-attachments/assets/d4050853-c972-42e0-9060-7073a5d3768f" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="457" height="78" alt="Screenshot 2026-07-29 183553" src="https://github.com/user-attachments/assets/6fdb9927-cdc9-433c-99d9-2af7ecb64bfc" />





grep -R ubuntu /etc
## OUTPUT


<img width="1743" height="710" alt="Screenshot 2026-07-29 183956" src="https://github.com/user-attachments/assets/1a3306b5-309b-4ab0-8258-897b299b4579" />




grep -w -n world newfile   
## OUTPUT




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


<img width="400" height="97" alt="Screenshot 2026-07-29 184703" src="https://github.com/user-attachments/assets/fe4e1cc1-4924-40a9-8dcf-8a0d1b770b07" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="388" height="111" alt="Screenshot 2026-07-29 184711" src="https://github.com/user-attachments/assets/2f0ca7c1-dc06-4ae8-86e7-20417fc01cb5" />





egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="417" height="117" alt="Screenshot 2026-07-29 190555" src="https://github.com/user-attachments/assets/2dab3d04-7ed9-40e0-8795-afffcfe2c640" />





egrep '(^hello)' newfile 
## OUTPUT

<img width="377" height="85" alt="Screenshot 2026-07-29 184723" src="https://github.com/user-attachments/assets/1ea2abc9-4263-43ce-8e77-389caf365d6c" />




egrep '(world$)' newfile 
## OUTPUT

<img width="370" height="97" alt="Screenshot 2026-07-29 184732" src="https://github.com/user-attachments/assets/99fcaa42-d3ea-4054-9640-c0d12dce2e55" />




egrep '(World$)' newfile 
## OUTPUT

<img width="368" height="90" alt="Screenshot 2026-07-29 184740" src="https://github.com/user-attachments/assets/563ced42-4caa-47dd-839d-a3d63a104fb3" />



egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="423" height="135" alt="Screenshot 2026-07-29 184747" src="https://github.com/user-attachments/assets/160ec735-ec0a-4b95-94ba-77d97344919d" />




egrep '[1-9]' newfile 
## OUTPUT

<img width="325" height="76" alt="Screenshot 2026-07-29 184754" src="https://github.com/user-attachments/assets/99798eab-b1d6-4290-9b4d-d0bb7f9d09e6" />





egrep 'Linux.*world' newfile 
## OUTPUT

<img width="391" height="87" alt="Screenshot 2026-07-29 185200" src="https://github.com/user-attachments/assets/26d45d1e-018b-4112-8082-173b9bdbc088" />







egrep 'Linux.*World' newfile 
## OUTPUT

<img width="385" height="85" alt="Screenshot 2026-07-29 185207" src="https://github.com/user-attachments/assets/5a3accae-2256-4daa-8d1f-cb1b0af72a2a" />




egrep l{2} newfile
## OUTPUT


<img width="342" height="115" alt="Screenshot 2026-07-29 185213" src="https://github.com/user-attachments/assets/752495a8-e2fa-43eb-9b43-194592450612" />



egrep 's{1,2}' newfile
## OUTPUT 


<img width="366" height="132" alt="Screenshot 2026-07-29 185220" src="https://github.com/user-attachments/assets/7dd45b8d-4de4-4225-8645-519807b8834d" />


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





sed -n -e '$p' file23
## OUTPUT

<img width="375" height="92" alt="Screenshot 2026-07-29 190518" src="https://github.com/user-attachments/assets/9ef56f07-9d59-4d7b-a019-8b98bf1ef27c" />




sed  -e 's/Ram/Sita/' file23
## OUTPUT


<img width="387" height="282" alt="Screenshot 2026-07-29 190524" src="https://github.com/user-attachments/assets/81a86ba0-b78f-4f2f-a831-ee1f65c4745b" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="392" height="277" alt="Screenshot 2026-07-29 190532" src="https://github.com/user-attachments/assets/6add52ad-33fe-4cba-a94c-ebb0041a635c" />




sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="455" height="272" alt="Screenshot 2026-07-29 190602" src="https://github.com/user-attachments/assets/00afb997-235f-493d-b414-a76560d259be" />




sed -n -e '1,5p' file23
## OUTPUT
<img width="381" height="182" alt="Screenshot 2026-07-29 190609" src="https://github.com/user-attachments/assets/66aef699-214a-44c3-b9a8-792c1c9393d8" />





sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="380" height="141" alt="Screenshot 2026-07-29 190635" src="https://github.com/user-attachments/assets/0a8232a2-13b4-4dbc-8887-f47f017dbf8e" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="437" height="117" alt="Screenshot 2026-07-29 190640" src="https://github.com/user-attachments/assets/f428511a-5864-45ba-af29-b89f15551af2" />




seq 10 
## OUTPUT

<img width="400" height="311" alt="Screenshot 2026-07-29 190647" src="https://github.com/user-attachments/assets/d4d5cf1d-d558-4280-bfcb-40c3b333fc80" />




seq 10 | sed -n '4,6p'
## OUTPUT

<img width="341" height="128" alt="Screenshot 2026-07-29 190655" src="https://github.com/user-attachments/assets/232a10e6-9e69-4499-bf2e-0b4864be947f" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="355" height="135" alt="Screenshot 2026-07-29 190701" src="https://github.com/user-attachments/assets/a9d8fc53-a6fe-4c2f-bc43-726a097f2ec7" />




seq 3 | sed '2a hello'
## OUTPUT
<img width="362" height="161" alt="Screenshot 2026-07-29 190707" src="https://github.com/user-attachments/assets/f02a9a5b-85f0-42d2-a6f0-6b4f7a606588" />





seq 2 | sed '2i hello'
## OUTPUT

<img width="356" height="140" alt="Screenshot 2026-07-29 190713" src="https://github.com/user-attachments/assets/5bc73ca7-ff35-41d4-881a-5c9134816476" />



seq 10 | sed '2,9c hello'
## OUTPUT
<img width="426" height="132" alt="Screenshot 2026-07-29 190741" src="https://github.com/user-attachments/assets/bef010e7-7e8c-4a49-9b09-0c4945e2b137" />



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


<img width="406" height="128" alt="Screenshot 2026-07-29 190749" src="https://github.com/user-attachments/assets/b707a9b6-6ec3-4b60-b51f-4238151b0811" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="393" height="133" alt="Screenshot 2026-07-29 190756" src="https://github.com/user-attachments/assets/69612b26-beb7-4911-9eea-03519ab87a46" />



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

<img width="392" height="152" alt="Screenshot 2026-07-29 192622" src="https://github.com/user-attachments/assets/d2a9d299-0fa4-453d-97c2-05e02659d13d" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="537" height="156" alt="Screenshot 2026-07-29 192639" src="https://github.com/user-attachments/assets/bd28e4f1-4331-4fb1-985c-546efd570d67" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="412" height="257" alt="Screenshot 2026-07-29 192646" src="https://github.com/user-attachments/assets/f783b80a-29b6-4572-bb39-f8d87f131b25" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="655" height="508" alt="Screenshot 2026-07-29 192701" src="https://github.com/user-attachments/assets/7d3e732d-f9a8-4f49-9baa-9481acb1d311" />


tar -xvf backup.tar
## OUTPUT
<img width="432" height="265" alt="Screenshot 2026-07-29 192711" src="https://github.com/user-attachments/assets/b271fefb-a48d-4c13-85b1-ce7e50d20d2a" />

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT
<img width="835" height="392" alt="Screenshot 2026-07-29 192719" src="https://github.com/user-attachments/assets/96e5fa23-d91b-4f7f-b843-cb044d01788b" />

 
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
