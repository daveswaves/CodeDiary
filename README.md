# Code Diary

### @@@ Collection of advanced CLI list operations  
(eg. display files only, hidden files only, sort by modification time etc). [2025-01-29]  
*Documented in email*: `List files / folders advanced`

---

### @@@ Extensive examples of using GPG for public/private key encryption and digital signature. [2025-01-29]  
*Documented in email*: `Using GnuPG (GPG)`

---

### @@@ Working with IMDbDataFiles to list all films by a given actor or list films rated 7 or more etc. [2025-01-27]  
`/var/www/html/IMDbDataFiles/getActorFilms.sql`

---

### @@@ Harvard / MIT Courses [2025-01-27]  
*Links in email*: `CS50 SQL and other courses Harvard / MIT`

---

### @@@ Harvard CS50 Cybersecurity 6 part YouTube course. [2025-01-26]  
[CS50 Cybersecurity](https://youtu.be/watch?v=kmJlnUfMd7I&list=PLhQjrBD2T383Cqo5I1oRrbC1EKRAKGKUE)

---

### @@@ Running SQLite on the command line [2025-01-23]  
*Documented in email*: `Running SQLite on the command line`

### Import a TSV file:
```sh
sqlite3 db_name.db3 ".mode tabs" ".import tsv_name.tsv tbl_name"
```
### Importing compressed files.
'tsv.gz' files cannot be ipmorted directly, but the following is possible:
```sh
gunzip -c tsv_name.tsv.gz | sqlite3 db_name.db3 ".mode tabs" ".import /dev/stdin tbl_name"
# Explainer:
# Decompresses file content to stdout (avoid manually decompressing the file),
# which then gets piped to stdin and imported into database.
```
### View compressed file directly.
```sh
zless file_name.tsv.gz
# Explainer:
# File can be viewed a page at a time. Search file using '/search_term'
# 'n' jumps to next occurrence of the search term.
# 'space' moves forward one screen.
# 'q' to quit.

# Use the following for case-insensitive search:
LESS=-i zless data.tsv.gz
```
---

### @@@ Updating VS Code [2025-01-20]
```sh
$ sudo apt update
$ sudo apt install code
```

---

### @@@ Harvard CS50’s Introduction to Programming with Python [2025-01-14]  
[CS50 Python](https://youtu.be/nLRL_NcnK-4)

---

### @@@ Harvard CS50x 2024 Lecture [2025-01-14]  
[CS50x 2024](https://youtu.be/watch?v=3LPJfIKxwWc&list=PLhQjrBD2T381WAHyx1pq-sBfykqMBI7V4)

---

### @@@ A collection of python scripts exploring seedSigner functionality (eg. animated QR codes) [2025 early Jan]
```
~/pypo/src/decode_temporal_qr_imgs.py
~/pypo/src/embit_generates_bip39_recovery_phrase.py
etc.
```

---

### @@@ Updating Sublime Text [2024-12-21]  
```js
$ wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/sublimehq-archive.gpg > /dev/null
$ echo "deb https://download.sublimetext.com/ apt/stable/" | sudo tee /etc/apt/sources.list.d/sublime-text.list
$ sudo apt update
$ sudo apt upgrade sublime-text
$ subl --version
//-> Sublime Text Build 4180

// Note: Opening from Dock bar may still launch old version.
// I found that running subl command in terminal opened the latest version.
// Remove from Dock then select 'Add to Favorites' on Sublime icon opened on command line.
```

---

### @@@ Bash script to install required version of Node JS. [2024-11-27]  
Attached to email: `Install Node JS Bash Script`

---

### @@@ Bash scripts. [2024-11-28 & 29]
```js
~/bash_scripts/
/*
Note: Assortment of bash tasks:
     copy_files.sh
     dir_tree_report.sh
     rename_files.sh
     install_node.sh
     permissions_and_exec_set.sh
     etc.
*/
```
