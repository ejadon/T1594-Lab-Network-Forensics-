# T1594-Lab-Network-Forensics-

## Scenario

Adversaries may search websites owned by the victim for information that can be used during targeting. Victim-owned websites may contain a variety of details, including names of departments/divisions, physical locations, and data about key employees such as names, roles, and contact info (ex: Email Addresses). These sites may also have details highlighting business operations and relationships.[1]

Adversaries may search victim-owned websites to gather actionable information. Information from these sources may reveal opportunities for other forms of reconnaissance (ex: Phishing for Information or Search Open Technical Databases), establishing operational resources (ex: Establish Accounts or Compromise Accounts), and/or initial access (ex: Trusted Relationship or Phishing).

### Tools Used

- ZEEK
- BRIM

## Steps

Loading Zeek logs in Brim Security. How many HTTP requests are there? 
- Ref: Right clicked on HTTP request and chose count by field 
![Screenshot 2024-10-01 at 9 49 33 PM](https://github.com/user-attachments/assets/9b5c3b57-73e9-47cb-849c-13a9f30c5866)


What is the domain of the targeted website?
- Ref: Right-clicked on Host and chose count by field. The host shown has the most requests which strongly indicates it's the targeted website 
![Screenshot 2024-10-01 at 9 50 30 PM](https://github.com/user-attachments/assets/b8f67469-868d-46e0-add0-f7a3b2c316b7)


What is the tool used by the attacker to crawl the website?
- Ref: The IP with the most requests is likely the attackers. Next, I queried the DNS request which resulted in portswigger.net. This is the company behind Burp Suite, a penetration-testing website.
![Screenshot 2024-10-01 at 9 52 06 PM](https://github.com/user-attachments/assets/8fe866d9-5f2e-44ee-b813-687f2b025573)
![Screenshot 2024-10-01 at 9 53 59 PM](https://github.com/user-attachments/assets/c5a493c7-0bf3-4b99-b0f2-6eb3cb77785f)


How many web pages the attacker was able to access?

-Ref: Right-clicked on status code. 200 is the code for a successfully completed request = 2116
![Screenshot 2024-10-01 at 9 55 15 PM](https://github.com/user-attachments/assets/43c5fe75-306b-44dd-99fe-95d51a514528)


What is the browser used by the attacker? (Format: Browser_Name Version)

-Ref: Below is the agent field and show the browser used 
![Screenshot 2024-10-01 at 9 56 34 PM](https://github.com/user-attachments/assets/597e11c2-ba7b-434c-9b58-6f59aad6f744)






