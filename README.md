# Cybersecurity-CTF-Labs-Collection-Race-Conditions-Business-Logic-Abuse
A curated index of hands-on CTF labs covering race conditions, TOCTOU attacks, concurrent request abuse, double-spending, and e-commerce client-side logic flaws from Learn SecByte.
# Race Conditions & Business Logic Abuse CTF Labs Collection

A structured, searchable index of hands-on cybersecurity labs focusing on race conditions, Time-of-Check to Time-of-Use (TOCTOU) attacks, concurrent request execution, and e-commerce business logic flaws hosted on Learn SecByte.

This repository is designed for web application security testers, penetration testers, CTF players, software developers, and SOC/AppSec engineers learning how to identify, exploit, and remediate race conditions and flawed trust assumptions in web applications.

---

## Table of Contents
- [Introduction](#introduction)
- [Lab Collection & Index](#lab-collection--index)
- [Categories](#categories)
  - [Client-Side Trust & Price Manipulation](#client-side-trust--price-manipulation)
  - [Race Conditions & Concurrent Request Abuse](#race-conditions--concurrent-request-abuse)
  - [TOCTOU & File/System Concurrency](#toctou--filesystem-concurrency)
- [Learning Path](#learning-path)
- [How to Use the Labs](#how-to-use-the-labs)
- [Disclaimer](#disclaimer)

---

## Introduction

Modern web applications frequently suffer from two critical architectural pitfalls: trusting client-side inputs and failing to handle concurrent state changes safely. When servers rely on client-provided values or execute multi-step database/filesystem operations without proper locking or atomic transactions, attackers can manipulate transaction flows, bypass payment mechanisms, or exploit subtle timing windows.

This repository organizes hands-on security labs from Learn SecByte into clear, structured learning paths covering web concurrency and business logic auditing.

---

## Lab Collection & Index

| Lab Title | Target Focus | Primary Category | Access Link |
| :--- | :--- | :--- | :--- |
| **Cart Manipulation** | E-Commerce | Client-Side Trust | [Access Lab](https://learn.secbyte.org/ctf/cart-manipulation-client-side-trust) |
| **Price Manipulation** | E-Commerce | Parameter Tampering | [Access Lab](https://learn.secbyte.org/ctf/price-manipulation-trusting-the-client-too-much) |
| **Coupon Manipulation** | E-Commerce | Discount Validation Flaws | [Access Lab](https://learn.secbyte.org/ctf/coupon-manipulation-abusing-client-side-discounts) |
| **Business Logic Abuse** | Web Application | Workflow Integrity | [Access Lab](https://learn.secbyte.org/ctf/business-logic-abuse-trust-the-flow-not-the-user) |
| **Concurrent Request Abuse** | Web Application | Web Transaction Racing | [Access Lab](https://learn.secbyte.org/ctf/concurrent-request-abuse-racing-web-transactions) |
| **File Race Condition** | File System | TOCTOU / File Operations | [Access Lab](https://learn.secbyte.org/ctf/file-race-condition-winning-the-toc-tou-window) |
| **Registration Race** | Identity / Auth | Account Creation Concurrency | [Access Lab](https://learn.secbyte.org/ctf/registration-race-exploiting-and-defending-account-creation-) |
| **Payment Race** | Financial / Checkout | Timing & Transaction Abuse | [Access Lab](https://learn.secbyte.org/ctf/payment-race-timing-the-checkout) |
| **Coupon Race** | E-Commerce | Single-Use Discount Abuse | [Access Lab](https://learn.secbyte.org/ctf/coupon-race) |
| **Double-Spend Blockchain** | Blockchain / Ledger | Transaction Racing | [Access Lab](https://learn.secbyte.org/ctf/double-spend-blockchain-transaction-race-conditions) |
| **TOCTOU Attacks** | Operating Systems / Web | Race Condition Fundamentals | [Access Lab](https://learn.secbyte.org/ctf/toctou-attacks-race-conditions) |
| **TOCTOU in Security** | Systems Security | Defense & Race Conditions | [Access Lab](https://learn.secbyte.org/ctf/toctou-attacks-race-conditions-in-security) |

---

## Categories

### Client-Side Trust & Price Manipulation
Hands-on labs detailing parameter tampering, client-side discount calculations, and insecure workflow assumptions:

* **Cart Manipulation:** Exploiting applications that trust client-supplied shopping cart parameters.
  * Lab Link: https://learn.secbyte.org/ctf/cart-manipulation-client-side-trust
* **Price Manipulation:** Overriding item prices during checkout by altering hidden fields and client requests.
  * Lab Link: https://learn.secbyte.org/ctf/price-manipulation-trusting-the-client-too-much
* **Coupon Manipulation:** Subverting client-side discount logic to apply unauthorized promotional codes.
  * Lab Link: https://learn.secbyte.org/ctf/coupon-manipulation-abusing-client-side-discounts
* **Business Logic Abuse:** Analyzing application workflow state machines and enforcing robust server-side validation.
  * Lab Link: https://learn.secbyte.org/ctf/business-logic-abuse-trust-the-flow-not-the-user

### Race Conditions & Concurrent Request Abuse
Practical security labs demonstrating how asynchronous operations and missing mutex locks allow request racing:

* **Concurrent Request Abuse:** Sending parallel HTTP requests to trigger unexpected state transitions in web transactions.
  * Lab Link: https://learn.secbyte.org/ctf/concurrent-request-abuse-racing-web-transactions
* **Registration Race:** Exploiting race conditions during user registration to duplicate accounts or bypass limits.
  * Lab Link: https://learn.secbyte.org/ctf/registration-race-exploiting-and-defending-account-creation-
* **Payment Race:** Timing concurrent checkout requests to process multiple orders against a single payment or credit allowance.
  * Lab Link: https://learn.secbyte.org/ctf/payment-race-timing-the-checkout
* **Coupon Race:** Reusing single-use coupons multiple times simultaneously by firing parallel requests before state updates complete.
  * Lab Link: https://learn.secbyte.org/ctf/coupon-race
* **Double-Spend Blockchain Race:** Simulating race condition attacks across blockchain transactions and unconfirmed mempools.
  * Lab Link: https://learn.secbyte.org/ctf/double-spend-blockchain-transaction-race-conditions

### TOCTOU & File/System Concurrency
Labs focused on low-level and file-system level Time-of-Check to Time-of-Use race condition mechanics:

* **File Race Condition:** Exploiting tiny timing windows between file privilege verification and execution/reading operations.
  * Lab Link: https://learn.secbyte.org/ctf/file-race-condition-winning-the-toc-tou-window
* **TOCTOU Fundamentals:** Fundamentals of Time-of-Check to Time-of-Use race conditions across software architecture.
  * Lab Link: https://learn.secbyte.org/ctf/toctou-attacks-race-conditions
* **TOCTOU Security & Defense:** Defensive patterns, file locking strategies, and atomic operations to eliminate TOCTOU vulnerabilities.
  * Lab Link: https://learn.secbyte.org/ctf/toctou-attacks-race-conditions-in-security

---

## Learning Path

Follow this structured roadmap to master web application logic and concurrency auditing:

1. **Client-Side Parameter & Logic Auditing**
   - Test application endpoints for trusted client inputs, price tampering, and flawed workflow logic.
2. **Introduction to Race Conditions**
   - Learn the mechanics of HTTP request synchronization and concurrent execution.
   - Practice single-use coupon reuse and user registration race conditions.
3. **Financial & Checkout Concurrency**
   - Execute payment timing attacks and analyze ledger-based double-spend race windows.
4. **Low-Level TOCTOU & Systems Security**
   - Study Time-of-Check to Time-of-Use flaws in file uploads and system routines.
   - Implement database locks, atomic operations, and anti-racing controls.

---

## How to Use the Labs

1. Select a practice scenario from the index table or category sections above.
2. Access the target environment directly on Learn SecByte.
3. Use web proxies (e.g., Burp Suite Turbo Intruder) or custom scripts to execute concurrent requests and test logic controls.
4. Review defense recommendations to learn how database locks, atomic steps, and token synchronization protect applications.

---

## Disclaimer

This repository is strictly intended for educational research, defensive security training, and authorized penetration testing. All concepts, code patterns, and lab environments are designed to help developers and security practitioners secure modern applications. Performing unauthorized attacks or logic abuse against live commercial platforms without explicit written permission is illegal.
