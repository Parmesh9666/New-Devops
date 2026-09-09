
1. access

Access is system call and it is mainly used in C or C++ programs to check permissions.

**In shell

If [ -r test.sh ]; then
  echo "File is readable"
fi

-r --> Read permission
-w --> Write permission
-x --> Execute permission
-e --> File exists
-d --> Directory exists

2. basename

Basename we can used to extract the file name from the full file path by removing the directory path.

--> basename /home/hp/New-Devops/test.sh

Output:- test.sh

3. compress

compress is used to reduse the size of files and to save disk space.

Common linux commands are:-
gzip, tar, zip,

4. cat

Cat command we can use mainly to view the content of the file and using cat we can create new file and we can merge the files.

cat file.txt --> It will show the content of the file
cat > file.txt --> To create new file
cat file1.txt file2.txt > merged.txt --> It will merge the the file content to one file
cat -n file.txt --> It will display content along with line numbers
cat -s file.txt --> It will suppress repeated empty lines
cat -E file.txt --> It will disply content of the file with $ sysmbol at the end of every line

5. cksum

This is used to display checksum value and file size. Commanly used after copying or transferring files.

cksum test.txt

6. cmp

Cmp used to compare two files content.

cmp test1.txt test2.txt

7. cp

Copy used to copy the files and directories from one location to another location and create duplicate the files

cp test.txt copy.txt --> It will create duplicate the file in same directory
cp test.txt /home/bin/ --> Copy file from one location to another location

8. cpio

This command is used to create, Extract and copy archive files. The name cpio stands for copy in and copy out.

**Create Sample Files

mkdir cpio_example
cd cpio_example
echo "This is file 1" > file1.txt
echo "This is file 2" > file2.txt
echo "This is file 3" > file3.txt
mkdir subdir
echo "This is a file in a subdirectory" > subdir/file4.txt

**Create the Archive

find . -name "*.txt" | cpio -ov > archive.cpio

cpio -o: Uses copy-out mode to create an archive.
-v: Displays the names of files being added to the archive.

9. csplit

This command is used to split a larger file into multiple smaller files.

csplit test.txt 2

10. cut

This command is used to extract specific parts of each line from a file or input. You can extract data based on byte position, character position, or fields separated by a delimiter

cut -d " " -f 2 text.txt
-d " ": Sets space as the field delimiter.
-f 2: Extracts the second field from each line.

cut -d " " -f 1,2 sample.txt --> It will print first and second field from the file content
cut -b 1,2,3 state.txt --> It will print the 1,2,3 bytes
cut -b 1-3,5-7 state.txt --> It will print bytes from 1 to 3 and 5 to 7
cut -c 2,5,7 state.txt --> It will display characters at positions 2, 5, and 7
cut -c 1-7 state.txt -->  It will display characters from 1 to 7

11. diff

We can use this command to compare two files line by line to identify differnces and debugging the code.

diff a.txt b.txt

diff -c file1.txt file2.txt --> To view differences in context mode.

12. diff3

This command we can use to compare 3 files line by line.

diff3 a.txt b.txt c.txt

13. echo
 
Echo command we can use to display lines of text and strings that are passed as arguments.

echo "Hello world" --> It will print Hell world
echo -e "Geeks \bfor \bGeeks" --> it removes all the spaces in between the text
echo -e "Geeks \nfor \nGeeks" --> creates a new line from where it is used.

14. expand

The expand command in Linux is used to convert TAB characters (\t) into spaces in a text file.

expand file.txt --> This converts the tabs into spaces
expand -t 4 file.txt --> This treats each tab as spacing according to a tab stop of 4 columns.

15. file

The file command is used to determine the type or format of a file.
file email.py --> Displays type of 'email.py'
file -b emai.py --> Shows just the file type

16. fold

The fold command is used to wrap long lines of text into smaller lines based on a specified width.

fold test.txt

17. head

The head command used to display the first few lines one or more files directly in the terminal.
Default it will print first 10 lines from selected file.

head sample.txt --> it will print first 10 lines 
head -20 sample.txt --> it will print first 20 lines

18. join
 
The join command merges lines from two files based on a common key field.

join file1.txt file2.txt

19. less
 
The less command is used to view the contents of a file one page at a time without opening it in an editor, making it ideal for reading large files efficiently.

less test.txt
less -F /home/Mandeep/test/test.txt --> Exits immediately if the entire file fits on the first screen.

20. ln

The 'ln' command is used to create links between files. These links can either be hard links or soft (symbolic) links.

