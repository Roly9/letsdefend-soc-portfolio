# SOC170 – Possible LFI Attack

## 1. Alert Overview
- Event ID: 120  
- Rule: Passwd Found in Requested URL  
- Date: Mar 1, 2022  
- Verdict: True Positive  

---

## 2. Incident Summary

A suspicious HTTP request attempted to access sensitive system files using directory traversal techniques.

The request targeted system files such as `/etc/passwd`, which is commonly used in Local File Inclusion (LFI) attacks to extract sensitive data.

---

## 3. Investigation

### Step 1: Payload Analysis
- The request contained: ../../../../etc/passwd

- - This indicates a directory traversal attempt.

---

### Step 2: Traffic Analysis
- Source: External IP  
- Destination: Internal Web Server  
- Direction: Internet → Internal  

---

### Step 3: Log Review
- HTTP Status Code: 500  
- Response Size: 0 bytes  

This indicates the request failed and was not processed successfully.

---

### Step 4: Attack Validation
- No file content returned  
- No suspicious outbound activity  

---

## 4. Conclusion

- Attack Type: LFI  
- Verdict: True Positive  
- Success: No  
- Escalation: Not required  

The activity represents a real attack attempt, even though it was unsuccessful.

---

## 5. Skills Demonstrated

- Log analysis  
- Web attack detection  
- HTTP response interpretation  
- Threat validation 

<img width="1413" height="499" alt="Screenshot 2026-03-27 163217" src="https://github.com/user-attachments/assets/cba05df7-ce72-4e46-900c-7cf629af6999" />

