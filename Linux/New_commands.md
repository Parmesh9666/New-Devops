
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