ln test.txt sample.txt --> creating a hard link
ln -s test.txt /home/etc/sample.txt --> creating a soft link

21. locate

The locate command is a fast and efficient tool used to find files by their name.

locate sample.txt
locate -e sample.txt --> Print Only Existing Files

22. look

The look command is used to display lines that begin with a specified string.

look ab test.sh --> it will print the all content starting ab
look "#include" Assignment.txt

23. more

The more command is used to view the contents of a text file one screen (or page) at a time in the terminal

more test.txt

24. mv

he mv (move) command is used to move or rename files and directories. It does not create a copy of the file

mv test.txt sample.txt

25. od

The od (octal dump) command is a versatile tool used to display file contents in various formats, with the default being octal

od -b input.txt --> Display in Octal Format
od -c input.txt --> Display in Character Format

26. paste

It is used to join files horizontally (parallel merging) by outputting lines consisting of lines from each file specified, separated by tab as delimiter, to the standard output.

paste test.txt sample.txt
paste -d "|" number state capital --> Only one character is specified

output

1|Arunachal Pradesh|Itanagar
2|Assam|Dispur
3|Andhra Pradesh|Hyderabad
4|Bihar|Patna
5|Chhattisgrah|Raipur

27. readlink

The 'readlink' command is a valuable tool used to print resolved symbolic links or canonical file names.

readlink NetHood --> it will show the symbolic link of NetHood
readlink -f NetHood --> This option canonicalize by following every symlink in every component of the given name recursively; all but the last component must exist.

28. rename

Changing the names of files in Linux is something we often do, and the "rename" command is like a helpful friend for this job.
It's a tool you use on the command line in Linux to change the names of lots of files all at once.

sudo apt-get install rename

29. rev

When you reverse text in the terminal, you use a command (like rev) to take a string or file input and output the text with the character order reversed, directly in the terminal window.

echo "enter the text" |rev
rev test.txt

30. rm

The rm command in Linux is used to delete files and directories permanently from the file system. It removes data immediately without sending it to any recycle bin, so deleted files cannot be recovered.

rm test.txt
rm -rf test.txt --> recursively and forcefully

31. shred

The shred command is used to securely overwrite the contents of a file, making it much harder to recover the original data.

shred secret.txt --> By default, shred overwrites the file several times and leaves the file itself in place.
shred -u secret.txt --> Overwrite the file and Remove/delete the file

32. sort

The sort command is used to sort a file, arranging the records in a particular order.

sort file.txt --> To sort the lines alphabetically
sort -r file.txt --> To sort in reverse order
sort -n file.txt --> Sorts a file numerically

33. split

The split command lets you break a large file into smaller chunks for easier storage, transfer, or analysis. By default it creates 1000-line pieces and auto-names them with 
alphabetic suffixes like PREFIXaa, PREFIXab

split index.txt
split -l 4 index.txt split_file --> Split File Based on Number of Lines
split -b 16 index.txt index --> Split File Based on File Size

34. tac 

tac is same as cat but it shows content in reverse 

tac example.txt

35. tail

Tail Command is used to display the last part of a file, showing recent content such as logs or updates.
By default, it shows the last 10 lines of a file.

tail state.txt
tail -20 test.txt

36. tar

The tar command (short for Tape Archive) is a powerful tool used to create, view, extract, and manage archive files.

tar -cvf file.tar *.csv --> to create
tar -xvf file.tar --> to extract the tar file
tar -tvf file.tar --> to displays the archive contents without extract

37. touch

The touch command in Linux is used to create an empty file or update the access and modification timestamps of existing files.

touch gfg1.txt gfg2.txt gfg3.txt

38. uniq

The uniq command in Linux is used to detect, report, or remove adjacent duplicate lines from a text file or standard input.

uniq kt.txt --> to remove duplicate from the file
uniq -d kt.txt --> to print duplicate lines only
uniq -c kt.txt --> to print count of lines
uniq -u kt.txt --> to show lines that appear only once

39. wc

The wc command in Linux is used to count lines, words, characters, and bytes in a file or from input you provide.

wc state.txt
wc -l state.txt --> number of lines in a file.
wc -w state.txt --> Number of Words in a file

Directory Operations Commands
=============================

1. cd 

The cd (Change Directory) command is used to navigate between directories in the file system.

cd Documents 
cd dir_1/dir_2/dir_3
cd and cd ~ --> Both commands perform same. It will change directory to home directory from any location.
cd .. --> Move to Parent or One Level Up from the Current Directory

