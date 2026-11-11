# MeshChat reliability-fix candidate

This branch keeps the original `MeshChat.zip` intact and applies the reviewed source changes from `MeshChat-fixes.patch.gz.b64` during the GitHub Actions build.

## Build
The workflow at `.github/workflows/android-build.yml`:
1. Extracts the original source archive.
2. Applies the reliability patch.
3. Builds the Android debug APK.
4. Runs the pure-Kotlin core verification suite.
5. Publishes the APK as a workflow artifact.

## Important
The core verification suite has passed locally (73 checks). Android compilation and physical-device interoperability are still pending. Do not treat this candidate as production-ready until BLE, Wi-Fi Direct, file transfer, background calls, and lock-screen behavior are tested on at least two real Android phones.

The original `main` branch and original source archive are not modified by this candidate branch.
