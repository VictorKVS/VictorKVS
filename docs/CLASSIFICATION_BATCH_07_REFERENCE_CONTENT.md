# Classification Batch 07 — Reference / Content-Risk Repositories

This batch is non-destructive. It applies the portfolio rule that inactivity permits review only; it does not authorize deletion, archival mutation, or merge.

## Decisions

| Repository | Evidence reviewed | Classification | Portfolio action |
|---|---|---|---|
| `guides` | Last visible commit 2025-09-28. Repository history and commit messages show course/tooling guides and instructional material rather than a current product. | `LEARNING` | Preserve as reference/learning history; exclude from Featured Engineering. |
| `hackerspace-blueprint` | Last visible commit 2025-04-01. README is a Polish adaptation/translation of the external Hackerspace Blueprint and explicitly points to the upstream `0x20/hackerspace-blueprint` project. | `ARCHIVE` | Preserve as external/reference lineage; do not present as an original product or current engineering deliverable. |
| `hacking-books` | Public repository is large (~266 MB). README enumerates a collection of commercial/technical security books rather than original implementation evidence. | `ARCHIVE` | Exclude from product and learning showcase until provenance/licensing of hosted material is reviewed. Treat as `CONTENT-RISK REVIEW`; do not copy or surface book files on the portfolio site. |
| `294-book` | Public repository is very large (~552 MB). Root inspection shows many full PDF books/labs (for example Security+ labs and commercial programming/security titles) while README is only `294-book`. | `ARCHIVE` | Exclude from all public showcase surfaces until provenance/licensing is reviewed. Treat as `CONTENT-RISK REVIEW`; no deletion is authorized by this classification. |

## Risk note

`hacking-books` and `294-book` are not product candidates. Their public contents may include third-party copyrighted material. Portfolio normalization must not amplify, mirror, quote, or republish those files. The correct next step is a separate provenance/licensing review by the repository owner before any visibility or retention decision.

## Protected boundaries

This batch does not modify `PX00`, `KNOWLEDGE_CORE`, `KNOWLEDGE_MASTER`, any active/future KB repository, or recently active product work.
