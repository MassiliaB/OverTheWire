#### level 0
First SSH to the level Bandit0 with the password bandit0
➜  ~ ssh bandit0@bandit.labs.overthewire.org -p 2220

```bash
bandit0@bandit:~$ ls
readme
bandit0@bandit:~$ cat readme
****XQwcBdpmTEzi3bvBHMM9H66vVXjL
```

#### level 1

```bash
bandit1@bandit:~$ cat ./-
****zSaX8Mk1RTb1CNQoXTcYZWU6lgzi
```

#### level 2

```bash
bandit2@bandit:~$ cat 'spaces in this filename'
****0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
```

#### level 3

```bash
bandit3@bandit:~/inhere$ ls -la
total 12
drwxr-xr-x 2 root    root    4096 Oct  5  2023 .
drwxr-xr-x 3 root    root    4096 Oct  5  2023 ..
-rw-r----- 1 bandit4 bandit3   33 Oct  5  2023 .hidden
bandit3@bandit:~/inhere$ cat .hidden
****BBsr6aMMoJ2HjW067dm8EgX26xNe
```

#### level 4

```bash
bandit4@bandit:~/inhere$ cat ./-file07
****WWI6bB37kxfiCQZqUdOIYfr6eEeqR
```

#### level 5

```bash
bandit5@bandit:~/inhere$ find . -type f -size 1033c
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat maybehere07/.file2
****vucdmLnm8I7Vl7jG1ApGSfjYKqJU
```

#### level 6

```bash
bandit6@bandit:~$ find / -type f -user bandit7 2>/dev/null
/etc/bandit_pass/bandit7
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
****toNQU2XfjmMtWA8u5rN4vzqu4v99S
```

#### level 7

```bash
bandit7@bandit:~$ cat data.txt | grep millionth
******TZC0XvTetK0S9xNwm25STk5iWrBvP
```

#### level 8

```bash
bandit8@bandit:~$ cat data.txt | sort | uniq -u
****32PlfYiZbn3PhVK3XOGSlNInNE00t
```

#### level 9

```bash
bandit9@bandit:~$ cat data.txt | grep -a "====="
========== the ========== password ========== is
========== ****LIi6J3kTb8A7j9LgrywtEUlyyp6s
```

#### level 10

```bash
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==
bandit10@bandit:~$ cat data.txt  | base64 -d
The password is ****ziLdR2RKNdNYFNb6nVCKzphlXHBM
```

#### level 11

```bash
bandit11@bandit:~$ cat data.txt
Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi
# Go to Dcode.fr to decode the string :
# Your password is ******FSmZwKKOP0XbFXOoW8chDz5yVRv
```

#### level 12

```bash
bandit12@bandit:/tmp$ file exe
exe: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp$ mv exe exe.bzip2
bandit12@bandit:/tmp$ mv exe.bzip2 exe.bz2
bandit12@bandit:/tmp$ bzip2 -d exe.bz2
bandit12@bandit:/tmp$ ls exe
exe
bandit12@bandit:/tmp$ file exe
exe: gzip compressed data, was "data4.bin", last modified: Thu Oct  5 06:19:20 2023, max compression, from Unix, original size modulo 2^32 20480
bandit12@bandit:/tmp$ mv exe exe.gzip
bandit12@bandit:/tmp$ gzip -d exe.gzip
gzip: exe.gzip: unknown suffix -- ignored
bandit12@bandit:/tmp$ mv exe.gzip exe.gz
bandit12@bandit:/tmp$ gzip -d exe.gz
bandit12@bandit:/tmp$ ls
exe
bandit12@bandit:/tmp$ file exe
exe: POSIX tar archive (GNU)
bandit12@bandit:/tmp$ tar xvf exe
data4.bin
bandit12@bandit:/tmp$ file data4.bin
data4.bin: POSIX tar archive (GNU)
bandit12@bandit:/tmp$ tar xvf data4.bin
data5.bin
bandit12@bandit:/tmp$ file data5.bin
data5.bin: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp$ mv data5.bin data5.bz2
bandit12@bandit:/tmp$ bzip2 -d data5.bz2
bandit12@bandit:/tmp$ ls
data4.bin  data5  exe
bandit12@bandit:/tmp$ file data5
data5: POSIX tar archive (GNU)
bandit12@bandit:/tmp$ tar xvf data5
data6.bin
bandit12@bandit:/tmp$ file data6.bin
data6.bin: POSIX tar archive (GNU)
bandit12@bandit:/tmp$ tar xvf data6.bin
data8.bin
bandit12@bandit:/tmp$ file data8.bin
data8.bin: gzip compressed data, was "data9.bin", last modified: Thu Oct  5 06:19:20 2023, max compression, from Unix, original size modulo 2^32 20819
bandit12@bandit:/tmp$ mv data8.bin data8.gz
bandit12@bandit:/tmp$ gunzip data8.gz
bandit12@bandit:/tmp$ ls
data4.bin  data5  data6.bin  data8  exe
bandit12@bandit:/tmp$ file data8
data8: ASCII text
bandit12@bandit:/tmp$ cat data8
******JmK4l0QPmxfEyHS0B7wIfckK4wNnuk
```

