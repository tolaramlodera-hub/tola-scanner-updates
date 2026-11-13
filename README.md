# Tola Scanner Android Updates

This public repository hosts the update feed and release APKs for the Tola Scanner Android app.

## Update feed

The app will check:
`https://raw.githubusercontent.com/tolaramlodera-hub/tola-scanner-updates/main/latest.json`

When publishing a new Android build:
1. Create a GitHub Release in this repository.
2. Attach the signed APK as `tola-scanner.apk`.
3. Update `latest.json` with the new version, version code, release notes, and APK download URL.
4. Keep the same Android signing key for every future release. Never commit the keystore or passwords here.

## Signing requirement

Android accepts an in-place update only when the new APK is signed with the same certificate as the installed app. The first debug APK was built by CI using a runner-generated debug key, so it cannot be guaranteed to accept future releases signed with a permanent key. A one-time uninstall/reinstall may be required when switching to permanent release signing.
