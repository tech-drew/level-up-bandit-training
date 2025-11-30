# Bandit Notes

# Level 0
- Goal: SSH login
- Commands used:
- ssh bandit01@bandit.labs.overthewire.org -p 2220
- Notes and learning points:
  - password = `bandit0`
  - p option lets you specify the ssh port.
  - List a name before an ip/hostname followed by @ to login to a specific user via ssh.

# Level 0 -> 1
- Goal: Read the file `readme`
- username bandit0
- password bandit0
- Commands used:
- ls -la
- cat readme
- Notes and learning points:
-  password = `ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If`

# Level 1 -> 2
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

# Level 2 -> 3
- Goal: Deal with spaces in filenames (quoting or escaping)
- username ssh bandit2@bandit.labs.overthewire.org -p 2220
- password 263JGJPfgU6LtdEvgfWU1XP5yac29mFx
- Commands used:
- ls -la
- cat -- '--spaces in this filename'
- Notes and learning points:

# Level 3 -> 4
- Goal: Identify hidden files (dotfiles) to find the password
- username ssh bandit3@bandit.labs.overthewire.org -p 2220
- password MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
- Commands used:
- ls -la
- cd inhere
- vi '...Hiding-From-You'
- Notes and learning points:

**Current Level**
# Level 4 -> 5
- Goal: Use `file` to find a human-readable file among many
- username ssh bandit4@bandit.labs.overthewire.org -p 2220
- password 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
- Commands used:
- Notes and learning points:

# Level 07
- Goal: Find a file of specific size and permissions
- Commands used:
- Notes and learning points:

# Level 08
- Goal: Locate a file by user/group ownership
- Commands used:
- Notes and learning points:

# Level 09
- Goal: Use `grep` to extract a line containing a keyword
- Commands used:
- Notes and learning points:

# Level 10
- Goal: Use `sort` + `uniq -u` to find the unique line
- Commands used:
- Notes and learning points:

# Level 11
- Goal: Extract strings from a binary using `strings`
- Commands used:
- Notes and learning points:

# Level 12
- Goal: Decode a Base64-encoded file
- Commands used:
- Notes and learning points:

# Level 13
- Goal: Decode ROT13‑encoded text using `tr`
- Commands used:
- Notes and learning points:

# Level 14
- Goal: Reverse a hexdump and decompress data to reveal password
- Commands used:
- Notes and learning points:

# Level 15
- Goal: Use an SSH key to log in and read a file
- Commands used:
- Notes and learning points:

# Level 16
- Goal: Connect to a service using `nc` (netcat)
- Commands used:
- Notes and learning points:

# Level 17
- Goal: Use `openssl s_client` to talk over SSL/TLS
- Commands used:
- Notes and learning points:

# Level 18
- Goal: Scan for open ports, identify and connect to a service
- Commands used:
- Notes and learning points:

# Level 19
- Goal: Compare two files (`diff`) to find hidden data
- Commands used:
- Notes and learning points:

# Level 20
- Goal: Run a command on the remote host via SSH
- Commands used:
- Notes and learning points:

# Level 21
- Goal: Explore SUID permissions and their implications
- Commands used:
- Notes and learning points:

# Level 22
- Goal: Use a SUID-set binary that triggers a background service
- Commands used:
- Notes and learning points:

# Level 23
- Goal: Examine cron jobs to understand what is being executed
- Commands used:
- Notes and learning points:

# Level 24
- Goal: Leverage a cron-script mechanism to retrieve the password
- Commands used:
- Notes and learning points:

# Level 25
- Goal: Write a script that cron will execute to expose the password
- Commands used:
- Notes and learning points:

# Level 26
- Goal: Brute-force a 4-digit PIN via a daemon listening on a port
- Commands used:
- Notes and learning points:

# Level 27
- Goal: Escape a restricted shell environment using `more` or `vim`
- Commands used:
- Notes and learning points:

# Level 28
- Goal: Use SUID binary + editor skills to further escape
- Commands used:
- Notes and learning points:

# Level 29
- Goal: Clone and inspect a Git repository to find the secret
- Commands used:
- Notes and learning points:

# Level 30
- Goal: Use Git commit history to locate removed or hidden data
- Commands used:
- Notes and learning points:

# Level 31
- Goal: Explore Git tags or branches to find the required file
- Commands used:
- Notes and learning points:

# Level 32
- Goal: Interact with the Git repo: make commits, push, or inspect `.git` directory
- Commands used:
- Notes and learning points:

# Level 33
- Goal: Use Git environment variables or weird escapes to reveal information
- Commands used:
- Notes and learning points:

# Level 34
- Goal: Endgame — run a special shell, read `README.txt`, and finish the challenge
- Commands used:
- Notes and learning points:

ssh bandit0@bandit.labs.overthewire.org -p 2220
cat readme
