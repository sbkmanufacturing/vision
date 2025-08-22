# SBK Vision - Firebase Setup

## IMPORTANT: How to Fix Firestore Permission Errors

You are seeing "Missing or insufficient permissions" because your Firestore database is locked down by default. To fix this, you need to update your Firestore security rules in the Firebase Console.

Follow these steps carefully:

1.  **Open the `firestore.rules` file** located in the root directory of this project.
2.  **Copy the entire content** of that file.
3.  Go to the **[Firebase Console](https://console.firebase.google.com/)** and select your project (`sbk-vision`).
4.  In the left-hand navigation menu, under the "Build" section, click on **Firestore Database**.
5.  At the top of the Firestore Database page, click on the **"Rules"** tab.
6.  You will see an editor with the default rules. **Delete all the text** in the editor.
7.  **Paste the rules** you copied from the `firestore.rules` file into the editor.
8.  Click the **"Publish"** button.

Once you publish these new rules, the permission errors in your application will be resolved, and all data-saving features will work correctly. These rules allow any user who is logged in to read and write data, which is suitable for development.
