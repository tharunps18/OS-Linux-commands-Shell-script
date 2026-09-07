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
<img width="562" height="151" alt="435476566-61cb86e7-1de8-4a77-836f-28e9f721446d" src="https://github.com/user-attachments/assets/5c6ed07a-e99a-406c-b832-4029f9d4d768" />



cat < file2
## OUTPUT
<img width="592" height="167" alt="435476575-2da4c987-aaf4-41c1-906f-0f147a3ee9ee" src="https://github.com/user-attachments/assets/c6263924-ce22-489f-a2f1-254d9aae7112" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="559" height="43" alt="435476586-fa9cec5b-09d6-4895-a3a3-7f9fa6a3e4cc" src="https://github.com/user-attachments/assets/190bff26-257c-4895-b593-bba162597e05" />

comm file1 file2
 ## OUTPUT
<img width="524" height="244" alt="435476591-0be680ec-a7fe-4d61-ae74-1c4f47f1b2e5" src="https://github.com/user-attachments/assets/4ca1344e-5ffe-44ec-add7-0890787c97df" />

 
diff file1 file2
## OUTPUT
<img width="526" height="244" alt="435476601-87d212e9-3c87-4a78-8832-f344af1c8761" src="https://github.com/user-attachments/assets/d258b07b-a710-403d-b7d3-f1952b7fc9e6" />


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
<img width="508" height="67" alt="435484710-a3cb0aba-8b34-4174-a86c-89da961e6933" src="https://github.com/user-attachments/assets/fcfa6361-70ae-4f5a-a173-8ba3127c878c" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="562" height="86" alt="435484722-3cd37e16-b566-4061-81d7-5da5f227b257" src="https://github.com/user-attachments/assets/1b8be800-a4b3-4759-a195-dec582d4fa1c" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="560" height="85" alt="435484727-ba23214d-93da-4329-92b5-a01328cb5095" src="https://github.com/user-attachments/assets/7e17444e-c8a5-4cd6-9d6f-baded951f88a" />


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
<img width="539" height="44" alt="435484735-2d8c5cac-0295-4a24-9c46-9ce9e6c5d238" src="https://github.com/user-attachments/assets/b3057e20-ab8a-459b-af99-6de5ec0e9ef2" />



grep hello newfile 
## OUTPUT
<img width="530" height="47" alt="435484738-08d7f4d3-22f7-4617-9e3d-7607cb0e331a" src="https://github.com/user-attachments/assets/ca92e7a9-0f16-4bcf-b04e-3177ac9c24ee" />




grep -v hello newfile 
## OUTPUT

<img width="552" height="44" alt="435484746-923d5a2a-ad89-4a56-b6ca-b00147ae7e58" src="https://github.com/user-attachments/assets/8357174c-e186-48ca-820a-636073f99a8c" />


cat newfile | grep -i "hello"
## OUTPUT
<img width="595" height="89" alt="435484749-9dd25b79-965d-4a86-a1d6-7dc459cc784d" src="https://github.com/user-attachments/assets/6d949274-3ef0-4c3c-8688-9ce11471cf3d" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="595" height="89" alt="435484749-9dd25b79-965d-4a86-a1d6-7dc459cc784d" src="https://github.com/user-attachments/assets/a6658a89-020d-4c48-9f9f-3435336f9616" />




grep -R ubuntu /etc
## OUTPUT
<img width="599" height="602" alt="435484765-8ff47514-f6a0-441a-9370-7547f742ed7f" src="https://github.com/user-attachments/assets/144ac063-875a-425d-a52f-5a0ffcffceb9" />



grep -w -n world newfile   
## OUTPUT
<img width="589" height="67" alt="435484783-040f3735-330a-46a3-bfb7-a9a47760df80" src="https://github.com/user-attachments/assets/abff3912-85c6-44a8-b5d3-44906cd78191" />


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
<img width="600" height="90" alt="435484784-53054dbe-676f-4ffd-92ca-235d521c6a0d" src="https://github.com/user-attachments/assets/70059bb0-2ee7-4d94-8f16-e30ed00e7c72" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="595" height="86" alt="435484793-d5982c6c-9269-4a80-b41d-952d0123c726" src="https://github.com/user-attachments/assets/0815c606-d8fa-487e-a459-6e76bade12d1" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="600" height="89" alt="435484800-a4e91f55-09a5-422d-9b7f-9e6845749462" src="https://github.com/user-attachments/assets/f785600d-1da7-48d1-af71-c1fb81e52bdf" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="587" height="47" alt="435484809-83b4a680-cbca-4bd0-9543-b68618fe43e2" src="https://github.com/user-attachments/assets/fce21795-a5b4-4310-ae82-40d5ce674d93" />



