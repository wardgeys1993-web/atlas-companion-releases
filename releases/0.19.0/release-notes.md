# Atlas app 0.19.0, Atlas Engine 0.24.0

Atlas Engine 0.24 adds native text and tool execution for Qwen3.5 9B,
Gemma 4 12B and Qwen3.5 35B A3B. Managed inference remains available as fallback.
Model weights are separate downloads.

The 35B runtime now selects and caches compressed experts on the GPU. A bounded
32-step greedy development test improved by about 48 percent with matching
generated token IDs. This is not a guarantee for every prompt or hardware
configuration. Actual model-selected tools still take about
8 to 13 seconds. Cached startup varies with memory and file-cache conditions;
fresh source-prefix preparation takes longer. Precision and 32K context remain.

Atlas now keeps a Windows taskbar entry when minimized. Native restoration
keeps the same model instance. The notification-area controls remain available,
and application Quit exits normally. Forced monitor placement is removed.

Exact calculator and file commands remain available while a large model loads.
Approved writes, independent readbacks, denied writes and Stop/recovery were
checked in the actual desktop app. Qwen 9B, Gemma and the managed fallback
were checked separately.

Android includes optional home Wi-Fi welcomes, secure delivery of fresh arrivals
and wake-phrase punctuation fixes. Existing pairing and saved conversations are
preserved. Device permission, alarm and background behavior still need field
validation; this release does not claim full-product or physical-device acceptance.

The installer and signed update include the native Python/CUDA runtime and
managed integration helpers. Personal stores, keys, models and environments are
excluded. See the bundled engine timeline for the earlier development milestones.
