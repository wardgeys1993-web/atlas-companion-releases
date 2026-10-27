# Atlas Companion 0.19.6, Atlas Engine 0.30.0

Qwen3-Next can reuse the existing bounded host expert cache for selected short prompt transfers. Longer requests and unavailable cache paths use the existing staged transfers. Memory limits and pressure handling remain in place.

For an explicit write and read, native 80B can avoid a redundant model answer check only when the built-in tool results and file evidence prove the exact final answer. Approvals, denied actions and uncertain results keep the normal checks.

Existing Qwen, Gemma and managed inference paths remain available. Startup and latency vary with cached state, request and hardware. Android receives matching release metadata. Scoped tests do not establish full-product or physical-device verification.
