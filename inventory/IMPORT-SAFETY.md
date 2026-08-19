# Body Kitchen source and import safety

Product policy draft — 2026-08-19. This is an engineering and product baseline, not a substitute for review by qualified IP/privacy counsel before public launch.

## Governing product rule

**Import cooking knowledge; reference creator media.**

The system may transform functional cooking facts into a private recipe draft. It does not treat public visibility, screenshot capability, a platform download button, or machine-readable page data as permission to commercially republish a creator's photography, video, narration, or expressive recipe prose.

## Default source behavior

| Source | Default ingestion | Media treatment | Public sharing |
|---|---|---|---|
| User-authored recipe | Save directly | User controls their own upload | Shareable with explicit confirmation |
| Typed craving or rough idea | Save directly, then shape | Body Kitchen originals only | Shareable after user review |
| Recipe website URL | Parse permitted structured facts; preserve URL and author | Remote image only when permitted; otherwise original site link | User adaptation and attribution, not copied page |
| YouTube URL | Approved metadata and official embedded player | Never download/rehost by default | Embed/link plus user's adaptation |
| TikTok URL | Official embed/display path when available | Never download/rehost by default | Embed/link plus user's adaptation |
| Screenshot | Ephemeral private processing | Raw image deleted after extraction unless user deliberately retains it privately | Raw screenshot always stripped |
| Licensed creator media | Follow the specific license and provenance record | Use only within granted scope | Only as the license permits |

## Three-layer object boundary

Body Kitchen deliberately stores three separate objects:

1. **Private source reference** — the user's optional original screenshot or media reference. By default this stays in browser IndexedDB on that device. A temporary cloud processing copy, when a production extractor requires one, has a short enforced TTL.
2. **Personal recipe memory** — durable structured cooking facts, rewritten steps, provenance, private notes, preferences, cook history, and a pointer to any device-local source. It never embeds the source blob.
3. **Kitchen Table post** — a newly constructed allowlisted public object. It is not the personal recipe with a public flag.

Deleting layer 1 keeps layers 2 and 3 intact. Removing a public post does not erase the user's private recipe memory. Local source IDs and blobs never cross the community serialization boundary.

## Screenshot lifecycle

1. User selects an image locally.
2. Client validates image type and size before upload.
3. Backend places it in an isolated temporary object with a short expiration.
4. OCR/vision extracts proposed ingredients, quantities, equipment, actions, and source clues.
5. Safety-relevant uncertainty remains explicit; the model cannot invent temperatures or doneness.
6. User receives a private proposed recipe draft.
7. The raw image and derived source-media crops are deleted automatically after processing.
8. Persist only the structured draft, source URL/creator when known, provenance fields, and user corrections.
9. No screenshot, crop, embedding, or transcript enters model-training corpora.
10. Community publication runs through a source-media stripping gate.

If processing fails, the raw image still expires. Retention must not silently extend because a job failed or entered a retry queue.

## Minimal provenance model

Every imported recipe stores:

```json
{
  "source_kind": "website | youtube | tiktok | screenshot | user_original | licensed",
  "source_url": null,
  "source_creator": null,
  "source_title": null,
  "imported_at": "ISO-8601",
  "raw_media_retained": false,
  "training_allowed": false,
  "public_share_allowed": false,
  "license_basis": "embed | user_original | explicit_license | facts_only | private_reference",
  "extraction_confidence": {},
  "user_confirmed": false
}
```

Provenance survives edits and recipe forks. Removing the visible source field never removes the underlying audit record.

## Public-share sanitizer

Before creating a community post, build a new allowlisted payload rather than copying the private recipe object and deleting selected fields.

Allowed by default:
- user's own title and summary
- user's own finished-food media
- user's tested substitutions
- actual effort, time, cleanup, sensory notes, and review
- user-authored rewritten instructions
- original source attribution and link
- licensed or official embed identifiers within their permitted scope

Excluded by default:
- imported screenshots and crops
- downloaded source videos
- copied source photography
- full source transcripts or captions
- copied expressive directions
- temporary OCR text
- private notes and household context
- hidden provenance/audit data

A user cannot override excluded source-media classes merely by checking a generic “I have permission” box. Creator-owned media needs verifiable ownership or a recorded license.

## Creator controls

Public launch requires:
- report/claim action on every attributed entry
- copyright and impersonation report categories
- creator identity verification path
- rapid unpublish/temporary hide capability
- counter-notice and appeal process designed with counsel
- repeat-infringer policy
- immutable moderation/audit history
- block future imports from a creator or domain when legally required
- attribution correction without losing user notes

Removal of source media does not need to delete a user's genuinely original private notes. Public availability and private recipe memory are separate records.

## Platform-specific implementation

### TikTok
Use supported embed or Display API behavior where available. Preserve creator attribution and a route to the original post. Do not infer reuse permission from the platform download setting.

### YouTube
Use the official embedded player and approved metadata APIs. Deep-link to useful timestamps. Do not download video or assume public captions can be copied into the product. Creator-authorized integrations may expose richer step-level clips.

### Recipe websites
Prefer clearly exposed Recipe structured data and publisher partnerships. Respect access controls and source terms. Convert functional facts into newly written action steps; do not reproduce page photography, stories, or distinctive prose by default.

## Visual Cook Path media order

1. User's own media.
2. Verifiably licensed creator media.
3. Official platform embed or timestamped deep link.
4. Body Kitchen's original diagrams/action animations.
5. Text-only accessible fallback.

Generated visuals illustrate arrangement and technique. They are not evidence of safe internal temperature, food freshness, allergen absence, or doneness.

## Privacy and security requirements

- encrypted transit and temporary storage
- short server-side TTL enforced independently of app state
- deletion verification and retention metrics
- no filename persistence when unnecessary
- malware/type/size validation
- private-by-default imports
- no training by default or bundled consent
- account export excludes expired source blobs because they no longer exist
- deletion and community-unpublish are distinct operations
- logs contain object IDs and policy events, not image contents

## Acceptance tests

1. Screenshot processing completes and the raw object is absent after TTL.
2. Failed OCR leaves no permanent source blob.
3. Community serializer cannot emit screenshot/crop fields.
4. Imported TikTok/YouTube entries contain an embed/deep link, never a downloaded asset URL.
5. A private recipe's notes survive public source-media removal.
6. Creator claim immediately hides affected public media while preserving the audit record.
7. Training datasets reject every item where `training_allowed` is not explicitly true under a separate valid license.
8. User can understand attribution and privacy without completing a legal questionnaire.
