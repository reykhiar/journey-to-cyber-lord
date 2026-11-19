# TryHackMe: Defensive Security Intro
- **Platform:** TryHackMe
- **Focus Area:** Defensive Security, Alert Triage, Incident Response Basics

## 1. Overview
An introductory blue-team simulation using a security dashboard (`Security Hub`) to identify suspicious alerts, investigate probing activity against sensitive web paths, and deploy containment/protection measures.

## 2. Alert Triage & Investigation
- Identified a critical alert involving probing of administrative web pages from IP `32.122.195.63`.
- Reviewed attempted paths (`https://fakebank.thm/admin`, `https://fakebank.thm/login`, and `https://fakebank.thm/backup`) and confirmed `https://fakebank.thm/admin` as the most recent target while checking whether access succeeded.

## 3. Response & Mitigation
Applied layered response actions on the dashboard:
1. Blocked the attacker IP (`32.122.195.63`).
2. Slowed down requests to sensitive/admin pages.
3. Enabled protection filters to mitigate probing attempts.

## 4. Key Takeaways
- Effective defense requires spotting high-priority signals among dashboard noise and investigating what the attacker actually tried or reached.
- Combining IP blocking, rate limiting, and protection rules provides stronger containment than relying on a single control.