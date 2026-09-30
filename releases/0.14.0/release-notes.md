# Atlas Companion 0.14.0

## What changed

The floating Windows companion and native Android app now share the original amber Atlas identity. The chest mark and triangular frame recur in the interface while chat keeps its compact layout. On the tested owner's PC, Quiet visuals removes the heavy idle flicker and still permits deliberate movement across both displays.

Desktop Free Roam can use the visible Screen Sense opt-in to build a coarse, transient map of text-like edges and motion. Atlas chooses quieter positions, can edge-dock beside active video, and can be dragged and parked on either screen. The map is a placement aid, not semantic video understanding. The scan sends no captured pixels, OCR text or window titles to the companion page or model. Turning Screen Sense off stops its sampling.

The companion adds **Choose your brain** for a local CPU, memory, GPU and disk scan, a curated model recommendation, explicit network consent, verified download and healthy-load activation. Existing installations can open it from Settings. It still requires a compatible Windows llama.cpp runtime and Python environment. This release does not bundle models or claim support for every GPU.

Studio gains eight scoped operating-assistant workflows. It can guide the owner to one named Windows control and request approval for one accessible button press; run a selected project-local Python test after an engineering mission and allow one repair pass; watch one chosen output for a stable write; accept an owner correction between plan steps; compare project files with a prior checkpoint; use bounded local OBS and fixed-recipe Blender adapters; offer an expiring conversation excerpt to a paired phone; and publish explicitly selected text files as an encrypted offline Pocket Project. Phone notes and up to two small photos return only to a sealed desktop review inbox. Import requires owner approval and creates new files rather than overwriting source files.

The existing Android alarms, timers, private notes and Pocket Tools remain available offline. The phone is still a guest of the desktop: paired TLS, certificate pinning, scoped credentials, taint handling and approval rules remain in force. The Android app does not gain a general computer-control bridge.

## Verification and limits

The final 0.14.0 desktop candidate passed all 368 deterministic suites with Atlas closed. Android passed 96 unit tests, lint with zero errors and 31 warnings, and the debug APK build. The APK reports version 0.14.0, code 23, and the same signing certificate as the installed app. It installed over 0.13.1 on a OnePlus without changing the original install date, launched its release journal and home screen, and passed the physical Pocket Tool viewport rendering test. The source export contained 1,031 files and passed both the private-data audit and Gitleaks with zero findings. A live WPF fixture confirmed named-control discovery, and a local Blender 4.1 run produced a valid scene and decoded PNG.

The signed desktop archive and published asset hashes must be verified before publication. A test result is not a claim that the new phone handoff, offline project return, OBS recording or one-button press has been accepted on physical hardware. The button press stopped safely when Windows refused unattended foreground activation. Alarm volume, lock-screen behavior, voice interruption and stereo balance still need hands-on checks. The PC starter still cannot wake a Wi-Fi-only computer from sleep or power-off.

## Update path

Android 0.14.0 uses version code 23. It must keep the installed signing certificate and preserve app data. The desktop update archive must be signed from an audited, history-free source snapshot. The release assets and both update manifests must be checked against their exact byte hashes after publication. A new developer setup starts from source and must provide the compatible runtime and model dependencies described in [Choose your brain](BRAIN_SETUP.md).
