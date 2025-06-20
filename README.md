# IDS(Intrusion Detection System)
A basic Intrusion Detection System (IDS) implemented using suricata with additional ruleset that monitors network traffic for suspicious activity and potential threats, alerting users in real-time.

# Features

✅ Real-time packet capture and analysis

🔍 Signature-based attack detection (e.g., known threats like port scans, DoS)

📈 Logging and alerting system

🛠️ Extensible for new rules and models

# Installation
🔽 Download the Rule File
```
wget https://github.com/kr-anish/IDS/raw/main/anish.rules
```
Download Suricata
```
sudo apt install suricata
suricata --version
```

✅ Change the File location
```
sudo mv ~/Downloads/anish.rules /etc/suricata
```
Update the file location in suricata.yaml under rule-files
```
sudo gedit /etc/suricata/suricata.yaml
```
![Image](https://github.com/user-attachments/assets/8303ecfa-6da3-4dc0-b84e-71aff24ac9d2)

# Usage
Start suricata
```
sudo systemctl start suricata
```
Stop suricata
```
sudo systemctl stop suricata
```
Check status
```
sudo systemctl status suricata
```
![Image](https://github.com/user-attachments/assets/f1733e94-c8ee-4891-ad6c-1ba178dafdf2)

# Attack

Ping
```
ping <ip>
```
Port scanning
```
nmap <ip>
```
![Image](https://github.com/user-attachments/assets/84d99e43-85bf-4102-a0dc-d51b06189d8d)

# Logs

Fast logs
```
sudo cat /var/log/suricata/fast.log
```
![Image](https://github.com/user-attachments/assets/d7fcc431-971d-4681-b7d8-aca42c89e47a)

JSON logs
```
sudo tail -f /var/log/suricata/eve.json | jq 'select(.event_type=="alert")'
```



