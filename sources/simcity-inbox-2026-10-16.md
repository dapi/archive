# Inbox on the primary organization map

- Date: 16 October 2026.
- Status: selected for the authenticated Corp organization map.
- Tool: OpenRouter Image API via curl, model `openai/gpt-image-2`; API fallback
  after the built-in ImageGen transport failed and the direct OpenAI key had no credits.
- Parameters: `quality: medium`, `aspect_ratio: 16:9`, `n: 1`, buffered response.
- Input: `assets/simcity/hq-simcity-primary.png`, preserved unchanged.
- Output: `assets/simcity/hq-simcity-primary-inbox-20261016.png`, 1536 × 864 PNG.
- Consumer copy: `~/code/corp.pismenny.ru/assets/simcity/organization-primary-inbox-20261016.png`.
- Textual SSOT: `repo://dapi/hq/governance/organization-architecture.md`.
- Public gallery delivery: not requested for this change; the archive commit
  skips automatic Pages delivery. The authenticated Corp deployment is separate.

## Visual review

Exactly eight distinct rooms are present: HQ, Inbox, Content, Research, Sales,
Media, Legal and Finance. All nameplates are spelled correctly. Inbox is a
warm-lit intake and routing office above HQ. Existing scenes retain their roles,
navy background, isometric construction, furniture and dotted connections.
No department label is cropped. The previous selected original remains in the
historical gallery and asset inventory.

## Asset checksums

- Input SHA-256: `4e28d13472150a63f5c4d25322b7be5ec010a55bcf88f041e9b0b0aab2dbe3dc`.
- Output SHA-256: `878d9f27a00f33e22d03f119aa4fc249f3d458b8da6520148786f72b54774d8e`.

## Exact edit prompt

```text
Use case: precise-object-edit
Asset type: primary organization map for the existing Personal Corp website.
Input image: EDIT TARGET and exact style reference.

Update this map to show the now-active INBOX department as a seventh satellite office. Retain HQ and all six existing department identities. Produce exactly EIGHT distinct office dioramas total, with these exact readable black nameplates in cream uppercase letters:
HQ
CONTENT
RESEARCH
SALES
MEDIA
LEGAL
FINANCE
INBOX

INBOX must be a real separate warm-lit office scene, equal in visual importance to the other active departments: an intake coordinator sorting incoming email and documents at a computer, organized incoming/outgoing document trays, a wall routing board showing simple arrows and colored cards without text. Connect INBOX directly to HQ with the same dotted cable and square connector nodes. It represents intake and handoff, not sales or finance.

Composition: keep the central HQ largest. Arrange seven satellite offices compactly around HQ. Use the upper-center gap for INBOX, moving CONTENT toward the upper left and RESEARCH toward the upper right and adjusting the other offices only as needed for clean separation. Every room and nameplate must fit wholly inside the image; no overlaps, no cut-off rooms, no crowded labels. Keep wide approximately 16:9 framing and maximize readable scene size. Preserve identities of the six existing scenes: CONTENT editor/manuscripts; RESEARCH sources/books/analysis; SALES CRM/pipeline; MEDIA video/audio monitors/camera/light/headphones; LEGAL contracts/scales; FINANCE spreadsheets/charts.

Preserve the established image's art direction: deep navy subtly textured background, warm gray isometric cutaway offices, finely illustrated SimCity-like dioramas, soft warm lighting, wood furniture, plants, individual seated workers, dark rounded rectangular nameplates, dotted cable routes and square junction blocks. Same detailed illustration style, perspective, palette and rendering. No selection rings or browser UI. No extra departments, no duplicates, no missing names, no OPS label, no random pseudo-text, no watermark. All eight labels must be exactly correct.
```

## Consumer verification

The authenticated Corp deployment was checked on 16 October 2026 using app
commit `810eb16` and image tag `snapshot-9fac9275b11d`.

- The served PNG checksum matches the archived output above.
- All eight office hotspots and all eight illustrated nameplates select the
  corresponding department; Inbox opens its own workspace.
- Desktop 1440 × 1050 and mobile 390 × 844 have no horizontal overflow.
- The sticky header, financial privacy toggle and both directory modes work.
- `npm run build`, `npm run check` and `git diff --check` passed.
