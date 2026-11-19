# TryHackMe: Offensive Security Intro
- **Platform:** TryHackMe
- **Focus Area:** Web Enumeration, Access Control Concepts

## 1. Overview
An introductory hands-on lab covering offensive vs. defensive security concepts, hidden directory discovery, and broken/missing access control on a simulated banking web application (`fakebank.thm`).

## 2. Reconnaissance & Enumeration
Using `dirb` against `http://fakebank.thm`, unlinked paths were discovered:
- `/bank-transfer` (HTTP `200`)
- `/images` (HTTP `301`)

## 3. Exploitation / Finding Walkthrough
1. Inspected account `8881` in the FakeBank web application.
2. Navigated directly to `http://fakebank.thm/bank-transfer`, revealing an accessible admin deposit interface without requiring authentication.
3. Deposited `2000` into account `8881` to demonstrate unauthorized functional access.

## 4. Remediation & Key Takeaways
- Hiding a URL is **security by obscurity**, not proper access control.
- Sensitive administrative endpoints such as `/bank-transfer` must enforce authentication and authorization checks before processing requests.