
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


