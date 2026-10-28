# Fushidara KO Android — 1.05.9 mobile r3

Extract `Fushidara_KO_A33_v1.05.9_r3.zip` and install the APK. Package ID and signing certificate match r1/r2; version code 1050903 allows an update installation.

Fix Android system bars reappearing after launch: the original desktop window preference called `window_set_mode(WINDOW_MODE_WINDOWED)`, which disables immersive mode on Android. On Android the game now applies fullscreen instead and reapplies it on application focus/resume. Export explicitly sets `screen/immersive_mode=true` and `screen/edge_to_edge=false`; the actual APK startup arguments include `--fullscreen` and omit `--edge_to_edge`.

The original 1280×720 / 16:9 canvas, letterboxing, MOD entry in game settings, MOD Close button and Android Back handling remain. Swiping from a screen edge can temporarily show Android system bars, as expected for immersive mode. This update does not delete saved games.

Validation: all packaged assets, APK signatures and alignment verified; four screen dimensions, four repeated settings-to-MOD open/close cycles and Android Back regression tests passed. Release-runtime startup passed. Physical Galaxy A33 testing has not been performed.

ARM64 Android 7.0+; Godot 4.7.2; OpenGL compatibility. Actual ZIP contents are uploaded using Git LFS due to the 100 MiB ordinary Git blob limit. SHA-256 is in `SHA256SUMS`. Each version has a separate branch.
