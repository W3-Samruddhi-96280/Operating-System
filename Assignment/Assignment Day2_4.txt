# Create a file named "data.txt" and write the following lines in it(write as it is).  
Linux is open source.  
In Linux everything is file 
files have permissions.  
files have inode no.  
files have size.  
there are several types of files 



samruddhi@samruddhi-VirtualBox:~$ touch data.txt
samruddhi@samruddhi-VirtualBox:~$ cat>data.txt
Linux is open source.
In Linus everyting is file.
file have permissions.
files have inode no.
file have size.
there are serveral types of files.
samruddhi@samruddhi-VirtualBox:~$ uname
Linux
samruddhi@samruddhi-VirtualBox:~$ cat data.txt
Linux is open source.
In Linus everyting is file.
file have permissions.
files have inode no.
file have size.
there are serveral types of files.
------------------------------------------------------------
 
# compose the commands  fulfilled following requirement 
# i. count the no. of words ,characters and lines from above 
2 file.(man wc) 
 samruddhi@samruddhi-VirtualBox:~$ wc -w -m -l data.txt
  6  25 145 data.txt

  --------------------------------------------------
# ii. list the lines having word "files" (man grep)  
samruddhi@samruddhi-VirtualBox:~$ grep -w "files" data.txt
files have inode no.
there are serveral types of files.
----------------------------------------------------
# iii. list the lines having word "file" (man grep)  
samruddhi@samruddhi-VirtualBox:~$ grep -w "file" data.txt
In Linus everyting is file.
file have permissions.
file have size.

-----------------------------------------------------------

# iv. list the lines which don't have word "files" (man grep)  
samruddhi@samruddhi-VirtualBox:~$ grep -v "file" data.txt
Linux is open source.

-------------------------------------------------------
# v. list the lines having word "have" . (man grep) 
samruddhi@samruddhi-VirtualBox:~$ grep -w "have" data.txt
file have permissions.
files have inode no.
file have size.
samruddhi@samrud
------------------------------------------ 
# vi. list the lines starts with letter "f" (man grep) 
samruddhi@samruddhi-VirtualBox:~$ grep "^f" data.txt
file have permissions.
files have inode no.
file have size.
------------------------------------------------------ 
# vii. list the lines ends with "." (man grep)

samruddhi@samruddhi-VirtualBox:~$ grep ".$" data.txt
Linux is open source.
In Linus everyting is file.
file have permissions.
files have inode no.
file have size.
there are serveral types of files.
samruddhi@samruddhi-VirtualBox:

----------------------------------------------------------
# viii. list only first two lines.(man head)  
samruddhi@samruddhi-VirtualBox:~$ head -2 data.txt
Linux is open source.
In Linus everyting is file.

amruddhi@samruddhi-VirtualBox:~$ cat data.txt
Linux is open source.
In Linus everyting is file.
file have permissions.
files have inode no.
file have size.
there are serveral types of files.
--------------------------------------------------------------
# ix. list only last three lines.(man tail)  

samruddhi@samruddhi-VirtualBox:~$ tail -3 data.txt
files have inode no.
file have size.
there are serveral types of files.
samruddhi@samruddhi-VirtualBo

-------------------------------------------------------------
x. list line no.3,4 and 5 . (man head and tail) 

samruddhi@samruddhi-VirtualBox:~$ head -n -5 data.txt |tail -n -3
Linux is open source.
samruddhi@samruddhi-VirtualBox:~$ tail -n+3 data.txt | head -n 3
file have permissions.
files have inode no.
file have size.
samruddhi@samruddhi-VirtualBox:~$ cat -n data.txt
     1	Linux is open source.
     2	In Linus everyting is file.
     3	file have permissions.
     4	files have inode no.
     5	file have size.
     6	there are serveral types of files.
samruddhi@samruddhi-VirtualBox:~$ 
--------------------------------------------------------------
 
 