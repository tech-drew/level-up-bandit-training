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
- type has some common options:f (file), d (directory), l (symbolic link)
- size has some common options:c (bytes), k (kilobytes), M (megabytes), G (gigabytes), T (terabytes)
- ! not besides -execure you could use -user for something not created by a user
- find . -type f -size 1033c ! -user -bob   This command looks for file this size not owned by bob
  
# Level 6 → 7 
- Goal: Locate a file by user/group ownership
- username ssh bandit6@bandit.labs.overthewire.org -p 2220
- password HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
- Commands used:
- find / -type f -size 33c -user bandit7 2>/dev/null
- Notes and learning points:
- Use the same find command but searching for a user
- Use pipe redirection to eliminate errors

# Level 7 → 8 
- Goal: Use `grep` to extract a line containing a keyword
- username ssh bandit7@bandit.labs.overthewire.org -p 2220
- password morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
- Commands used:
- grep millionth data.txt
- Notes and learning points:


# Level 8 → 9 
- username ssh bandit8@bandit.labs.overthewire.org -p 2220
- password dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc 
- Goal: Use `sort` + `uniq -u` to find the unique line
- Commands used:
- cat data.txt
- sort data.txt | uniq -u
- Notes and learning points:
- I used the uniq command for the first time. I was unaware of this command.
- uniq looks like it is a really useful linux command

# Level 9 → 10 
- username ssh bandit9@bandit.labs.overthewire.org -p 2220
- password 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
- Goal: Extract strings from a binary using `strings`
- Commands used:g
- grep -o '=.*' data.txt Searches for strings
- strings data.txt | grep -o '=.*' Searches binary formating for the grep pattern
- Notes and learning points:
- strings prints human readible content from a file

# Level 10 → 11 
- username ssh bandit10@bandit.labs.overthewire.org -p 2220
- password FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
- Goal: Decode a Base64-encoded file
- Commands used:
- cat data.txt
- base64 -d -data.txt | strings
- Notes and learning points:
- The -d decodeds the base64 file. Without the -d flag the base64 command encodes the information.
- If a file mainly contains letters and numbers like the below it is possible to have base64 encoding
- `U29tZSBleGFtcGxlIHRleHQgdGhhdCBpcyBjb250YWluZWQgd2l0aCBhbiBpbWFnZQ==`

# Level 11 → 12 
- username ssh bandit11@bandit.labs.overthewire.org -p 2220
- password dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
- Goal: Decode ROT13‑encoded text using `tr`
- Commands used:
- cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
- Notes and learning points:
- `tr` command replaces one set of characters with another set of characters
- syntax for `tr` is `tr 'from' to'`
- So `A-Za-z` is replacing all uppecase and lowercase letters.
- For Rot13 A should be N and Z should be M so using `N-ZA-Mn-za-M` shifts everything to the correct Rot13 character
- After you shift a character to Rot13, you can apply it again to get the original characters. So Rot13 is reversible.
- Rot13 was commonly used in the 1980s/1990s in forums to talk about spoilers.
- People could decode the Rot13 message if they wanted to read it.
- Not encrpytion, simply obfuscation.

# Level 12 → 13 
- username ssh bandit12@bandit.labs.overthewire.org -p 2220
- password 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
- Goal: Reverse a hexdump and decompress data to reveal password
- Commands used:
- cd tmp
- mktemp -d
- cd /tmp/tmp.1jIVCI0kE
- xxd -r data.hex data
- file data
- mv data data.gz
- gunzip data.gz
   22  file data
   23  mv data data.bz2
   24  bunzip2 data.bz2
   25  file data
   26  mv data data.gz
   27  gunzip data.gz
   28  file data
   29  tar xf data
   30  file data
   31  tar xf data
   32  file data
   33  ls -l
   34  mv data5.bin data
   35  file data
   36  tar xf data
   37  ls -l
   38  mv data6.bin data
   39  file data
   40* mv data8 data.bz2
   41  bunzip2 data.bz2
   42  file data
   43  tar xf data
   44  ls -l
   45  mv data8.bin data
   46  file data
   47  mv data data.gz
   48  gunzip data.gz
   49  file data
   50  cat data
- Notes and learning points:

# Level 13 → 14 **Current Level**
- username ssh bandit13@bandit.labs.overthewire.org -p 2220
- password FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
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
