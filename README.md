# Boarding House Payment Monitoring System

A console-based payment monitoring and room management system written in Python.  
It supports **Admin** and **Tenant** portals with features such as room tracking, bill generation, GCash and cash payment submissions, verification workflows, and JSON data persistence.

---

## Features

### Admin Portal
* **Room Management:** View room capacities, occupancy status, and monthly rent details.
* **Tenant Management:** Create and delete tenant accounts, and view registered tenant lists.
* **Billing Operations:** Generate or update bills across categories (*Monthly Rent*, *Electricity*, *Water*) with due-date validation.
* **Payment Verification:** Review pending tenant payment submissions, approve/reject transactions, and record GCash reference numbers.
* **System Settings:** View administrator GCash details.

### Tenant Portal
* **My Bills & Balances:** View individual bill categories, amounts paid, remaining balances, due dates, and payment statuses.
* **Payment Submission:** Submit payments via **Cash** or **GCash** with reference number checking and pending status prevention.
* **Payment History:** Access a full record of approved payment receipts.
* **GCash Reference:** View official GCash payment details.

---

## System Credentials

### Admin Login
* **Username:** `admin`
* **Password:** `admin123`

### Default GCash Details
* **Account Name:** Boarding House Admin
* **GCash Number:** `0951-538-6038`

---

## Room Configuration & Billing Categories

### Default Rooms
Room | Monthly Rent | Capacity
--- | --- | ---
**R101** | PHP 2,500.00 | 1 Slot
**R102** | PHP 2,500.00 | 1 Slot
**R201** | PHP 3,000.00 | 1 Slot
**R202** | PHP 3,000.00 | 1 Slot

### Bill Categories
* Monthly Rent
* Electricity
* Water

---

## Installation & Execution

### Prerequisites
* Python 3.x installed on your computer.

### How to Run
1. Save the source code as a `.py` file (e.g., `boarding_house.py`).
2. Open your terminal or command prompt.
3. Run the application:

```bash
python boarding_house.py

or

python3 boarding_house.py

Key Technical Behaviors
1. JSON Data Persistence: Automatically loads and saves state (boarding_house_data.json) for rooms, tenants, bills, submissions, and records.
2. Input & Date Validation: Ensures due dates are in YYYY-MM-DD format and prevents setting past dates.
3. Duplicate GCash Reference Check: Rejects recycled or already-submitted GCash reference numbers.
4. Pending Payment Guard: Prevents tenants from submitting multiple pending payments for the same bill category while awaiting admin approval.
5. Formatted Table Display: Built-in dynamic column alignment for clean terminal interface rendering.

File Structure
.
├── boarding_house.py          # Main Python program code
└── boarding_house_data.json   # Auto-generated JSON database file

Author
Created as a student project for boarding house management simulation.

Feel free to fork, customize, or integrate with a database or Web GUI!
