### Introduction for Students

## What is Snort?
Snort is an open-source Network Intrusion Detection and Prevention System (IDS/IPS). It monitors network traffic, analyzes packets, and detects suspicious or potentially malicious activities using predefined rules.

Snort is widely used in cybersecurity to monitor networks and identify possible threats.

***learn more about Snort***: https://www.snort.org

## Recommended Ubuntu Version -- Important Lesson Learned
# Recommendation:
Use Ubuntu 24.04 LTS for this lab, unless your Snort version or installation method requires a different supported release.

# A Lesson From My Own Experience
During my Snort lab setup, I faced compatibility and configuration difficulties while working with my Ubuntu environment cause I have the newer version which doesn't have Snort 2. I did some research and found that you can still download it but the process was very difficult like first downloading dependencies, libraries etc etc i spent 2+ hours trying to download Snort 2 on my newer Ubuntu version but then i give up cause there were so much errors in configuration files and code So i decided to download older UbuntuVM ISO 24.04. 
This experience taught me an important lesson: choosing the right OS version before starting a cybersecurity lab can save a lot of time.

## My Advice to Students
- Prefer Ubuntu 24.04 LTS for this lab
- Check Snort's compatibility with your Ubuntu version before installation
- Follow installation instructions that match your OS
- Don't immediately assume every installation error is caused by your configuration
- Verify dependencies and pakage availability before spending hours troubleshooting
