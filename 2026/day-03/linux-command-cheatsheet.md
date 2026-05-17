## Process management command
# Monitoring Processes
These commands allow you to see what is currently running and how much CPU or memory they are consuming.
1. ps (Process Status): Provides a static snapshot of current processes.
Example: ps aux lists every process running on the system with detailed info like user, PID, and CPU usage.

2. top: Displays a real-time, interactive list of processes, automatically updating every few seconds.
Example: Simply type top in the terminal to see a live view of resource-heavy tasks.

3. htop: An enhanced, user-friendly version of top with color-coded graphs and mouse support.

## Terminating Processes
When a program becomes unresponsive or needs to be stopped, you use these commands to send signals to the process.
1. kill: Sends a signal (usually SIGTERM or SIGKILL) to a specific PID.
2. kill <PID> politely requests PID 1234 to stop.
3. kill -9 <PID> forcefully terminates it.
4. killall: Terminates all processes that match a specific name.

## Utility Commands
pgrep: 
Finds the PID of a process based on its name.
1. pgrep chrome returns the PIDs of all Chrome processes.
2. uptime: Shows how long the system has been running and the current system load average


## File Systems Commands

Linux file system commands allow you to navigate, manage, and manipulate files and directories directly from the terminal. 
1. pwd (Print Working Directory): Shows the full path of the directory you are currently in.
   Example: pwd might output /home/user/Documents.
2. ls (List): Lists the files and directories in your current location.
   Example: ls -l shows a detailed list with file sizes and permissions.
3. cd (Change Directory): Used to move between folders.

## File & Directory Management

These commands are used to create, copy, move, and delete data.mkdir (Make Directory): 
1. mkdir new_folder-->creates a folder named "new_folder".
2. touch: Creates a new, empty file .
   Example: touch report.txt creates an empty file named "report.txt".
3. cp (Copy): Copies files or directories from one place to another.
   Example: cp file.txt /home/user/backup/ copies the file to a backup folder.
4. mv (Move/Rename): Moves a file to a new location or renames it.
   Example: mv oldname.txt newname.txt renames the file.
5. rm (Remove): Deletes files or directories permanently.
   Example: rm file.txt deletes a file;
6. rm -r folder_name deletes a folder and everything inside it.
   
7. cat (Concatenate): File Content these to look inside files without fully opening an editor.
   Displays the entire content of a file in the terminal.
   Example: cat notes.txt  -->prints the text of notes.txt to your screen.

8. head / tail: Shows the beginning or the end of a file.
   Example: tail -n 10 log.txt displays the last 10 lines of a log file.

9. grep: Searches for a specific pattern or text within files.
   Example: grep "error" server.log finds every line containing "error".

## Disk & Permissions
These commands help manage how the system stores data and who can access it.

1. df (Disk Free): Shows the amount of available and used disk space on your file systems.
   Example: df -h provides this info in "human-readable" format (GB/MB).
   
2. chmod (Change Mode): Changes the read, write, and execute permissions of a file.
   Example: chmod 755 script.sh makes a script executable by the owner.
   
3. find: Searches for files and directories based on names, size, or time.
   Example: find . -name "*.jpg" finds all JPEG files in the current directory.
   
   For more detailed information on any command, you can use the man (manual) command, such as man ls,
   to see all available options and syntax.


## Networking commands
1. ipconfig or ip addr --> to show ip address
2. ping --> to ping the host
   Example: ping google.com or ping -c 4 google.com (Sends 4 packets to Google and stops).
3. raceroute --> Displays every "hop" (router) a packet passes through to reach its destination.
   It is essential for finding where a network path is broken.
   Example: traceroute 8.8.8.8
4. dig: The standard tool for querying DNS name servers for specific records (A, MX, CNAME, etc.).
   Example: dig google.com

