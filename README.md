# CTS-QR v1.0 RCE
Unauthenticated RCE on CTS-QR v1.0 // Tested on: Lockdown CTF from TryHackMe

### Usage
The usage is very simple, you just need to pass the base url for the target system, and it'll do the rest. Some paths may alter depending on how the installation process of CTS-QR ocurred in the target.
`$ python3 exploit.py http://target.tld`

### Explanation
The script uses a SQL Injection vulnerability on /admin login form to bypass the authentication mechanism, abuses an unrestricted file upload vulnerability at /admin/?page=system_info to upload a php backdoor, which leads to an unauthenticated user being able to remotely execute code on the vulnerable system.
