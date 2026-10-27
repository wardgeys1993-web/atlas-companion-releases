# Atlas Companion 0.19.5, Atlas Engine 0.29.0

Native Qwen3-Next token generation uses dedicated compressed Q3_K expert operations, with the existing arithmetic and generic execution fallback preserved. A bounded, lazily populated host cache reuses compressed expert data. Allocation retains the existing host-memory reserve; memory pressure and model unload explicitly release the cache. The GPU expert budget and context remain unchanged.

After complete model validation, large expert banks use bounded file reads while dense weights retain small read-only mappings. This avoids retaining the full expert-bank mapping during fresh prompt preparation. Exact expert bytes and compressed-operation outputs are checked independently.

Model-content validation overlaps initialization, and the inference worker delays tensor-library initialization until model loading needs it. Full model-byte validation and separate prepared-prefix identities remain in force. Prompt routing preserves the original assignment order while grouping it in one pass.

Incomplete expert uploads are discarded from the GPU cache after errors or cancellation, so a later request cannot reuse unfinished entries. Existing Qwen, Gemma and managed inference fallback paths remain available. Tool approvals and receipt checks are unchanged.

Warm generation gains depend on the prompt and expert-cache working set. First prompt preparation and initial requests remain more expensive. Android receives matching release metadata with no new phone features. Scoped app acceptance and release validation are recorded separately; no physical-device or full-product verification claim is made.
