
# 📘 SAP NetWeaver Application Server – Notes

---

## 📦 What is it?

- **NetWeaver** – SAP’s older technology foundation or **platform**
- **Application Server** – A system that **runs applications and processes business logic**

---

## 🔁 NetWeaver was like the BTP of old days

| Old (On-Premise)              | Modern (Cloud)                   |
|------------------------------|----------------------------------|
| SAP NetWeaver (AS ABAP/Java) | SAP BTP (Kyma, Cloud Foundry, etc.) |
| Runs on your server          | Runs in the cloud                |
| ABAP or Java stack           | Node.js, Python, Java, ABAP      |
| Used for: Reports, BAPIs, Enhancements | Used for: Extensions, APIs, AI, Integrations |

---

## 🏗️ Architecture

- **Client-server principle**
- 3 layers:

### 1. Presentation Layer
- Where users interact (SAP GUI, browser, Fiori)

### 2. Application Layer
- The brain: runs ABAP/Java programs
- Includes:

#### Dispatcher
- Someone who assigns work
- Like a **traffic controller** in the SAP application server
- It receives user requests and distributes them to **available work processes**

#### Work Processes
- A **worker** that does the actual job — runs ABAP code, updates DB, creates reports, etc.
- Types:

| Type         | What it does                          |
|--------------|---------------------------------------|
| Dialog (D)   | Handles user requests                 |
| Update (U)   | Does updates to the database          |
| Background (B) | Runs scheduled jobs                |
| Enqueue (E)  | Manages locking of data (to avoid conflicts) |
| Spool (S)    | Manages printing tasks                |

### 3. Database Layer
- Stores the actual business data
- RDBMS (Relational Database Management System)

---

## 🔄 Layer Deployment

- Layers can be on the **same system** or on **different systems**, depending on the setup:
  - In **basic setup**, App + DB are often on the **same server**
  - In **larger setups**, they’re on **different servers** for performance and security

---

## 🚀 Process of ABAP Program Execution

### Example: A program where user enters Airline ID and sees airline details

1. User logs into system → screen is displayed
2. User enters data and presses enter/clicks button
3. System loads the program on the **application server**
4. Runtime system gets program from **repository**
5. The program runs (may consist of **modularized units**)
6. Additional input/validation/logic is processed
7. Required data is fetched from the **database** using reusable programs
8. Data is placed into a **data object** (usually a structure)
9. The data is then **formatted into a list** and displayed to the user

---
