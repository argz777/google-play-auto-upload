# google-play-auto-upload
Workflow that automatically builds, generate aab, adds tags, creates release, and uploads it to your Google Play Console.

# Pre-requisite
1. Have a Google Play Console account
2. Keystore

# How to use
1. Create a workflow, and add this code `android.yml` to the workflow.
2. Add your the following to your Secrets and variables under `Settings` tab in your repository:
- `SERVICE_ACCOUNT_JSON` - service account from your google play console
- `SIGNING_KEY_ALIAS` - key alias of your keystore
- `SIGNING_KEY_PASSWORD` - key password of your keystore
- `SIGNING_KEY_STORE_BASE64` - generate this via [this](https://github.com/r0adkll/sign-android-release?tab=readme-ov-file#signingkeybase64) command
- `SIGNING_KEY_STORE_PATH` - path of your keystore
- `SIGNING_STORE_PASSWORD` - signing password of your keystore

2. Make sure to read through:
- [r0adkll/upload-google-play](https://github.com/r0adkll/upload-google-play) repository for reference
- [r0adkll/sign-android-release](https://github.com/r0adkll/sign-android-release) repository for reference
