# Atlas Companion 0.11.0: A companion you can count on

Android version 0.11.0, code 17.

This update focuses on keeping your work intact when you switch chats, lose a connection, or come back later.

## On your phone

- **Private drafts for every conversation.** Unsent text and attached photos stay with the correct chat and survive reopening the app. You can compose and use on-device dictation offline. Nothing is sent automatically.
- **A proper conversation library.** Search titles, rename chats, archive them, copy a transcript or delete the phone copy. Older encrypted transcripts that disappeared from the list are recovered where available. Deleting the phone copy does not delete the separate desktop context or memory.
- **Cleaner connection recovery.** A dropped connection ends an interrupted reply instead of leaving the chat busy. Atlas does not replay requests when it reconnects. Optional local diagnostics describe connection stages without exposing chats, network addresses or pairing credentials.
- **More dependable voice controls.** Quick Settings talk waits for the connection to be ready. Stop handling is improved when Atlas mentions the word during a longer reply. Physical microphone testing is still needed.
- **Updates that remain available offline.** An already downloaded APK stays available for review even if the next update check cannot reach the network.
- **More accessible approvals.** Approval prompts announce themselves and put keyboard focus on the safe default. Physical TalkBack validation remains pending.

## Companion and Atlas OS work in this development batch

The updated local desktop source adds individual phone pairing revocation, conversation management and memory correction. It also tightens Stop and late-approval handling, scheduled-action provenance, model context budgeting, coding repair review, encrypted storage, signed desktop ZIP updates and browser action isolation. A startup audio crash was also fixed by giving playback its own output stream and keeping native Stop/close calls on that stream's owning thread.

**The Android APK does not install these desktop changes. Restart the updated desktop Companion to load them.** Older shared phone pairings stay valid until you explicitly revoke them; new QR pairings receive separate credentials.

## Still being worked on

Adaptive YouTube caption capture and reliable automatic caption enabling are not included as completed fixes. Real OnePlus voice, background, accessibility and update-install checks remain separate from automated tests.

## Install

In Atlas, open **Companion > App update > Check now**. The app can download this release from GitHub away from home, then Android asks before installation. The APK retains the existing signing identity. You can also download the APK below.

## Verification

- Android APK: 62 automated tests passed; lint has zero errors and 31 warnings.
- Signing certificate matches 0.10.4. APK version, size and SHA-256 match the attached updater manifest.
- Desktop: 352 of 357 suites passed the broad run; all five affected legacy expectations passed after corrections, with additional pairing-revocation, gateway and browser-isolation regressions passing.
- Six additional audio/voice regression checks pass after the startup fix. The restarted desktop reports version 0.11.0 and brain ready over its authenticated gateway.
- Rendered compact and large-text layouts were inspected. Real OnePlus installation and hardware-dependent behavior still need confirmation.
