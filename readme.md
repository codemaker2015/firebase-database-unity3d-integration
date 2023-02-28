# Firebase Database Quickstart

The Firebase Database Unity Sample demonstrates
[Firebase Realtime Database](https://firebase.google.com/docs/database/)
with the [Firebase Unity SDK](https://firebase.google.com/docs/unity/setup)
inside the Unity Editor.

## Running the Sample inside the Editor

  - Download the
    [Firebase Unity SDK](https://firebase.google.com/download/unity)
    and unzip it somewhere convenient.
  - Open the sample project in the Unity editor.
    - Select the **File > Open Project** menu item.
    - If Unity Hub appears, click **Add**.  Otherwise click **Open**.
    - Navigate to the sample directory `testapp` in the file dialog and click
      **Open**.
      - You might be prompted to upgrade the project to your version of Unity.
        Click **Confirm** to upgrade the project and continue.
  - Open the scene `MainScene`.
    - Navigate to `Assets/Firebase/Sample/Database` in the **Project** window.
    - Double click on the `MainScene` file to open it.
  - Import the Firebase Database plugin.
    - Select the **Assets > Import Package > Custom Package** menu item.
    - From the [Firebase Unity SDK](https://firebase.google.com/download/unity)
      downloaded previously, import `FirebaseDatabase.unitypackage`.
    - When the **Import Unity Package** window appears, click the **Import**
      button.
  - Turn off secure access. 
    [Configure your rules for public access.](https://firebase.google.com/docs/database/security/quickstart#sample-rules)

  - Register your Android app with Firebase.
    - Create a Unity project in the
      [Firebase console](https://firebase.google.com/console/).
    - Associate your project to an app by clicking the **Add app** button,
      and selecting the **Unity** icon.
      - You should use `com.google.firebase.unity.database.testapp` as the
        **Android package name** while you're testing.
        - If you do not use the prescribed package name, you will need to update
          the bundle identifier as described in the
          **Optional: Update the Project Bundle Identifier** below.
      - Android apps must be signed by a key, and the key's signature must
        be registered to your project in the Firebase Console. To
        [generate a SHA1](https://developers.google.com/android/guides/client-auth),
        first you will need to set the keystore in the Unity project.
        - Locate the **Publishing Settings** under **Player Settings** in the
          Unity editor.
        - Select an existing keystore, or create a new keystore using the
          toggle.
        - Select an existing key, or create a new key using **Create a new
          key**.
        - After setting the keystore and key, you can generate a SHA1 by
          running this command:
          ```
          keytool -list -v -keystore <path_to_keystore> -alias <key_name>
          ```
        - Copy the SHA1 digest string into your clipboard.
        - Navigate to your Android App in your firebase console.
          - From the main console view, click on your Android App at the top and
            click the gear to open the settings page.
          - Scroll down to your apps at the bottom of the page and click on
            **Add Fingerprint**.
        - Paste the SHA1 digest of your key into the form.  The SHA1 box
          will illuminate if the string is valid.  If it's not valid, check
          that you have copied the entire SHA1 digest string.
    - Download the `google-services.json` file associated with your
        Firebase project from the console.
        This file identifies your Android app to the Firebase backend, and will
        need to be included in the sample later.
      - For further details please refer to the
        [general instructions](https://firebase.google.com/docs/android/setup)
        page which describes how to configure a Firebase application for
        Android.
  - Open the sample project in the Unity editor.
    - Select the **File > Open Project** menu item.
    - If Unity Hub appears, click **Add**. Otherwise click **Open**.
    - Navigate to the sample directory `testapp` in the file dialog and click
      **Open**.
      - You might be prompted to upgrade the project to your version of Unity.
        Click **Confirm** to upgrade the project and continue.
  - Open the scene `MainScene`.
    - Navigate to `Assets/Firebase/Sample/Database` in the **Project** window.
    - Double click on the `MainScene` file to open it.
      - You might be prompted to upgrade the project to your version of Unity.
        Click **Confirm** to upgrade the project and continue.
  - Import the Firebase Database plugin.
    - Select the **Assets > Import Package > Custom Package** menu item.
    - From the [Firebase Unity SDK](https://firebase.google.com/download/unity)
      downloaded previously, import `FirebaseDatabase.unitypackage`.
    - When the **Import Unity Package** window appears, click the **Import**
      button.
  - Add the `google-services.json` file to the project.
    - Navigate to the `Assets/Firebase/Sample/Database` folder in the
      **Project** window.
    - Drag the `google-services.json` downloaded from the Firebase console
      into the folder.
      - NOTE: `google-services.json` can be placed anywhere under the `Assets`
        folder.
  - Optional: Update the Project Bundle Identifier.
    - If you did not use `com.google.firebase.unity.database.testapp`
      as the **Android package name** when you created your app in the Firebase
      Console, you will need to update the sample's Bundle Identifier.
      - Select the **File > Build Settings** menu option.
      - Select **Android** in the **Platform** list.
      - Click **Player Settings**.
      - In the **Settings for Android** panel scroll down to
        **Bundle Identifier** and update the value to the Android package name
        you provided when you registered your app with Firebase.
  - Build for Android.
    - Select the **File > Build Settings** menu option.
    - Select **Android** in the **Platform** list.
    - Click **Switch Platform** to select **Android** as the target platform.
    - Wait for the spinner (compiling) icon to stop in the bottom right corner
      of the Unity status bar.
    - Click **Build and Run**.