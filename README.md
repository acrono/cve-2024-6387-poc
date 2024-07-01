# cve-2024-6387-poc
> a signal handler race condition in OpenSSH's server (sshd)

- 7etsuo

## Description

An exploit for CVE-2024-6387, targeting a signal handler race condition in OpenSSH's server (`sshd`) on glibc-based Linux systems. The vulnerability allows for remote code execution as root due to async-signal-unsafe functions being called in the `SIGALRM` handler.

## Exploit Details

### Vulnerability Summary

The exploit targets the `SIGALRM` handler race condition in OpenSSH's `sshd`:
- **Affected Versions**: OpenSSH 8.5p1 to 9.8p1.
- **Exploit**: Remote code execution as root due to the vulnerable `SIGALRM` handler calling async-signal-unsafe functions.