#### level 13

```bash
bandit13@bandit:~$ ls
sshkey.private
bandit13@bandit:~$ cat sshkey.private
-----BEGIN RSA PRIVATE KEY-----
****
-----END RSA PRIVATE KEY-----

➜  ~ ssh -i ssh.priv bandit14@bandit.labs.overthewire.org -p 2220
```

#### Level 14

```bash
bandit14@bandit:~$ cat /etc/bandit_pass/bandit14 | nc localhost 30000
Correct!
****gmIXJ6fShzhT2avhotn4Zcka6tnt
```

#### Level 15

```bash
bandit15@bandit:~$ ncat --ssl localhost 30001
****gmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
****fApK4SeyHwDlI9SXGR50qclOAil1
```

#### Level 16

```bash
bandit16@bandit:~$ ncat --ssl localhost 31790
****fApK4SeyHwDlI9SXGR50qclOAil1
Correct!
-----BEGIN RSA PRIVATE KEY-----
****
-----END RSA PRIVATE KEY-----
```

#### Level 17

```bash
bandit17@bandit:~$ diff passwords.new passwords.old 
42c42
< ****tuuCLF6fFzUpnagiMN8ssu9LFrdg
---
> ****wdNHncnmCNxuAt0KtKVq185ZU7AW
```

#### level18

```bash
➜ ssh bandit18@bandit.labs.overthewire.org -p 2220 /bin/bash
cat readme
****fNnAbc1naukrpqDYcF95h7HoMTrC
```

#### level19

```bash
bandit19@bandit:~$ ./bandit20-do cat /etc/bandit_pass/bandit20
****zJaVykI6W36BkBU0mJTCM8rR95XT
```

#### level20

```bash
bandit20@bandit:~$ nc -nlvp 1234
Listening on 0.0.0.0 1234
Connection received on 127.0.0.1 50800
****zJaVykI6W36BkBU0mJTCM8rR95XT
****F7oVjkddltPSrdKEFOllh9V1IBcq
```

#### level21

```bash
bandit21@bandit:~$ cat /etc/cron.d/cronjob_bandit22 
@reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
* * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
bandit21@bandit:~$ cat /usr/bin/cronjob_bandit22.sh
#!/bin/bash
chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
bandit21@bandit:~$ cat  /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
****zAdTM2z9DiFEQ2mGlwngMfj4EZff
```

#### level22

```bash
bandit22@bandit:~$ cat /etc/cron.d/cronjob_bandit23 
@reboot bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
* * * * * bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
bandit22@bandit:~$ cat /usr/bin/cronjob_bandit23.sh
#!/bin/bash

myname=$(whoami)
mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)

echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"

cat /etc/bandit_pass/$myname > /tmp/$mytarget
bandit22@bandit:~$ echo I am user bandit23 | md5sum | cut -d ' ' -f 1
****19486bfbbc3663ea0fbe81326349
bandit22@bandit:~$ cat /tmp/****19486bfbbc3663ea0fbe81326349
****Y2aiA672PsMmh9puTQuhoz8SyR2G
```

#### level23

