# Code Diary

### ➤ Vue JS Let's Build an Offline-First Vue App. [2025-02 / early Feb]
A Laracasts project that codes a PWA notes app, using IndexedDB to store data offline,  
and Tiptap - the open-source headless WYSIWG editor.  
[https://laracasts.com/series/lets-build-an-offline-first-vue-app](https://laracasts.com/series/lets-build-an-offline-first-vue-app)

---

### ➤ Vue JS Filter Table. [2025-02-07]
This project uses multiple components to create a filterable and searchable table that connects to a backend JSON table.  
It utilises `Express.js`, a lightweight web server, and `CORS` middleware to enable cross-domain requests.

Records can be searched by name, title, or status. Radio buttons allow filtering between past records or today's records,  
while checkboxes enable filtering by status: In Progress, Completed and Not Started.  
All filters and search operations can be combined for more refined results.
[GitHub](https://github.com/daveswaves/vuejs_filter_table)

---

### ➤ Collection of advanced CLI list operations  
(eg. display files only, hidden files only, sort by modification time etc). [2025-01-29]  
*Documented in email*: `List files / folders advanced`

---

### ➤ Extensive examples of using GPG for public/private key encryption and digital signature. [2025-01-29]  
*Documented in email*: `Using GnuPG (GPG)`

---

### ➤ Using bash to list most recently updated files [2025 Jan]
```sh
# Lists all files (including sub dir files) and displays their modified dates (newest first).
# This is saved as an alias: 'mod_files'
find . -type f ! -path "*/node_modules/*" ! -path "*/.git/*" -printf "%TY-%Tm-%Td %TH:%TM %p\n" | sort -r

# Only lists files updated today (saved as 'mods_today' alias). Both ignore the node_modules/  and .git/ directories.
find . -type f ! -path "*/node_modules/*" ! -path "*/.git/*" -newermt "$(date +%Y-%m-%d)" -printf "%TY-%Tm-%Td %TH:%TM %p\n" | sort -r
```
---

### ➤ Working with IMDbDataFiles to list all films by a given actor or list films rated 7 or more etc. [2025-01-27]  
`/var/www/html/IMDbDataFiles/getActorFilms.sql`

---

### ➤ Harvard / MIT Courses [2025-01-27]  
*Links in email*: `CS50 SQL and other courses Harvard / MIT`

---

### ➤ Harvard CS50 Cybersecurity 6 part YouTube course. [2025-01-26]  
[CS50 Cybersecurity](https://youtu.be/watch?v=kmJlnUfMd7I&list=PLhQjrBD2T383Cqo5I1oRrbC1EKRAKGKUE)

---

### ➤ Running SQLite on the command line [2025-01-23]  
*Documented in email*: `Running SQLite on the command line`

### Import a TSV file:
```sh
sqlite3 db_name.db3 ".mode tabs" ".import tsv_name.tsv tbl_name"
```
### Importing compressed files.
'tsv.gz' files cannot be imported directly, but the following is possible:
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

### ➤ Updating VS Code [2025-01-20]
```sh
$ sudo apt update
$ sudo apt install code
```

---

### ➤ Harvard CS50’s Introduction to Programming with Python [2025-01-14]  
[CS50 Python](https://youtu.be/nLRL_NcnK-4)

---

### ➤ Harvard CS50x 2024 Lecture [2025-01-14]  
[CS50x 2024](https://youtu.be/watch?v=3LPJfIKxwWc&list=PLhQjrBD2T381WAHyx1pq-sBfykqMBI7V4)

---

### ➤ Proof-of-Work Python script [2025-01-13] 
```
~/pypo/src/animated_pow.py
```
This is still under development. The objective is to emulate the difficulty adjustment algorithm  
which adjusts automatically to make the PoW process run for a fixed amount of time (eg. 1 minute).  
The target threshold gets stored in the header in nBits format.

---

### ➤ A collection of python scripts exploring seedSigner functionality (eg. animated QR codes) [2025 early Jan]
```
~/pypo/src/decode_temporal_qr_imgs.py
~/pypo/src/embit_generates_bip39_recovery_phrase.py
etc.
```

---

### ➤ Updating Sublime Text [2024-12-21]  
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

### ➤ Bash script to install required version of Node JS. [2024-11-27]  
Attached to email: `Install Node JS Bash Script`

---

### ➤ Bash scripts. [2024-11-28 & 29]
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
