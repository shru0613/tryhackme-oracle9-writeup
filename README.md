# Oracle 9 - TryHackMe Writeup

## Room Link
[Oracle 9 on TryHackMe](https://tryhackme.com/room/oracle9) *(Add actual link if different)*

## Description
Oracle 9 is a TryHackMe room focusing on penetration testing and AI prompt injection techniques. The target is a machine with IP `10.10.233.17` featuring multiple open and closed ports. The challenge involves scanning the target, exploiting the AI chatbot interface, and retrieving hidden information.

## Tools Used
- **Nmap** — for port scanning and service enumeration  
- **Empire** — for creating payloads and managing listeners  
- **Starkiller** — for exploitation and staging payloads  

## Target Details
- **IP Address:** 10.10.233.17  
- **Open Ports:** 80 (HTTP)  
- **Filtered/Closed Ports:**  
  - 22 (Closed)  
  - 53 (Error/Filtered)  

## Methodology / Steps Taken
1. **Port Scanning:**  
   Ran Nmap to discover open ports. Found port 80 open with an HTTP interface. Ports 22 was closed, and 53 showed errors or filtering.

2. **Enumeration:**  
   Explored the web interface on port 80. Identified the Oracle chatbot as the main interaction point.

3. **Exploitation:**  
   Used prompt injection techniques through the chatbot interface to bypass restrictions.

4. **Payload Delivery:**  
   Created listeners and stagers using Empire and Starkiller tools to manage reverse shells or payload delivery where applicable.

5. **Retrieval:**  
   Extracted the hidden “sealed transmission” message from the Oracle chatbot by sending a crafted access override prompt.

## Outcome
Successfully bypassed the Oracle chatbot’s input filter and retrieved the classified transmission. This room emphasized the importance of AI security and prompt injection vulnerabilities.

## Notes
- Ports 22 and 53 were inaccessible or filtered, focusing the attack surface primarily on port 80.
- No traditional shell access was obtained; the main challenge revolved around the chatbot interaction.

---

*Feel free to contribute, raise issues, or suggest improvements!*

---

### Author
*Shru0613*