```bash
bandit23@bandit:~$ cat /etc/cron.d/cronjob_bandit24 
@reboot bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
* * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
bandit23@bandit:~$ cat /usr/bin/cronjob_bandit24.sh
#!/bin/bash

myname=$(whoami)

cd /var/spool/$myname/foo
echo "Executing and deleting all scripts in /var/spool/$myname/foo:"
for i in * .*;
do
    if [ "$i" != "." -a "$i" != ".." ];
    then
        echo "Handling $i"
        owner="$(stat --format "%U" ./$i)"
        if [ "${owner}" = "bandit23" ]; then
            timeout -s 9 60 ./$i
        fi
        rm -f ./$i
    fi
done

bandit23@bandit:~$ cd /var/spool/bandit24/
bandit23@bandit:/var/spool/bandit24$ ls
foo
bandit23@bandit:/var/spool/bandit24$ echo "cat /etc/bandit_pass/bandit24 > /tmp/pass" > /tmp/exec 
bandit23@bandit:/var/spool/bandit24$ chmod 755 /tmp/exec
bandit23@bandit:/var/spool/bandit24$ mv /tmp/exec foo/
bandit23@bandit:/var/spool/bandit24$ cat /tmp/pass
****XJ1PBSsPSnvsjI8p759leLZ9GGar
```

#### level24

```bash
bandit24@bandit:/tmp/dir$ for i in {0000..5555}; do     echo "****XJ1PBSsPSnvsjI8p759leLZ9GGar $i" >> pass.txt; done
bandit24@bandit:/tmp/dir$ for i in {5555..9999}; do     echo "****XJ1PBSsPSnvsjI8p759leLZ9GGar $i" >> pass1.txt; done
bandit24@bandit:/tmp/dir$ cat pass.txt | nc localhost 30002 | grep -v "Wrong! Please enter the correct pincode. Try again."
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
Timeout. Exiting.
bandit24@bandit:/tmp/dir$ cat pass1.txt | nc localhost 30002 | grep -v "Wrong! Please enter the correct pincode. Try again."
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
Correct!
The password of user bandit25 is ****owMYrmu23Ol8hiZh9UvD0O9hpx8d

Exiting.
```

#### level25

```bash
bandit25@bandit:~$ ls
bandit26.sshkey
bandit25@bandit:~$ cat bandit26.sshkey 
-----BEGIN RSA PRIVATE KEY-----
****
-----END RSA PRIVATE KEY-----

bandit25@bandit:~$ cat /etc/passwd
...
bandit26:x:11026:11026:bandit level 26:/home/bandit26:/usr/bin/showtext
...
```

#### level26

```bash
ssh -i ssh.priv bandit26@bandit.labs.overthewire.org -p 2220
# execute on a tiny screen and use v in the interactive mode to activate vim and then escape with a shell 
:set shell=/bin/bash
:!/bin/bash                   
[No write since last change]
bandit26@bandit:~$ ls
bandit27-do  text.txt
$ ./bandit27-do cat /etc/bandit_pass/bandit27
****BuifNMas1hcUFk70ZmqkhUU2EuaS
```

#### level27

```bash
bandit27@bandit:/tmp/dir$ git clone ssh://bandit27-git@localhost:2220/home/bandit27-git/repo 
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit27/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit27/.ssh/known_hosts).
                         _                     _ _ _   
                        | |__   __ _ _ __   __| (_) |_ 
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_ 
                        |_.__/ \__,_|_| |_|\__,_|_|\__|
                                                       

                      This is an OverTheWire game server. 
            More information on http://www.overthewire.org/wargames

bandit27-git@localhost's password: 
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
Receiving objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
bandit27@bandit:/tmp/dir$ cd repo
bandit27@bandit:/tmp/dir/repo$ ls
README
bandit27@bandit:/tmp/dir/repo$ cat README 
The password to the next level is: ****L161y9rsbcJIsFHuw35rjaOM19nR
```

#### level28

