# VisualPrompt — Marketing Strategy

> Internal strategy doc. Not user-facing. Lives next to the marketing site so writers, designers, and agents touching `site/` can stay on-message.

---

## 1. North Star

**VisualPrompt is the bridge between AI image generation and people who don't (and don't want to) speak AI.**

Curious humans have an image in their head. AI can paint almost anything. The space between those two — prompt-engineering, jargon, magic words, trial-and-error — is what we replace. We give people **a remote control for AI images** instead of a vocabulary test.

In one line for outside use:

> *"Make AI pictures the way you actually pictured them."*

In one line for ourselves:

> *Bridge AI ↔ Mensch — for people who have **no idea** about AI and don't want one.*

---

## 2. Target Audience

We are **explicitly not** chasing professional AI artists, ML engineers, or prompt-savvy power users. They have other tools and don't need a bridge — they *are* the bridge in their own workflows.

### Primary segment — "AI-curious normals"

People who:

- Have heard of ChatGPT and "those AI images", maybe tried Midjourney/DALL·E once.
- Bounced off because the output never matched what they imagined.
- Don't know what "seed", "denoising", "ControlNet", "CFG scale", or "rule of thirds" means — and shouldn't have to.
- Have a clear *picture in their head* but no patience for prompt rabbit holes.

### Sub-personas

| Persona | What they want | What hurts today |
|--------|----------------|------------------|
| **Hobbyist Hannah** — 32, knits, journals, makes Pinterest boards | A cover image for her newsletter that looks how she imagined it | The cat is always in the wrong corner; gives up after 6 prompts |
| **Small-shop Sven** — runs a one-person Etsy / Shopify | A product mockup, a banner, a quick social ad | Stock photos look generic, prompt tools require a course |
| **Teacher Tobi** — primary school | A friendly illustration of "two kids sharing a sandwich under a tree" | AI keeps adding extra arms, weird hands, three kids |
| **Creator Clara** — TikTok / blog, 15k followers | A specific scene that matches today's post | Spends 40 min wrangling prompts, ends up screenshotting Pinterest |
| **Curious Karim** — never tried AI seriously | "Just want to make something cool with my idea" | Every tutorial assumes prior knowledge |

### Anti-personas (do not optimize for)

- ML researchers, AI engineers.
- Professional concept artists with established Stable Diffusion / ComfyUI workflows.
- Bulk SEO image farms.

---

## 3. Positioning

**Category:** Spatial image direction tool / AI image co-pilot for non-experts.

**Primary frame:** "Lego for AI images." You snap a few shapes into place, frame the picture like you would a phone camera, write a normal sentence, done.

**Against alternatives:**

- vs. **prompt-only tools (Midjourney, DALL·E, etc.):** You direct the picture instead of describing it.
- vs. **pro-grade controllable AI (ComfyUI, A1111, ControlNet):** No installs, no graphs, no jargon. Browser-only.
- vs. **traditional design tools (Canva, Figma):** You don't draw or layout — you stage. AI does the rest.

**One-liners we can rotate:**

- "Place it. Frame it. Describe it. The AI does the painting."
- "The remote control for AI images."
- "Stop typing prompts. Start placing things."
- "AI is great at painting. Bad at reading your mind. We sit in between."
- "Direct AI like a tiny film set."

---

## 4. Messaging Pillars

Every page, ad, post, or video should ladder up to **one** of these. If it doesn't, cut it.

### Pillar A — Control without complexity

*You are the director. AI is the painter.*

- Place objects in 3D where you want them.
- Frame the camera the way you'd frame a phone photo.
- The AI fills in colors, light, mood, materials.

### Pillar B — No AI knowledge required

*If you can drag, click, and write a sentence, you can use this.*

- No prompt engineering.
- No "negative prompts", "samplers", "checkpoints".
- No tutorials before you make something good.

### Pillar C — Match the picture in your head

*The result actually looks like what you imagined — not what the AI guessed.*

- Layout stays put across re-rolls.
- The cat is where you put the cat.
- Re-generate variations without re-explaining the scene.

### Anti-pillars (don't say these on outbound)

- Pipeline talk, "diffusion", "latent space".
- "Spatial prompting" as a *term* (works internally; reads cold to civilians).
- "Edge functions / Supabase / infra".
- Anything implying you should already understand AI to start.

---

## 5. MVP Scope & Honesty

The current product **only** does **still images**. Marketing must reflect that.

**Allowed claims today**

- AI image generation, controllable.
- 3D scene staging in the browser.
- Camera framing + plain-language description → image.
- Iteration on the same scene.

**Not yet — must not appear on landing or ads**

- Video generation.
- Animation, multi-frame, timelapse.
- Pro-grade fidelity guarantees.
- Team collaboration / sharing flows we haven't shipped.

When video ships, we'll add a dedicated section, not retcon the homepage. Trust beats hype.

---

## 6. Channels & Tactics

Ranked by fit for the primary segment, not by what's trendy.

### 6.1 Owned & search

- **Landing page (`visualprompt.io`)** — primary funnel. Plain language. One CTA: *Open the editor*.
- **SEO long-tail content** ("how to make a specific scene with AI", "AI image without prompts", "AI image generator that listens to me") — blog posts under `/blog/` later. Targets people *frustrated* with prompts, not people *researching* prompts.

