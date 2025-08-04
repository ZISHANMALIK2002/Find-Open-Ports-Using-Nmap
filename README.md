# 🔍 How to Find Open Ports Using Nmap – Step-by-Step Guide 
Nmap (Network Mapper) is a powerful open-source tool used to discover hosts and services on a computer network by sending packets and analyzing the responses. Here's how to use it to find open ports on a target machine.
##  Step 1: Open the Command Prompt (CMD)
- Press Windows + R
- Type cmd and hit Enter
[This will launch the command-line interface.]
## Step 2: Find Your IP Address
- In the Command Prompt, type: ipconfig
- Look for the section labeled IPv4 Address under your active network adapter.
- Example: 192.168.1.10 [This is the IP address of your machine within the local network.]
##  Step 3: Copy the IP Address
- Use your mouse or keyboard to highlight and copy the IPv4 address.
- You’ll use this address as the target in Nmap.
## Step 4: Open the Nmap Tool
- Launch the Nmap GUI (called Zenmap) if installed, or use the command-line version.
- If you haven't installed Nmap, download it from the official website: [https://nmap.org/download.html]
##  Step 5: Paste the IP in the Target Field
- In Zenmap, paste the copied IP address into the Target field.
- In the Command field (optional), use a scan command like: nmap -sS 192.168.1.10 (This performs a stealth SYN scan.)
## Step 6: Start the Scan
- Click the "Scan" button if using Zenmap
- Or press Enter if you're using the command-line
- Nmap will begin scanning the target IP for open ports.
## Step 7: Analyze the Results
- After the scan completes, Nmap will list open ports, their services, and states.
- Example output:.
  
| PORT | STATE | SERVICE |
|------|-------|---------|
| 22/tcp | open | ssh |
| 80/tcp | open | http |
| 443/tcp | open | https |
##  Common Nmap Commands for Port Scanning


| Command                    | Description                           |
| -------------------------- | ------------------------------------- |
| `nmap <target>`            | Basic scan of the target IP or domain |
| `nmap -sS <target>`        | Stealth (SYN) scan                    |
| `nmap -p 1-65535 <target>` | Scan all ports                        |
| `nmap -A <target>`         | Aggressive scan (OS + services)       |
| `nmap -T4 <target>`        | Faster scan speed                     |

## ⚠️ Note
- Make sure you have permission before scanning a network or device. Unauthorized scanning may be considered illegal or intrusive.
- Use Nmap responsibly and only on systems you own or are authorized to test.
