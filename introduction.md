# Linux  
 
Linux is a free, open source operating system founded by Linus Torvalds.

## Contents

[Linux directories](https://github.com/thatcatfromspace/linux/blob/main/introduction.md#linux-directories)
[The /dev directory](https://github.com/thatcatfromspace/linux/blob/main/introduction.md#the-dev-directory)
[Essential Linux commands](https://github.com/thatcatfromspace/linux/blob/main/introduction.md#essential-linux-commands)
[General purpose utilities](https://github.com/thatcatfromspace/linux/blob/main/introduction.md#general-purpose-utlities)
[Communication commands](https://github.com/thatcatfromspace/linux/blob/main/introduction.md#communication-commands)
[Shell Variables](https://github.com/thatcatfromspace/linux/blob/main/introduction.md#shell-variables), [Environment Variables](https://github.com/thatcatfromspace/linux/blob/main/introduction.md#environment-variables) & [Shell Operations](https://github.com/thatcatfromspace/linux/blob/main/introduction.md#shell-operations)
[Compression utility](https://github.com/thatcatfromspace/linux/blob/main/introduction.md#compression-utility)

## Topics to cover

- Linux commands

- about Linux

- command line arguments

- string handling

- file handling

- multiple compilation

## Linux directories

- `/bin` - contains software binaries

- `/sbin` - contains essential binaries, require root privileges

- `/dev`- device file system

- `/home` - contains user files

- `/media` - contains different media devices

- `/mnt` - contains different mount points

- `/proc` - contains processes

- `/root` - acts as the home directory for the root user

- `/etc` - contains user details like password

- `/lib` - contains shared libraries, kernel modules

- `/boot` - contains boot loaders like grub

- `/var` - contains data that changes frequently while the system is running

- `/usr` - contains spool, cache etc.,

- `/tmp` - stores temporary files

- `/opt` - stores non-essential software, like the ones the user installs

- `/misc` - miscellaneous files

### The /dev directory

Beautifully demonstrates how everything in Linux is treated as a file, including devices.

Upon performing `ls -l` in the `/dev` directory, we see different 1 character strings in the leftmost column.

The first character specifies the type:

`-` - regular file

`d` - directory

`c` - character (level)

`b` - block (level)

`l` - link (symlink)

`p` - pipe

## Essential Linux commands

Linux has a plethora of commands used to achieve almost all functions using the terminal.

#### man

`man` is the system's manual pager. This command can be used to view the manual for any application. For example, `man gcc`

displays the full manual for the GNU C compiler.

Full manual [here](https://man7.org/linux/man-pages/man1/man.1.html).

### more

This command is used to view the contents of a text file directly in the terminal.

`man` is a filter for paging through text one screenful at a time. Users should realize that`less` provides more emulation plus extensive enhancements, which is kind of ironic.

Usage is quite straightforward. `more text.txt` displays the contents of the file `text.txt`.

Full manual [here](https://man7.org/linux/man-pages/man1/more.1.html).

### mkdir

Command used to create a new directory only if it doesn't already exist.

Usage: `mkdir dirname`

Full manual [here](https://man7.org/linux/man-pages/man1/mkdir.1.html).

`mkdir`, like most other Linux commands, can be paired with flags for more specific use cases.

A few flags include:

 `-m`, `--mode`=_MODE_: set file mode (as in chmod), which is usually a number.
 
 `-p`, `--parents`: no error if existing, make parent directories as needed,  with their file modes unaffected by any `-m` option.

### rmdir

Opposite of `mkdir`. Removes a specified **empty** directory. For directories that have contents within, use `rm -r`.

Full manual [here](https://man7.org/linux/man-pages/man1/rmdir.1.html).

### ls

Probably the most important and most used Linux command. This command lists the contents of a directory.

A few flags include:

`-a`, `--all`: lists hidden files (starting with `.`)

`-r`, `--reverse`: prints the contents in reverse

`-F`, `--classify`: appends indicators  (one of */=>@|) to the entries.

`-R`, `--rescursive`: lists sub-directories recursively.

`-x`: lists entries by lines instead of columns

`-i`, `--inode`: print the index number of each file.

`-l`, `--long`: use a long listing format

### cat

`cat` is a versatile command with multiple uses. When used without any symbols, `cat` concatenates the contents of two files and prints it to `stdout`.

`cat ><file>` toggles an editor mode where text can be inserted directly into the file. Use `Ctrl + C` to close editor mode.

Full manual [here](https://www.man7.org/linux/man-pages/man1/cat.1.html).

### echo

`echo hello` prints `hello` to the output.

### rm

Removes specified file from the directory.

Full manual [here](https://man7.org/linux/man-pages/man1/rm.1.htmlhttps://man7.org/linux/man-pages/man1/rm.1.html).

### cp

Copies files/directories from SOURCE to DEST. Takes in two arguments by default.

Full manual [here](https://man7.org/linux/man-pages/man1/cp.1.html).


## General purpose utilities

### pwd

`pwd` prints name of current/working directory.

Full manual [here](https://man7.org/linux/man-pages/man1/pwd.1.html).

### date

Prints the full system date and time.

### passwd

The `passwd` command changes passwords for user accounts. A normal user may only change the password for their own account, while the superuser may change the password for any account.

Full manual [here](https://man7.org/linux/man-pages/man1/passwd.1.html).

### wc

Print newline, word, and byte counts for each FILE, and a total line if more than one FILE is specified.

### who

Show who is logged in.

Full manual [here](https://man7.org/linux/man-pages/man1/who.1.html).

### file

Determines the file type.

Full manual [here](https://man7.org/linux/man-pages/man1/file.1.html).

### script

`script` makes a typescript of everything on your terminal session. The terminal data are stored in raw form to the log file and information about timing to another (optional) structured log file.

Full manual [here](https://man7.org/linux/man-pages/man1/script.1.html).

### cal

Displays a simple calendar.

Full manual [here](https://man7.org/linux/man-pages/man1/cal.1.html).

### tty

`tty` prints the file name of the terminal connected to standard input.

Full manual [here]( https://man7.org/linux/man-pages/man1/tty.1.html#).


### uname

Prints system information.

Full manual [here](https://man7.org/linux/man-pages/man1/uname.1.html).

### banner

Really fun command is used to create large, ASCII art-style text banners on the terminal. It takes a text string as input and converts it into a banner made up of block characters. This is often used for decorative or informational purposes in scripts or terminal messages.

Full manual [here](https://man7.org/linux/man-pages/man6/banner.6.html).

### df

The `df` command is used to display information about disk space usage on Linux systems. It shows the total, used, and available disk space for mounted file systems. This command is valuable for monitoring disk usage and identifying potential storage issues.

Full manual [here](https://man7.org/linux/man-pages/man1/df.1.html).

### du

The `du` command is used to estimate and display the disk space usage of files and directories. It provides information on the space consumed by each file or directory, aiding in identifying large files or directories.

Full manual [here](https://man7.org/linux/man-pages/man1/du.1.html).

### chmod

The `chmod` command is used to change the permissions of a file or directory in Linux. It allows users to specify who can read, write, and execute a file. Permissions are adjusted using symbolic or octal notation.

Full manual [here](https://man7.org/linux/man-pages/man1/chmod.1.html).

### chgrp

The `chgrp` command is used to change the group ownership of a file or directory in Linux. It allows users to assign a specific group to a file, providing group-level access control.

Full manual [here](https://man7.org/linux/man-pages/man1/chgrp.1.html).

### chown

The `chown` command is used to change the user and group ownership of a file or directory in Linux. It allows users to assign ownership to a specific user and group, controlling access permissions.

Full manual [here](https://man7.org/linux/man-pages/man1/chown.1.html).

### find

The `find` command is used for searching files and directories based on various criteria such as name, type, or size. It is a powerful and flexible tool for locating files in a directory hierarchy.

Full manual [here](https://man7.org/linux/man-pages/man1/find.1.html).

### cmp

The `cmp` command is used to compare two files byte by byte and displays the first differing bytes and their respective byte numbers. It helps identify the exact location and nature of differences between two files.

Full manual [here](https://man7.org/linux/man-pages/man1/cmp.1.html).

### comm

The `comm` command is used to compare two sorted files line by line and display the lines that are common, unique to the first file, and unique to the second file. It is useful for finding similarities and differences between files.

Full manual [here](https://man7.org/linux/man-pages/man1/comm.1.html).

### diff

The `diff` command is used to compare the contents of two files line by line. It highlights the differences, making it easier to understand changes between versions of a file.

Full manual [here](https://man7.org/linux/man-pages/man1/diff.1.html).

### spell

The `spell` command is used to check the spelling of words in a text file. It identifies potentially misspelled words, providing suggestions for corrections.

Full manual [here](https://man7.org/linux/man-pages/man1/spell.1.html).

### umask

The `umask` command is used to set the default file and directory permissions for new files created by a user. It helps control the security settings applied to files and directories upon creation.

Full manual [here](https://man7.org/linux/man-pages/man2/umask.2.html).

### basename

The `basename` command is used to strip directory and suffix information from a file path, leaving only the base filename. It is useful for extracting filenames from full paths.

Full manual [here](https://man7.org/linux/man-pages/man1/basename.1.html).

### split

The `split` command is used to split a file into smaller parts. It is often used for breaking up large files into more manageable pieces for easier storage or transmission.

Full manual [here](https://man7.org/linux/man-pages/man1/split.1.html).

### finger

The `finger` command is used to display information about users on a system. It provides details such as login time, idle time, and a user's plan. However, its usage has declined in favor of more modern user information tools.

Full manual [here](https://man7.org/linux/man-pages/man1/finger.1.html).

### stty

The `stty` command is used to change and print terminal line settings in Unix-like operating systems. It allows users to configure various aspects of terminal behavior, such as echo settings and control characters.

Full manual [here](https://man7.org/linux/man-pages/man1/stty.1.html).

### sleep

The `sleep` command is used to introduce a delay for a specified amount of time. It is often used in shell scripts to pause execution for a set duration.

Full manual [here](https://man7.org/linux/man-pages/man1/sleep.1.html).

### history

The `history` command is used to display a list of previously executed commands in the current shell session. It provides a record of commands for reference and allows users to repeat or modify previous commands.

Full manual [here](https://man7.org/linux/man-pages/man3/history.3.html).

### alias

The `alias` command is used to create shortcuts or alternate names for longer commands. It allows users to define custom abbreviations for frequently used commands.

Full manual [here](https://man7.org/linux/man-pages/man1/alias.1p.html).

### unalias

The `unalias` command is used to remove aliases previously defined with the `alias` command. It helps in managing and cleaning up the alias environment.

Full manual [here](https://man7.org/linux/man-pages/man1/unalias.1p.html).

### bc

The `bc` command is an arbitrary-precision calculator language. It allows users to perform mathematical calculations with a wide range of precision and supports various mathematical functions.

Full manual [here](https://man7.org/linux/man-pages/man1/bc.1.html).

### join

The `join` command is used to combine lines from two files based on a common field. It is particularly useful for merging data from different sources.

Full manual [here](https://man7.org/linux/man-pages/man1/join.1.html).


## Simple filters

### head

The `head` command is used to display the first few lines of a text file. By default, it shows the first 10 lines, but you can specify a different number with the `-n` option.

Full manual [here](https://man7.org/linux/man-pages/man1/head.1.html).

### tail

The `tail` command is used to display the last few lines of a text file. By default, it shows the last 10 lines, but you can specify a different number with the `-n` option.

Full manual [here](https://man7.org/linux/man-pages/man1/tail.1.html).

### cut

The `cut` command is used to extract specific sections (columns) from each line of a file or from piped input. It is often used for working with delimited text files.

Full manual [here](https://man7.org/linux/man-pages/man1/cut.1.html).

### paste

The `paste` command is used to merge lines of files horizontally by concatenating corresponding lines from each file. It is often used in conjunction with other commands or scripts.

Full manual [here](https://man7.org/linux/man-pages/man1/paste.1.html).

### expr

The `expr` command is used for evaluating expressions in shell scripts. It supports basic arithmetic operations, string comparisons, and other expressions.

Full manual [here](https://man7.org/linux/man-pages/man1/expr.1.html).

### sort

The `sort` command is used to sort lines of text files or input streams. It can be customized to sort based on different criteria, such as numeric values or specific fields within each line.

Full manual [here](https://man7.org/linux/man-pages/man1/sort.1.html).

### tr

The `tr` command is used for translating or deleting characters. It is often used for simple character transformations in a text stream.

Full manual [here](https://man7.org/linux/man-pages/man1/tr.1.html).

### pr

The `pr` command is used to format and paginate text files for printing. It provides options to control page layout, headers, and footers.

Full manual [here](https://man7.org/linux/man-pages/man1/pr.1.html).

### nl

The `nl` command is used to number lines in a text file. It is often used for adding line numbers to the contents of a file.

Full manual [here](https://man7.org/linux/man-pages/man1/nl.1.html).

### uniq

The `uniq` command is used to filter out repeated lines in a sorted text file or input stream. It is often used in combination with the `sort` command.

Full manual [here](https://man7.org/linux/man-pages/man1/uniq.1.html).


## Communication commands

### ifconfig

The `ifconfig` command is used to configure and display information about network interfaces on Unix-like operating systems. It provides details such as IP addresses, network masks, and interface status.

Full manual [here](https://man7.org/linux/man-pages/man8/ifconfig.8.html).

### netstat

The `netstat` command displays information about network connections, routing tables, interface statistics, masquerade connections, and multicast memberships. It is a versatile tool for monitoring and troubleshooting network-related issues.

Full manual [here](https://man7.org/linux/man-pages/man8/netstat.8.html).

### ftp

The `ftp` command is a file transfer protocol used to interact with FTP servers. It allows users to upload or download files to and from remote servers using the File Transfer Protocol.

Full manual [here](https://man7.org/linux/man-pages/man1/ftp.1.html).

### route

The `route` command is used to view and manipulate the IP routing table. It displays or modifies the system's routing information, which determines the path that network packets take to reach their destination.

Full manual [here](https://man7.org/linux/man-pages/man8/route.8.html).

### whois

The `whois` command is used to query the WHOIS database, which contains information about domain registrations and IP allocations. It provides details about the owner, registration date, and contact information for a domain.

Full manual [here](https://man7.org/linux/man-pages/man1/whois.1.html).

### tracepath

The `tracepath` command is similar to `traceroute` and is used to discover the network path packets take to reach a destination. It provides information about the routers or hops between the source and destination.

Full manual [here](https://man7.org/linux/man-pages/man8/tracepath.8.html).

### ip

The `ip` command is a powerful tool for configuring and displaying information about network interfaces, routing, and tunneling. It is part of the iproute2 suite and is the successor to `ifconfig` and `route`.

Full manual [here](https://man7.org/linux/man-pages/man8/ip.8.html).

### ping

The `ping` command is used to test the reachability of a host on an Internet Protocol (IP) network. It sends ICMP Echo Request messages to the destination and reports the round-trip time and packet loss.

Full manual [here](https://man7.org/linux/man-pages/man8/ping.8.html).

### Shell Variables:

1. **SHELL:**
   - **Description:** Contains the path to the user's preferred shell.
   - **Example:** `/bin/bash`
   
2. **TERM:**
   - **Description:** Specifies the terminal type or emulator in use, affecting how text is displayed.
   - **Example:** `xterm`

3. **MAIL:**
   - **Description:** Specifies the location of the user's mailbox.
   - **Example:** `/var/mail/username`

4. **PS1:**
   - **Description:** Defines the primary prompt string for the shell.
   - **Example:** `\u@\h:\w\$`

5. **PS2:**
   - **Description:** Defines the secondary prompt string used when more input is expected.
   - **Example:** `> `

6. **USER:**
   - **Description:** Stores the username of the current user.
   - **Example:** `john_doe`

7. **LOGNAME:**
   - **Description:** Holds the login name of the user.
   - **Example:** `john_doe`

### Set Options:

8. **set - and set +:**
   - **Description:** Enables or disables options or attributes within a script or shell session.

9. **set -x:**
   - **Description:** Enables debugging by printing each command to standard error before executing it.

10. **set +x:**
	- **Description:** Disables the debugging mode set by `set -x`.

11. **set no clobber:**
	- **Description:** Prevents overwriting existing files with the `>` operator in redirection.

12. **set \` \`:**
	- **Description:** Forces the shell to treat adjacent whitespace as a single delimiter when parsing commands.

### Environment Variables:

13. **setenv:**
	- **Description:** Command used in some shells (e.g., csh) to set environment variables.

14. **unset:**
	- **Description:** Removes the value and existence of a variable or function.

### Shell Operations:

15. **Merging Streams:**
	- **Description:** Combining the standard output and standard error streams, often done using `2>&1`.

16. **wait:**
	- **Description:** Pauses execution until all background processes are complete.

17. **. profile:**
	- **Description:** Reads and executes commands from the user's profile file, often used during login.

### Miscellaneous:

18. **vacation:**
	- **Description:** A utility that informs users about the sender's absence via email auto-replies.

19. **.plan:**
	- **Description:** A user's plan file, traditionally used to leave messages or plans for other users to see.

20. **.project:**
	- **Description:** A file where users can describe their ongoing projects for others to view.


## Compression utility
### compress

The `compress` command is utilized to compress files using the compress algorithm. It replaces the original file with a compressed version having the extension `.Z`.

Full manual [here](https://man7.org/linux/man-pages/man1/compress.1.html).

### uncompress

The `uncompress` command is employed to decompress files compressed with `compress`. It restores the original file from its compressed version.

Full manual [here](https://man7.org/linux/man-pages/man1/uncompress.1.html).

### gzip

The `gzip` command is employed to compress files using the `gzip` compression algorithm. It creates a compressed file with the extension `.gz`.

Full manual [here](https://man7.org/linux/man-pages/man1/gzip.1.html).

### gunzip

The `gunzip` command is used to decompress files compressed with `gzip`. It restores the original file from its compressed version.

Full manual [here](https://man7.org/linux/man-pages/man1/gunzip.1.html).

### tar

The `tar` command is employed for creating and manipulating archive files. It can combine multiple files and directories into a single archive, optionally compressing the archive using tools like `gzip`.

Full manual [here](https://man7.org/linux/man-pages/man1/tar.1.html).

- To create an archive: `tar -cvf archive.tar file1 file2 directory`
- To extract an archive: `tar -xvf archive.tar`
- To compress while creating: `tar -czvf archive.tar.gz file1 file2 directory`


