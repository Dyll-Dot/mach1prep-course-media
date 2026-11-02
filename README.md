# Mach1Prep course media

Published lesson media for the Mach1Prep course (narration audio, chart images and lesson timelines). Files are stored as **GitHub Release assets**, never in Git history. Each file is named by its SHA-256 content hash, so a name never changes meaning.

| Release | Served on | Holds |
|---|---|---|
| `staging` | the preview site only | lessons waiting for review (style-lab demos and new modules) |
| `live` | preflightdesk.app | approved lessons |

The website (`Dyll-Dot/preflightdesk`) lists the exact hashes it may serve in `server/course-media.json`; its server downloads each file once, checks the hash and caches it.

**How files arrive:** the studio (`Dyll-Dot/mach1prep-course-studio`, `tools/stage_media.py`) pushes the hashed files to a short-lived branch `incoming/<release>`. The **Ingest media** workflow checks every name against its content, uploads the files to that release and deletes the branch.

Chart excerpts are FAA charts labelled "not for navigation". Narration in `staging` may come from a free text-to-speech plan and is for review only.