2. dir

The dir command is used to list the contents of a directory, providing an overview of the files and folders within it.

dir -a --> Display All Files Including Hidden Files
dir -l --author --> Displays author of all the files. -l is required to display the contents in the form of a list.

3. dirname

The dirname command is used to extract the directory/path portion from a file path. It removes the final filename from the path.

dirname /home/user/app/application.log --> Output:- /home/user/app

4. dirs

dirs command shell builtin is used to display the list of currently remembered directories. By default, it includes the directory you are currently in.

Hp@DESKTOP-6522LF5 MINGW64 ~/Downloads/New-Devops/Linux (main)
$ dirs
Output below:
~/Downloads/New-Devops/Linux

5. du

The du (Disk Usage) command is used to estimate and display file and directory space usage. 
It helps users identify which files or directories consume the most disk space.

du -h

6. find

The find command is used to search for files and directories based on name, type, size, date, or other conditions.

find / -name "sample.txt"
find / -name *.txt 
find / -name sample.txt -exec rm -i {} \; --> to find and Confirm File Deletion
find ./GFG -empty --> To find empty files and directories
find /path/to/search -mtime -7 --> files modified within the last 7 days

7. lsblk

lsblk stands for List Block Devices. It is used to view disks, partitions, and their mount points on a Linux server.

lsblk --> to List All Block Devices in Linux
lsblk -a --> to Display All Devices, Including Empty Ones
lsblk -b --> to Print sizes in bytes instead of the more human-readable formats

8. mkdir

The mkdir command stands for “make directory” and is used to create new folders quickly and efficiently from the terminal.

mkdir jayesh
mkdir jayesh_1 jayesh_2 jayesh_3

9. mount

The mount command is used to attach a filesystem, disk, or partition to a directory (mount point) so that we can access its files.

mount --> to List Currently Mounted File Systems on Linux

10. pwd

The pwd command displays the full path of your current working directory from the root directory.

Hp@DESKTOP-6522LF5 MINGW64 ~/Downloads/New-Devops/Linux (main)
$ pwd
/c/Users/Hp/Downloads/New-Devops/Linux
Hp@DESKTOP-6522LF5 MINGW64 ~/Downloads/New-Devops/Linux (main)

11. rmdir

The rmdir command in Linux is used to safely remove empty directories from the filesystem.

rmdir dir1 dir2 dir3

12. tree

The tree command displays files and directories in a hierarchical/tree structure. 
It is useful for quickly understanding the structure of an application or project.

tree --> it will show all dir 
tree /opt/app --> Show a specific directory

File Permission and Ownership Commands
======================================

1. chmod 

The chmod (change mode) command in Linux/UNIX is used to modify file and directory permissions.

chmod 745 newfile.txt

2. chattr

chattr stands for change attributes. It is used to change special attributes of files and directories on Linux filesystems.

lsattr file.txt
lsattr -d mydirectory

3. chown

chown stands for Change Owner. It is used to change the owner and/or group of a file or directory.

Syntax:
chown owner_name file_name

Command:
chown master file1.txt

4. chgrp

The `chgrp` command in Linux is used to change the group ownership of a file or directory. All files in Linux belong to an owner and a group

chgrp developers file1.txt file2.txt file3.txt

User Management Commands
=========================

1. chage

If you mean the Linux chage command, it is used to manage password aging and account expiration settings for a user.

sudo chage -l root --> List Account Aging Information
sudo chage -d 2018-12-01 root --> Set Last Password Change Date
sudo chage -E root --> Set Account Expiry Date
sudo chage -W 2 root --> Set Password Expiry Warning

2. chfn

chfn command allows you to change a user's name and other details easily. 'chfn' stands for Change finger

sudo chfn -f Shivang123 shivang --> change the full name on the account.
sudo chfn -w 124567890 shivang --> change the work phone number on the account.
sudo chfn -r 9999 shivang --> change the room number on the account.
sudo chfn -h 123456 shivang --> change the home phone number on the account.

3. chpasswd

chpasswd command is used to change password although passwd command can also do same. 
But it changes the password of one user at a time so for multiple users chpasswd is used.

chpasswd -c SHA512
user1:user1_password
user2:user2_password
user3:user3_password

4. finger

The finger command is used to display information about Linux users, such as their login name, terminal, login time, 
and sometimes their full name or other account details.

finger param --> It will retrieve User Information
finger -s param --> It will Check Idle Status and Login Details

5. id