egrep '(world$)' newfile 
## OUTPUT
<img width="586" height="68" alt="435484816-b6f7da62-1325-4190-901c-68e3a44f5a24" src="https://github.com/user-attachments/assets/83317c2b-79d3-42d0-963a-cfc8200c9721" />



egrep '(World$)' newfile 
## OUTPUT

<img width="594" height="45" alt="435484826-fa8534ad-a787-47db-b4e1-a199d9b7200b" src="https://github.com/user-attachments/assets/6e6751d0-8c39-4722-8909-754789f2c293" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="598" height="112" alt="435484833-e3a96c08-e52b-4572-86d3-eaa202a368cd" src="https://github.com/user-attachments/assets/c2375281-4e10-48d7-9581-3d58cb5ff4c2" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="573" height="53" alt="435484842-416896c5-6137-4628-82e4-38781ce098dc" src="https://github.com/user-attachments/assets/dbe17a4b-89d3-426a-888a-7e04ab39b274" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="591" height="72" alt="435484848-a1a44282-04f8-47bc-a4c4-783f91cb7775" src="https://github.com/user-attachments/assets/c99eedb0-ea39-4167-a2ff-840bf88fe9c7" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="598" height="71" alt="435484853-6b6ac47d-ef35-45fb-a7a6-3de49a9f672c" src="https://github.com/user-attachments/assets/79395cc8-18ec-441f-bdf3-a68c9a467473" />


egrep l{2} newfile
## OUTPUT
<img width="536" height="69" alt="435484858-eab0df42-726c-4ee8-aad6-1bf326baa420" src="https://github.com/user-attachments/assets/37c86662-a830-4633-81a9-d626f8311abc" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="569" height="86" alt="435484865-e4be4a8c-39d6-4823-81dc-ec117b06b362" src="https://github.com/user-attachments/assets/b7fa40af-16fc-4eed-b788-72be1c684870" />


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
<img width="549" height="41" alt="435484888-6026e5a2-9cf5-4f1e-8770-455b97af8b95" src="https://github.com/user-attachments/assets/32a07242-1af4-437f-b8e9-3e4758e4a0cc" />



sed -n -e '$p' file23
## OUTPUT
<img width="553" height="43" alt="435484889-65a07dc7-7e32-4312-a092-249e9a589a1d" src="https://github.com/user-attachments/assets/b75de511-2ba0-495b-a04d-8c3a97e4846c" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="597" height="219" alt="435484891-26628422-48a9-4318-ac3f-86d57322e134" src="https://github.com/user-attachments/assets/2fcffdd3-9650-4285-bf90-f60c8b9ccf9e" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="593" height="221" alt="435484890-159d7aa4-00b3-4fd5-8859-ca560b508daa" src="https://github.com/user-attachments/assets/4d990337-7e96-44a8-89fc-6e43e9e7a344" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="596" height="220" alt="435484903-311ebe12-437a-468d-87c0-f4f2ad03dc2d" src="https://github.com/user-attachments/assets/f9232e0d-827c-4629-966d-3bab3e758926" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="571" height="134" alt="435484912-05f26895-fecc-46ec-9743-371414166fb0" src="https://github.com/user-attachments/assets/0350f000-faa4-4578-99c7-37c16716c249" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="594" height="110" alt="435484915-b0c320ad-c36b-4f48-8934-09eda949854a" src="https://github.com/user-attachments/assets/83a22e73-7975-4733-bd75-cf1640adaa0e" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="596" height="93" alt="435484926-a0a776b6-c4a8-4a2a-9faf-36fcc86998d3" src="https://github.com/user-attachments/assets/a7aa91cd-cc92-49b8-af79-0a1873314994" />



seq 10 
## OUTPUT
<img width="407" height="245" alt="435484929-0cab3a69-1988-41ef-ac84-b7cd2b5c22eb" src="https://github.com/user-attachments/assets/ceee87be-c28f-4d10-9d61-f438e8cc2191" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="559" height="90" alt="435484938-3c6bc7b2-713d-4e97-9929-8f150549cffe" src="https://github.com/user-attachments/assets/c344af98-26dd-44fd-acb5-5c88a3334823" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="575" height="91" alt="435484946-e7178556-3c87-479d-b296-462fbc2212aa" src="https://github.com/user-attachments/assets/65cbc34d-0bb1-40ff-9602-a4143b67a709" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="568" height="117" alt="435484955-0e9076bb-82ee-4265-8b29-4c27bb29bcf2" src="https://github.com/user-attachments/assets/356b42a4-ee83-4cea-a253-927fc7268384" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="559" height="92" alt="435484957-1b252fa6-5cb0-4acd-83e5-ebd855b56a8c" src="https://github.com/user-attachments/assets/c4099407-1adb-461a-b5e6-d00be8cebc01" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="583" height="90" alt="435484961-5461073a-61e8-4ae5-ac59-303744b78c1e" src="https://github.com/user-attachments/assets/6167e454-c4b6-4fde-9758-8523ee858f28" />



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="595" height="111" alt="435484963-70676c92-6598-4d83-8063-bb29625bb83d" src="https://github.com/user-attachments/assets/20da1fac-24de-43bd-b940-aeff9a2d1186" />



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
<img width="458" height="134" alt="435484972-b28ec752-baf1-4d45-98d3-7ebc29e14734" src="https://github.com/user-attachments/assets/ad97c1bb-03bd-407d-a15a-2f170d424f7b" />


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
<img width="454" height="136" alt="435484976-af3ad046-1f1b-4079-b64e-9946909f419f" src="https://github.com/user-attachments/assets/0f010419-5527-4d50-97d2-dfb1cb1952d2" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="602" height="223" alt="435484981-f28e9afd-d790-44e3-aaba-8d5e39216f40" src="https://github.com/user-attachments/assets/d40db652-e54d-4df1-a3ea-d74fdc414017" />

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

