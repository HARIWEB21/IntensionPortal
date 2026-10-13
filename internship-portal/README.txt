INTERNHUB - COLLEGE INTERNSHIP PORTAL
=====================================

This version is designed to run in restricted PHP environments such as ByteXL
where mysqli/pdo_mysql may not be installed. It therefore uses a lightweight
JSON datastore in data/ and requires no database PHP extension.

FEATURES
- Student and Company registration/login
- Password hashing and session authentication
- Student profile + PDF resume upload (5 MB max)
- Internship search by keyword/location
- Internship application and duplicate protection
- Student application tracking
- Company internship publishing
- Open/Closed internship control
- Applicant status management
- Responsive modern UI

RUN
1. Extract the project.
2. Make sure the project parent folder and uploads/ folder are writable by PHP. The app creates a private `internhub_data/` folder automatically.
3. Start: php -S 0.0.0.0:8080 -t internship-portal
4. Open the ByteXL forwarded URL.
5. Register a Student and a Company account and test the workflow.

The original MySQL connection details remain in config/database.php for future
migration to MySQL, but this portable build does not call mysqli, mysqli_report,
or pdo_mysql, so the missing-extension 500 error is removed.
