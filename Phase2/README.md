# ICS344 Project - Phase 2:
---

## Phase 2 Overview

In this phase, we analyzed SSH attack logs collected from the victim machine using Splunk.  
We visualized the attack behavior through dashboard pie charts, line charts, and tables.

---

## Tools Used

- Splunk Enterprise
- Kali Linux
- Metasploitable3
- Python 

---

## Steps and Screenshots

---

### Step 1: Opening Splunk Interface

- We successfully launched Splunk in the browser to start the analysis.

![Splunk Interface](Steps/phase_2_splunk_interface_1.PNG)

---

### Step 2: Viewing Splunk Home Page

- Verified that Splunk was running properly and ready to add data.

![Splunk Home Page](Steps/phase_2_splunk_home_page_2.PNG)

---

### Step 3: Adding Victim Logs to Splunk

- Uploaded the victim's `auth.log` file (`victim_auth.log`) for analysis.

![Adding Victim Logs](Steps/phase_2_adding_victim_4.PNG)

---

### Step 4: Adding Attacker Logs to Splunk

- Attempted to monitor any relevant attacker-side logs.

![Attacker Logs](Steps/phase_2_attacker_logs_3.PNG)

---

### Step 5: Viewing Correct Victim Logs

- Searched for SSH login attempts in the uploaded victim logs.

![Logs of Victim](phase_2_logs_victim_5.PNG)

---

### Step 6: Building the Line Chart (SSH Login Attempts Over Time)

- Created a **Line Chart** to show the number of SSH login attempts over time.

![Line Chart](Steps/phase_2_line_7.PNG)

---

### Step 7: Search Command for Line Chart

- Used Splunk query to generate the line chart visualization.

![Line Chart Command](Steps/phase_2_line_command_8.PNG)

---

### Step 8: Building the Pie Chart (Success vs Failure)

- Created a **Pie Chart** showing the ratio of successful vs failed SSH login attempts.

![Pie Chart](Steps/phase_2_piet_command_9.PNG)

---

### Step 9: Successful vs Failure Login Visualization

- Visualization clearly showed the success and failure SSH login attempts split.

![Success vs Failure](Steps/phase_2_s_vs_f_6....PNG)

---

### Step 10: Building the Table View

- Created a **Table View** to list raw login attempts with timestamps.

![Table View](Steps/phase_2_table_view_10.PNG)

---


## Key Observations

- The majority of login attempts were failures, indicating brute-force attacks.
- A small percentage of login attempts were successful.
- Attack patterns were spread across different timestamps.

---

## Conclusion

Through the use of Splunk, we were able to successfully visualize and analyze SSH login behavior on the victim machine, detecting patterns of attack attempts, and categorizing them into successful and failed connections.

