# VisualPrompt (visualprompt.io)

This repository publishes the **public marketing site** for [VisualPrompt](https://visualprompt.io) via **GitHub Pages**. Deployed HTML/CSS lives under [`site/`](site/).

Separate private repositories ship the authenticated **web editor** (hosted at **https://app.visualprompt.io**) and backend services—do not assume implementation details live here.

---

## Context for collaborators & autonomous agents

**One-line pitch.** VisualPrompt is a browser scene editor where users compose **3D layout and camera framing** alongside a plain-language brief. That combined intent is treated as the **visual prompt** for downstream generative pipelines (still / video)—reducing ambiguity compared with text-alone spatial descriptions.

### Problem orientation

Traditional image/video prompting relies heavily on prose. Humans struggle to precisely describe relative positions, occlusion, horizons, depth ordering, etc. Models interpret wording inconsistently → composition drift across rerolls. VisualPrompt’s bet: **editable geometry + viewport snapshots** grounded in spatial structure produce more stable creative direction **when the generation stack consumes scene-aligned context.**

### Canonical URLs

| Surface | Host | Repo / notes |
|--------|------|----------------|
| Marketing & docs | https://visualprompt.io | **This repo** (`site/` deployed to Pages) |
| Product (editor UI) | https://app.visualprompt.io | Hosted separately (not here) |

When linking externally or configuring OAuth redirect URLs in other systems, distinguish **apex marketing** (`visualprompt.io`) from **`app`** (editor).

### Vocabulary & mental model

- **Scene / layout** — Placed entities, vertical offsets, grouping; the authoritative spatial arrangement the user iterated on.
- **Visual prompt** — The **paired** pairing of authored language + grounded scene/visual context exported or consumed by generators (conceptual—not a single file type in this repo).
- **Entity** — Spawnable primitive or asset handle users drag onto the Ground plane then refine.
- **Viewport / framing** — Orbit camera, FOV-ish controls—creative direction often lives here as strongly as prose.
- **Blueprint / sprites** *(product concepts)* — The application stack supports persistent projects and blueprint/thumbnail workflows; implementation is **not** in this static repo.

Use **“Spatial prompting”** or **“visual prompt”** consistently in outward-facing language; reserve **VisualPrompt** for the product brand.

### What belongs in **this** repository

✅ Landing copy updates, typography, layouts, imagery (add under `site/`).

✅ GitHub Actions that publish `site/` to Pages.

✅ High-level README / DNS notes meant for engineers and tooling.

❌ Vite bundles, Three.js editor code, Supabase schemas, CI for the SPA—those live elsewhere.

Agents editing this repo should **not** scaffold a full SPA here unless deliberately changing product scope.

---

## Repository layout

```
site/
  index.html       # Landing page markup
  styles.css       # Page styles (no bundler required)
  CNAME            # Tells Pages the apex host (must match Pages custom-domain setting)

.github/workflows/
  deploy-github-pages.yml   # Publishes `site/` on push to main
```

---

## Local preview

Serve `site/` with any static file server:

```bash
cd site && python3 -m http.server 8080
```

Open http://localhost:8080/

---

## GitHub Pages setup (once per repo)

1. GitHub repository **Settings → Pages**.
2. **Build and deployment → Source**: select **GitHub Actions** (not *Deploy from a branch* unless you deliberately prefer that workflow).
3. Merge or push `.github/workflows/deploy-github-pages.yml` to **`main`**; allow the workflow to complete.
4. Still under Pages, enter **Custom domain**: `visualprompt.io` → Save → wait for DNS check ✅ → toggle **Enforce HTTPS** after cert issuance.

Repeat checks if you rotate DNS or recreate the Pages environment.

---

## DNS records for `visualprompt.io` → GitHub Pages

Configure these **at your DNS provider** for the `visualprompt.io` zone:

### Apex (`visualprompt.io`)

Add **four `A` records** for `@` (some UIs label this root / apex):

| Type | Host / Name | Value |
|------|--------------|-------|
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |

**Optional but recommended IPv6**: add **`AAAA`** records similarly:

| Type | Host / Name | Value |
|------|--------------|-------|
| AAAA | `@` | `2606:50c0:8000::153` |
| AAAA | `@` | `2606:50c0:8001::153` |
| AAAA | `@` | `2606:50c0:8002::153` |
| AAAA | `@` | `2606:50c0:8003::153` |

> GitHub publishes the authoritative addresses in **[GitHub Docs → Managing a custom domain for GitHub Pages](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site#configuring-an-apex-domain)**—verify there if IPs change during your onboarding.

### `www` subdomain (optional)

| Type | Host / Name | Value |
|------|--------------|-------|
| CNAME | `www` | `visualprompt-io.github.io` |

Adapt the canonical target casing to your Pages default host (GitHub lowercases hostname resolution). Configure `www.visualprompt.io` as an **additional** domain in Pages if you route traffic there—GitHub expects both apex and `www` when using both DNS entries.

Propagation can take minutes to hours. Once GitHub verifies the domain for this repository it issues (or renovates) the TLS certificate.

---

## Maintainer checklist after DNS go-live

- [ ] Pages UI shows ✅ next to **visualprompt.io** + DNS **Check** succeeded.
- [ ] **Enforce HTTPS** checked.
- [ ] Editor still reachable at https://app.visualprompt.io (`app` `A`/DNS points at your infra, unrelated to Pages).
- [ ] OAuth / Magic-link redirect URLs listing both hosts where applicable.

---

## License & ownership

Marketing assets and prose are proprietary unless otherwise labeled. Unauthorized redistribution of generated marketing packs does not waive rights in the broader VisualPrompt codebase.
