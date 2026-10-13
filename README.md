# InventoryTrack — Department Inventory & Student Item Issue Management

A responsive browser-based prototype for Problem Statement #5. It manages departmental inventory, individually tracked assets, registered students, issue/return transactions, 15-day due dates, renewals, overdue visibility, stock adjustments, and CSV reports.

## Run it
1. Open **index.html** in a modern browser, or enable GitHub Pages in **Settings → Pages** and choose the main branch / root.
2. The app starts with demonstration records (10 development boards, 20 USB cables, adapters, laptops and sample students).
3. Use the top-right selector to switch between **Coordinator view** and **Student view**.
4. Data is saved in this browser's localStorage. Use the browser on the same device/profile to see saved records.

## Implemented workflows
- Register students; issue items only to registered students.
- Track individually tagged assets separately from quantity-based reusable items.
- Check available stock before issue; prevent over-issuing and concurrent assignment of the same tagged asset.
- Calculate due date as issue date + 15 calendar days.
- Submit renewal requests; due date changes only after coordinator approval, by 15 days from the current due date.
- Record partial/full returns, receiving staff, date, condition, and notes.
- Show overdue records and upcoming due dates.
- Add inventory items, update locations/details, record stock adjustments and asset status/condition changes.
- Export inventory and issue-history CSV files; maintain an in-browser audit trail.

## Important prototype limitations
This is a **front-end demonstration**, not a production-secure multi-user system. It stores data locally in the browser, and the role selector is a demo switch—not authentication or authorization. Multiple users/devices will not share data. For real department use, connect a backend API and database, add secure login/role-based access control, server-side validation, backups, and tested concurrency handling. Do not enter sensitive student data into this prototype.

## Suggested production stack
- Frontend: this responsive HTML/CSS/JavaScript UI
- Backend: Python Flask or Node.js API
- Database: PostgreSQL / SQLite for a single-machine deployment
- Authentication: password hashing, secure sessions, coordinator/student roles
- Testing: due-date, stock concurrency, partial return, renewal approval, lost/damaged stock and audit-log tests

## Project
Repository: https://github.com/astha248-modi/codresevent
