# Fushidara KO Android — 1.05.9 mobile r5

Extract `Fushidara_KO_A33_v1.05.9_r5.zip` and update the installed APK. App ID/signing certificate are unchanged; version code is 1050905.

Fix MOD stats and relationship synchronization:
- Numeric fields and relationship selectors continuously show current game state, including a focused numeric field when no text edit is pending. Display refresh never writes values or creates locks.
- Temporary MOD holds are scoped to one State instance and reset before processing a different save/new game.
- Explicit MOD holds on affection, mood, development, relationships and supported character stats use the native game's stat locks. The game's existing individual/unlock-all controls are authoritative; MOD never restores old held values after unlocking.
- No duplicate unlock-all button was added. Deliberate locks stored in a save are preserved on load and can be released using the original game controls.
- Unconfigured growth modifiers now match the original game's neutral defaults instead of silently using 0.1 multipliers. Explicitly saved custom modifiers are preserved.

Validation: an actual conversation changed affection 39→41 and relation stranger→friend; MOD numeric and relationship fields updated immediately. Tests covered cross-save isolation, focused-but-unedited fields, manual edits without holds, explicit holds, existing native unlock-all, unlocked save/load persistence and settings reset/import. Existing 16:9/UI and all 88 expression previews/locks/save-load regression tests passed. APK signatures/alignment/assets and release-runtime startup verified. Physical Galaxy A33 testing has not been performed.

The expression selector, heart-eye preference, original 1280×720 / 16:9 canvas, settings MOD entry and Android immersive fullscreen remain available. ARM64 Android 7.0+ / Godot 4.7.2 / OpenGL compatibility. Existing saves are not deleted.

Actual ZIP content uses Git LFS due to the 100 MiB ordinary Git blob limit; SHA-256 is in `SHA256SUMS`. Earlier releases remain on separate version branches.
