# Fushidara KO Android — 1.05.9 mobile r2

Download `Fushidara_KO_A33_v1.05.9_r2.zip`, extract it, and install the APK inside. The package ID and signing certificate match r1, and the version code is increased to allow updating the installed app.

Changes:
- Preserve the original 1280×720 (16:9) game canvas with letterboxing instead of expanding to the device aspect ratio.
- Remove the disappearing floating F2/Esc/collapse toolbar.
- Add a permanent MOD panel entry in the game's settings footer.
- Add a touch Close button in the MOD panel; Android Back also closes it.

Validation: four screen dimensions retained a 1280×720 logical viewport; four repeated settings-to-MOD open/close cycles and Android Back handling passed. Release-runtime startup, APK signatures, alignment, and all packaged assets were verified. Physical Galaxy A33 testing has not been performed.

ARM64 Android 7.0+; Godot 4.7.2; OpenGL compatibility renderer. Existing saves are not deleted by this update.

The ZIP's actual content is stored in Git LFS due to GitHub's 100 MiB ordinary-file limit. `SHA256SUMS` records its SHA-256. This version has its own branch; r1 is preserved.
