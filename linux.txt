# 1. File and Directory Management
ls: Lists directory contents.
cd: Changes the current directory.
pwd: Prints the current directory.
mkdir: Creates a new directory.
rmdir: Removes an empty directory.
touch: Creates an empty file.
cp: Copies files or directories.
mv: Moves or renames files or directories.
rm: Removes files or directories.
find: Searches for files and directories.
locate: Finds files by name using a pre-built index.
tree: Displays directories in a tree-like format.

2. File Viewing
cat: Concatenates and displays file content.
less: Displays file content one screen at a time.
more: Similar to less, but with fewer features.
head: Displays the first few lines of a file.
tail: Displays the last few lines of a file.
nano: Opens a file in the nano text editor.
vim: Opens a file in the Vim text editor.
wc: Counts lines, words, and characters in a file.
3. File Permissions and Ownership
chmod: Changes file permissions.
chown: Changes file ownership.
chgrp: Changes the group ownership of a file.
4. Compression and Archiving
tar: Archives files.
gzip: Compresses files using gzip.
gunzip: Decompresses gzip files.
zip: Creates a zip archive.
unzip: Extracts files from a zip archive.
5. Networking
ping: Tests network connectivity.
ifconfig: Displays or configures network interfaces.
ip: Displays or configures network interfaces (preferred over ifconfig).
netstat: Displays network connections and statistics.
curl: Transfers data from or to a server.
wget: Downloads files from the web.
ssh: Connects to a remote server via SSH.
scp: Securely copies files between systems.
rsync: Synchronizes files between systems.
6. Disk Usage and Management
df: Displays disk space usage.
du: Displays directory size.
mount: Mounts a filesystem.
umount: Unmounts a filesystem.
lsblk: Lists information about block devices.
fdisk: Manages disk partitions.
mkfs: Formats a filesystem.
blkid: Displays block device attributes.
7. System Monitoring
top: Displays real-time system performance.
htop: Interactive process viewer (better than top).
ps: Displays active processes.
uptime: Shows system uptime.
free: Displays memory usage.
vmstat: Displays system performance metrics.
iostat: Displays CPU and I/O statistics.
8. Package Management
Debian-Based Systems (e.g., Ubuntu)
apt-get: Installs, updates, and removes packages.
apt: Modern alternative to apt-get.
dpkg: Low-level package management.
Red Hat-Based Systems (e.g., CentOS, Fedora)
yum: Installs, updates, and removes packages.
dnf: Modern alternative to yum.
rpm: Manages RPM packages.
9. Process Management
kill: Sends a signal to terminate a process.
killall: Terminates all processes by name.
pkill: Terminates processes by name or attributes.
bg: Resumes a background job.
fg: Resumes a foreground job.
jobs: Lists active jobs.
10. User Management
who: Displays logged-in users.
whoami: Displays the current user.
id: Displays user and group IDs.
adduser: Adds a new user.
deluser: Deletes a user.
passwd: Changes a user password.
usermod: Modifies user accounts.
groups: Displays user groups.
11. System Information
uname: Displays system information.
hostname: Displays or sets the hostname.
dmesg: Displays system boot messages.
uptime: Displays system uptime.
lscpu: Displays CPU information.
lsusb: Lists USB devices.
lspci: Lists PCI devices.
12. Permissions and Access Control
umask: Sets file permission defaults.
sudo: Runs commands with superuser privileges.
su: Switches user accounts.
13. Shell Utilities
echo: Displays text or variables.
alias: Creates command shortcuts.
history: Displays command history.
clear: Clears the terminal screen.
14. Development and Scripting
gcc: Compiles C programs.
make: Builds programs from source.
bash: Starts a Bash shell.
sh: Executes shell scripts.
15. Miscellaneous
date: Displays or sets the system date and time.
cal: Displays a calendar.
sleep: Delays execution.
man: Displays the manual for a command.
info: Displays command documentation.
help: Displays help for shell-built-in commands.





