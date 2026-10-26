# Atlas Companion 0.19.1, Atlas Engine 0.25.0

Gemma now groups resident compressed weights by layer, reuses decoded weights
without redundant transfers, and captures resident decode segments while
streaming other layers. Prompt processing can reuse bounded decoded layers.
Precision, context capacity and memory reserves remain unchanged.

A controlled development comparison with one GiB of GPU memory occupied reduced
prompt processing from 5.8 to 2.6 seconds and token forward steps from 286 to
210 milliseconds, with identical compared logits. These are component timings,
not general throughput guarantees. Actual Companion calculator requests took
5.9 to 6.7 seconds. Cached startup still varied around 14 to 19 seconds;
fresh model preparation takes longer.

Explicit supported tool requests now steer validated native tool openings while
the model supplies arguments. Calculator results require matching execution
receipts. Denied actions report the denial rather than claiming completion.
Qwen and the managed inference fallback passed separate runtime checks.

Windows Security controls expose existing Microsoft Defender protection status,
approved scans, signature updates, Windows update searches, and reviewed active
threat remediation. They use Windows permissions and retain action approval.
Read-only status and a harmless custom scan command were checked in Companion.
Actual malware removal, protection-setting changes and update searches were not
live tested. This is not a new antivirus driver or a complete third-party
vulnerability scanner. A completed command does not certify a clean computer.

Android 0.19.1 carries matching release metadata; no new Android behavior is
claimed. Existing model downloads, conversations, settings and pairing remain
separate from the public package. Physical voice and full-product acceptance
remain outside this release's verified scope.