### 6.2 Short-form video — highest leverage for this audience

- **TikTok / Reels / YouTube Shorts** in this exact loop:
  1. "I asked AI to draw X. Look what I got." *(disaster)*
  2. "Now watch what happens when I just **place** it." *(VisualPrompt)*
  3. *(Result that matches the brief.)*
- Time-to-payoff under 20s. No voiceover jargon.
- Captioning matters more than narration; many users watch silent.

### 6.3 Communities (warm, not spammy)

- r/ArtificialInteligence, r/AIArt, r/midjourney (especially threads with "the cat keeps moving" complaints).
- Hobby subreddits where image generation hurts: r/Etsy, r/EtsySellers, r/blogging, r/Teachers, r/dndmaps.
- Discord servers for AI-curious creators (not pro AI art servers).

Format: **show, don't pitch.** Post a 20s before/after with VisualPrompt mentioned at the end.

### 6.4 Newsletter / collab

- Cross-promo with creator newsletters that already speak to non-technical creatives (newsletters about journaling, small-business tools, indie creators). Lower CAC than paid for warm-intent audiences.

### 6.5 Paid (later, not at MVP)

- Hold paid until organic loops are proven. When we turn it on, target by **interest** (Pinterest, Etsy seller tools, Canva users) not by "AI" — our segment doesn't self-identify as AI users.

---

## 7. Content Themes

A backlog any contributor can pull from. All themes have one job: show that **you stay in charge**.

1. **"Prompt vs. Place"** — the same idea typed-in vs. staged-in.
2. **"AI keeps moving the cat"** — pain content; ends with the fix.
3. **"I can't draw" series** — turn napkin sketches / mental images into clean AI images via staging.
4. **Use-case drops** — Etsy listing mockup, blog cover, school worksheet illustration, D&D map, RPG character on a specific cliff, etc.
5. **"No AI knowledge required" walkthroughs** — 90-second "first image" video.
6. **Behind-the-glass** — short pieces that **demystify** AI image generation in plain words. Builds trust without lecturing.

---

## 8. Brand Voice

- **Plain.** Talk like a smart friend, not a launch deck.
- **Warm.** People feel dumb around AI; we never make that worse.
- **Concrete.** "The cat ends up where you put the cat" beats "deterministic spatial coherence".
- **Light.** A bit of wink is fine. AI marketing is exhausting; lightness is differentiation.
- **No emoji-spam, no `✨`, no "unleash", no "supercharge".**

Forbidden words in outbound copy: *unleash, supercharge, revolutionize, paradigm, AI-powered (as filler), seamless, leverage, harness, robust*.

Preferred: *place, frame, describe, direct, stage, snap, drag, tweak, redo, again, cosy, off, weird, just*.

---

## 9. Funnel & KPIs

Lightweight metrics for a small team. Don't dashboard until volume justifies it.

| Stage | Metric | Why it matters |
|-------|--------|----------------|
| Awareness | Short-form video views, share rate | Cheap signal that the hook lands |
| Site interest | Landing → "Open editor" click-through % | Page-level message-fit |
| Activation | First image successfully generated within session | "Did the bridge actually work?" |
| Retention | Day-7 return rate | Did the result match their head, not just once |
| Word-of-mouth | Self-reported "friend told me" / referrer data | Bridge users *love telling other curious normals* |

Target floor for landing → editor CTR at MVP: **≥ 8%** of unique visitors. Anything below that is a copy problem first, product second.

---

## 10. Marketing Site Content Rules

Specific to this repo (`site/`). Treat as authoritative for landing copy.

1. **English only** on the public page (segment is global; German tagline is internal).
2. **No video promises** until video ships.
3. **No infra name-drops** (no Supabase, edge functions, Three.js, etc. on landing).
4. **Lead with empathy, then product.** First fold = the problem they feel; second fold = how we solve it.
5. **Asymmetric layouts allowed and encouraged.** Avoid the "three identical card" template look — it reads "AI startup boilerplate".
6. **Show the product** at least once above the fold or directly after the hero. Placeholder ok during MVP; never ship a homepage with zero product visual.
7. **Single primary CTA** site-wide: *Open VisualPrompt* → `https://app.visualprompt.io/`. Secondary CTAs allowed (scroll-down anchors, short-form video links).
8. **No AI-generated hero images** on the marketing site. We sell control over AI; using slop hero art breaks the pitch. Real screenshots, simple SVG illustrations, or plain typography.

---

## 11. Roadmap-Aware Messaging Hooks

When these ship, the homepage gets a new section — not a rewrite.

- **Video generation** → new section "Now also moving pictures", same staging metaphor.
- **Templates / starter scenes** → "Don't start from a blank stage."
- **Sharing / collab** → "Hand the scene to a friend." (Targets the "ask a friend who's good at AI" workaround we replace.)
- **Mobile capture** → "Use a phone photo as the starting frame."

Until each of these is real in production, they live here, not on the site.

---

## 12. TL;DR for anyone editing the landing page

- Audience: people who don't understand AI and don't want to.
- Promise: you direct, AI paints, the result matches your head.
- Tone: plain, warm, light. Not a deck.
- Scope today: **still images only**.
- Visuals: real screenshots or simple geometric SVGs. No AI-slop hero art.
- Layout: asymmetric over symmetric. One primary CTA.
