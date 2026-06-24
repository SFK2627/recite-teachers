Recitation Central Multi-Teacher

Firebase project:
- recitation-central-mteacher

Upload all files in this ZIP directly to the root of the new GitHub repo.

Main URL:
- index.html redirects to mt-index.html
- Use the GitHub Pages URL of the new repo.

Required Firebase setup:
1. Authentication -> Sign-in method -> enable Email/Password.
2. Authentication -> Users -> Add teacher accounts.
3. Firestore Database -> create database.
4. Firestore Rules -> paste FIREBASE_RULES_MULTITEACHER.txt.

Data structure:
- teachers/{teacherUid}
- teachers/{teacherUid}/students
- teachers/{teacherUid}/sections
- teachers/{teacherUid}/recitationLogs

Pages:
- mt-index.html: teacher portal and viewer link generator
- mt-import.html: import students for signed-in teacher
- mt-admin.html: manage/export signed-in teacher data
- mt-scanner.html: record signed-in teacher recitations
- mt-view.html?teacher=TEACHER_UID: public leaderboard for a teacher

Student import columns:
- Student ID
- Full Name
- Section
- Gender

Gender notes:
- Use Male or Female.
- Gender is used in Export Totals XLSX so each section tab sorts Boys first, then Girls, then blank/unknown.

Export Totals:
- Downloads an XLSX file.
- Each section is placed on its own sheet/tab.
- Columns are Student ID, Full Name, Points, Gender, Latest Points, Latest Recitation.

Term calendar:
- Term 1: June 1 to September 9.
- Term 2: September 10 to December 15.
- Term 3: January 4 to April 3.
- Scanner records each scan with the current term and school year.
- Admin and public viewer can switch between Current Term, Term 1, Term 2, Term 3, and All Time.
- No need to delete old points when a new term starts.

Credits:
- Headers include: Developed by Mr. John Rey Tubello (Sir JR).

Notes:
- Teacher pages require Firebase Auth login.
- Public leaderboard does not require login.
- Student data does not mix across teachers.
