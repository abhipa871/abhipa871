# Hey, I'm Abhi

I study computer science, physics, and machine learning, and I like building projects that let me poke at models from the inside instead of only treating them like APIs.

Right now, this GitHub is a mix of research code, class-adjacent experiments, hackathon projects, and things I built because I wanted to understand an idea better. Some of the more interesting ones are below.

## Quick Links

- LinkedIn: [linkedin.com/in/abhi-patel-655808241](https://www.linkedin.com/in/abhi-patel-655808241/)
- GitHub: [github.com/abhipa871](https://github.com/abhipa871)

## School

- University of Michigan, M.S. Computer Science and Engineering, Aug. 2026 - Dec. 2027
- Rutgers University, B.S. Computer Science and Physics, Summa Cum Laude, May 2026
- Former Technical Chair, Rutgers AI Club

## Projects

### [ReAgent](https://github.com/Alred-79/hackprinceton-final)
A HackPrinceton project about making multi-agent systems easier to break, inspect, and harden before they touch anything important.

It simulates failure cases like schema drift, tool misuse, unsupported claims, approval boundaries, replay risk, and side effects. The fun part is that it treats reliability as something executable, not just a diagram with arrows and good intentions.

Built with React, TypeScript, FastAPI, LangGraph, Pydantic AI, and SQLite. Won Best Use of Enter.pro at HackPrinceton Spring 2026.

### [selfie-agent](https://github.com/abhipa871/selfie-agent)
A small Python package for SelfIE-style hidden-state injection experiments on Hugging Face causal language models.

The basic idea is: generate an answer, grab hidden states from specific tokens/layers, inject them into an interpretation prompt, and see what the model says those internal states are doing. I built it to make representation probing experiments easier to repeat across models instead of rewriting hook code every time.

Includes batch/aligned injection modes, chat-template handling, quantized model loading, and support for model families like Gemma, Llama, Qwen, and K2-V2.

### [MedCLIPDinoTxt](https://github.com/abhipa871/MedCLIPDinoTxt)
A fork of MedCLIP where I tried replacing the usual visual encoder with DINOv3 and testing whether those self-supervised visual features helped medical image-text alignment.

The project pivoted to ROCO because the original MIMIC-CXR/CheXpert setup was painful to make practical in the time I had. The results were not magically better, which was honestly the useful part: DINOv3 is strong, but the dataset, loss, freezing strategy, and projection head all matter a lot.

The repo includes the DINOv3 vision wrapper, ROCO dataset/collator code, training utilities, retrieval evaluation, and notes from the final report.

### [ToolGeneration / Luma Chat](https://github.com/abhipa871/ToolGeneration)
A ChatGPT-style interface for talking to local and hosted model providers through one frontend.

This one is more full-stack infrastructure than model research: streaming responses, provider adapters, Supabase auth, stored conversations, BYOK-style server-side credential handling, and support for OpenAI-compatible APIs, Ollama, vLLM, SGLang, and Hugging Face endpoints.

It started from wanting a cleaner way to swap model backends without rebuilding the whole app around each provider.

### [moodmusic](https://github.com/abhipa871/moodmusic)
A voice-to-mood music recommender.

The browser records a short voice clip, a FastAPI backend runs emotion classification with a Wav2Vec2 checkpoint, and the frontend uses Spotify search to suggest tracks that fit the detected mood. It is a smaller project, but it ties together audio ML, frontend state, API design, and external-service integration in a nice compact loop.

Built with React, TypeScript, FastAPI, Wav2Vec2, FFmpeg/pydub, and the Spotify API.

### [SnapKV](https://github.com/abhipa871/SnapKVCacheLLMPaperImplementation) and [H2O Cache](https://github.com/abhipa871/H2OCacheLLMPaperImplementation)
Paper implementation repos for long-context KV-cache compression ideas in Qwen3.5-style models.

These are the kind of repos I make when I want to understand a paper at the level where the masks, positions, padding behavior, and cache updates actually work. SnapKV focuses on prompt KV compression using attention-based token selection; H2O Cache focuses on heavy-hitter plus recent-window eviction.

They include modified Qwen attention/model code, tests, and evaluation notebooks for checking whether the cache policies behave sanely.

## Stuff I've Worked With

Python, TypeScript, JavaScript, Java, SQL, PyTorch, Transformers, Hugging Face, LangGraph, Pydantic AI, FastAPI, Next.js, React, Supabase, AWS S3, Git, and Linux.