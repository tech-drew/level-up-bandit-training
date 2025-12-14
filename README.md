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

| Level        | Status | Description                                                            |
|--------------|--------|------------------------------------------------------------------------|
| 00 → 01      | ✅     | SSH login — connect to the Bandit server.                              |
| 01 → 02      | ✅     | Read the file `readme` in the home directory to find the next password. |
| 02 → 03      | ✅     | Handle a file with a special name (`-`).                               |
| 03 → 04      | ✅     | Deal with spaces in filenames (quoting or escaping).                   |
| 04 → 05      | ✅     | Use `file` to find a human-readable file among many.                   |
| 05 → 06      | ✅     | Find a file of specific size and permissions.                          |
| 06 → 07      | ✅     | Locate a file by user/group ownership.                                 |
| 07 → 08      | ✅     | Use `grep` to extract a line containing a keyword.                      |
| 08 → 09      | ✅     | Use `sort` + `uniq -u` to find the unique line.                         |
| 09 → 10      | ✅     | Extract strings from a binary using `strings`.                          |
| 10 → 11      | ✅     | Decode a Base64‑encoded file to get the password.                      |
| 11 → 12      | ⬜     | Decode ROT13‑encoded text using `tr`.                                  |
| 12 → 13      | ⬜     | Reverse a hexdump and decompress data to reveal password.              |
| 13 → 14      | ⬜     | Use an SSH key to log in and read a file.                              |
| 14 → 15      | ⬜     | Connect to a service using `nc` (netcat) to send/receive the password. |
| 15 → 16      | ⬜     | Use `openssl s_client` to communicate over SSL/TLS.                    |
| 16 → 17      | ⬜     | Scan for open ports, identify and connect to a service.                |
| 17 → 18      | ⬜     | Compare two files to find hidden differences.                          |
| 18 → 19      | ⬜     | Run a command remotely via SSH to retrieve the password.               |
| 19 → 20      | ⬜     | Explore SUID permissions and use them to your advantage.               |
| 20 → 21      | ⬜     | Use a SUID‑set binary that triggers a system action.                   |
| 21 → 22      | ⬜     | Inspect cron jobs to understand scheduled actions.                     |
| 22 → 23      | ⬜     | Exploit a cron‑based mechanism to obtain the password.                 |
| 23 → 24      | ⬜     | Write a script executed by cron to reveal the password.                |
| 24 → 25      | ⬜     | Brute‑force a 4‑digit PIN via a service on a port.                     |
| 25 → 26      | ⬜     | Escape a restricted shell (e.g., via `more` or `vim`).                 |
| 26 → 27      | ⬜     | Use a SUID binary + editor trick to escalate further.                  |
| 27 → 28      | ⬜     | Clone and inspect a Git repository to find secrets.                    |
| 28 → 29      | ⬜     | Examine Git commit history for removed or hidden data.                 |
| 29 → 30      | ⬜     | Explore Git tags/branches to locate the needed info.                   |
| 30 → 31      | ⬜     | Use Git operations or `.git` internals to uncover data.                |
| 31 → 32      | ⬜     | Use environment variables or odd Git behaviors to reveal info.         |
| 32 → 33      | ⬜     | Complete the challenge: run the special shell and finish Bandit.       |