```bash
bandit28@bandit:~$ cd /tmp
bandit28@bandit:/tmp$ mkdir dir
bandit28@bandit:/tmp$ cd dir
bandit28@bandit:/tmp/dir$ git clone  ssh://bandit28-git@localhost:2220/home/bandit28-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit28/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit28/.ssh/known_hosts).
                         _                     _ _ _   
                        | |__   __ _ _ __   __| (_) |_ 
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_ 
                        |_.__/ \__,_|_| |_|\__,_|_|\__|
                                                       

                      This is an OverTheWire game server. 
            More information on http://www.overthewire.org/wargames

bandit28-git@localhost's password: 
remote: Enumerating objects: 9, done.
remote: Counting objects: 100% (9/9), done.
remote: Compressing objects: 100% (6/6), done.
remote: Total 9 (delta 2), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (9/9), done.
Resolving deltas: 100% (2/2), done.
bandit28@bandit:/tmp/dir$ ls
repo
bandit28@bandit:/tmp/dir$ cd repo
bandit28@bandit:/tmp/dir/repo$ ls
README.md
bandit28@bandit:/tmp/dir/repo$ cat README.md 
# Bandit Notes
Some notes for level29 of bandit.

## credentials

- username: bandit29
- password: xxxxxxxxxx

bandit28@bandit:/tmp/dir/repo$ git show
commit 14f754b3ba6531a2b89df6ccae6446e8969a41f3 (HEAD -> master, origin/master, origin/HEAD)
Author: Morla Porla <morla@overthewire.org>
Date:   Thu Oct 5 06:19:41 2023 +0000

    fix info leak

diff --git a/README.md b/README.md
index b302105..5c6457b 100644
--- a/README.md
+++ b/README.md
@@ -4,5 +4,5 @@ Some notes for level29 of bandit.
 ## credentials
 
 - username: bandit29
-- password: ****mcwNYcFS6vmPHIUSI3ShmsrQZK8S
+- password: xxxxxxxxxx

```

#### level29

```bash
bandit29@bandit:~$ cd /tmp
bandit29@bandit:/tmp$ mkdir dir29
bandit29@bandit:/tmp$ cd dir29
bandit29@bandit:/tmp/dir29$ ls
bandit29@bandit:/tmp/dir29$ git clone ssh://bandit29-git@localhost:2220/home/bandit29-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit29/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit29/.ssh/known_hosts).
                         _                     _ _ _   
                        | |__   __ _ _ __   __| (_) |_ 
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_ 
                        |_.__/ \__,_|_| |_|\__,_|_|\__|
                                                       

                      This is an OverTheWire game server. 
            More information on http://www.overthewire.org/wargames

bandit29-git@localhost`s password: 
remote: Enumerating objects: 16, done.
remote: Counting objects: 100% (16/16), done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 16 (delta 2), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (16/16), done.
Resolving deltas: 100% (2/2), done.
bandit29@bandit:/tmp/dir29$ ls
repo
bandit29@bandit:/tmp/dir29$ cd repo
bandit29@bandit:/tmp/dir29/repo$ ls
README.md
bandit29@bandit:/tmp/dir29/repo$ cat README.md 
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: <no passwords in production!>

bandit29@bandit:/tmp/dir29/repo$ git checkout 
dev                  master               origin/HEAD          origin/sploits-dev 
HEAD                 origin/dev           origin/master        sploits-dev 
bandit29@bandit:/tmp/dir29/repo$ git checkout dev
Branch 'dev' set up to track remote branch 'dev' from 'origin'.
Switched to a new branch 'dev'
bandit29@bandit:/tmp/dir29/repo$ cat README.md 
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: ****3HpNGlTIdnjUrdAlPzc2L6y9EOnS
```

#### level30

```bash
bandit30@bandit:~$ cd /tmp
bandit30@bandit:/tmp$ cd dir30
bandit30@bandit:/tmp/dir30$ ls
repo
bandit30@bandit:/tmp/dir30$ cd repo
bandit30@bandit:/tmp/dir30/repo$ ls
README.md
bandit30@bandit:/tmp/dir30/repo$ git checkout 
FETCH_HEAD      master          origin/HEAD     secret          
HEAD            ORIG_HEAD       origin/master
bandit30@bandit:/tmp/dir30/repo$ git checkout secret
fatal: reference is not a tree: secret
bandit30@bandit:/tmp/dir30/repo$ cat README.md 
just an epmty file... muahaha
bandit30@bandit:/tmp/dir30/repo$ git reset --hard secret
error: object 831aac2e2341f009e40e46392a4f5dd318483019 is a blob, not a commit
fatal: Could not parse object 'secret'.
# L’option `-t` me permet de connaître le type de fichier analysé
bandit30@bandit:/tmp/dir30/repo$ git cat-file -t secret
blob
# L’option `-p` me permet d’afficher le contenu de ce fichier
bandit30@bandit:/tmp/dir30/repo$ git cat-file -p secret
****zGDlzhAlerFJ2cAiz1D41JW1Mhmt
```

#### level31

```bash
bandit31@bandit:~$ cd /tmp
bandit31@bandit:/tmp$ mkdir dir31
bandit31@bandit:/tmp$ cd dir31
bandit31@bandit:/tmp/dir31$ ls
bandit31@bandit:/tmp/dir31$ git clone ssh://bandit31-git@localhost:2220/home/bandit31-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit31/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit31/.ssh/known_hosts).
                         _                     _ _ _   
                        | |__   __ _ _ __   __| (_) |_ 
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_ 
                        |_.__/ \__,_|_| |_|\__,_|_|\__|
                                                       

                      This is an OverTheWire game server. 
            More information on http://www.overthewire.org/wargames

