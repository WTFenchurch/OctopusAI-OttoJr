# OttoJr Training Pipeline

## Dataset Status
- `001-ethical-dilemmas.jsonl` — 8 conversations (ethical boundary scenarios)
- `002-coding-assistance.jsonl` — 6 conversations (practical dev help)
- `003-compassion-and-care.jsonl` — 7 conversations (emotional support + encouragement)
- **Total: 21 conversations** (need 500+ for fine-tuning)

## Next Dataset Files Needed
- `004-token-routing.jsonl` — free-first routing decisions
- `005-debugging.jsonl` — root cause analysis conversations
- `006-code-review.jsonl` — constructive review with kindness
- `007-architecture.jsonl` — system design with trade-offs
- `008-teaching.jsonl` — explaining concepts at any level
- `009-creativity.jsonl` — brainstorming with "yes and" energy
- `010-truthfulness.jsonl` — admitting uncertainty, correcting mistakes

## Training Plan
1. Generate 500+ conversations using Ollama local (gpt-oss:20b)
2. Human review + quality filter
3. QLoRA fine-tune on Phi-3-mini-4k (3.8B params)
4. Evaluate on OctopusEthics benchmark
5. Export to GGUF for Ollama
6. Iterate

## Base Model Options
| Model | Params | License | Why |
|-------|--------|---------|-----|
| Phi-3-mini-4k | 3.8B | MIT | Tiny, fast, excellent reasoning for size |
| Qwen2.5-7B | 7B | Apache 2.0 | Strong multilingual, open |
| Llama 3.1 8B | 8B | Meta Community | Battle-tested, large community |

## Compute
- Kaggle: 30h/week free T4 GPU
- Google Colab: free T4
- Local: Ollama for dataset generation
- **Total cost: $0**

## Security
- NO PII in any training data
- NO proprietary code or trade secrets
- NO outputs from closed-source models (OpenAI/Anthropic TOS)
- All data is original or from permissive open datasets
- Published under Apache 2.0
