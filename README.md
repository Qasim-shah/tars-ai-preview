# Tars AI — original AI on your Mac

![Tars AI research preview](https://tarsailab.com/social/tars-preview.png)

An experimental **28.3M-parameter language model trained from scratch on a 16 GB M4 Mac mini**. Original Tars weights, an original BPE tokenizer, and local inference through Apple MLX. There is no pretrained-model or hosted-model fallback.

**[Try the free Mac preview](https://tarsailab.com/#download)** · [Launch notes and share kit](https://tarsailab.com/share) · [Report a reproducible result](https://github.com/Qasim-shah/tars-ai-preview/issues/new)

## What exists today

- Free research preview 0.7.1 for Apple Silicon Macs.
- 28,320,256 parameters, an 8,192-token original vocabulary and a 1,024-token context.
- Chat history stays in the downloaded app's local folder.
- First setup downloads a private Python/MLX runtime and 113 MB of checksum-verified weights. Generation then works offline.
- No account or subscription is required for the free preview.

This project uses AI-assisted development. The model itself is trained locally from original weights, rather than wrapping a downloaded pretrained assistant.

## Try it

1. Download and unzip the preview from [tarsailab.com](https://tarsailab.com/#download).
2. Open `Setup.command` with internet available for the first setup.
3. Open `Start.command`, use `localhost:8421`, and keep its Terminal window open.

Tested on Apple M4 with 16 GB memory and macOS 26.2. This is an unsigned developer preview. Intel Macs and iPhone-only inference are not supported. Model parts in this repository's release are data for the installer; use `Setup.command` to assemble and verify them.

## What it cannot reliably do yet

It makes mistakes, can lose conversation context and can repeat itself. Autonomous tools are disabled. Personality controls are not reliably followed. It is not a production agent or a substitute for a capable general assistant.

The released checkpoint scored 3/40 on reserved repair math, 10/40 on repair reasoning, and 15/40 on experimental tool tasks. A separate restricted short-function suite scored 32/32; that does not establish general coding ability. The website documents these limits alongside a recorded local example.

## What is next

Current model work targets remembering a previous result, handling corrections and following a second math instruction while checking previous math, reasoning, coding and tool-use performance. New candidates are reviewed before replacing the active weights; training loss alone is not a release criterion.

Tars AI Personal v1 is planned at **$29 once** with permanent offline licensing and a native workbench. **Paid checkout is closed** while that release is prepared. Those native workbench features are separate from the current free preview.

## Help improve it

Please include the preview version, Mac chip/memory, exact prompt, actual response and expected behavior in a [public issue](https://github.com/Qasim-shah/tars-ai-preview/issues/new). Remove private information first. Setup reports, repetitive follow-ups and reproducible failures are especially useful.

Released weights SHA-256: `4adc197e70ac6f18056f26c2d9900f5b9e9b7cf8604fa925abce0d9bab6f1e42`. [Download checksums](https://tarsailab.com/releases/0.7.1-preview/SHA256SUMS.txt).
