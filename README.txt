SafeShare Real-Time Prototype

This package adds a Firebase Realtime Database connection to the two-phone demo.

SETUP
1. Create a Firebase project.
2. Add a Web App and copy its Firebase config.
3. Replace the placeholder firebaseConfig in index.html.
4. Create Realtime Database.
5. For initial testing only, you may use the included rules. They are NOT production-secure.
6. Deploy index.html to GitHub Pages.

FLOW
Owner -> creates 6-digit code -> selects approved sharing -> publishes.
Viewer -> enters code -> dashboard receives approved fields in real time.
Owner can revoke by deleting the pairing/share record.

IMPORTANT SECURITY
The included rules are deliberately simple for a prototype and allow public read/write.
Do NOT use them for real private data or production.
A production release needs Firebase Authentication, per-user authorization rules,
short-lived pairing tokens, rate limits, audit logs, encryption in transit, and
strict separation between owner and viewer permissions.

This prototype does not secretly access messages, passwords, other apps, camera/mic,
or unrestricted files.
