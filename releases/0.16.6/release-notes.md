# Atlas Companion 0.16.6

Windows desktop companion and native Android app. Android versionCode: 31.

## Changes

Release preflight validates the bounded phone notes before creating immutable version tags.

The Android APK compresses its native libraries while retaining all four CPU architectures. Every debug assembly checks the resulting APK against the existing 100 MiB updater limit. The download limit and signing identity stay unchanged.

This release includes the development work since 0.15.0: shared encrypted memory and its Brain view, local voice options, desktop chat and companion improvements, and explicit phone speech-pack setup. Android repairs cover alarm scheduling across clock changes, duplicate alarm delivery, draft recovery, approval controls and photo review. The optional fidelity voice model now passes its correct checksum and can be selected.

## Known limitations and verification

Repeated Hey Atlas wake detection is not reliable on the tested phone. A temporary sensitivity trial reacted once but failed subsequent attempts; that temporary profile was restored. This release does not claim to fix standby. Default INT8 morning synthesis, live brief flows, photo answers after a desktop restart and remaining device variants need further verification. Full capability certification remains incomplete.

GitHub security and regression checks passed on the development source before release preparation. The release coordinator requires the full desktop gate, Android tests and lint, exact-source artifact builds, privacy scans and downloaded draft verification before publication. Checksums and release provenance bind each download to its source and test evidence.

No personal stores, pairing credentials, model weights or signing keys belong in the release. Existing update signatures and normal approval requirements remain in effect.
