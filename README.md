# Cowrie Honeypot Project

This repository contains my Cowrie honeypot setup, a medium-interaction SSH and Telnet honeypot designed to log brute force attacks and the activities of attackers.  

## Project Overview

Cowrie is a honeypot that emulates an SSH and Telnet server, capturing attacker commands, login attempts, and malware uploads. This project includes:

- Cowrie honeypot files and configuration
- Optional integration  tcpdump for monitoring and logging network traffic
- Logs stored under `var/log/` for analysis

## Directory Structure


cowrie/
├── bin/
├── etc/
├── src/
├── var/ # logs
├── cowrie-env/ # Python virtual environment
├── honeyfs/ # fake filesystem for attackers
├── README.md
├── .gitignore
└── requirements.txt


## Setup

### 1. Install Dependencies

```bash
# Create Python virtual environment
python3 -m venv cowrie-env
source cowrie-env/bin/activate

# Install required packages
pip install -r requirements.txt


#Run Cowrie

# Activate virtual environment
source cowrie-env/bin/activate

# Run Cowrie
bin/cowrie start


# Monitoring
# I used  tcpdump alongside Cowrie to capture and analyze network traffic 
#and stored  the traffic in test.pcap
sudo tcpdump -i wlan0 -w test.pcap


 
