The Low-to-No-Cost OSCP Study Guide
A methodical, phase-by-phase path to OSCP readiness. Almost everything here is free. The only unavoidable paid item is the OSCP exam + PEN-200 course itself (buy that last, once you're consistently solving boxes solo). A few optional paid resources are flagged clearly and kept cheap.
How to use this guide: Work the phases in order. Don't skip ahead to box-grinding before you have the fundamentals — you'll just get frustrated. Take notes constantly (see the Notes & Reporting section — this is not optional, it's the actual skill). When you can solve TJ Null's list boxes without walkthroughs, you're ready to buy the exam.
---
Mindset & Ground Rules
"Try Harder" is real, but so is knowing when to look. Give every problem an honest attempt before reaching for a walkthrough. When you do use one, understand why, then redo the box from scratch later.
Enumerate more than you think you need to. Most stuck moments are missed enumeration, not missing skills.
Take notes from day one. Your personal methodology notes are what you'll rely on in the exam.
Practice report writing early. People fail OSCP on the report, not just the hacking.
Only practice on systems you own or are explicitly authorized to attack (the labs and platforms below). Never point tools at anything else.
---
Phase 1 — Foundations (Weeks 1–4)
Goal: Linux comfort, networking basics, light scripting.
You can't exploit what you can't navigate. Build fluency first.
OverTheWire: Bandit — the single best free intro to the Linux shell. Do all levels.
https://overthewire.org/wargames/bandit/
TryHackMe: Pre Security path (free rooms) — networking, Linux, web basics.
https://tryhackme.com/path/outline/presecurity
TryHackMe: Complete Beginner path (mostly free) — start it after Pre Security.
https://tryhackme.com/path/outline/beginner
Linux Journey — clean, free Linux fundamentals reference.
https://linuxjourney.com/
Networking basics — Professor Messer's free Network+ videos are excellent for TCP/IP, ports, protocols.
https://www.professormesser.com/network-plus/n10-009/n10-009-video/n10-009-training-course/
Bash + Python basics — just enough to read and modify scripts:
Bash: https://linuxconfig.org/bash-scripting-tutorial
Python: https://www.learnpython.org/
Checkpoint: You can move around a Linux filesystem, use pipes/grep/find, explain what a port and a service are, and read a simple Bash/Python script without panic.
---
Phase 2 — Core Pentesting Methodology (Weeks 5–10)
Goal: the enumeration → exploitation → foothold loop, plus web fundamentals.
TryHackMe: Jr Penetration Tester path — the backbone of this phase.
https://tryhackme.com/path/outline/jrpenetrationtester
Nmap, deeply — learn service/version detection and NSE scripts, not just `-sV`.
Official reference: https://nmap.org/book/man.html
THM Nmap rooms are in the Jr Pentester path.
PortSwigger Web Security Academy — free, world-class web exploitation labs. Start the Apprentice labs: SQL injection, XSS, authentication, file upload, directory traversal.
https://portswigger.net/web-security/all-labs
Enumeration habit-building — internalize this reference:
https://book.hacktricks.xyz/ (HackTricks — your single most-used reference for the rest of this journey)
Checkpoint: Given an IP, you instinctively enumerate all services, identify versions, find web content, and know how to research a service for known vulnerabilities.
---
Phase 3 — Privilege Escalation (Weeks 11–14)
Goal: turn a foothold into full control of a box (Linux + Windows).
TryHackMe rooms:
Linux PrivEsc: https://tryhackme.com/room/linuxprivesc
Windows PrivEsc: https://tryhackme.com/room/windowsprivesc20
Common Linux Privesc: https://tryhackme.com/room/commonlinuxprivesc
The classic Linux privesc reference (g0tmi1k):
https://blog.g0tmi1k.com/2011/08/basic-linux-privilege-escalation/
PEASS-ng (LinPEAS / WinPEAS) — the enumeration scripts everyone uses. Learn to read their output, not just run them.
https://github.com/peass-ng/PEASS-ng
PayloadsAllTheThings — payloads and privesc techniques reference.
https://github.com/swisskyrepo/PayloadsAllTheThings
GTFOBins (Linux) and LOLBAS (Windows) — abusing legit binaries:
https://gtfobins.github.io/
https://lolbas-project.github.io/
Checkpoint: After getting a low-priv shell, you can enumerate the box, spot a privesc vector, and get root/SYSTEM without a walkthrough on easy targets.
---
Phase 4 — Box Grinding (Weeks 15–22) — the most important phase
Goal: independently solve OSCP-like machines, building a repeatable methodology.
This is where readiness is actually built. Aim for 2–3 boxes per week. Try each box yourself first; only watch a walkthrough after a genuine attempt, and always re-document the path in your own words.
TJ Null's OSCP-like list — the community-standard list of HTB + PG + VulnHub boxes that mirror OSCP difficulty. This is your primary curriculum for this phase.
https://docs.google.com/spreadsheets/d/1dwSMIAPIam0PuRBkCiDI88pU3yzrqqHkDtBngUHNCw8/
Practice targets (free / cheap):
VulnHub — completely free downloadable vulnerable VMs (run locally in VirtualBox/VMware).
https://www.vulnhub.com/
HackTheBox — free active machines rotate; retired machines need VIP (~$14–20/mo) and are most of TJ Null's list. Worth the subscription during this phase.
https://www.hackthebox.com/
Proving Grounds Play (free tier) and Practice (~$19/mo, most exam-representative) — from OffSec themselves.
https://www.offsec.com/labs/
Walkthrough resources (use after trying):
IppSec — free video walkthroughs that teach methodology. Search by box at https://ippsec.rocks/
0xdf write-ups: https://0xdf.gitlab.io/
Build your own methodology cheat sheet as you go (enumeration commands, common privesc checks, pivots). This becomes your exam playbook.
Checkpoint: You can take an unseen "easy" or "medium" box and own it end-to-end without help, and you have a written methodology you trust.
---
Phase 5 — Buffer Overflow & Exam Simulation (Weeks 23–24)
Goal: cover the classic stack BOF fundamentals and rehearse exam conditions.
Note: classic stack buffer overflow is a smaller part of the current exam than it used to be, but the fundamentals are still worth knowing and are very learnable.
TryHackMe: Buffer Overflow Prep (free room — the standard practice ground):
https://tryhackme.com/room/bufferoverflowprep
dostackbufferoverflowgood — clear, classic walkthrough of the technique:
https://github.com/justinsteven/dostackbufferoverflowgood
TCM Security's free BOF walkthrough (part of his free content): search "The Cyber Mentor buffer overflow" on YouTube.
Exam simulation: Pick 3–4 unseen boxes, give yourself a strict time limit, and write a practice report for each as if grading. Time pressure + reporting is the real exam skill.
Checkpoint: You can walk through a basic stack BOF from fuzzing to shell, and you can produce a clean, reproducible report under time pressure.
---
Notes & Reporting (Do This The Whole Way Through)
This is the part most people underinvest in and then regret.
Note-taking tools (free):
Obsidian — https://obsidian.md/
CherryTree — https://www.giuspen.com/cherrytree/
Notion (free tier) — https://www.notion.so/
What to capture for every box: target IP, full enumeration output, every command that worked (and key ones that didn't), screenshots, the foothold path, the privesc path, and the flags/proof.
Report writing:
Official OffSec report template & guidance: https://help.offsec.com/hc/en-us/articles/360046787731-PEN-200-Reporting-Requirements
TJ Null / community sample reports: search "OSCP exam report template noraj" — https://github.com/noraj/OSCP-Exam-Report-Template-Markdown
Practice writing a report for at least 10 of your Phase 4 boxes, not just the exam sim ones.
---
Free / Cheap Learning Channels & References (Use Throughout)
IppSec (YouTube) — methodology via box walkthroughs. https://www.youtube.com/@ippsec
The Cyber Mentor / Heath Adams (YouTube) — free Practical Ethical Hacking content. https://www.youtube.com/@TCMSecurityAcademy
HackTricks — the reference you'll open most. https://book.hacktricks.xyz/
PayloadsAllTheThings — https://github.com/swisskyrepo/PayloadsAllTheThings
OSCP-specific community notes: https://github.com/0xsyr0/OSCP (curated cheat-sheet collection)
---
Optional Paid Resources (Only If You Want Them)
Kept cheap and ordered by value. None are required except the exam.
HackTheBox VIP/VIP+ (~$14–20/mo) — unlocks retired machines (most of TJ Null's list). Best paid upgrade for Phase 4.
Proving Grounds Practice (~$19/mo) — closest feel to the actual exam machines.
TryHackMe Premium (~$10–14/mo) — worth it during Phases 1–3 for the structured paths; can cancel once you hit box-grinding.
TCM Security – Practical Ethical Hacking (~$30, frequent sales) — excellent cheap beginner-to-intermediate course. https://academy.tcm-sec.com/
PEN-200 + OSCP exam — the real thing. ~$1,649 for the 90-day course bundle, or a higher "Learn One" annual tier with a year of lab access + two exam attempts. Buy this last. Confirm current pricing/bundles at https://www.offsec.com/courses/pen-200/ (prices change often).
Lean recommended spend: TCM PEH (~$30) + a couple months of THM Premium during foundations → HTB VIP + PG Practice during box-grinding → PEN-200/OSCP when you're consistently solving boxes solo. That keeps you well under ~$50/month until the cert itself.
---
Quick Readiness Checklist (Are You Exam-Ready?)
[ ] You enumerate thoroughly and automatically, every time.
[ ] You can exploit common web vulns (SQLi, file upload, LFI/RFI, command injection) by hand.
[ ] You can get a foothold and then escalate on both Linux and Windows without walkthroughs on easy/medium boxes.
[ ] You've solved a solid chunk of TJ Null's list solo.
[ ] You can do a basic stack buffer overflow start to finish.
[ ] You have a personal methodology cheat sheet you trust under pressure.
[ ] You've written 10+ practice reports and can produce a clean one under time limits.
When most of these are checked, buy the exam. Good luck — and Try Harder.
---
Note: Prices, course bundles, and exam structure change. Always confirm current details on the official OffSec site before purchasing. Links were accurate as of mid-2026.
