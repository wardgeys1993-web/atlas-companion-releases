# Atlas Companion 0.19.3, Atlas Engine 0.27.0

Atlas Engine adds native text and tool support for Qwen3.6 35B A3B Abliterated V2 and experimental Qwen3-Next 80B A3B Thinking Abliterated. The new Next adapter supports its combined recurrent projections, Q3_K/BF16 compressed weights and official JSON tool protocol through the existing tensor runtime and bounded CUDA execution.

Both models passed actual Companion calculator, approved file creation and readback, declined-write, cancellation/recovery, Composer and clean-shutdown checks. Next honors the launcher's thinking setting and stops required tool generation only after validating a complete declared call. Its expert cache is bounded to preserve GPU headroom. The larger model's app tests used thinking disabled; broad reasoning quality and consistently low latency are not established.

Precise supplied-file requests retain normal approvals, schema validation and completion receipts. Host tool-schema caching reduces repeated path checks. Existing Qwen 9B, Qwen3.5 35B, Gemma and the independent managed inference fallback remain available.

Model files are separate downloads pinned to exact revisions and full SHA256 digests. Publisher modification labels do not guarantee quality or behavior. Android has matching release metadata with no new phone features.
