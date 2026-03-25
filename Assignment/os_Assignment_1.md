Linux Commands Assignments - II
1. List the directory contents date wise sorted. ( man ls)

jadha@Samruddhi96280W3 MINGW64 /
$ ls -lt
total 6228
dr-xr-xr-x 9 jadha 197609       0 Mar 23 15:50 proc/
drwxr-xr-x 1 jadha 197609       0 Mar 23 15:50 tmp/
drwxr-xr-x 1 jadha 197609       0 Feb 26 19:21 etc/
drwxr-xr-x 1 jadha 197609       0 Feb 26 19:20 cmd/
drwxr-xr-x 1 jadha 197609       0 Feb 26 19:20 dev/
-rw-r--r-- 1 jadha 197609 1786278 Feb 26 19:20 unins000.dat
-rw-r--r-- 1 jadha 197609   25363 Feb 26 19:20 unins000.msg
drwxr-xr-x 1 jadha 197609       0 Feb 26 19:20 bin/
drwxr-xr-x 1 jadha 197609       0 Feb 26 19:20 usr/
drwxr-xr-x 1 jadha 197609       0 Feb 26 19:20 mingw64/
-rwxr-xr-x 1 jadha 197609 3684608 Feb 26 19:11 unins000.exe*
-rw-r--r-- 1 jadha 197609  286359 Aug 19  2025 ReleaseNotes.html
-rw-r--r-- 1 jadha 197609   18765 Aug 19  2025 LICENSE.txt
-rwxr-xr-x 1 jadha 197609  138656 Aug 19  2025 git-bash.exe*
-rwxr-xr-x 1 jadha 197609  138128 Aug 19  2025 git-cmd.exe*

ls -t
To display all files based on last modified date and time. Most recent is at top and old
are at bottom.

ls -l
To display long listing of files



2. List the directory contents size wise sorted


jadha@Samruddhi96280W3 MINGW64 ~
$ ls -ls
total 16179
    0 drwxr-xr-x 1 jadha 197609        0 Feb 17 23:32  AppData/
    0 lrwxrwxrwx 1 jadha 197609       30 Feb 17 23:32 'Application Data' -> /c/Users/jadha/AppData/Roaming/
    0 drwxr-xr-x 1 jadha 197609        0 Feb 18 06:38  Contacts/
    0 lrwxrwxrwx 1 jadha 197609       58 Feb 17 23:32  Cookies -> /c/Users/jadha/AppData/Local/Microsoft/Windows/INetCookies/
    4 drwxr-xr-x 1 jadha 197609        0 Feb 19 08:13  Documents/
    8 drwxr-xr-x 1 jadha 197609        0 Mar 23 21:32  Downloads/
    0 drwxr-xr-x 1 jadha 197609        0 Feb 18 06:38  Favorites/
    4 drwxr-xr-x 1 jadha 197609        0 Mar 24 06:43  IntelGraphicsProfiles/
    0 drwxr-xr-x 1 jadha 197609        0 Feb 18 06:38  Links/
    0 lrwxrwxrwx 1 jadha 197609       28 Feb 17 23:32 'Local Settings' -> /c/Users/jadha/AppData/Local/
    0 drwxr-xr-x 1 jadha 197609        0 Feb 18 06:38  Music/
    0 lrwxrwxrwx 1 jadha 197609       24 Feb 17 23:32 'My Documents' -> /c/Users/jadha/Documents/




3. List directory contents along with inode number

An inode (index node) is a unique ID number that the operating system assigns to every file and directory on a disk.
Think of it like a social security number for a file:
The filename is just a label for humans.
The inode is the actual identifier the system uses to find where the data is physically stored on the hard drive.

ls -i
- To display all files including inode number.
- i-node is the address of location, where file attributes are stored.
- i-node is the address of the location, where file attributes are stored.


jadha@Samruddhi96280W3 MINGW64 /
$ ls -i
 1688849860303570 LICENSE.txt
 1688849860303569 ReleaseNotes.html
 2533274790403889 bin/
 2251799813688501 cmd/
 3377699720531107 dev/
 2251799813688489 etc/
 2251799813688545 git-bash.exe*
 2251799813688546 git-cmd.exe*
 2251799813688547 mingw64/
                2 proc/
33776997205308554 tmp/
 2251799813688487 unins000.dat
 2251799813688488 unins000.exe*


 

4. List the contents of the subdirectory

jadha@Samruddhi96280W3 MINGW64 ~
$ cd /samruddhi

jadha@Samruddhi96280W3 MINGW64 /samruddhi
$ ls
Assign1.txt



5. Create a file and write surname and name