The id command in Linux is used to display a user’s identity information, including the user name, 
User ID (UID), Group ID (GID), and group memberships.

id --> Display Identity of the Current User
id -g master --> To find a specific user's GID
id -G master --> List All Groups a User Belongs To
id -u master --> To Find the UID of a Specific User

6. passwd

The passwd command is used to change or manage a user's password in Linux.

passwd --> To change your own password
sudo passwd user1 --> To Change Another User's Password
passwd -e user1 --> To Force a User to Change Password on Next Login
sudo passwd -l user2 --> To Lock and Unlock a User Account
sudo passwd -u user2 --> To unlock the account
sudo passwd -x 30 user3 --> To Set Password Expiry (Maximum Password Age)

7. pinky

The pinky command is a lightweight alternative to the finger command. It displays information about currently logged-in users.

pinky --> To get the details of logged in users
pinky param --> To get the report of a single user
pinky -f --> To avoid printing column headings
pinky -w --> To remove the name column
pinky -i --> To remove the name and where column
pinky -q --> To remove the name, idle and where columns
pinky -l param --> To get complete details of a user(long view)

8. username

Username is the name used to identify a user account on a Linux system.

whoami --> to Check User Name in Linux
id --> Find username along with user ID and groups

9. useradd

The useradd command is used to create a new user account in Linux.

sudo useradd param --> This creates the user param.
sudo useradd -m -s /bin/bash param --> Create user with a specific shell
sudo useradd -m -G developers param --> Create user and assign a group

10. userdel

The userdel command is used to delete/remove a user account from a Linux system.

sudo userdel -f param --> Forcefully deletes a user account, even if the user is currently logged in.
sudo userdel -r param --> This will delete the user’s account along with all files in their home directory.
userdel -h --> Displays the help message with command syntax and available options.

11. usermod

The usermod command is used to modify an existing Linux user account.

sudo usermod -c "This is test user" test_user --> To add a comment for a user
sudo usermod -d /home/manav test_user --> To change the home directory of a user
sudo usermod -e 2020-05-29 test_user --> To change the expiry date of a user 
sudo usermod -g manav test_user --> To change the group of a user

12. users

The users command displays the usernames of users currently logged into the Linux.

users --help --> Displaying Help Information
users --version --> Displaying the Version of users

13. who

The who command displays information about users currently logged into the Linux.

who --> It will display current logged in users and time stamp
who am i --> Show current user

14. whoami

The whoami command displays the username of the currently logged-in user.

whoami --> It will display username of the current logged into server

Command	       Purpose
who	           Shows all users currently logged in
whoami	       Shows your current username

Group Management Commands
=========================

1. groupadd

The groupadd command is used to create a new group in Linux.

sudo groupadd developers --> Crate a group named developers and uses sudo for administrative privileges.
sudo groupadd -g 1500 developers --> Create a group with specific GID

2. groupdel

The groupdel command is used to delete an existing group from a Linux system.

sudo groupdel developers --> This removes developers group
sudo groupdel -f developers --> Deletes a group named developers even if it is set as the primary group of a user.


3. groupmod

groupmod command is used to modify or change the existing group on Linux system. It can be handled by superuser or root user.

groupmod -n group_new group_old --> This command will change the group group_old to group_new using -n option.

4. groups

The groups command is used to display the group memberships of a user.

groups --> Display Group Membership of Current User
groups demon --> Viewing Group Memberships of a Specific User
groups root --> Display Group Membership of root User
groups user1 user2 user3 --> Checking Multiple Users at Once

5. gpasswd

The gpasswd command is used to manage users and administrators of Linux groups. It is commonly used to add or remove users from a group.

sudo gpasswd -a john developers --> Add a user to a group
sudo gpasswd -d john developers --> Remove a user from a group
sudo gpasswd developers --> Set a group password

Process Management Commands
===========================

1. accton

'accton' is one of important Linux/Unix command which is used by the administrator to monitor user activities.
It is used to turn on or turn off the process for accounting or change the info process accounting file.

accton on --> Turning On Process Accounting
accton off --> To turn off the process for accounting.


2. bg

The bg command is used to resume a suspended job and run it in the background.

3. chrt

chrt' command in Linux is known for manipulating the real-time attributes of a process. 
It sets or retrieves the real-time scheduling attributes of an existing PID, or runs the command with the given attributes.

4. fg

The fg command in Linux is used to bring a background job to the foreground.

5. kill

The kill command in Linux is used to send signals to processes in order to control their execution.

