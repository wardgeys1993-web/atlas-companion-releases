# Atlas Companion 0.19.2, Atlas Engine 0.26.0

Qwen3.5 35B A3B generates tokens faster through exact-order wide compressed
expert reads and a larger expert cache sized at model loading. The cache keeps
the existing memory reserve. Model precision and context capacity are retained.

A bounded Companion comparison improved median generation from 17.4 to 26.4
tokens per second, about 52 percent. Two controls and two ordinary candidate
runs retained every generated token. The test used a 27,804-token stable prefix,
a fixed 32-token greedy continuation and three measured repeats per run.
Sampling is included; prompt processing and loading are excluded. Background
activity was present. Other workloads and hardware will vary.

Gemma uses compiler-free attention setup and layer-major prompt preparation.
An alternating trained-model comparison reduced 8,192-token prompt preparation
from 17.22 to 10.41 seconds, with identical compared logits. This is component
preparation time. Cached Gemma readiness still varied around 13 to 17 seconds;
first source-cache preparation takes longer, and host completion outliers remain.

Fully specified tool requests can use focused model input while retaining the
original policy, complete tool catalog, argument checks, execution receipts and
action approval. Real calculator, approved file/readback, declined-write,
cancellation and recovery checks passed. Qwen 9B, Gemma and the independent
managed inference fallback passed separate app checks.

Startup remains sensitive to weight reads and background activity. The 35B
candidate's cached run took about 29 seconds in this session; initial source
preparation took longer. No broad startup improvement is claimed.

Android 0.19.2 carries matching release metadata. Physical voice and complete
product acceptance remain outside the verified scope.