<img width="586" height="113" alt="435484993-3ba3d64c-a3e6-4269-9b90-14d88cf4f923" src="https://github.com/user-attachments/assets/dc25d46b-4bc3-4cb7-834e-3a7cc3fe45d7" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="593" height="118" alt="435484999-c747a341-5400-43f3-9fde-5b2a76a555f2" src="https://github.com/user-attachments/assets/e5ac1b5f-965d-4aa8-84f4-d0d21dc94a8e" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="558" height="200" alt="435485003-ba86f53d-22da-49e4-8966-c97cd2353907" src="https://github.com/user-attachments/assets/7cc4adad-d50b-4443-9771-09d044ecd27c" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="598" height="226" alt="435485007-37c71627-0cd8-4d92-9564-a87bcea4ba41" src="https://github.com/user-attachments/assets/41d5df0c-d8a8-4951-ac50-12e563587188" />


tar -xvf backup.tar
## OUTPUT
<img width="591" height="220" alt="435485027-ba8e7f74-33d8-456a-8cc9-d787f9c191bd" src="https://github.com/user-attachments/assets/58239357-f228-4c63-9494-05c35c018a1e" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="560" height="48" alt="435485039-106bfc3b-1368-435c-a76e-f83b26cb9ba4" src="https://github.com/user-attachments/assets/cc9b5c0f-ef60-4a8c-9d02-137b603e364c" />

gunzip backup.tar.gz
## OUTPUT
<img width="606" height="113" alt="435485046-93015354-0b49-447d-9692-b024f3f786f8" src="https://github.com/user-attachments/assets/fdc1bbd2-15f2-4d76-b596-3c5f3a8af1e7" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="593" height="92" alt="435485053-84953d19-b787-4d04-a8c3-a19a085ae3f5" src="https://github.com/user-attachments/assets/0ad498a3-039c-4063-8069-68b56788698e" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="526" height="87" alt="435485059-40b450be-bec8-4562-a880-c450939f6729" src="https://github.com/user-attachments/assets/2c1dd1a1-3e21-4734-8d13-04c0dd996762" />


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

 <img width="598" height="353" alt="435485535-debbba16-b7c8-46ce-b86c-cb798492563e" src="https://github.com/user-attachments/assets/34cf3c13-ab14-45c8-b608-c2fbf3aa8740" />

ls file1
## OUTPUT
<img width="434" height="48" alt="435485539-97098a87-4f4d-4ae6-97d4-6d0889b3f129" src="https://github.com/user-attachments/assets/58aa7ffd-372f-4a9d-8fe2-ce29711c8e43" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="411" height="44" alt="435485542-a2b93b30-9816-4608-932c-e62816a84d08" src="https://github.com/user-attachments/assets/c18b7ddb-7902-47f9-b27b-7f1e5c855a3f" />

abcd
 
echo $?
 ## OUTPUT
<img width="427" height="43" alt="435485552-1155a135-60a3-49cb-85a4-98f5cdd1ac45" src="https://github.com/user-attachments/assets/45479c03-caad-46f6-9bd9-2296d6c4b942" />


 
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

<img width="546" height="162" alt="435485555-f2f67ff0-93b1-47de-b835-94dd62c89625" src="https://github.com/user-attachments/assets/fc708c9a-a927-4947-afc0-8ac10181bfc2" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="565" height="91" alt="435485564-47e8867b-4412-4a6b-990d-fed61cb49dc8" src="https://github.com/user-attachments/assets/b041f365-c4af-4c30-aef0-d9df4eccf660" />


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
<img width="565" height="91" alt="435485586-f67462c8-405b-4d51-b278-1f6513f455b0" src="https://github.com/user-attachments/assets/6d26ed8a-8c29-4340-b47b-3970c75301bd" />

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

