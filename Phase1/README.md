# Phase 1: Setup and Compromise the Service

## 📋 Group Information

- **Group Number:** 1
- **Students:**
  - KHALID BUKHARI – 202013420
  - OSAMAH ALNAHARI – 202183290
  - OSAMA ALIBRAHIM – 202035080

---

## 📚 Work Distribution

The work was done through Teams meetings, where each member participated to complete the project.

---

## 🛠️ Environment Setup

- **Victim Machine:** Metasploitable3 (Ubuntu 14.04)

  - SSH service running and reachable.

  ![SSH Service Status](steps/phase%201%20SSH%20status%20for%20attacking%205.PNG)

- **Victim IP Address:**

  - IP: `192.168.56.104`

  ![Victim IP Address](steps/phase%20ip%20of%20victim%202.PNG)

- **Attacker Machine:** Kali Linux

  - Metasploit Framework installed and initialized.

  ![Metasploit Initialization](steps/phase%201%20meta%20initialization%201.PNG)

---

## 🎯 Target Service

- **Selected Vulnerable Service:** SSH (`port 22`)

---

## 🔥 Attack 1: Using Metasploit Framework

- **Tool:** Metasploit auxiliary module `scanner/ssh/ssh_login`
- **Steps:**

  1. Initialize Metasploit (`msfconsole`).

     ![Metasploit Initialization](steps/phase%201%20metasploit%20in%20kali%206.PNG)

  2. Set module parameters:

     - Target IP: `192.168.56.104`
     - Username: `vagrant`
     - Password: `vagrant`

     ![Setting Metasploit Parameters](steps/phase%201%20metasploit%20parameters%207.PNG)

  3. Execute the attack.

     - Successful login and session creation.

     ![Successful SSH Attack with Metasploit](steps/phase%201%20attacking%20ssh%207.PNG)

- **Connectivity Check:**

  - Verified network communication between attacker and victim.

    ![Ping from Attacker](steps/phase%201%20pinging%20from%20attacket%20to%20vicitm%204.PNG)

    ![Ping from Host](steps/phase%201%20pinging%20from%20host%20to%20victim%203.PNG)

---

## 🧠 Attack 2: Using Custom Script

- **Tool:** Python (with `paramiko` library for SSH automation)
- **Steps:**

  1. Developed a custom script `script.py` to connect via SSH.

     ![Custom Script Code](steps/phase%201%20script%209.PNG)

  2. The script successfully connected to the victim and executed the `whoami` command.

     ![Custom Script Attack Result](steps/phase%201%20script%20attack%208.PNG)

---

## 📷 Screenshots Location

All evidence screenshots are available in the `/steps` folder and properly named for easy reference.
