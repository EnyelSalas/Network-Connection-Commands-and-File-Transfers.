# Linux Network and File Tranfer Command

Welcome to the **Linux Network Command Cheat Sheet**! This repository provides a categorized collection of essential network-related commands for Linux systems. It is designed for **educational purposes**, helping users quickly access and learn the commands they need for daily tasks, certifications, or professional development.

---

## Table of Contents
- [scp Command Examples](#scp-command-examples)
- [curl Command Examples](#curl-command-examples)
- [rsync Command Examples](#rsync-command-examples)
- [wget Command Examples](#wget-command-examples)
- [Contributions](#contributions)

---

## scp Command Examples
- **Copy a file to a remote system**: `scp abc.txt xyz@<ip_address_of_xyz>:/home/xyz/Desktop`
- **Copy a file from a remote system**: `scp xyz@<ip_address_of_xyz>:/remote/user/home/abc.txt .`
- **Copy multiple files to a remote system**: `scp abc.txt def.txt xyz@<ip_address_of_xyz>:/home/xyz/Desktop`
- **Copy an entire directory to a remote system**: `scp -r ~/Desktop/test xyz@<ip_address_of_xyz>:/home/xyz/Desktop`
- **Enable verbose mode to see transfer details**: `scp -v abc.txt xyz@<ip_address_of_xyz>:/home/xyz/Desktop`
- **Copy files between two remote systems**: `scp abc@<ip_address_of_abc>:<path_of_file_or_folder> xyz@<ip_address_of_xyz>:<path_of_file_or_folder>`
- **Enable compression for faster transfer**: `scp -C abc.txt xyz@<ip_address_of_xyz>:/home/xyz/Desktop`
- **Limit bandwidth during file transfer**: `scp -l 800 abc.txt xyz@<ip_address_of_xyz>:/home/xyz/Desktop`
- **Preserve original file attributes**: `scp -p abc.txt xyz@<ip_address_of_xyz>:/home/xyz/Desktop`
- **Suppress output (quiet mode)**: `scp -q abc.txt xyz@<ip_address_of_xyz>:/home/xyz/Desktop`

---

## curl Command Examples
- **Get a response from a server**: `curl http://info.cern.ch/`
- **Save a file with the default name**: `curl -O http://www.google.com/robots.txt`
- **Save a file with a custom name**: `curl -o googleRobots.txt http://www.google.com/robots.txt`
- **Download multiple files**: `curl -O url1 -O url2 -O url3`
- **Download files only if they are newer**: `curl -z "DD MMM YY MM:HH:SS" url`
- **Resume an interrupted download**: `curl -C - url`
- **Upload a file**: `curl -T uploadFile.txt http://upload.server.com/files`
- **Delete a file from a server**: `curl -X DELETE http://upload.server.com/files/deleteFile.txt`
- **Avoid redirects**: `curl -L http://www.google.com`
- **Authenticate with a username and password**: `curl -u username:password http://server.com/files/tasks.txt`
- **Limit data transfer rate**: `curl --limit-rate 10K url`
- **Get header information only**: `curl -I http://www.google.com/robots.txt`
- **Change User-Agent**: `curl -A "Mozilla/5.0" http://server.com/file.png`
- **Send data to a server (POST request)**: `curl -d "token=xyz&name=test" http://api.server.com`
- **Write cookies to a file**: `curl -c cookies.txt http://www.google.com`
- **Read cookies from a file**: `curl -b cookies.txt http://www.google.com`

---

## rsync Command Examples
- **Sync local files (one-way sync)**: `rsync A/ Backup-A-dir/`
- **Sync files to a remote system**: `rsync A/ user@remote:/path/to/Backup`
- **Two-way sync with delete**: `rsync A/ Backup-A-dir/ --delete`
- **Delete source files after transfer**: `rsync A/ Backup-A-dir/ --remove-source-files`
- **Include and exclude files by pattern**: `rsync A/ Backup-A-dir/ --include=*.py --exclude=*.tmp`
- **Transfer over SSH**: `rsync -e ssh A/ user@remote:/Backup`
- **Enable verbose output**: `rsync -v A/ Backup-A-dir/`
- **Dry run (simulate transfer)**: `rsync -n A/ Backup-A-dir/`
- **Show progress of transfer**: `rsync --progress A/ Backup-A-dir/`
- **Compress data during transfer**: `rsync -z A/ Backup-A-dir/`
- **Recursive file copy**: `rsync -r A/ Backup-A-dir/`
- **Preserve metadata (archive mode)**: `rsync -a A/ Backup-A-dir/`
- **Set a file size limit**: `rsync --max-size='100K' A/ Backup-A-dir/`
- **Set bandwidth limit**: `rsync --bwlimit=100 A/ Backup-A-dir/`
- **Resume incomplete transfer**: `rsync --append A/ Backup-A-dir/`

---

## wget Command Examples
- **Download a file**: `wget <URL>`
- **Save with a custom name**: `wget -O customName.txt <URL>`
- **Download to a specific directory**: `wget -P /path/to/dir <URL>`
- **Download in the background**: `wget -b <URL>`
- **Download multiple files**: `wget -i urls.txt`
- **Resume interrupted download**: `wget -c <URL>`
- **Retry download multiple times**: `wget --tries=50 <URL>`
- **Limit download speed**: `wget --limit-rate=500k <URL>`

---

## Contributions
This cheat sheet is a work in progress. Contributions are welcome! Feel free to submit issues or pull requests to improve this resource.
