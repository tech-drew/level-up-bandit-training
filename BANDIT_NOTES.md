# Bandit Notes

# Level 0
- Goal: SSH login
- Commands used:
- ssh bandit01@bandit.labs.overthewire.org -p 2220
- Notes and learning points:
  - password = `bandit0`
  - p option lets you specify the ssh port.
  - List a name before an ip/hostname followed by @ to login to a specific user via ssh.

# Level 0 → 1
- Goal: Read the file `readme`
- username bandit0
- password bandit0
- Commands used:
- ls -la
- cat readme
- Notes and learning points:
-  password = `ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If`

# Level 1 → 2
- Goal: Handle a file with a special name (`-`)
- username ssh bandit1@bandit.labs.overthewire.org -p 2220
- password ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
- Commands used:
- ls -la
- vi -
- Notes and learning points:
- password = `263JGJPfgU6LtdEvgfWU1XP5yac29mFx`
- You should be able to view the file with `cat -- -`.
- cat did not work for me so I used vi as my fallback option.

# Level 2 → 3
- Goal: Deal with spaces in filenames (quoting or escaping)
- username ssh bandit2@bandit.labs.overthewire.org -p 2220
- password 263JGJPfgU6LtdEvgfWU1XP5yac29mFx
- Commands used:
- ls -la
- cat -- '--spaces in this filename'
- Notes and learning points:

# Level 3 → 4
- Goal: Identify hidden files (dotfiles) to find the password
- username ssh bandit3@bandit.labs.overthewire.org -p 2220
- password MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
- Commands used:
- ls -la
- cd inhere
- vi '...Hiding-From-You'
- Notes and learning points:

# Level 4 → 5
- Goal: Use `file` to find a human-readable file among many
- username ssh bandit4@bandit.labs.overthewire.org -p 2220
- password 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
- Commands used:
- cd inhere
- ls -la
- vi -- '-file01'
- vi -- '-file02'
- vi -- '-file03'
- vi -- '-file04'
- vi -- '-file05'
- vi -- '-file06'
- vi -- '-file07'
- vi -- '-file08'
- vi -- '-file09'
- Notes and learning points:
- I used vi to scan each file individually to solve the problem.
- The method I used to solve the problem works but is inefficent.
- The intended solution is to use 'file'
- 'file ./*' will show you the formatting of each file. Look for the ASCII text file. 


# Level 5 → 6 
- Goal: Find a file of specific size and permissions
- username ssh bandit5@bandit.labs.overthewire.org -p 2220
- password 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
- Commands used:
- ls -la
- cd inhere
- find . -type f -size 1033c ! -executable
- cd ./maybehere07/
- cat .file2
- Notes and learning points:
- Add in notes for this level later.
  
# Level 6 → 7 **Current Level**
- Goal: Locate a file by user/group ownership
- ssh bandit5@bandit.labs.overthewire.org -p 2220
- password HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
- Commands used:
- Notes and learning points:

# Level 7 → 8
- Goal: Use `grep` to extract a line containing a keyword
- Commands used:
- Notes and learning points:

# Level 8 → 9
- Goal: Use `sort` + `uniq -u` to find the unique line
- Commands used:
- Notes and learning points:

# Level 9 → 10
- Goal: Extract strings from a binary using `strings`
- Commands used:
- Notes and learning points:

# Level 10 → 11
- Goal: Decode a Base64-encoded file
- Commands used:
- Notes and learning points:

# Level 11 → 12
- Goal: Decode ROT13‑encoded text using `tr`
- Commands used:
- Notes and learning points:

# Level 12 → 13
- Goal: Reverse a hexdump and decompress data to reveal password
- Commands used:
- Notes and learning points:

# Level 13 → 14 
- Goal: Use an SSH key to log in and read a file
- Commands used:
- Notes and learning points:

# Level 14 → 15
- Goal: Connect to a service using `nc` (netcat)
- Commands used:
- Notes and learning points:

# Level 15 → 16
- Goal: Use `openssl s_client` to talk over SSL/TLS
- Commands used:
- Notes and learning points:

# Level 16 → 17
- Goal: Scan for open ports, identify and connect to a service
- Commands used:
- Notes and learning points:

# Level 17 → 18
- Goal: Compare two files (`diff`) to find hidden data
- Commands used:
- Notes and learning points:

# Level 18 → 19
- Goal: Run a command on the remote host via SSH
- Commands used:
- Notes and learning points:

# Level 19 → 20
- Goal: Explore SUID permissions and their implications
- Commands used:
- Notes and learning points:

# Level 20 → 21
- Goal: Use a SUID-set binary that triggers a background service
- Commands used:
- Notes and learning points:

# Level 21 → 22
- Goal: Examine cron jobs to understand what is being executed
- Commands used:
- Notes and learning points:

# Level 22 → 23
- Goal: Leverage a cron-script mechanism to retrieve the password
- Commands used:
- Notes and learning points:

# Level 23 → 24
- Goal: Write a script that cron will execute to expose the password
- Commands used:
- Notes and learning points:

# Level 24 → 25
- Goal: Brute-force a 4-digit PIN via a daemon listening on a port
- Commands used:
- Notes and learning points:

# Level 25 → 26
- Goal: Escape a restricted shell environment using `more` or `vim`
- Commands used:
- Notes and learning points:

# Level 26 → 27
- Goal: Use SUID binary + editor skills to further escape
- Commands used:
- Notes and learning points:

# Level 27 → 28
- Goal: Clone and inspect a Git repository to find the secret
- Commands used:
- Notes and learning points:

# Level 28 → 29
- Goal: Use Git commit history to locate removed or hidden data
- Commands used:
- Notes and learning points:

# Level 29 → 30
- Goal: Explore Git tags or branches to find the required file
- Commands used:
- Notes and learning points:

# Level 30 → 31
- Goal: Interact with the Git repo: make commits, push, or inspect `.git` directory
- Commands used:
- Notes and learning points:

# Level 31 → 32
- Goal: Use Git environment variables or weird escapes to reveal information
- Commands used:
- Notes and learning points:

# Level 32 → 33
- Goal: Endgame — run a special shell, read `README.txt`, and finish the challenge
- Commands used:
- Notes and learning points:
