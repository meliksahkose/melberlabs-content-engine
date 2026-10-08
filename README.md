# MelberLabs Content Engine

> A brand-agnostic AI content system that plans, edits, voices and publishes short-form video and social posts, with capacity for **100–150 finished pieces a day**. It runs the social accounts of every MelberLabs app and is reused for client brands.

Designed and built by [İbrahim Melikşah Köse](https://github.com/meliksahkose) at [MelberLabs](https://melberlabs.com)

## What it does
- **Daily planning.** A deterministic planner turns per-brand configs and banks of hooks, scripts and prompts into a daily plan for each brand and platform (TikTok, Instagram, X, Reddit), with captions and posting times.
- **Trend research.** Pulls trending sounds and competitor content through Apify, so every reel can use a current, platform-native sound.
- **Production.** Turns raw clips, screen recordings and 3D phone mockups into finished vertical videos: animated hooks, captions, transitions, end cards and music ducking.
- **Voice.** Generates per-brand narration with ElevenLabs and aligns captions word by word with Whisper.
- **Adobe and render bridges.** Scripted After Effects, Premiere and Photoshop, plus Remotion and HyperFrames for code-driven motion graphics.
- **Publishing.** A Playwright-driven poster with a persistent browser profile per account. A human confirms the final post.
- **Studio app.** A local desktop UI per brand per day: produce, edit, post, engage, and a brief box that hands edits to a coding agent.

## Engineering decisions
- **Config over code.** A new brand is a TOML file (voice, colours, handles, platform rules), which is why the same engine serves apps, e-commerce stores and client work.
- **Quality gates.** Automated audits check every render for unreadable source text, off-brand products and timing problems before a human sees it.
- **Stack:** Python · ffmpeg · faster-whisper · ElevenLabs API · Apify · Remotion (React) · HyperFrames/GSAP · After Effects/Premiere scripting (ExtendScript, CEP) · Playwright · WSL2 render workers.

---
<sub>Source code is private. Happy to demo it in an interview: meliksahkose90@gmail.com</sub>
