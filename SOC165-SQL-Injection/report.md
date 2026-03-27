# SOC165 – SQL Injection Attempt

## 1. Alert Overview
- Event ID: 115  
- Rule: Possible SQL Injection Payload Detected  
- Date: Feb 25, 2022  
- Verdict: True Positive  

---

## 2. Incident Summary

A suspicious web request containing a SQL injection payload was detected targeting a web application.

SQL injection attacks attempt to manipulate database queries using malicious input, potentially allowing attackers to access or modify sensitive data.

---

## 3. Investigation

### Step 1: Payload Analysis
- The URL was encoded  
- After decoding, it revealed SQL injection patterns such as: OR 1=1

- 
This confirms a SQL injection attempt.

---

### Step 2: Log Correlation
- Multiple requests from same source IP  
- Similar payloads observed  

---

### Step 3: Response Analysis
- HTTP Status Code: 500  
- No valid data returned  

This indicates the attack failed.

---

### Step 4: Threat Validation
- External attacker IP  
- No evidence of internal testing  

---

## 4. Conclusion

- Attack Type: SQL Injection  
- Verdict: True Positive  
- Success: No  
- Escalation: Not required  

Even though the attack failed, it is considered malicious due to clear intent.

---

## 5. Skills Demonstrated

- SQL injection detection  
- URL decoding  
- Log correlation  
- Threat analysis 
<img width="1410" height="502" alt="Screenshot 2026-03-27 163842" src="https://github.com/user-attachments/assets/bdac8ef8-153a-4a1e-9d4a-a8dfab6822d9" />

<img width="1366" height="266" alt="Screenshot 2026-03-27 163854" src="https://github.com/user-attachments/assets/01e853f3-cba6-4293-b088-f98a0e8e9939" />


