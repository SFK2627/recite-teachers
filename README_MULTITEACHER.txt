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

Notes:
- Teacher pages require Firebase Auth login.
- Public leaderboard does not require login.
- Student data does not mix across teachers.
