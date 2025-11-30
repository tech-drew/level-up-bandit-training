# Level-Up Bandit Training

A hands-on Linux learning project documenting my journey through the [OverTheWire Bandit](https://overthewire.org/wargames/bandit/) challenges. This repository serves as both a personal learning journal and a structured guide to mastering Linux fundamentals, including file permissions, shell scripting, networking, and system administration.

---

## Project Status: Work in Progress
This repo is actively being updated with level outlines, notes, and commands as I progress. The goal is to maintain a complete, organized journal of Linux command-line skills and problem-solving experience.

---

## Project Goals

- Strengthen Linux command-line and system administration skills.
- Build a documented, resume-ready portfolio of practical Linux experience.
- Serve as a foundation for advanced projects, including home labs, containerization, and CI/CD workflows.
- Provide a structured, reusable learning resource for others exploring Linux fundamentals.

---

## Progress Tracker

| Level        | Status | Description |
|-------------|--------|-------------|
| 00 → 01     | ✅    | SSH login — connect to the Bandit server. |
| 01 → 02     | ✅    | Read the file `readme` in the home directory to find the next password. |
| 02 → 03     | ✅    | Handle a file with a special name (`-`). |
| 03 → 04     | ⬜    | Deal with spaces in filenames (quoting or escaping). |
| 04 → 05     | ⬜    | Identify hidden files (dotfiles) to find the password. |
| 05 → 06     | ⬜    | Use `file` to find a human-readable file among many. |
| 06 → 07     | ⬜    | Find a file of specific size and permissions. |
| 07 → 08     | ⬜    | Locate a file by user/group ownership. |
| 08 → 09     | ⬜    | Use `grep` to extract a line containing a keyword. |
| 09 → 10     | ⬜    | Use `sort` + `uniq -u` to find the unique line. |
| 10 → 11     | ⬜    | Extract strings from a binary using `strings`. |
| 11 → 12     | ⬜    | Decode a Base64-encoded file to get the password. |
| 12 → 13     | ⬜    | Decode ROT13‑encoded text using `tr`. |
| 13 → 14     | ⬜    | Reverse a hexdump and decompress data to reveal password. |
| 14 → 15     | ⬜    | Use an SSH key to log in and read a file. |
| 15 → 16     | ⬜    | Connect to a service using `nc` (netcat) to send/receive the password. |
| 16 → 17     | ⬜    | Use `openssl s_client` to talk over SSL/TLS. |
| 17 → 18     | ⬜    | Scan for open ports, identify and connect to a service. |
| 18 → 19     | ⬜    | Compare two files (`diff`-style) to find hidden data. |
| 19 → 20     | ⬜    | Run a command on the remote host via SSH to get the next password. |
| 20 → 21     | ⬜    | Explore SUID permissions and their implications. |
| 21 → 22     | ⬜    | Use a SUID‑set binary that triggers a background service. |
| 22 → 23     | ⬜    | Examine cron jobs to understand what is being executed. |
| 23 → 24     | ⬜    | Leverage a cron-script mechanism to retrieve the password. |
| 24 → 25     | ⬜    | Write a script that cron will execute to expose the password. |
| 25 → 26     | ⬜    | Brute-force a 4-digit PIN via a daemon listening on a port. |
| 26 → 27     | ⬜    | Escape a restricted shell environment using `more` or `vim`. |
| 27 → 28     | ⬜    | Use SUID binary + editor skills to further escape. |
| 28 → 29     | ⬜    | Clone and inspect a Git repository to find the secret. |
| 29 → 30     | ⬜    | Use Git commit history to locate removed or hidden data. |
| 30 → 31     | ⬜    | Explore Git tags or branches to find the required file. |
| 31 → 32     | ⬜    | Interact with the Git repo: make commits, push, or inspect `.git` directory. |
| 32 → 33     | ⬜    | Use Git environment variables or weird escapes to reveal information. |
| 33 → 34     | ⬜    | Endgame: run a special shell, read `README.txt`, and celebrate completion. |


