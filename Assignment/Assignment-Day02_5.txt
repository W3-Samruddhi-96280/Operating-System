## Create file named grade.txt and write following contents in it. ( grep , cut ) 
 
--------------------- 
John Smith: A 
Mary Johnson: B 
Alex Rodriguez: C 
Emily Wong: A 
David Lee: B 
James Johnson: A 
Edwin Albert: B 
--------------------- 

amruddhi@samruddhi-VirtualBox:~$ touch grade.txt
samruddhi@samruddhi-VirtualBox:~$ cat> grade.txt
John Smitch : A
MAry Johnson : B
Alex Rodriguez : C
Emily Wong : A
David Lee : B
James Johnson: A
Edwin Albert : B
-----------------------                      
samruddhi@samruddhi-VirtualBox:~$ cat grade.txt
John Smitch : A
MAry Johnson : B
Alex Rodriguez : C
Emily Wong : A
David Lee : B
James Johnson: A
Edwin Albert : B
------
------------------------------------------------------------


 
## And compose commands to perform following operations  
 
# 1. Count the number of students. ( wc )  
samruddhi@samruddhi-VirtualBox:~$ wc -l grade.txt
8 grade.txt
samruddhi@samruddhi-VirtualBox:

-------------------------------------------------

# 2. List the students having grade A. ( grep ) 
samruddhi@samruddhi-VirtualBox:~$ grep -w "A" grade.txt
John Smitch : A
Emily Wong : A
James Johnson: A
----------------------------------------------------


# 3. List the students not having grade B. ( grep ) 
samruddhi@samruddhi-VirtualBox:~$ grep -v "B" grade.txt
John Smitch : A
Alex Rodriguez : C
Emily Wong : A
James Johnson: A
------------------------------------------------------

# 4. Print the count of students not having grade C. ( grep ) 
samruddhi@samruddhi-VirtualBox:~$ grep -n -v "C" grade.txt
1:John Smitch : A
2:MAry Johnson : B
4:Emily Wong : A
5:David Lee : B
6:James Johnson: A
7:Edwin Albert : B
8:-----------------------

samruddhi@samruddhi-VirtualBox:~$ grep -c -v "C" grade.txt
7
--------------------------------------------------------
# 5. List the student/students whose name starts with E & having grade B. ( grep )  
samruddhi@samruddhi-VirtualBox:~$ grep "^E" grade.txt
Emily Wong : A
Edwin Albert : B
samruddhi@samruddhi-VirtualBox:~$ grep "^E" grade.txt | grep "B"
Edwin Albert : B
-----------------------------------------------------------------
# 6. Show only Studetns first name & Last Name. ( cut ) 
samruddhi@samruddhi-VirtualBox:~$ cut -d ":" -f1 grade.txt 
John Smitch 
MAry Johnson 
Alex Rodriguez 
Emily Wong 
David Lee 
James Johnson
Edwin Albert 
----------------------- 

--------------------------------------------------------
# 7. Show only grades. ( cut ) 
samruddhi@samruddhi-VirtualBox:~$ cut -d ":" -f2 grade.txt
 A
 B
 C
 A
 B
 A
 B
-----------------------
samruddhi@samruddhi-VirtualBox:~$ 

-----------------------------------------------------------S
# 8. Show only first name & grades. ( cut )  
samruddhi@samruddhi-VirtualBox:~$ cut -d " " -f 1,4  grade.txt
John A
MAry B
Alex C
Emily A
David B
James
Edwin B
-----------------------
