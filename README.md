# S26 Stretch Probe – prototype

This project is a safe, non-root Android `SurfaceControl.Transaction.setScale()` test. It changes **only its own SurfaceView**. It does **not** modify COD Mobile and cannot prove cross-app control.

## Build

Push these project files to a GitHub repository and run the provided Actions workflow. Download the `S26StretchProbe-debug-apk` artifact after successful completion. Alternatively use Android Studio/Gradle with SDK 35 and `gradle :app:assembleDebug`.

## Test

1. Install APK, open it, tap `Eigene Surface horizontal 1,5x skalieren`.
2. Observe the blue test rectangle; the SurfaceView implementation may reset the transformation.
3. Tap `Skalierung zurücksetzen` to restore scale 1x1.

## Limitations

No Shizuku integration is implemented in this first prototype: a Shizuku shell does not automatically grant a valid foreign SurfaceControl handle. The COD check button explains this limitation; it does not claim to perform a privileged access test. No modification to game graphics, input or window settings occurs.
