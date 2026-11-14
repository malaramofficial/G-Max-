# G-Max — MeshChat

Native Android project for an offline-first, nearby messaging prototype.

- Android source project: [MeshChat.zip](./MeshChat.zip)
- Stack: Kotlin, Jetpack Compose, Material 3, Room, BLE GATT mesh, Wi-Fi Direct.
- The Android app is an experimental draft. Real-device BLE, Wi-Fi Direct, file transfer and voice-call behavior still require testing on at least two physical Android phones.

## Build

The project archive contains the Gradle Android project. Use JDK 17 and Gradle 8.9:

```sh
unzip MeshChat.zip
cd MeshChat
gradle assembleDebug testDebugUnitTest
bash core-verify/run.sh
```

GitHub Actions runs these checks on pushes and pull requests. Passing CI does not replace multi-device radio and call testing.
