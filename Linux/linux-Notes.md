## 1. File Operational Commands

* cat: Concatenate and display file content.
* cksum: Print CRC checksum and byte counts.
* cmp: Compare two files byte by byte.
* cp: Copy files and directories.
* cut: Remove sections from each line of files.
* diff: Compare files line by line.
* echo: Display a line of text or string.
* head: Output the first part of files.
* ln: Create links between files.
* more: View file content one screenful at a time.
* mv: Move or rename files and directories.
* rm: Remove files or directories.
* sort: Sort lines of text files.
* tail: Output the last part of files.
* tar: Archive utility to pack/unpack files.
* touch: Change file timestamps or create empty files.
* uniq: Report or omit repeated lines.
* wc: Print newline, word, and byte counts.

## 2. Directory Operations Commands

* cd: Change the working directory.
* dir: List directory contents.
* dirname: Strip last component from file name.
* dirs: Display the list of currently remembered directories.
* du: Estimate file space usage.
* find: Search for files in a directory hierarchy.
* mkdir: Create new directories.
* mount: Mount a file system.
* pwd: Print name of current/working directory.
* rmdir: Remove empty directories.

## 3. File Permission and Ownership Commands

* chmod: Change file mode bits (permissions).
* chown: Change file owner and group.
* chgrp: Change group ownership.

## 4. User Management Commands

* passwd: Change user password.
* username: Dummy placeholder for target user identification.
* useradd: Create a new user or update default new user information.
* usermod: Modify a user account.
* users: Print the user names of users currently logged in.
* who: Show who is logged on.
* whoami: Print effective user ID.

## 5. Process Management Commands

* kill: Send a signal to a process (usually to stop it).
* ps: Report a snapshot of the current processes.
* top: Display Linux processes in real-time.
* htop: Interactive process viewer and system monitor.
* time: Run programs and summarize system resource usage.
* watch: Execute a program periodically, showing output fullscreen.
* vmstat: Report virtual memory statistics.
* uptime: Tell how long the system has been running.

## 6. Networking Commands

* arp: Manipulate the system ARP cache.
* curl: Transfer data from or to a server.
* host: DNS lookup utility.
* hostid: Print the numeric identifier for the current host.
* hostname: Show or set the system's host name.
* hostnamectl: Control the system hostname.
* ifconfig: Configure a network interface.
* iftop: Display bandwidth usage on an interface by host.
* ifup: Bring a network interface up.
* ip: Show / manipulate routing, network devices, interfaces and tunnels.
* ipcrm: Remove certain IPC resources.
* ipcs: Provide information on IPC facilities.
* iptables: Administration tool for IPv4 packet filtering and NAT.
* iptables-save: Dump iptables rules to stdout.
* iwconfig: Configure a wireless network interface.
* nc (netcat): Arbitrary data transfer and network debugging.
* netstat: Print network connections, routing tables, and interface statistics.
* nmcli: Command-line tool for controlling NetworkManager.
* nslookup: Query Internet name servers interactively.
* ping: Send ICMP ECHO_REQUEST to network hosts.
* rcp: Secure remote file copy (legacy).
* route: Show / manipulate the IP routing table.
* rsync: Fast, versatile, remote and local file-copying tool.
* scp: Secure copy (remote file copy program).
* ssh: OpenSSH SSH client (remote login program).
* tracepath: Trace path to a network host discovering MTU along the way.
* traceroute: Print the route packets trace to network host.
* vnstat: Console-based network traffic monitor.
* wget: Non-interactive network downloader.

## 8. Package Management Commands

* apt: Command-line interface for the package management system.
* apt-get: APT package handling utility (low-level).
* aptitude: High-level interface to the package manager.

## 9. Job Scheduling Commands

* atd: Run jobs queued for later execution.
* atrm: Delete jobs, identified by their job number.
* atq: List the user's pending jobs.
* batch: Execute commands when system load levels permit.
* cron: Daemon to execute scheduled commands.
* crontab: Maintain crontab files for individual users.

## 10. Disk and File System Commands

* cfdisk: Display or manipulate a disk partition table with a text-user interface.
* df: Report file system disk space usage.
* dosfsck: Check and repair MS-DOS file systems.
* dump: Ext2/3 file system backup.
* dumpe2fs: Dump ext2/ext3/ext4 file system information.
* fdisk: Manipulate disk partition table.
* mount: Mount a file system.
* restore: Restore files from a backup created by dump.
* sync: Flush file system buffers.

## 11. Hardware and System Information Commands

* acpi: Shows battery status and other ACPI information.
* acpi_available: Test whether ACPI subsystem is available.
* acpid: Advanced Configuration and Power Interface event daemon.
* arch: Print machine hardware name (same as uname -m).
* dmesg: Print or control the kernel ring buffer.
* dmidecode: Tool for dumping a computer's DMI table contents in human-readable format.
* dstat: Versatile resource statistics tool.
* free: Display amount of free and used memory in the system.
* hdparm: Get/set SATA/IDE device parameters.
* hwclock: Query or set the hardware clock (RTC).
* iostat: Report Central Processing Unit (CPU) statistics and input/output statistics for devices.
* iotop: Simple top-like I/O monitor.
* lsusb: List USB devices.
* lshw: List hardware configuration details.
* uname: Print system information.

