
# Pwn.college

### Linux essentials
soft links: A hard link is an alternate address that indexes that data --- accesses to the hard link and accesses to the original file are completely identical, in that they immediately yield the necessary data.
hard links: A soft/symbolic link, instead, contains the original file name. When you access the symbolic link, Linux will realize that it is a symbolic link, read the original file name, and then (typically) automatically access that file.

Create symbolic link with `ln -s TARGET LINK_NAME. TARGET`

e.g.:
```
hacker@dojo:~$ cat /tmp/myfile 
This is my file! 
hacker@dojo:~$ ln -s /tmp/myfile /home/hacker/ourfile 
hacker@dojo:~$ cat ~/ourfile 
This is my file! 
hacker@dojo:~$
```

file command can take a file name and tell the type of file, can recognize symbolic links

Wildcard
- \* (multi chars) 
- ? (single char)
-  [] is a wildcard for some subset of potential characters, specified within the brackets. e.g. [pwn] will match the character p, w, or n.
  
  
> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE5MjYwODIyNDEsODI2NDMxNTMxXX0=
-->