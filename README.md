# Fushidara KO Android — 1.05.9 mobile r4

Extract `Fushidara_KO_A33_v1.05.9_r4.zip` and install the APK as an update over the previous build. Package ID and signing certificate are unchanged; version code is 1050904.

Open game Settings → MOD panel → 표정 (Expressions):
- Toggle off automatic heart eyes caused by development, without changing development statistics or gameplay rules. Original automatic behavior is the default.
- Select any of the four characters and choose from 22 actual face-image previews to lock that character's standing portrait and face icons.
- Fixed selections take priority over reactions, sleep/hypnosis expressions and blinking. Manually selecting heart eyes is still allowed when automatic heart eyes are blocked.
- Return one character or all characters to automatic expressions. The independent automatic-heart blocking setting is preserved by resetting fixed faces.
- Choices are stored in normal saved-game state and survive save/load.

Validation: all 88 thumbnails exist and are distinct (22 per character); all 88 fixed-expression choices, automatic resets, heart blocking, unchanged game statistics, blink locking, actual State save/load, original 16:9 canvas, repeated MOD open/close and Android Back tests passed. Release runtime startup, APK signatures, alignment and all packaged assets were verified. Physical Galaxy A33 testing has not been performed.

The 1280×720 / 16:9 canvas and Android immersive fullscreen fixes from r3 are retained. ARM64 Android 7.0+ / Godot 4.7.2 / OpenGL compatibility. This update does not delete saved games.

Actual ZIP content is uploaded using Git LFS due to the 100 MiB normal Git file limit. SHA-256 is in `SHA256SUMS`. Earlier releases remain on their separate version branches.