<img width="548" height="135" alt="435485590-a74eca48-c272-4323-8563-44bcbfcfc715" src="https://github.com/user-attachments/assets/6da2df2f-bd4f-4cb8-b5ab-e76556aea0f6" />


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
<img width="554" height="110" alt="435485594-ceabd713-451c-4573-b607-302b23b6eed7" src="https://github.com/user-attachments/assets/690ebb49-4b0a-45d2-9f0a-e3d6b1d115ec" />

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
<img width="555" height="138" alt="435485600-60989f38-9c3d-4c3f-a5c2-47e7ee5c2fe7" src="https://github.com/user-attachments/assets/832090bf-f9c5-4ac4-a54c-a8718a25b763" />

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
<img width="567" height="90" alt="435485613-a20cb91e-5c82-4cdc-8676-f86a6d5479df" src="https://github.com/user-attachments/assets/d9e7a975-62b9-4ac9-919c-6ce3bb486563" />


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
<img width="560" height="83" alt="435485617-a2a1fa20-ab48-45aa-b93a-fed3a3310f34" src="https://github.com/user-attachments/assets/e4bb3333-e75d-415a-bdd7-85499acb7eb3" />

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
<img width="547" height="204" alt="435485659-692694c1-c08c-46de-9e0b-e46aaf711fe5" src="https://github.com/user-attachments/assets/daec9f07-5587-4fc6-a37e-0a34f86350a7" />

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

<img width="587" height="218" alt="435485694-202b1e17-0d91-4d63-a465-1768cffec29b" src="https://github.com/user-attachments/assets/0b3ba4ef-734a-42d4-8100-3bfebf75cfe7" />

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
<img width="562" height="153" alt="435485701-d7de662f-ee3c-4a83-948e-49aa016f275a" src="https://github.com/user-attachments/assets/e563353f-4089-41a4-9a91-feea18765eef" />

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
<img width="572" height="155" alt="435485704-790bdcee-63eb-4fcd-902d-4e5196cb71b0" src="https://github.com/user-attachments/assets/050430ff-df31-453a-8ba4-c5ead6f9e2b0" />

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
<img width="565" height="305" alt="435485717-17ad8470-7aa4-4a2a-9d43-d74dd7db87f1" src="https://github.com/user-attachments/assets/3d25888f-b67a-4887-9b67-c6e25231bce5" />

 
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
 <img width="583" height="179" alt="435485743-213f2fe7-c200-423e-bbda-a0a472eb8c99" src="https://github.com/user-attachments/assets/f72396e3-36e4-4d0c-b329-ad07e0d274e6" />

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
<img width="544" height="93" alt="435485750-fab37407-b4fe-4e19-8b3e-26d8b2e108e4" src="https://github.com/user-attachments/assets/9f02690a-660e-4482-a526-b6f3a36cb9a1" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="548" height="91" alt="435485752-7f6e8618-5d66-4268-bc1c-a47a0af657ba" src="https://github.com/user-attachments/assets/8fb60c74-2746-4288-b10b-9f5b532bd621" />



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

 <img width="546" height="71" alt="435485762-057858f2-961b-401a-a630-c1cd86dc4761" src="https://github.com/user-attachments/assets/feaf7d5b-83e1-4476-87ff-0fb7e1a56bdc" />

 ./funcex.sh 1 2
<img width="519" height="47" alt="435485765-b0ce8ec1-0b10-494a-b950-b637ce5f2b9d" src="https://github.com/user-attachments/assets/404a4dc4-7106-4b41-aebd-3615548f648b" />

 
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
<img width="570" height="93" alt="435485774-3e7a27e7-377d-4835-810b-f949d8525cd2" src="https://github.com/user-attachments/assets/9964ae2e-194c-4c17-94a0-8fd2bb69e71c" />

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
<img width="571" height="110" alt="435485780-096eacd3-7d26-4766-a801-fe72352a9c7c" src="https://github.com/user-attachments/assets/164337d6-2730-46b1-b26c-6a9240ae2256" />

 
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
 <img width="568" height="329" alt="435485784-c645bea3-c8a1-48a7-9d78-031c9ba4b021" src="https://github.com/user-attachments/assets/467af86f-c444-42ab-8701-242708ec82ba" />

 
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
 <img width="557" height="309" alt="435485793-1ea4aea2-8868-4f08-99c7-ec4653eaab8b" src="https://github.com/user-attachments/assets/d3d93b32-fcac-4fa2-af28-288bc5124e5e" />

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
<img width="582" height="112" alt="435485799-d7eb5a4f-f597-4d3f-9e9a-ac93356b3fe7" src="https://github.com/user-attachments/assets/8375ca20-7f3a-4740-abc3-54300d1bffc3" />


# RESULT:
The Commands are executed successfully.
