Data Tampering & Backdoor File Upload at Universitas Islam Riau

This repository documents two security vulnerabilities discovered at https://app.eng.uir.ac
:

Data Tampering in GET Request.

Backdoor File Upload vulnerability.

Tools Used:

Burp Suite: For detecting data tampering and file upload issues.

Vulnerabilities:
1. Data Tampering:

An attacker can manipulate GET request parameters to modify sensitive data.

Example:
GET /mhs_index.php?data=someSensitiveData HTTP/1.1

2. Backdoor File Upload:

An attacker can upload a malicious file (e.g., PHP shell) through a manipulated GET request.

Example:
GET /mhs_index.php?file=malicious_file.php HTTP/1.1

Steps to Reproduce:

Visit https://app.eng.uir.ac.id/mhs_index.php
.

Modify GET request parameters using Burp Suite.

Observe the unauthorized changes or file uploads.

Mitigation:

Use POST instead of GET for sensitive data.

Validate and sanitize all inputs, including files.
