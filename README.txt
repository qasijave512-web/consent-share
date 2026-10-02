SafeShare P2P Media Upgrade

This version avoids Firebase Storage. Firebase Realtime Database is used only for temporary pairing and WebRTC signaling. Selected photos/videos are transferred directly between the two browsers using WebRTC DataChannel.

GITHUB
1. Replace index.html in the GitHub Pages repository.
2. Replace database.rules.json in the repository.
3. Commit changes.
4. If you have an installed PWA, refresh it. If it keeps showing the old UI, close it and reopen the GitHub Pages site in Chrome, or clear the site's cached data.

FIREBASE
In Realtime Database -> Rules, publish the rules from database.rules.json.
No Firebase Storage upgrade is required for this prototype.

TEST
OWNER PHONE
- Open SafeShare.
- Create pairing code.
- Give code to the viewer.
- Viewer enters code and connects.
- Wait for "Direct connection ready."
- Select specific photos/videos.
- Press Send selected media.

VIEWER PHONE
- Open SafeShare.
- Choose Viewer.
- Enter the code.
- Connect.
- Received media appears in the Photos & videos section.

LIMITS
- Media is not stored in Firebase; it exists in the viewer page memory while that page is open.
- Prototype max file size is 100 MB per file.
- Direct P2P may fail on some networks because no TURN server is included.
- Production use needs Firebase Authentication, strict per-user rules, a TURN service, expiration/revocation, and abuse protections.
- This app never scans an entire gallery or accesses private messages, passwords, other apps, hidden camera/microphone feeds, or files the owner did not select.
