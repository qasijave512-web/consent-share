SafeShare Media Upgrade

This version adds explicit, user-selected photo/video sharing.

SETUP
1. In Firebase Console, enable Storage (Build -> Storage).
2. For prototype testing, use the temporary/test rules Firebase provides.
3. Upload index.html to GitHub Pages, replacing the previous index.html.
4. Open SafeShare on the owner phone.
5. Create a pairing code.
6. Choose photos/videos with the file picker. Only the files the owner selects are uploaded.
7. Tap Upload selected media.
8. The paired viewer sees the shared photos/videos in the dashboard.

LIMITS
- This does NOT scan the whole gallery automatically.
- It does NOT access hidden files, private messages, passwords, other apps, camera, or microphone.
- Production use needs Firebase Authentication and strict Storage/Database rules so only the paired viewer can access the media.
- Prototype upload limit per selected file: 50 MB.