bandit31-git@localhost's password: 
Connection closed by 127.0.0.1 port 2220
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
bandit31@bandit:/tmp/dir31$ 
bandit31@bandit:/tmp/dir31$ ls
bandit31@bandit:/tmp/dir31$ git clone ssh://bandit31-git@localhost:2220/home/bandit31-git/repo 
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit31/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit31/.ssh/known_hosts).
                         _                     _ _ _   
                        | |__   __ _ _ __   __| (_) |_ 
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_ 
                        |_.__/ \__,_|_| |_|\__,_|_|\__|
                                                       

                      This is an OverTheWire game server. 
            More information on http://www.overthewire.org/wargames

bandit31-git@localhost's password: 
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (4/4), done.
bandit31@bandit:/tmp/dir31$ ls
repo
bandit31@bandit:/tmp/dir31$ cd repo
bandit31@bandit:/tmp/dir31/repo$ ls
README.md
bandit31@bandit:/tmp/dir31/repo$ cat README.md 
This time your task is to push a file to the remote repository.

Details:
    File name: key.txt
    Content: 'May I come in?'
    Branch: master

bandit31@bandit:/tmp/dir31/repo$ echo "May I come in?" > key.txt
bandit31@bandit:/tmp/dir31/repo$ ls
key.txt  README.md
bandit31@bandit:/tmp/dir31/repo$ git checkout master 
Already on 'master'
Your branch is up to date with 'origin/master'.
bandit31@bandit:/tmp/dir31/repo$ git add key.txt 
The following paths are ignored by one of your .gitignore files:
key.txt
hint: Use -f if you really want to add them.
hint: Turn this message off by running
hint: "git config advice.addIgnoredFile false"
bandit31@bandit:/tmp/dir31/repo$ git add -f  key.txt 
bandit31@bandit:/tmp/dir31/repo$ git commit -m "key"
[master 58fa0b2] key
 1 file changed, 1 insertion(+)
 create mode 100644 key.txt
bandit31@bandit:/tmp/dir31/repo$ git push
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit31/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit31/.ssh/known_hosts).
                         _                     _ _ _   
                        | |__   __ _ _ __   __| (_) |_ 
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_ 
                        |_.__/ \__,_|_| |_|\__,_|_|\__|
                                                       

                      This is an OverTheWire game server. 
            More information on http://www.overthewire.org/wargames

bandit31-git@localhost's password: 
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 2 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 318 bytes | 318.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote: ### Attempting to validate files... ####
remote: 
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote: 
remote: Well done! Here is the password for the next level:
remote: ****vG56y58BXzv98yZGdO7ATVL5dW8y 
remote: 
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote: 
To ssh://localhost:2220/home/bandit31-git/repo
 ! [remote rejected] master -> master (pre-receive hook declined)
error: failed to push some refs to 'ssh://localhost:2220/home/bandit31-git/repo'
```

#### level32

```bash
➜  ~ ssh bandit32@bandit.labs.overthewire.org -p 2220 
                         _                     _ _ _   
                        | |__   __ _ _ __   __| (_) |_ 
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_ 
                        |_.__/ \__,_|_| |_|\__,_|_|\__|
                                                       

                      This is an OverTheWire game server. 
            More information on http://www.overthewire.org/wargames

bandit32@bandit.labs.overthewire.org's password: 
WELCOME TO THE UPPERCASE SHELL
>> $
sh: 1: $: Permission denied
>> $$
sh: 1: 1365328: Permission denied
>> $0
$ whoami
bandit33
$ cat /etc/bandit_pass/bandit33
****63fHiFqcWWJG9rLiLDtPm45KzUKy
```

#### level33

```bash
bandit33@bandit:~$ cat README.txt 
Congratulations on solving the last level of this game!

At this moment, there are no more levels to play in this game. However, we are constantly working
on new levels and will most likely expand this game with more levels soon.
Keep an eye out for an announcement on our usual communication channels!
In the meantime, you could play some of our other wargames.

If you have an idea for an awesome new level, please let us know!
```
