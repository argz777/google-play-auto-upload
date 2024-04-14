# google-play-auto-upload
Workflow that triggers upon push to master branch:
1. Cleans and Builds app APK and AAB
2. Signs APK / AAB
3. Uploads APK / AAB to Firebase App Distribution for testers
4. Uploads APK / AAB to Google Play Console for production

# Pre-requisite
1. Have a Google Play Console account
2. Keystore

# How to use
1. Create a workflow, and add this code `android.yml` to the workflow.
2. Add your the following to your Secrets and variables under `Settings` tab in your repository:
- `SERVICE_ACCOUNT_JSON` - service account from your google play console (Follow [this](https://github.com/r0adkll/upload-google-play?tab=readme-ov-file#configure-service-account) instruction)
- `SIGNING_KEY_ALIAS` - key alias of your keystore
- `SIGNING_KEY_PASSWORD` - key password of your keystore
- `SIGNING_KEY_STORE_BASE64` - generate this via [this](https://github.com/r0adkll/sign-android-release?tab=readme-ov-file#signingkeybase64) command
- `SIGNING_KEY_STORE_PATH` - path of your keystore
- `SIGNING_STORE_PASSWORD` - signing password of your keystore
- `FIREBASE_APP_ID` - App ID found in your Firebase Console > Project Settings > Your Apps. E.g.: `1:1234567890123942955466829:android:1234567890abc123abc123`
- `CREDENTIAL_FILE_CONTENT` - service account from your google play console (Follow [this](https://github.com/wzieba/Firebase-Distribution-Github-Action?tab=readme-ov-file#servicecredentialsfilecontent) instruction)

2. Make sure to read through:
- [r0adkll/upload-google-play](https://github.com/r0adkll/upload-google-play) repository for reference
- [r0adkll/sign-android-release](https://github.com/r0adkll/sign-android-release) repository for reference
- [wzieba/Firebase-Distribution-Github-Action](https://github.com/wzieba/Firebase-Distribution-Github-Action) repository for reference
