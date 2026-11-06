DYNATRACE ALERT TRACKER - NO LOGIN VERSION

This version has NO login page, no username/password authentication, and no superuser setup.
The “Entered By” value is typed manually while adding or editing an alert.

Run on Windows:
1. Extract this ZIP.
2. Open Command Prompt in the extracted folder.
3. Run these commands:

   py -m venv .venv
   .venv\Scripts\activate
   python -m pip install -r requirements.txt
   python manage.py migrate
   python manage.py runserver

4. Open http://127.0.0.1:8000/

Features:
- Black-and-white dashboard
- Separate Add Alert page
- Saves and returns to Alert Records table
- Date, Alert Name, Triggered Time, Tower, Update, Status, Entered By
- Tower choices: Linux, Windows, Network, Tools, Other
- Selecting Other shows a field for the tower name
- Edit and Delete for each record
- SQLite database stored locally in db.sqlite3

Important:
This is for local testing. Without login, anyone who can access the running site can view,
add, edit, or delete records. For 20 team members to share records, deploy centrally using
company-approved hosting and a shared database, and add suitable access controls.
