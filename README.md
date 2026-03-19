Task: -03
API Security Risk Analysis (Modern SaaS Skill)

 By Future Interns

•	Target: - JSONPlaceholder (Test API)
https://jsonplaceholder.typicode.com

•	Prepared by: RUDRAKUMAR JOSHI (Cyber security intern)	
•	Date: [17/03/2026]













	




Executive Summary

This report presents the findings of a read-only API Security Risk Analysis conducted on publicly available demo APIs, including JSONPlaceholder and ReqRes. The objective of this assessment was to evaluate API security posture, identify potential risks, and provide actionable recommendations aligned with industry best practices.
During the assessment, multiple API endpoints were analysed using tools such as Postman and browser developer tools. The analysis focused on key security areas including authentication mechanisms, data exposure, request/response handling, and access control validation.
The findings indicate that while these APIs are designed for testing and demonstration purposes, they exhibit several common API security weaknesses that are frequently observed in real-world SaaS applications. These include lack of authentication enforcement on certain endpoints, excessive data exposure in API responses, and absence of strict access control validation.
Although no active exploitation was performed (in compliance with ethical and scope guidelines), the identified issues highlight potential risks such as unauthorized data access, information leakage, and misuse of API functionality if similar patterns exist in production environments.
Each identified risk has been categorized based on its severity and potential business impact. Clear and practical remediation steps have been provided to help improve API security posture, including implementing proper authentication, enforcing role-based access control, minimizing data exposure, and applying secure API design principles.






Objective
The main objectives of this task are:
•	Analyse public or test APIs.
•	Identify common API security risks.
•	Assess authentication and access control.
•	Explain risks in simple business language.
•	Suggest clear remediation steps.
This task focuses on thinking like a security consultant, not breaking systems.

Scope & Ethics
Allowed
•	Testing public or demo APIs
•	Read-only requests (GET, safe POST where allowed)
•	Documentation-based analysis
•	Header, token, and response inspection
Not Allowed
•	Exploitation or bypass attempts
•	Flooding / DoS testing
•	Attacking private or production APIs
Always stay ethical and legal.



Tools & Technologies Used

API Testing & Inspection
•	Postman
https://www.postman.com
•	Insomnia
https://insomnia.rest
•	Browser DevTools
(Inspect requests, headers, responses)
  Documentation & Reporting
•	Google Docs / MS Word / PDF

Sample APIs You Can Safely Use
Use demo or public APIs only:
  JSONPlaceholder (Test API)
https://jsonplaceholder.typicode.com
  ReqRes (API Testing Platform)
https://reqres.in
  Public APIs Collection
https://github.com/public-apis/public-apis



Methodology For API Security Risk Analysis
The API Security Risk Analysis was conducted using a structured and ethical approach, focusing on read-only testing of publicly available APIs such as JSONPlaceholder and ReqRes. The objective was to simulate how a security consultant evaluates API security without causing any disruption or unauthorized access.
1. API Selection & Scope Definition
A publicly accessible demo API was selected to ensure compliance with ethical guidelines. The scope was limited to:
•	Public endpoints
•	Read-only operations (GET requests)
•	Documentation-based analysis
No exploitation or intrusive testing was performed.
Our target is a JSONPlaceholder to test the API.
Selection of API Endpoints:
•	https://jsonplaceholder.typicode.com
•	https://jsonplaceholder.typicode.com/guide/
•	https://github.com/sponsors/typicode
•	https://my-json-server.typicode.com
There are the End Point of the Api for the target website or API.
 


















2. Documentation Review
The API documentation was carefully analysed to understand:
•	Available endpoints and parameters
•	Authentication mechanisms (if any)
•	Request and response formats
•	Intended functionality
This step helped identify expected vs actual behavior during testing.
  
This is a document in open the DevTool.


 
This is a file inside the Document css file contain the data design for the website.















3. API Testing & Traffic Inspection
API endpoints were tested using tools like Postman and browser Developer Tools.
The following aspects were inspected:
•	Request methods (GET, POST where allowed)
•	Headers (Authorization, Content-Type, etc.)
•	Query parameters and payloads
•	Response status codes and data structure
 
This image show the network Traffic inspection.
 
This image show the general Headers for this API.

4. Authentication & Authorization Analysis
The assessment evaluated whether APIs properly enforce:
•	Authentication (API keys, tokens, or none)
•	Authorization (role-based or user-based access control)
Special attention was given to:
•	Endpoints accessible without authentication
•	Potential for unauthorized data access
 
This is a POSTMAN TOOL to see the all the data about the authentication process of API.

5. Data Exposure Analysis
API responses were analysed to check for:
•	Sensitive data exposure (emails, IDs, tokens)
•	Excessive data in responses (over-sharing)
•	Lack of data filtering or masking
6. Security Misconfiguration Checks
The API was evaluated for common security misconfigurations, including:
•	Missing security headers
•	Improper error messages revealing system details
•	Lack of rate limiting indicators

7. Risk Identification & Classification
Identified issues were mapped to common API security risks (aligned with OWASP API Security Top 10).
Each risk was classified based on:
•	Severity (Low / Medium / High)
•	Potential business impact
•	Likelihood of exploitation
1. No Authentication Mechanism
•	Description: API endpoints are accessible without any authentication (no API key, no token).
•	Example Endpoint: /users, /posts
•	Risk Level:  High
Impact:
•	Anyone can access all data
•	No user verification
•	Potential for data scraping
Recommendation:
•	Implement authentication (JWT, API Keys)
•	Restrict access to authorized users only

2. Broken Access Control
•	Description: No role-based or user-based access restrictions are enforced.
•	Risk Level:  High
Impact:
•	Users can access all resources without permission
•	No separation between users
Recommendation:
•	Apply Role-Based Access Control (RBAC)
•	Enforce authorization checks on each request

3. Excessive Data Exposure
•	Description: API returns complete datasets without filtering.
•	Example: /users returns email, address, phone, etc.
•	Risk Level: Medium
Impact:
•	Sensitive data may be exposed
•	In real apps → privacy violation
Recommendation:
•	Return only necessary fields
•	Mask sensitive information

4. No Rate Limiting
•	Description: No visible limit on number of requests.
•	Risk Level:  Medium
Impact:
•	API abuse possible
•	Risk of DoS (Denial of Service)
Recommendation:
•	Implement rate limiting (e.g., 100 requests/minute)
•	Use throttling and monitoring

5. Lack of Security Headers
•	Description: Important security headers are missing.
•	Risk Level:  Low
Impact:
•	Increased vulnerability to attacks like XSS
•	Weak client-side protection
Recommendation:
•	Add headers like:
o	Content-Security-Policy
o	X-Content-Type-Options
o	X-Frame-Options
6. No Input Validation (Simulated POST)
•	Description: API accepts POST requests but does not validate input (mock behavior).
•	Risk Level:  Low
Impact:
•	In real apps → injection risks
•	Invalid data handling
Recommendation:
•	Implement input validation
•	Use server-side validation rules



8. Remediation Recommendations
For each identified risk, practical and industry-recommended solutions were provided, such as:
•	Implementing authentication and authorization
•	Reducing data exposure
•	Applying secure API design practices


Conclusion
The API Security Risk Analysis conducted on JSONPlaceholder demonstrates several common security weaknesses that are frequently observed in modern APIs. Although the API is intentionally designed as an open testing platform, the absence of essential security controls highlights critical risks that would be severe in a real-world production environment.


