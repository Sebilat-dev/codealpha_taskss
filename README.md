# Task 4: Network Intrusion Detection System (Suricata)

##  Objective
To set up and configure a network-based intrusion detection system (IDS) using Suricata to monitor and detect suspicious network activity.

---

##  Tools Used
- Kali Linux  
- Suricata  

---

##  Steps Performed

### 1. Identified Network Interface
Used the command below to identify the active network interface:


ip a


📷 Screenshot:

![Interface](1_interface.png)

---

### 2. Configured Custom Rule
Added an ICMP detection rule in:


/etc/suricata/rules/local.rules


📷 Screenshot:

![Rule Added](2_rule_added.png)

---

### 3. Started Suricata Monitoring
Ran Suricata to monitor live traffic:


sudo suricata -i eth0


📷 Screenshot:

![Suricata Running](3_suricata_running.png)

---

### 4. Generated Traffic & Verified Alerts
Generated ICMP traffic using:


ping google.com


Checked alerts:


sudo cat /var/log/suricata/fast.log


📷 Screenshot:

![Alert Detected](4_alert_detected.png)

---

##  Result
Suricata successfully detected ICMP traffic and generated alerts, confirming proper IDS configuration.

---

##  Conclusion
This task demonstrated how Suricata can monitor network traffic and detect suspicious activity using custom rules in a real-time environment.
