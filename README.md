# HTB: Dante - Walkthrough

**Machine Name:** Dante  
**Platform:** HackTheBox  
**Difficulty:** Easy / Medium  
**OS:** Linux  
**Author:** Anvi (from Maham)  
**Date:** January 2026  
**Goal:** Get user flag & root flag

## Summary

Dante ek Linux web server machine hai jisme WordPress site hai. Humne FTP se info li, robots.txt se flag nikala, WordPress brute-force kiya, theme editor se reverse shell li, password reuse se user mila aur SUID find binary se root access kiya.

## Enumeration / Recon

### Network Scan

Subnet scan kiya live hosts dhundne ke liye:

```bash
nmap -sn -T4 10.10.110.0/24 -oN active-hosts
