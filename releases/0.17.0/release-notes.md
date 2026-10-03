# Atlas Companion 0.17.0: Nocturne and Raevin

Windows desktop companion and native Android app. Android versionCode: 32.

## Changes

Nocturne introduces obsidian surfaces, silver typography and restrained blue light across desktop chat, the full workspace, Build Studio, memory, model setup and quick commands. Android carries the same direction through Chat, Projects, Home and Signals, with refined pairing, memory, libraries, launcher, widget and alarm screens.

Raevin is a natural charcoal raven with blue wing particles. Its 32 authored gestures continuously interpolate independent head, wings, body and eyelids, including blended interruptions and blinking. Desktop Canvas and native Android Compose use the same motion data. Reduced motion, Android lifecycle and battery-saving behavior remain supported.

The release checks also caught and repaired greeting/outcome gesture handling, immediate pose changes when interrupting a gesture, and clipped workspace controls at small window sizes. The full release gate now includes the Nocturne shell and shared raven motion suites.

Existing package and protocol identifiers, pairing and the Hey Atlas wake phrase are retained, so this remains an update to the existing app.

## Verification and known limitations

The implementation passed six targeted desktop suites, all 145 Android unit tests, debug assembly and lint before release preparation. An isolated normal Qt preview measured approximately 60 frames per second. Physical-phone frame pacing and hardware acceptance remain unverified. Raven gestures are perched motions, without flight or beak lip sync.

Repeated Hey Atlas wake detection remains experimental and unreliable on the tested phone. This visual release does not claim to fix wake-word recall. Outstanding real-device voice, briefing and photo journeys still require acceptance.

The release coordinator requires the full desktop gate, Android unit tests and lint, secret and payload privacy scans, builds from the exact source tag, signing identity and version checks, and downloaded draft verification before publication. SHA256SUMS.txt and release-provenance.json identify the exact files and source commit.
