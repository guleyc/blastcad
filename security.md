---
layout: page
title: Session & Security (AuthGuard)
nav_order: 6
---

# Session & Security (AuthGuard)
{: .no_toc }

Data integrity is the highest priority in BlastCAD. To prevent data loss and unauthorized access, the platform employs a robust session management system known as **AuthGuard**.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 1. The "Ghost Login" Prevention

In typical web applications, users can sometimes experience a "Ghost Login" — a scenario where the security token expires in the background, but the user interface remains active. If a user attempts to save hours of complex ring designs with an expired token, the server will reject the request, potentially resulting in catastrophic data loss.

BlastCAD entirely eliminates this risk through its **AuthGuard** architecture.

## 2. How AuthGuard Works

AuthGuard acts as a global sentry between the BlastCAD interface and the backend API servers. 

### JWT (JSON Web Tokens)
All communications are secured using encrypted JWTs. These tokens carry your authentication status and have a strict expiration timeline to ensure security.

### Axios Interceptor
BlastCAD utilizes a centralized API client. Every response from the server is automatically intercepted and checked:
1. **Valid Request:** If the token is valid, the data is processed normally.
2. **Expired Token (401 Unauthorized):** If the server detects an expired token, it responds with a `401` error. 

## 3. UI Lockdown & Data Preservation

When a `401 Unauthorized` response is intercepted, the following automated safety protocol triggers instantly:

1. **Global State Update:** The application state changes to `isSessionExpired = true`.
2. **Interface Lockdown:** The entire BlastCAD workspace is immediately overlaid with a secure, blurred lock screen. This prevents any further actions or API calls that would inevitably fail.
3. **Data Freezing:** Your current unsaved workspace (holes, cad drawings, charge rules) remains frozen securely in the background.
4. **Secure Re-entry:** The user is prompted with a clear warning and a button to re-authenticate. Once logged back in, the lock screen is lifted, and you can resume exactly where you left off.

## 4. Local Storage Management
Upon a deliberate user logout, BlastCAD ensures complete data hygiene by immediately purging all local storage parameters, including:
* `blastcad_token`
* Cached engineering entities and local project states.