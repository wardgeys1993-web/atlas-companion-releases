# Atlas Companion 0.19.4, Atlas Engine 0.28.0

Scoped actual Companion checks passed normal A/B/A activation, model-specific cache hits, different calculator requests, exact approved file creation/readback, declined writes and saved-role restoration. Qwen 9B, Gemma, Qwen3-Next 80B and the independent managed fallback also passed preservation checks.

Prepared system and tool prompt states are stored in separate entries keyed by their full validated model, prompt and runtime identity. Qwen3.6 and the original Qwen3.5 35B can retain their own prepared states instead of replacing one architecture-wide cache slot. First preparation is still required, and incompatible or damaged cache entries rebuild through normal prompt processing.

A shared eight GiB and eight-entry disk limit bounds stored prepared-prefix caches, with least-recently-used eviction and process-safe maintenance. Full model identity, file hash and tensor validation remain in force. Inference precision, context and tool permissions are unchanged.

Native model activation uses the existing lazy backend factory, avoiding unnecessary model-framework imports in the UI host. Remotely resolved approval requests are also removed from the pending approval queue.

Existing Qwen, Gemma and managed inference fallback remain available. Release transfers give each artifact its own existing command deadline, preventing a large combined upload from consuming the entire transfer window. Android receives matching release metadata with no new phone features.

Full model loading is still required when switching, and first prompt preparation remains expensive. The app checks establish functional API, DOM, Composer, native window-state and filesystem behavior. Pixel capture was unavailable, so no visual acceptance claim is made.
