# Atlas Companion 0.15.0

## Shared conversations

Desktop and paired Android chats use one DPAPI-sealed desktop archive. Android keeps an encrypted local cache for offline access. Phone sessions use UUID aliases, bounded message pages and deletion tombstones so a stale phone cannot recreate a conversation removed on the desktop. A quiet editor records concise notes from older conversations while preserving the original turns.

## Approved desktop actions

Atlas can enter a Windows Search query and invoke one exact accessible result. It can inspect and activate named controls in one selected application window. When an app exposes no usable accessibility action, a local OCR pass can identify one unique visible text target and click it after checking focus, window geometry and hit ownership again. Screen text remains untrusted, and each action requires approval. File writes and web actions keep their existing separate guards.

## Phone web access

A paired phone can request one web search without first using the desktop chat. Approval is returned to that same phone and grants outbound access only for its current worker thread. A separate `/web on` request needs approval and remains active until `/web off`. Other phone commands retain guest restrictions.

## Local image assets

For a confirmed website build, Atlas plans up to two images with the source files. A smaller local model drafts the image prompts, the main model releases GPU memory, and a temporary loopback Ming Image runtime renders the assets. Atlas restores the main model before building the site. The runtime is optional and its files stay outside the source tree. One direct 1024 by 1024 render on a 12 GiB RTX 3060 completed in 462.7 seconds; the output was visually inspected and contained no PNG prompt metadata.

## Windows first install

The Atlas-branded `AtlasSetup-0.15.0.exe` gives first-time users a single starting point. It verifies the signed desktop archive, checks for x64 Python 3.12 and a working llama.cpp runtime, downloads missing pinned components from their official sources with integrity checks, creates the locked Python environment, and installs the floating Companion with shortcuts. The model remains a separate, explicit first-run choice. Existing working runtimes, models and private data are preserved when setup is rerun. See the [installer guide](INSTALLER.md) for the exact bootstrap and verification scope.

## Verification

The desktop deterministic suite passed 374 of 374 tests with Atlas closed. Android passed 98 unit tests, lint and debug assembly. Live desktop checks selected a Windows Search result, activated Calculator controls and clicked a classic Notepad menu through OCR. The frozen Windows setup installed a fresh isolated copy with a new locked Python environment and verified CPU llama.cpp runtime. Its launcher opened the floating Companion from a per-user application folder, where the first-run model chooser rendered and detected the local GPU, memory and disk space. The official CUDA runtime was also downloaded, verified and started on an RTX 3060. A clean Windows machine without Python has not been physically tested. The phone web approval path has automated tests; a physical-device check is separate from these results.