## 12. Compression and Archiving Commands

* ar: Create, modify, and extract from archives.
* bzcmp: Compare bzip2 compressed files.
* bzdiff: Compare bzip2 compressed files line by line.
* bzgrep: Search bzip2 compressed files for a regular expression.
* bzip2: A block-sorting file compressor.
* bzless: View bzip2 compressed text files screen by screen.
* bzmore: View bzip2 compressed text files.
* gunzip: Decompress files compressed with gzip.
* gzip: Compress or expand files.
* gzexe: Compress executable files in place.
* zip: Package and compress (archive) files.
* zdiff: Compare compressed files.
* zgrep: Search compressed files for a regular expression.

## 13. Text Processing and Formatting Commands

* awk: Pattern scanning and processing language.
* aspell: Interactive spell checker.
* banner: Print large banner text.
* bc: An arbitrary precision calculator language.
* col: Filter reverse line-feeds from input.
* colcrt: Filter nroff output for CRT preview.
* colrm: Remove columns from a file.
* column: Columnate lists into neat tabular forms.
* dc: An arbitrary precision calculator.
* egrep: Search file(s) for an extended regular expression (grep -E).
* fgrep: Search file(s) for a fixed-string regular expression (grep -F).
* fmt: Simple optimal text formatter.
* grep: Print lines matching a pattern.
* sdiff: Side-by-side merge of file differences.
* sed: Stream editor for filtering and transforming text.
* tr: Translate or delete characters.
* unix2dos: Convert text file format from ISO/Mac/Unix to MS-DOS.

## 14. Kernel and Module Management Commands

* depmod: Generate modules.dep and map files.
* insmod: Simple program to insert a module into the Linux Kernel.
* lsmod: Show the status of modules in the Linux Kernel.
* modinfo: Show information about a Linux Kernel module.
* rmmod: Simple program to remove a module from the Linux Kernel.
* systemctl: Control the systemd system and service manager.

## 15. System Control and Power Commands

* halt: Instruct the hardware to stop all CPU functions.
* poweroff: Send an ACPI command to power down the system.
* reboot: Restart the system.
* shutdown: Bring the system down securely.

## 16. Logging and Monitoring Commands

* journalctl: Query the systemd journal logs.
* last: Show a list of last logged-in users.
* history: GNU History Library command wrapper to view past executed terminal runs.
* sar: Collect, report, or save system activity information.
* script: Make typescript of terminal session.
* scriptreplay: Play back typescripts created by script.

## 17. Checksum and File Integrity Commands

* md5sum: Compute and check MD5 message digest.
* cksum: Print CRC checksum and byte counts.
* sum: Checksum and count the blocks in a file.

## 18. Date and Time Commands

* cal: Display a calendar.
* date: Print or set the system date and time.
* uptime: Tell how long the system has been running.

## 19. Mail and User Communication Commands

* biff: Mail arrival notification tool.
* mailq: Print the mail queue summary.
* write: Send a message to another logged-in user.
* wall: Write a message to all logged-in users.

## 20. Printing and Media Commands

* amixer: Command-line mixer for ALSA soundcard driver.
* aplay: Command-line sound recorder and player for ALSA soundcard driver.
* aplaymidi: Play standard MIDI files.
* cupsd: Common UNIX Printing System daemon.
* eject: Eject removable media.
* import: Capture an X server screen and save it to file (ImageMagick tool).

## 21. Shell Built-in and Scripting Commands

* alias: Define or display aliases.
* bind: Set or view Readline key bindings.
* break: Exit from within a for, while, or until loop.
* builtin: Run a shell builtin command instead of an executable program.
* case: Multi-way conditional branch command.
* continue: Skip the rest of the current iteration of a loop.
* declare: Declare variables and give them attributes.
* enable: Enable and disable builtin shell commands.
* env: Run a program in a modified environment.
* eval: Construct command by concatenating arguments.
* exec: Replace the shell process with the specified command.
* exit: Cause the shell to exit.
* expect: Programmed dialogue automation tool.
* export: Set an environment variable to be passed to child processes.
* expr: Evaluate expressions.
* factor: Factor numbers into primes.
* fc: Format and execute commands from history list.
* function: Define shell function blocks.
* for: Loop construct for iterating over list components.
* if: Conditional block statement.
* let: Evaluate arithmetic expressions on shell variables.
* printf: Format and print data.
* read: Read a line from standard input.
* return: Return from a shell function.
* select: Generate conditional choices menus.
* seq: Print a sequence of numbers.
* setsid: Run a program in a new session.
* shift: Shift positional parameters leftward.
* source: Execute commands from a file in the current shell context.
* type: Locate a command and describe its type classification.
* until: Loop construct executing until an exit criteria evaluated true.
* while: Loop construct executing while an exit condition evaluates true.
* yes: Output a string repeatedly until killed.
* sudo: Execute a command as another user (usually superuser).
* sleep: Delay for a specified amount of time.

