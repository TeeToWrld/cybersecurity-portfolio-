# Project 01 – Controlling SSH Access on AWS EC2 Using Security Groups

## 🛡️ Objective
This project demonstrates how to configure and test AWS Security Groups to allow or deny SSH access to EC2 instances. It simulates basic access control for cloud-based servers.

## 🧰 Tools Used
- AWS EC2
- AWS Security Groups
- Mac Terminal
- SSH Client
- Dynamic IP (used to simulate access control)

## 📝 Steps Taken
1. Launched two EC2 instances in the same region.
2. Created two security groups:
   - `Allow-SSH`: Permits SSH from my current IP.
   - `Deny-SSH`: No inbound SSH rule (blocks access).
3. Associated each instance with one of the security groups.
4. Connected to each instance via terminal:
   - Instance A connected successfully using:
     ```bash
     ssh -i altschool-key01.pem ec2-user@<instance-ip>
     ```
   - Instance B failed with a timeout error, as expected.
5. Verified that the SSH timeout was caused by lack of permissions in the security group.

## ✅ Results
- Instance A (allowed) was accessible via SSH.
- Instance B (denied) returned `Operation timed out`.
- Confirmed how AWS security groups enforce access policies based on IP.

## 💡 What I Learned
- How AWS Security Groups function as cloud firewalls.
- Importance of IP-based access control.
- That SSH access can be easily revoked or granted without restarting instances.
- How misconfigured rules can block access even when the server is running.


[Allow SSH](https://github.com/TeeToWrld/cybersecurity-portfolio-/blob/main/check%20for%20%20allowing%20only%20me%20access%20ssh.png)
[Deny SSH](https://github.com/TeeToWrld/cybersecurity-portfolio-/blob/main/check%20for%20denying%20ssh%20access.png)
[Instance A](https://github.com/TeeToWrld/cybersecurity-portfolio-/blob/main/instance%20A%202%20.png)
[instance A2](https://github.com/TeeToWrld/cybersecurity-portfolio-/blob/main/instance%20A.png)
---

🧠 *This project is part of my ongoing cybersecurity lab series, where I simulate real-world security scenarios while learning cloud and network security basics.*
