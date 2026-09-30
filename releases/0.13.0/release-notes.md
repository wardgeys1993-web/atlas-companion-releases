# Atlas Companion 0.13.0

## What changed

The `companion.local` Windows companion, launched in the compact floating form, now roams within the actual bounds of both displays. Its spoken output uses a small stereo bias based on the display where the companion is standing. The chat remains in the compact desktop surface. Android pairs to this running companion through the opt-in `--ear` listener.

Studio's **Pocket Tools** share action exports only a selected tool's HTML and JSON state. Paired Android devices can download an independent encrypted copy. Once downloaded, that copy runs and retains edits without the desktop or a model connection. Desktop refinements require a new explicit share action; the phone never silently replaces a saved copy. This is a portable small-tool workflow, not an autonomous app store or general website download feature.

Android can set a phone alarm or timer and create a private note after a matching phone-side approval. A scheduled alarm uses Android's alarm mechanism, then plays a bundled name-free Atlas voice line with a system tone and vibration. It offers Dismiss and a ten-minute Snooze. One-time is the default; daily, weekdays and selected days are supported. Exact-alarm permission may need enabling on Android 12 and later. The spoken line is fixed offline audio, not a live generated morning briefing.

The paired **Start Atlas on PC** action launches the desktop companion when Windows is awake and signed in but Atlas is closed. It authenticates against the saved phone identity and does not wake a sleeping or powered-off Wi-Fi PC. Local phone alarms, timers, notes and saved Pocket Tools remain available when the PC cannot be reached.

## Technical details

- The desktop owner publishes an explicitly chosen, bounded snapshot. Windows DPAPI seals it; the existing paired TLS channel serves an authenticated metadata list and an opaque-ID read endpoint.
- Android pins the desktop certificate and stores each selected phone copy under Android Keystore-backed AES-GCM. Generated HTML runs inside an opaque, restricted frame with bounded state exchange, no native action bridge, and no network or file access.
- Phone actions remain tied to the requesting paired session. Atlas waits for the device's approval and execution receipt before it reports success.
- Desktop update ZIPs are signed with Ed25519 and contain only audited application files. The APK keeps the installed debug signer and has a higher version code.

## Verification and limits

The full desktop deterministic gate passed **362 of 362 suites** with no unregistered tests before publication. The final Android build passed **88 unit tests** with no failures, `lintDebug` and `assembleDebug`. Earlier Pocket Tools changes passed 11 focused tests. Desktop Qt and Android Compose test previews were rendered and inspected. The production phone tool host also passed a Chromium sandbox test covering state restoration, message origin, network blocking and quota handling.

The public APK is **0.13.0, version code 21**. Its exact size, hash and signature are listed in the attached manifest and verified before release. The Android emulator on the release machine could not boot, so physical phone installation, alarm volume, lock-screen display, battery policy and the full PC-off Pocket Tools journey remain unverified. The desktop roaming and stereo effect were tested in simulated two-screen geometry; final speaker balance needs a human check.

The local model's generated tools vary in quality. A tool must use Atlas's supported state messages to preserve its edits. This release does not claim that every prompt yields a useful interface.
