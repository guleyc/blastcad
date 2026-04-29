---
layout: page
title: Session Security
permalink: /security/
---

# Session Security

To protect your engineering data and prevent unauthorized access, BlastCAD implements a robust **AuthGuard** system.

### Automatic Protection
If your session expires while working (e.g., JWT token timeout), the system will automatically lock the interface. This prevents further API requests that would fail and prompts a secure re-login to ensure no data is lost during the process.

### Encrypted Tokens
All communication between the frontend and the BlastCAD API is secured via **JSON Web Tokens (JWT)**. These tokens are handled through a central Axios client that automatically attaches authorization headers to every request.

### Data Privacy
* **Local Storage:** Authentication details are stored locally and cleared immediately upon logout.
* **Session Monitoring:** The application monitors 401 (Unauthorized) responses in real-time to trigger the security layer.