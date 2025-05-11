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
![image](https://github.com/user-attachments/assets/a21cd413-756b-4ffb-99ea-8f6d5ba27d94)




cat < file2
## OUTPUT

![image](https://github.com/user-attachments/assets/cd0d0a86-86e4-4426-a251-c8cae3714bc4)

# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/user-attachments/assets/c36791e3-6794-4a3b-9da0-28f1ce79b036)

comm file1 file2
 ## OUTPUT
![image](https://github.com/user-attachments/assets/08491b13-5d77-486d-8b8d-bf5cc5632492)

 
diff file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/d57e52da-7ede-429f-a225-757ec292e246)


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


![image](https://github.com/user-attachments/assets/2525a96e-4df1-4f99-8f06-5612a34b93c4)


cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/user-attachments/assets/34bd68b3-1a1c-4f23-8091-c101ad1163e6)


cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/5d1e2611-d510-450c-a3a1-db52b6b041cf)


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
![image](https://github.com/user-attachments/assets/1b838a58-27c8-4d75-96b4-68a5ca4d2e5b)



grep hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/f008381c-a48c-41b2-a6e0-f69fb3d2001e)



grep -v hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/ae428571-7736-46a9-ae4e-fce2add170ac)


cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/3a07b800-c5db-4293-aec7-19b79d5a4a53)



cat newfile | grep -i -c "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/7f9bdacb-f29c-42c7-be6a-e4ff69e4d813)



grep -R ubuntu /etc
## OUTPUT

![image](https://github.com/user-attachments/assets/538b8bc9-72a9-4568-a188-871a37c2251f)


grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/ae553da6-08c9-4fe9-9de5-f613eefc2e4a)


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

![image](https://github.com/user-attachments/assets/0f904de1-bb3a-470a-97b5-d10d2c3e46a7)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/ca363916-8f39-49c8-a2c4-46c103cef303)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/ffe71348-e1d5-4f2b-aa04-f4de7b6898df)



egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/27f1975c-b89c-4e65-8d72-e74e80eddb7d)


egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/75bbd450-cfbd-446b-a136-608bb8d35dbf)


egrep '(World$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/85daa668-7f28-4791-91de-e07252f51cc1)

egrep '((W|w)orld$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/b5db41b1-13bd-4272-bccb-173f5c020d0e)

egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/b607d33e-3636-410a-ad57-e7903f0629b0)


egrep 'Linux.*world' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/dc735f98-4506-4771-aa2c-79db38c57cad)

egrep 'Linux.*World' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/b31d0a96-3d43-4c54-a5e2-47c01696bb2f)

egrep l{2} newfile
## OUTPUT

![image](https://github.com/user-attachments/assets/0c42375b-4536-4572-81bc-a48bdc99062b)


egrep 's{1,2}' newfile
## OUTPUT 

![image](https://github.com/user-attachments/assets/00a38667-9432-41d9-92bb-e767caa85d41)

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

![image](https://github.com/user-attachments/assets/68a4009c-febf-4393-bd13-893a3d706b3a)


sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/732c9b02-94c4-42e5-b86c-f2f58ba2a72d)



sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/697245ea-76d9-42ff-8969-32968f0645f0)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/3ca55e50-9322-49f9-80ae-73099351c4d5)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/fbc17806-e9dd-4bd3-8498-3ce05fd27bb7)


sed -n -e '1,5p' file23
## OUTPUT



![image](https://github.com/user-attachments/assets/3d446092-c0d6-4fa7-84d0-77e4da1a0a64)


sed -n -e '2,/Joe/p' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/2045aee7-b01a-4cfa-8011-36db0d4259b7)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/506eedd8-7be9-4af4-997c-2263a2fc0061)


seq 10 
## OUTPUT


