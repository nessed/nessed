# Ali

Full-stack developer. I work on automation plumbing, LLM extraction pipelines with deterministic validation, and internal tools that businesses actually run on.

## JARVIS

**[github.com/nessed/jarvis](https://github.com/nessed/jarvis)**

A personal assistant I talk to over WhatsApp. A FastAPI webhook writes messages into a Supabase Postgres queue and my laptop pulls them off and runs them, so nothing expensive has to stay up in the cloud.

Memory is local. Facts go to SQLite, embeddings come from Ollama on loopback, search runs through sqlite-vec, and self-hosted Mem0 sits on top. Nothing personal leaves the machine. LLM calls go through a router that tries free tiers before paid ones.

Speech-to-text is Whisper large-v3 running on this laptop's XDNA NPU, built from source, 12.4x faster than CPU on the encoder. If the NPU graph will not load it aborts instead of quietly falling back, so a passing result cannot be a lie. Voice notes work in both directions.

The queue does atomic claim, checkpoint, retry, backoff, per-job timeout and dead-letter, with duplicate Meta redeliveries dropped at enqueue and again at send. Two independently supervised workers, so slow memory work cannot starve incoming messages.

In progress, phase 3 of 6. Python, FastAPI, Supabase, Ollama, whisper.cpp.

## Other projects

**[Pakistan Budget Extraction](https://github.com/nessed/Pakistan-Annual-Budget-Data-Validation-Extraction-Architecture)**
Dual-LLM extraction with rule-based validation over Pakistan's Annual Budget Statements, 2010 to 2027. Numbers reconcile against the printed source before anything is trusted. Python.

**[WhatsApp AI Assistant](https://github.com/nessed/whatsapp-echo-bot)**
Meta Cloud API to n8n to LLM and back, with idempotent run claiming, bounded conversation context, and logging in both directions. n8n, Meta Graph API, Supabase.

**[bytesOS](https://github.com/nessed/bytesOs)** ([live](https://bytes-os.vercel.app))
Orders, revenue, cost and debt tracking for a campus food business. Pulls live from the operating Google Sheet. TypeScript, Express, Google Sheets API.

**[LMDA Profit Hub](https://github.com/nessed/lmda-profit-hub)** ([live](https://lmda-profit-hub.vercel.app))
Internal dashboard for staff performance, workshops and operational KPIs, with role-gated routes. TypeScript, React, Supabase.

**[Akada](https://github.com/nessed/akada)** ([live](https://akada.vercel.app))
Academic planner: semester planning, task tracking, study-session analytics. TypeScript, React.

**[Song Studio Sessions](https://github.com/nessed/song-studio-sessions)** ([live](https://song-studio-sessions.vercel.app))
Workspace for managing audio projects, lyrics and session notes. TypeScript, React.

**[Todoist Flow](https://github.com/nessed/todoist-flow)** ([live](https://todoist-flow.vercel.app))
Todoist client with a serverless API layer handling OAuth, sessions and task views. TypeScript, Vercel Functions.

**[Training Directory](https://github.com/nessed/training-directory)** ([live](https://training-directory-silk.vercel.app))
Full-stack directory app with a typed schema layer. Next.js, Supabase, Drizzle ORM.

## Stack

TypeScript, JavaScript, Python, SQL, C++
React, Next.js, Tailwind, shadcn/ui
Node/Express, FastAPI, Supabase, PostgreSQL, SQLite, Drizzle, MongoDB
n8n, WhatsApp Cloud API, LLM APIs, Ollama, Google Sheets API

## Contact

Open to automation and internal-tooling work. Reach me through GitHub.
