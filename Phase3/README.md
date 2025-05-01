# ICS344 Project - Phase 3: Defensive Strategy Proposal

---

## Phase 3 Overview

In this phase, we implemented multiple defensive mechanisms to block SSH attacks on the victim machine (Metasploitable3).  
Each defense was tested before and after, and screenshots were taken to prove the effectiveness.

---

## Steps and Screenshots

---

### Step 1: Before Applying Defense

- SSH connection was successful without any restrictions.
- The attacker was able to connect using SSH easily.

![Before Defense 1](Steps/phase%203%20before%20defence%201.PNG)

---

### Step 2: Changing SSH Port (Defense Mechanism 1)

- Edited `/etc/ssh/sshd_config` to change SSH default port from **22** to **2222**.
- This reduces the chance of automated attacks that target port 22.

![Changing SSH Port](Steps/phase%203%20before%20defense%201%20changing%20ssh%20port%202.PNG)

---

### Step 3: Confirming the System Defense

- Verified system settings and SSH access before applying next layers of defense.

![System After ](Steps/phase%203%20defense%201%20complete%20with%20no%20attacks%203.PNG)

---

### Step 4: Confirming SSH Attack Before Defense 2

- Applying stronger defenses.

![Before Defense 2](Steps/phase%203%20system%20before%20defense%202%204.PNG)

---

### Step 5: Applying Defense 2 Completely (Stopping SSH Services)

- Stopped SSH services from being running.
- SSH service is now stopped meaning it will not accept any traffic.

![Defense 2 Completed](Steps/phase%203%20defense%202%20stopping%20ssh%205.PNG)

---

### Step 6: result of Stopping SSH

- Manually stopped SSH service using `sudo service ssh stop`.
- This blocks any new SSH sessions even if the attacker knows the new port.

![Stopping SSH Service](Steps/phase%203%20result%20of%20defense%202%206.PNG)

---

### Step 7: Confiriming SSH Before Defense 3 (Deleting SSH Server)

- Connection messages observed.

![D3](Steps/phase%203%20before%20defense%203%207.PNG)

---

### Step 8: Removing SSH Server Completely (Defense Mechanism 3)

- Fully removed the SSH server package using:

```bash
sudo apt-get purge openssh-server -y
sudo apt-get autoremove -y

```
![Removing SSH Server](Steps/phase%203%20defense%203%20removing%20SSH%20server%208.png)

### Step 9: Result of Defense 3

- Connection messages observed.

![After Defense 3](Steps/phase%203%20after%20defense%203%209.png)

---