jadha@Samruddhi96280W3 MINGW64 ~
$ cd /samruddhi


jadha@Samruddhi96280W3 MINGW64 /samruddhi
$ cat Assign1.txt
Surname: JAdhav
FirstName:Samruddhi

jadha@Samruddhi96280W3 MINGW64 /samruddhi
$ ls
Assign1.txt


ii. reopen the same file and check your name and address in
it.



jadha@Samruddhi96280W3 MINGW64 /samruddhi
$ cat  Assign1.txt
Surname: JAdhav
FirstName:Samruddhi
Address : Brahmangaon ,Kopargaon



6. Change timestamp
touch Assign1.txt


7. Create directory structure
mkdir one
cd one
touch 1.txt 11.txt 111.txt

mkdir two
cd two
touch 2.txt 22.txt 222.txt

mkdir three
cd three
touch 3.txt 33.txt 333.txt

mkdir four
cd four
touch 4.txt 44.txt 444.txt

mkdir five
cd five
touch 5.txt 55.txt 555.txt


8. Operationn

i. List contents of five

jadha@Samruddhi96280W3 MINGW64 /samruddhi/five
$ ls samruddhi/one/two/three/four/five

Output:
5.txt  55.txt  555.txt

another way:
jadha@Samruddhi96280W3 MINGW64 /samruddhi
$ ls
Assign1.txt  five/  four/  one/  three/  two/

jadha@Samruddhi96280W3 MINGW64 /samruddhi
$ cd five

jadha@Samruddhi96280W3 MINGW64 /samruddhi/five
$ ls
5.txt  55.txt  555.txt



ii. Write name in 44.txt
echo "Name: Samruddhi Jadhav" >> ~/one/two/three/four/44.txt


another way:
jadha@Samruddhi96280W3 MINGW64 /samruddhi/four
$ cat >> 44.txt
Name : Samruddhi Jadhav

jadha@Samruddhi96280W3 MINGW64 /samruddhi/four
$ cat 44.txt
Name : Samruddhi Jadhav

iii. Remove 555.txt
rm samruddhi/one/two/three/four/five/555.txt

iv. Change directory to five

jadha@Samruddhi96280W3 MINGW64 /samruddhi
$ cd one/two/three/four/five

jadha@Samruddhi96280W3 MINGW64 /samruddhi/one/two/three/four/five
$ pwd
/samruddhi/one/two/three/four/five



v. Write course name in 3.txt and read

echo "Course Name: MC" >> ../../3.txt

cat ../../3.txt


vi. List contents of directory two

ls ../../../
$ cat 222.txt


vii. remove file named "222.txt" which belongs to
directory "two" from current directory (i.e. five)


jadha@Samruddhi96280W3 MINGW64 /samruddhi/one/two/three/four/five
$ rm ../../../222.txt

ls ../../../


viii. Change directory to one

jadha@Samruddhi96280W3 MINGW64 /samruddhi/one/two/three/four/five
$ cd ../../../../

jadha@Samruddhi96280W3 MINGW64 /samruddhi/one
$ pwd
/samruddhi/one



x. remove directory named "five" from current directory
(i.e. one)

rmdir two/three/four/five
jadha@Samruddhi96280W3 MINGW64 /samruddhi/one
$ rmdir two/three/four/five
rmdir: failed to remove 'two/three/four/five': Directory not empty




jadha@Samruddhi96280W3 MINGW64 /samruddhi/one
$ rm -r two/three/four/five

-r: Stands for recursive. It tells Git Bash to go inside the folder 



xi. remove whole directory named "four" from current
directory (i.e. one)

jadha@Samruddhi96280W3 MINGW64 /samruddhi/one
$ rm -r two/three/four

jadha@Samruddhi96280W3 MINGW64 /samruddhi/one
$ ls -a two/three/four
ls: cannot access 'two/three/four': No such file or directory


xii. change to your home directory.

jadha@Samruddhi96280W3 MINGW64 /samruddhi/one
$ cd ~

jadha@Samruddhi96280W3 MINGW64 ~
$ pwd
/c/Users/jadha



9. change the time stamp of file named "3.txt" which resides
in directory named "three".(man touch)


jadha@Samruddhi96280W3 MINGW64 /samruddhi/one
$ touch two/three/3.txt


ls -l two/three/3.txt
-l two/three/3.txt

jadha@Samruddhi96280W3 MINGW64 /samruddhi/one
$ ls -l two/three/3.txt
-rw-r--r-- 1 jadha 197609 16 Mar 23 18:08 two/three/3.txt


ubnuntu

touch -t 202603231830 two/three/3.txt