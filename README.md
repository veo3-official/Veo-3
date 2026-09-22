# Veo 3

Veo3 is Google DeepMind's video generation model, the first major model to produce dialogue, sound effects and music natively.

> **Try Veo 3 online →** [https://veovideoai.com](https://veovideoai.com?utm_source=github&utm_medium=ugc&utm_campaign=veo3-official&utm_content=readme-top&utm_term=tier-b)

Veo 3 is the third generation of Google DeepMind's video generation model, announced at Google I/O in May 2025. Where Veo 2 produced silent clips, Veo 3 generates the soundtrack in the same pass as the pixels: characters speak with synchronized lip movement, footsteps and doors and traffic are placed where they should be, and ambient music follows the mood of the prompt. That single change is why Veo 3 clips spread so quickly across social media in mid-2025 and why "veo3" became the shorthand for realistic AI video with sound.

The model is built and hosted by Google DeepMind and distributed through Google's own products: the Gemini app, the Flow filmmaking tool, YouTube Shorts, the Gemini API in Google AI Studio and Vertex AI for enterprise. Veo 3 Fast, a cheaper and quicker variant, followed in July 2025, and image-to-video, 1080p output and vertical 9:16 video were added over the summer. Veo 3.1, released in October 2025, kept the same eight-second base clip but added reference images for consistent characters and objects, first-and-last-frame transitions, scene extension for longer pieces and richer audio; a later 3.1 update brought 4K output. Every frame carries a SynthID watermark.

Against OpenAI's Sora 2, Kuaishou's Kling, ByteDance's Seedance and MiniMax's Hailuo, Veo 3 is usually rated the most cinematic: physically plausible motion, faithful prompt following for camera and lighting, and the most convincing dialogue audio. Its trade-offs are the short base duration, higher price per second than the Chinese models, and the fact that access depends on a Google account, plan and country.

## Contents

- [What Veo 3 can do](#what-veo-3-can-do)
- [Versions](#versions)
- [How to access Veo 3](#how-to-access-veo-3)
- [Prompt examples](#prompt-examples)
- [Veo 3 vs alternatives](#veo-3-vs-alternatives)
- [Pricing](#pricing)
- [FAQ](#faq)
- [Links](#links)

## What Veo 3 can do

- Text-to-video and image-to-video with native audio: dialogue with lip sync, sound effects, ambience and music generated with the video, in many languages.
- Eight-second base clips at 720p or 1080p, 24 fps, in 16:9 or vertical 9:16; Veo 3.1 exposes 4, 6 and 8 second lengths in the API and adds 4K output.
- Reference images (up to 3) in Veo 3.1 to keep a character, product or setting consistent across generations.
- First-and-last-frame transitions: supply the start and end images and the model animates between them with matching sound.
- Scene extension: continue a Veo clip by another segment at a time, in Flow or via the API, to build sequences well beyond eight seconds.
- Precise camera and lighting control from the prompt: dolly, crane, handheld, lens choice, time of day, film stock and grading terms are followed closely.
- Object insertion and removal, and shot-to-shot editing, inside the Flow tool.
- Veo 3 Fast: a lower-cost, lower-latency variant with the same audio capability for high-volume or draft use.

Known limitations: each generation is at most eight seconds, so longer work depends on extension and stitching, and continuity can drift over several extensions. 1080p and 4K are restricted to certain aspect ratios and lengths, and 4K output is an upscale on the 3.1 line. Audio occasionally produces subtitles, garbled speech or the wrong language when the prompt is vague. Safety filters block real public figures, minors in many contexts, and violent or sexual material, and photorealistic people may be refused in some regions. Availability and quotas differ by country and by Google AI plan.

## Versions

| Version | Released | Notes |
|---|---|---|
| Veo 3 | 2025-05 | Announced at Google I/O; native audio, 8 second 720p clips, 16:9. Launched in the Gemini app for Ultra subscribers, Flow and Vertex AI preview. |
| Veo 3 Fast and image-to-video | 2025-07 | Cheaper, faster variant; image-to-video in the Gemini app and API; Veo 3 arrives in the paid Gemini API preview. |
| Veo 3 GA, 1080p and vertical | 2025-09 | Stable API model IDs veo-3.0-generate-001 and veo-3.0-fast-generate-001; 1080p output and 9:16 vertical; price cuts. |
| Veo 3.1 and Veo 3.1 Fast | 2025-10 | Reference images, first-and-last-frame with audio, scene extension, richer audio and better prompt adherence; Flow gains insert and remove. |
| Veo 3.1 update | 2025-12 | 4K output, vertical video in the API and longer extensions. |

## How to access Veo 3

Veo 3 is a closed model hosted by Google. Official ways to use it:

- Gemini app: Google AI Pro subscribers get a limited number of Veo 3 Fast generations per day; Google AI Ultra includes the highest quotas and the full-quality model.
- Flow (labs.google/flow): Google's filmmaking tool with scene builder, extension, reference ingredients and camera controls; also tied to AI Pro and AI Ultra credits.
- Gemini API in Google AI Studio: model IDs `veo-3.0-generate-001`, `veo-3.0-fast-generate-001`, `veo-3.1-generate-preview` and `veo-3.1-fast-generate-preview`, billed per second of output, paid tier only.
- Vertex AI for Google Cloud customers, with enterprise terms and regional endpoints.
- Bundled surfaces: YouTube Shorts (Veo 3 Fast), Canva, Adobe Firefly and third-party hosts such as fal.ai and Replicate.

Restrictions: the Gemini app and Flow rolled out first in the US and later to most other countries, quotas reset daily, photorealistic people are limited in some regions, and there is no free API tier for Veo. The simplest way to try the model without a Google subscription or a waitlist is [Veo 3](https://veovideoai.com), which offers pay-per-generation access.

**Fastest way to try it:** [Try Veo 3 online](https://veovideoai.com?utm_source=github&utm_medium=ugc&utm_campaign=veo3-official&utm_content=readme-access&utm_term=tier-b) — no waitlist, runs in the browser.

## Prompt examples

**Dialogue scene with lip sync**

```text
A weathered fisherman in a yellow raincoat stands on a pier at dawn, medium close-up, 35mm lens, soft grey light. He looks at the camera and says in a low voice: 'The sea doesn't care what you planned.' Gulls in the distance, rope creaking, gentle waves against the pilings.
```

**Handheld street documentary**

```text
Handheld tracking shot following a street food vendor in Bangkok at night as she flips noodles in a wok, flames bursting up, neon signs reflected in puddles. Natural sound: sizzling oil, scooters passing, crowd chatter, no music.
```

**Product macro with sound design**

```text
Extreme macro of a mechanical watch movement being assembled by tweezers, dramatic side lighting, shallow focus racking from gear to balance wheel. Crisp ticking, faint metallic clicks, quiet room tone, slow push-in, 8 seconds.
```

**Animated character (reference image, 3.1)**

```text
Use the attached character sheet. The fox in the blue scarf runs through an autumn forest, camera low and tracking alongside, leaves kicking up, 2D-inspired 3D animation look, warm afternoon light. Playful woodwind music and rustling leaves.
```

**First and last frame transition**

```text
Start frame: an empty white gallery wall. End frame: the same wall covered in a finished mural of a whale. 8 seconds, timelapse of the mural being painted by an unseen artist, brush strokes appearing in rapid succession, muffled gallery ambience and quick brush sounds.
```

## Veo 3 vs alternatives

| Model | Max resolution / duration | Native audio | Editing / references | Access | Price tier |
|---|---|---|---|---|---|
| Veo 3 / 3.1 (Google) | 1080p, 4K on 3.1, 8 s base with extension | Yes, dialogue with lip sync | Up to 3 references, first/last frame, extend, insert/remove in Flow | Gemini app, Flow, Gemini API, Vertex AI | Medium-high |
| Sora 2 (OpenAI) | 1080p (Pro), up to 15 s | Yes | Remix, cameos, storyboard | Sora app, ChatGPT, OpenAI API | Medium-high |
| Kling 2.6 (Kuaishou) | 1080p, 5 to 10 s | Yes | Elements references, first/last frame, motion brush | Kling app, Kling API, fal | Medium |
| Seedance 2.0 (ByteDance) | 1080p, up to 15 s | Yes, dialogue with lip sync | Up to 9 images, 3 videos, 3 audio references | Dreamina, CapCut, Volcano Engine / BytePlus API | Low-medium |
| Hailuo 2.3 (MiniMax) | 1080p, 6 or 10 s | No | First/last frame, subject reference | Hailuo app, MiniMax API | Low |

Veo 3 remains the reference point for audio quality and cinematic realism, and Veo 3.1 closed most of the gap on references and editing. Sora 2 offers longer single clips and a stronger social app, Kling and Seedance are cheaper per second and more widely mirrored by third-party hosts, and Hailuo is the budget option without native sound. Veo's main costs are price and the Google plan requirement.

## Pricing

As of the last public information, Google bills Veo on the Gemini API and Vertex AI per second of generated video, with Veo 3 and Veo 3.1 at a standard rate and the Fast variants at a fraction of it; the standard rate was cut substantially in September 2025 (Google listed Veo 3 at $0.40 per second and Veo 3 Fast at $0.15 per second at that point, and Veo 3.1 launched at the same rates). Higher resolutions may cost more. On the consumer side there is no per-clip price: Google AI Pro (around $20 per month) includes a daily allowance of Veo 3 Fast in the Gemini app and Flow credits, and Google AI Ultra (around $250 per month) includes the highest quotas. YouTube Shorts offers Veo 3 Fast free at lower resolution. Check the Gemini API pricing page for current numbers.

If you do not want a monthly plan, [Veo 3](https://veovideoai.com) provides pay-per-generation access, charged per clip.

## FAQ

**What is Veo 3?**

Veo 3 is Google DeepMind's video generation model, released in May 2025 as the first major model to generate synchronized audio, including dialogue, sound effects and music, alongside eight-second video clips from text or images.

**Is Veo 3 free?**

Mostly not. YouTube Shorts offers a free, lower-resolution Veo 3 Fast, but the Gemini app and Flow require Google AI Pro or Ultra, and the Gemini API has no free tier for Veo.

**Is there a Veo 3 API?**

Yes. Veo 3, Veo 3 Fast and Veo 3.1 are available in the Gemini API through Google AI Studio and on Vertex AI, billed per second of output, and are also resold by hosts such as fal.ai and Replicate.

**Does Veo 3 have an official GitHub repository?**

No. Veo 3 is a closed, hosted model and Google has not released weights or an official repository. This page collects publicly available information about it.

**How do I try Veo 3 online?**

Subscribe to Google AI Pro or Ultra and use the Gemini app or Flow, or use the Gemini API. For pay-per-generation access without a subscription or waitlist, use https://veovideoai.com.

**What are the limits of Veo 3?**

Each generation is at most eight seconds, so longer videos rely on extension and stitching; 1080p and 4K are tied to certain aspect ratios; safety filters block real public figures and some depictions of people; and quotas and availability vary by country and plan.

**What is the difference between Veo 3 and Veo 3.1?**

Veo 3.1 keeps the eight-second base clip and native audio but adds up to three reference images for consistency, first-and-last-frame transitions with sound, scene extension, richer audio, better prompt adherence and, in a later update, 4K output.

## Links

- [Veo (Google DeepMind, official)](https://deepmind.google/models/veo/)
- [Gemini API video generation docs](https://ai.google.dev/gemini-api/docs/video)
- [Flow by Google Labs](https://labs.google/flow)
- [Try Veo 3 online](https://veovideoai.com)

---

*This is an independent, community-maintained information repository about Veo 3. It is not affiliated with, endorsed by, or sponsored by Google DeepMind. All trademarks belong to their respective owners. Corrections welcome via issues.*

_Last reviewed: 2026-09-22_
