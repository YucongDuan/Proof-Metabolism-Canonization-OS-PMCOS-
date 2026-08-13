# Proof Metabolism & Canonization OS (PMCOS)

**A post-proof compiler for the era of proof abundance**

Authors: **Yucong Duan · Feng Wang**  
Version: **1.0.0** · 2026

PMCOS addresses a new bottleneck in mathematics: proof generation and machine verification can accelerate faster than human exposition, expert review, independent reconstruction, curricular absorption, and canonicalization.

It therefore refuses to build another proof generator. Instead, it transforms an existing proof artifact into a **Proof Passport** and a set of downstream knowledge-work objects:

- a non-aggregated six-stage lifecycle vector;
- a compact proof spine;
- a high-friction hinge map;
- a native-claim/external-alias bridge registry;
- an independent reconstruction suite;
- an expert talk-test packet;
- canonization candidates and textbook routes;
- a corpus metabolism atlas without a single leaderboard;
- deterministic release and replay ledgers.

## The breakthrough: friction conservation

AI-polished mathematical prose can erase the visible distinction between routine steps and genuinely novel hinges. PMCOS treats this as a form of **exposition debt**.

A high-load hinge must not be made to look trivial merely by smoother prose. Compression is permitted only when explanatory structure is added: dependency maps, worked local cases, bridge obligations, reader checkpoints, and independent reconstruction tasks.

## Six stages, no total score

PMCOS registers:

1. generation;
2. verification;
3. exposition;
4. publication;
5. digestion;
6. canonicalization.

The vector is deliberately non-aggregated. Machine verification cannot compensate for missing statement fidelity; publication cannot compensate for missing human reconstruction; a polished explanation cannot compensate for an unresolved external bridge.

## Quick start

No third-party runtime dependencies are required.

```bash
python run_demo.py
```

Or:

```bash
python -m proofmetabolism demo --out outputs/reference
python -m proofmetabolism audit examples/sample_semantic_proof.json --out outputs/one
python -m proofmetabolism corpus examples/manifests/*.json --out outputs/corpus
python -m proofmetabolism scan /path/to/local/repository --out outputs/scanned
```

Open:

```text
site/index.html
```

## Optional GitHub harvest

```bash
python -m proofmetabolism harvest \
  --owner YucongDuan \
  --query proof \
  --limit 100 \
  --out outputs/github
```

Set `GITHUB_TOKEN` for higher API limits. Harvested records are triage manifests only; they are not theorem certificates.

## Core outputs

For one proof:

```text
proof_passport.json
proof_passport.md
lifecycle_vector.json
friction_map.json
canonization_map.json
reconstruction_suite.json
reconstruction_suite.md
talk_test.md
digestion_debt.md
dashboard.html
release_hash_ledger.json
```

For a corpus:

```text
corpus_atlas.json
corpus_atlas.csv
corpus_dashboard.html
release_hash_ledger.json
```

## Interoperability

Adapters are included for:

- native PMCOS manifests;
- generic JSON and Markdown;
- ProofLedger-style claim/evidence packages;
- MATHWEAVE-style proof-exchange packets;
- FIDELIS-style fidelity-status packets;
- public GitHub README metadata.

## Scientific boundary

PMCOS does **not** certify that:

- a mathematical theorem is true;
- a classical open problem has been solved;
- an internal semantic closure is externally recognized;
- a finite computation proves an unbounded statement;
- a human understands a proof;
- a published result is canonical knowledge.

It certifies only the consistency of its own registry and generated audit artifacts. Human understanding requires identified human reconstruction and questioning; community acceptance and canonicalization require community processes.

## Representative public corpus seed

The bundled corpus seed is a representative audit of selected proof and proof-infrastructure repositories in Yucong Duan's public GitHub profile. It is deliberately conservative and records repository self-descriptions and declared boundaries. It is not a complete audit of all repositories, nor an independent certification of any theorem claim.

## License

Apache-2.0. See `LICENSE` and `NOTICE`.

## Release layout

```text
reports/                  Chinese and English reports in DOCX and PDF
assets/figures/           bilingual publication figures
proofmetabolism/          dependency-free Python runtime core
schemas/                  Proof Passport and human-attestation JSON Schemas
examples/                 single-proof examples and the twelve-repository corpus seed
outputs/reference/        replayed single-proof and corpus-atlas outputs
site/                     offline entry page and sample dashboard
dist/                     offline-installable Python wheel
```

## Offline wheel installation

```bash
python -m pip install --no-index dist/proofmetabolism-1.0.0-py3-none-any.whl
pmcos audit examples/sample_semantic_proof.json --out outputs/one
pmcos corpus examples/manifests/*.json --out outputs/corpus
```

The release has passed six automated tests, direct source execution, offline wheel installation in a clean virtual environment, single-proof audit generation, reconstruction of the twelve-repository corpus atlas, and release-hash verification. These checks establish software and registry consistency; they do not certify the external truth of any mathematical theorem.
