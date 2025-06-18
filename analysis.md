# 📊 Cowrie SSH Honeypot Attack Simulation – Analysis

## 🧪 Project Summary

In this simulation, we deployed a Cowrie SSH honeypot on an Ubuntu Server VM. From a Kali Linux VM, we simulated an attack by connecting via SSH and executing basic reconnaissance commands (`ls`, `whoami`, `cat /etc/passwd`). Cowrie captured all of this activity in detailed log files, allowing us to study attacker behavior in a controlled lab environment.

---

## 🔍 What Cowrie Logged

Here’s what Cowrie successfully recorded during the attack:

- **Connection Details**  
  Cowrie captured the attacker's IP address, connection port, and SSH client version.

- **Login Attempt**  
  It logged the credentials used:  
  `login attempt [root/123456] succeeded`

- **Commands Executed**  
  Every command typed in the fake shell was logged:  
  `ls`, `whoami`, `cat /etc/passwd`

- **Session Closed**  
  Cowrie noted how long the attacker was active and when they disconnected.

---

## 📄 Sample Log Output

```text
New connection: 192.168.40.91:55890 (192.168.40.83:2222) [session: 5f3667e3df30]
login attempt [root/123456] succeeded
CMD: ls
CMD: whoami
CMD: cat /etc/passwd
Connection lost after 12 seconds


## 🧠 What I Learned

- I learned how to deploy and simulate an attack on a real honeypot system using Cowrie.
- I saw how attackers typically behave once they gain access — starting with basic system info gathering.
- I understood how important it is for a security system to have proper logging to track activity.
- The `tail -f cowrie.log` command helped me view real-time attacker behavior.
- I now have hands-on experience analyzing attack logs and identifying suspicious activity.

---

## ✅ Conclusion

This project helped me gain practical cybersecurity experience by simulating a common SSH attack and observing it using a honeypot.  
Cowrie successfully captured:

- Login attempts  
- Shell commands  
- Session behaviors

It taught me how attackers operate in early-stage intrusions and how defenders can detect them through proper logging.

This was a valuable learning project for improving both red team (attacker) and blue team (defender) thinking.