![image](https://github.com/user-attachments/assets/f6b5ba78-88c5-4d30-abc7-8ccae77a4500)


seq 10 | sed -n '4,6p'
## OUTPUT


![image](https://github.com/user-attachments/assets/d15d0f8f-f8a1-4cb1-978b-b339ec845507)


seq 10 | sed -n '2,~4p'
## OUTPUT


![image](https://github.com/user-attachments/assets/ce0e5476-0656-4682-888e-112b43391099)


seq 3 | sed '2a hello'
## OUTPUT


![image](https://github.com/user-attachments/assets/59469e6e-6e55-44af-b0e1-91174d97a3ee)


seq 2 | sed '2i hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/d0aaf5f3-39c7-4f56-ad03-2d3cd824deab)


seq 10 | sed '2,9c hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/8b54a33e-467f-4684-bad4-6a540722151d)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/8b7cf8b2-3d74-4742-af09-83b029bd5257)



sed -n '2,4{s/$/*/;p}' file23



![image](https://github.com/user-attachments/assets/d094bac3-7eaa-43fb-a705-f617754f70f2)


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

![image](https://github.com/user-attachments/assets/23d232f4-dcbb-4452-a30e-c61524927bc6)


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



![image](https://github.com/user-attachments/assets/8a6b37c3-58a4-44ab-8977-393e61f65c09)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![image](https://github.com/user-attachments/assets/757d6afa-2879-4b45-87dc-247724903854)

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


![image](https://github.com/user-attachments/assets/8093b76e-8ec1-4854-9212-0b1b55ba393c)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT


![image](https://github.com/user-attachments/assets/4fb7c62d-e10b-49b3-8879-93deafc0a13b)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![image](https://github.com/user-attachments/assets/0734905e-7fdf-4212-8c12-7dfa99334da7)


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


![image](https://github.com/user-attachments/assets/cc9d318b-6584-42ef-9a5e-703687850181)

tar -xvf backup.tar
## OUTPUT

![image](https://github.com/user-attachments/assets/7a2b0709-3d97-414e-a080-48c2d19fb199)

gzip backup.tar

ls .gz
## OUTPUT

 ![image](https://github.com/user-attachments/assets/31a575bf-4f14-4bc9-98c6-f7e0fa558acf)

gunzip backup.tar.gz
## OUTPUT

![image](https://github.com/user-attachments/assets/5d72b698-60e4-4364-89cf-75601e0f0feb)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT


 ![image](https://github.com/user-attachments/assets/ac307fc9-b780-40da-8160-58174a21fb56)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![image](https://github.com/user-attachments/assets/d1349096-6bec-4517-9a41-e937c8961174)


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

![image](https://github.com/user-attachments/assets/a79e0830-9db8-4cb2-81d9-610b07347b82)

 
ls file1
## OUTPUT

![image](https://github.com/user-attachments/assets/2333ffd9-4c00-46dd-85c1-1bb01cc1366c)

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied


![image](https://github.com/user-attachments/assets/be62da5b-059e-4923-9eaa-ea118015f0db)
 
abcd
 
echo $?
 ## OUTPUT


![image](https://github.com/user-attachments/assets/173473e4-04fa-4dcb-a459-9dadcfe7933b)

 
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
## OUTPUT



![image](https://github.com/user-attachments/assets/ff67a5cf-7dc2-4855-a2df-8f968c389378)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


![image](https://github.com/user-attachments/assets/bb400efe-ffd6-47ca-aca0-eb291721dd4e)



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



![image](https://github.com/user-attachments/assets/7ceca6d4-c92b-41ae-b1f0-4f822fc41719)



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


![image](https://github.com/user-attachments/assets/eaf06629-7f96-4b2b-82a7-48f85d6c6a28)



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
## OUTPUT

![image](https://github.com/user-attachments/assets/fd049eeb-065a-4e76-84e1-e29f0651fd67)

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
## OUTPUT
![image](https://github.com/user-attachments/assets/2d068ed0-9a39-4d66-a568-459a3e1e26f2)

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
![image](https://github.com/user-attachments/assets/7073032d-a532-42ca-8d04-10d709458b3b)


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
![image](https://github.com/user-attachments/assets/9e9a9052-cb38-47ee-83ea-22b49770bc3b)

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
![image](https://github.com/user-attachments/assets/94e83bc8-b7be-4662-b6be-a5b516f441d7)
 
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
![image](https://github.com/user-attachments/assets/55280fd3-21a8-4c3e-b593-334f1789f278)
 
 
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
 
![image](https://github.com/user-attachments/assets/9120e2fa-00d7-411d-a963-98c74c7bc748)
 
 
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
 
 ![image](https://github.com/user-attachments/assets/f1703d79-0729-4271-ba91-bb82ade61d9c)

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
![image](https://github.com/user-attachments/assets/860bbaf2-cb5b-4c7c-af46-0e328a7e0d04)
 
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
 ![image](https://github.com/user-attachments/assets/1abc2e20-0d7e-4740-a6ba-c7f7e6f931b8)

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

![image](https://github.com/user-attachments/assets/454f6e16-5c57-4ec1-9d2d-6aa10470b176)

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
![image](https://github.com/user-attachments/assets/ffcc5c71-87d6-45d1-be9c-e24c94556653)

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
![image](https://github.com/user-attachments/assets/73d5361f-5604-444f-b9e1-45611371a092)

 
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
![image](https://github.com/user-attachments/assets/4de6184e-9ceb-43ab-a8fd-cd4df9dd6132)

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
 ![image](https://github.com/user-attachments/assets/09ae4f33-cf8e-4468-93d7-a1dc19f5b689)

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

![image](https://github.com/user-attachments/assets/c05786a9-5558-41ee-82e9-e5d30817ed42)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![image](https://github.com/user-attachments/assets/40af8925-516f-4077-9d8d-cffb9ec55b08)


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
 ![image](https://github.com/user-attachments/assets/efef5ba9-b088-430a-847a-c1ca8d18fdc1)

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
 ![image](https://github.com/user-attachments/assets/c42131b9-6ac4-486e-a997-507f0701dcdc)

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

![image](https://github.com/user-attachments/assets/388fd81a-63ea-4c2a-ad88-f8d532f48869)

# RESULT:
The Commands are executed successfully.
