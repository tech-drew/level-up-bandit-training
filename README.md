# Level-Up Bandit Training

A hands-on Linux learning project designed to document my journey through the [OverTheWire Bandit](https://overthewire.org/wargames/bandit/) challenges. This repository serves as both a personal learning journal and a structured guide to mastering Linux fundamentals, including file permissions, shell scripting, networking, and system administration.

---

## Project Goals

- Strengthen Linux command-line and system administration skills.
- Build a documented, resume-ready portfolio of practical Linux experience.
- Serve as a foundation for advanced projects, including home labs, containerization, and CI/CD workflows.
- Create a structured, reusable learning resource for others exploring Linux fundamentals.

---

## Progress Tracker

| Level        | Status | Description |
|-------------|--------|-------------|
| 00 → 01     | [X]    | SSH login — connect to the Bandit server. :contentReference[oaicite:1]{index=1}  
| 01 → 02     | [ ]    | Read the file `readme` in the home directory to find the next password. :contentReference[oaicite:2]{index=2}  
| 02 → 03     | [ ]    | Handle a file with a special name (`-`). :contentReference[oaicite:3]{index=3}  
| 03 → 04     | [ ]    | Deal with spaces in filenames (quoting or escaping). :contentReference[oaicite:4]{index=4}  
| 04 → 05     | [ ]    | Identify hidden files (dotfiles) to find the password. :contentReference[oaicite:5]{index=5}  
| 05 → 06     | [ ]    | Use `file` to find a human-readable file among many. :contentReference[oaicite:6]{index=6}  
| 06 → 07     | [ ]    | Find a file of specific size and permissions. :contentReference[oaicite:7]{index=7}  
| 07 → 08     | [ ]    | Locate a file by user/group ownership. :contentReference[oaicite:8]{index=8}  
| 08 → 09     | [ ]    | Use `grep` to extract a line containing a keyword. :contentReference[oaicite:9]{index=9}  
| 09 → 10     | [ ]    | Use `sort` + `uniq -u` to find the unique line. :contentReference[oaicite:10]{index=10}  
| 10 → 11     | [ ]    | Extract strings from a binary using `strings`. :contentReference[oaicite:11]{index=11}  
| 11 → 12     | [ ]    | Decode a Base64-encoded file to get the password. :contentReference[oaicite:12]{index=12}  
| 12 → 13     | [ ]    | Decode ROT13‑encoded text using `tr`. :contentReference[oaicite:13]{index=13}  
| 13 → 14     | [ ]    | Reverse a hexdump and decompress data to reveal password. :contentReference[oaicite:14]{index=14}  
| 14 → 15     | [ ]    | Use an SSH key to log in and read a file. :contentReference[oaicite:15]{index=15}  
| 15 → 16     | [ ]    | Connect to a service using `nc` (netcat) to send/receive the password. :contentReference[oaicite:16]{index=16}  
| 16 → 17     | [ ]    | Use `openssl s_client` to talk over SSL/TLS. :contentReference[oaicite:17]{index=17}  
| 17 → 18     | [ ]    | Scan for open ports, identify and connect to a service. :contentReference[oaicite:18]{index=18}  
| 18 → 19     | [ ]    | Compare two files (`diff`-style) to find hidden data. :contentReference[oaicite:19]{index=19}  
| 19 → 20     | [ ]    | Run a command on the remote host via SSH to get the next password. :contentReference[oaicite:20]{index=20}  
| 20 → 21     | [ ]    | Explore SUID permissions and their implications. :contentReference[oaicite:21]{index=21}  
| 21 → 22     | [ ]    | Use a SUID‑set binary that triggers a background service. :contentReference[oaicite:22]{index=22}  
| 22 → 23     | [ ]    | Examine cron jobs to understand what is being executed. :contentReference[oaicite:23]{index=23}  
| 23 → 24     | [ ]    | Leverage a cron-script mechanism to retrieve the password. :contentReference[oaicite:24]{index=24}  
| 24 → 25     | [ ]    | Write a script that cron will execute to expose the password. :contentReference[oaicite:25]{index=25}  
| 25 → 26     | [ ]    | Brute-force a 4-digit PIN via a daemon listening on a port. :contentReference[oaicite:26]{index=26}  
| 26 → 27     | [ ]    | Escape a restricted shell environment using `more` or `vim`. :contentReference[oaicite:27]{index=27}  
| 27 → 28     | [ ]    | Use SUID binary + editor skills to further escape. :contentReference[oaicite:28]{index=28}  
| 28 → 29     | [ ]    | Clone and inspect a Git repository to find the secret. :contentReference[oaicite:29]{index=29}  
| 29 → 30     | [ ]    | Use Git commit history to locate removed or hidden data. :contentReference[oaicite:30]{index=30}  
| 30 → 31     | [ ]    | Explore Git tags or branches to find the required file. :contentReference[oaicite:31]{index=31}  
| 31 → 32     | [ ]    | Interact with the Git repo: make commits, push, or inspect `.git` directory. :contentReference[oaicite:32]{index=32}  
| 32 → 33     | [ ]    | Use Git environment variables or weird escapes to reveal information. :contentReference[oaicite:33]{index=33}  
| 33 → 34     | [ ]    | Endgame: run a special shell, read `README.txt`, and celebrate completion. :contentReference[oaicite:34]{index=34} |

