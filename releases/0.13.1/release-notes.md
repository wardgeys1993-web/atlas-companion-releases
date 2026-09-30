# Atlas Companion 0.13.1

## What changed

Pocket Tools now displays saved Studio tools on Android phones where the player previously opened as a dark screen. On the tested OnePlus 15 running Android 16, the tool's native header and Close button were also hidden behind the WebView layer.

The player now replaces the library dialog when a tool opens, creates its WebView in the player window, and uses software compositing for that WebView. The trusted host sizes the sandboxed tool frame from the measured viewport and updates that height on resize. The network block, opaque frame, content security policy, denied device permissions, bounded state messages and encrypted phone storage remain in place.

The desktop companion has no behavior change in this patch. Its signed archive carries aligned 0.13.1 source and documentation.

## Verification

The Android unit tests and lint pass, and the debug APK builds with version code 22. A device regression test on the OnePlus checks both that the embedded frame has a nonzero height and that its content paints visible pixels. The actual paired flow was also exercised: a generic shot-list tool was created in desktop Studio, shared with the phone, downloaded into Pocket Tools, opened, edited from Pending to Filming, closed and reopened. The phone retained that edit. No personal memories or private notes were used for this test.

The phone was updated in place with the same signing certificate. Its existing app data was not cleared. The APK and signed desktop archive are checked against the attached manifests before publication. The source snapshot is independently audited for local data, credentials and identifying content.

The fixed offline player can open a saved copy without contacting the desktop by design. A physical test with the PC powered off has not been completed. Alarm loudness, lock-screen behavior, microphone performance and stereo balance still need separate hardware checks.

## Update path

Android 0.13.1 has version code 22 and uses the same signing certificate as 0.13.0. The paired desktop's private phone update channel and the public GitHub release both offer the immutable APK by hash. Existing Pocket Tools copies remain independent of any newer desktop copy. The desktop archive is signed and intended for an existing Atlas installation; a clean developer setup starts from the public source.