1. File and Directory Management
ls
Usage: List contents of a directory.
bash
Copy code
ls          # List files in the current directory
ls -l       # Detailed list (permissions, size, etc.)
ls -a       # List all files, including hidden ones
ls /etc     # List contents of the /etc directory
cd
Usage: Change directory.
bash
Copy code
cd /home          # Go to the /home directory
cd ..             # Go up one directory
cd ~/Documents    # Go to the Documents folder in your home directory
mkdir
Usage: Create directories.
bash
Copy code
mkdir new_folder            # Create a directory named "new_folder"
mkdir -p dir1/dir2/dir3     # Create nested directories
rm
Usage: Delete files or directories.
bash
Copy code
rm file.txt                # Remove a file
rm -r folder_name          # Remove a directory and its contents
rm -i file.txt             # Prompt before removing
2. File Viewing
cat
Usage: View the content of a file.
bash
Copy code
cat file.txt                # Display file content
cat file1.txt file2.txt     # Concatenate and display multiple files
less
Usage: View large files one screen at a time.
bash
Copy code
less largefile.txt          # Scroll with arrow keys
head
Usage: Display the first few lines of a file.
bash
Copy code
head file.txt               # Show the first 10 lines
head -n 5 file.txt          # Show the first 5 lines
tail
Usage: Display the last few lines of a file.
bash
Copy code
tail file.txt               # Show the last 10 lines
tail -f log.txt             # Show live updates to a file
3. File Permissions and Ownership
chmod
Usage: Change file permissions.
bash
Copy code
chmod 755 script.sh         # Assign read, write, execute for owner; read, execute for others
chmod u+x file.sh           # Add execute permission for the user
chmod -R 644 folder/        # Change permissions recursively
chown
Usage: Change file ownership.
bash
Copy code
chown user file.txt         # Change the owner of the file
chown user:group file.txt   # Change owner and group
chown -R user folder/       # Change ownership recursively
4. Compression and Archiving
tar
Usage: Archive files.
bash
Copy code
tar -cvf archive.tar file1 file2        # Create an archive
tar -xvf archive.tar                    # Extract an archive
tar -czvf archive.tar.gz folder/        # Create a compressed archive
gzip
Usage: Compress files.
bash
Copy code
gzip file.txt                          # Compress file
gunzip file.txt.gz                     # Decompress file
zip
Usage: Create a zip archive.
bash
Copy code
zip archive.zip file1 file2            # Create a zip archive
unzip archive.zip                      # Extract a zip archive
5. Networking
ping
Usage: Test network connectivity.
bash
Copy code
ping google.com                        # Send ICMP packets to test connectivity
ping -c 4 google.com                   # Send only 4 packets
curl
Usage: Transfer data from or to a server.
bash
Copy code
curl http://example.com                # Fetch content from a URL
curl -O http://example.com/file.txt    # Download a file
wget
Usage: Download files.
bash
Copy code
wget http://example.com/file.txt       # Download a file
wget -r http://example.com/folder/     # Download files recursively
scp
Usage: Copy files securely between machines.
bash
Copy code
scp file.txt user@remote:/path/to/dest # Copy file to a remote machine
scp user@remote:/path/to/file.txt ./   # Copy file from a remote machine
6. Disk Usage and Management
df
Usage: Display disk space usage.
bash
Copy code
df -h                                  # Display disk usage in human-readable format
du
Usage: Show directory size.
bash
Copy code
du -sh folder/                        # Display total size of a folder
du -h --max-depth=1                   # Show size of each subdirectory
lsblk
Usage: List block devices.
bash
Copy code
lsblk                                 # Show disk partitions and sizes
7. System Monitoring
top
Usage: Display real-time system performance.
bash
Copy code
top                                   # View processes and system stats
htop
Usage: Interactive process viewer.
bash
Copy code
htop                                  # Navigate with arrow keys, kill processes interactively
free
Usage: Display memory usage.
bash
Copy code
free -h                               # Show memory usage in human-readable format
8. Process Management
kill
Usage: Terminate a process.
bash
Copy code
kill PID                              # Kill a process by its PID
kill -9 PID                           # Force kill a process
jobs
Usage: List active jobs.
bash
Copy code
jobs                                  # Show background jobs
bg %1                                # Resume job 1 in the background
fg %1                                # Bring job 1 to the foreground
9. User Management
adduser
Usage: Add a new user.
bash
Copy code
sudo adduser username                 # Add a user
passwd
Usage: Change a user password.
bash
Copy code
sudo passwd username                  # Set a password for a user
10. Package Management
Debian-Based Systems
bash
Copy code
sudo apt update                       # Update package list
sudo apt install package_name         # Install a package
sudo apt remove package_name          # Remove a package
Red Hat-Based Systems
bash
Copy code
sudo yum install package_name         # Install a package
sudo yum remove package_name          # Remove a package



