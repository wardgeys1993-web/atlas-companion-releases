# Atlas Companion 0.19.7, Atlas Engine 0.31.0

The Qwen3-Next native chat template uses compact JSON formatting for tool definitions. Tool names, descriptions, argument schemas, validation and approval controls remain in place. The shorter prompt reduces the amount of first preparation; the model still sees a changed token sequence and behavior can vary by request.

For explicitly requested directory listing, file search and file reading, the native 80B selects the requested built-in read-only tool while preserving the normal validation and permission checks.

Previously prepared prefixes are validated against the new engine identity and may need rebuilding. Startup and generation speed depend on the model, prompt, hardware and cache state. Existing Qwen, Gemma and managed inference paths remain available. Android receives matching release metadata. Scoped tests do not establish full-product or physical-device verification.
