# Agent Prompt: Push BCP v1.2.1 to Encoded-Brands/bcp

## Your task

Push the contents of this package to the `bcp` repository in the `Encoded-Brands` GitHub organization. You are operating as the `Bruiserhq` GitHub user. Use `gh` CLI; assume it is authenticated.

This is the Brand Context Protocol baseline for Encoded Brands itself — the proof-of-concept BCP that demonstrates the standard. The files have already been through three rounds of evaluator review (final score 25/25). Your job is to commit and push, not to revise content.

## Files in this package

```
encoded-brands-bcp/
├── .well-known/
│   ├── brand.md
│   └── brand/
│       ├── voice.md
│       ├── values.md
│       ├── boundaries.md
│       ├── claims.md
│       └── representation.md
├── eval/
│   └── 2026-05-07-baseline.md
├── encoder/
│   └── eval/
│       └── results-row.tsv
└── README-AGENT.md  (this file)
```

## What to do

### Step 1: Clone the target repo

```bash
gh repo clone Encoded-Brands/bcp
cd bcp
```

If the repo does not exist yet, create it as a public repo under the org and initialize the structure:

```bash
gh repo create Encoded-Brands/bcp --public --description "Brand Context Protocol — open standard maintained by Encoded Brands. CC BY 4.0."
```

### Step 2: Place the BCP tree

Copy the six BCP files from this package into the repo at the standard path:

```bash
mkdir -p .well-known/brand
cp /path/to/package/.well-known/brand.md .well-known/brand.md
cp /path/to/package/.well-known/brand/voice.md .well-known/brand/voice.md
cp /path/to/package/.well-known/brand/values.md .well-known/brand/values.md
cp /path/to/package/.well-known/brand/boundaries.md .well-known/brand/boundaries.md
cp /path/to/package/.well-known/brand/claims.md .well-known/brand/claims.md
cp /path/to/package/.well-known/brand/representation.md .well-known/brand/representation.md
```

### Step 3: Place the eval record

```bash
mkdir -p eval
cp /path/to/package/eval/2026-05-07-baseline.md eval/2026-05-07-baseline.md
```

### Step 4: Append the TSV row to encoder eval results

The file `encoder/eval/results.tsv` should already exist with a header row in the `Encoded-Brands/encoder` repo (separate repo from this one). The provided file `results-row.tsv` is a single row to APPEND, not overwrite.

If the encoder repo lives separately at `Encoded-Brands/encoder`:

```bash
cd ..
gh repo clone Encoded-Brands/encoder
cd encoder
cat /path/to/package/encoder/eval/results-row.tsv >> eval/results.tsv
```

If `eval/results.tsv` does not exist yet, create it with a header first:

```bash
mkdir -p eval
echo -e "date\tsession_id\tcommit_or_na\tspecificity\tvoice_fidelity\tboundary_coverage\tclaims_rigor\trepresentation_accuracy\ttotal\tmodel\tbrand\tkeep_or_discard\tnotes" > eval/results.tsv
cat /path/to/package/encoder/eval/results-row.tsv >> eval/results.tsv
```

Commit and push the encoder repo separately:

```bash
git add eval/results.tsv
git commit -m "eval: append Encoded Brands baseline (25/25) to results.tsv"
git push
```

### Step 5: Commit and push the bcp repo

Back in the bcp repo, commit in two logical commits so the history is clean.

**Commit 1: the BCP tree**

```bash
cd ../bcp
git add .well-known/
git commit -m "bcp: v1.2.1 baseline for Encoded Brands

Three-pass evaluator review, final score 25/25.

- v1.0 baseline scored 9/25 (claims rigor 1, all others 2).
- v1.1 first rewrite scored 20/25 after structural fixes.
- v1.2 simplicity pass scored 25/25 with per-unit tightening.
- v1.2.1 texture repair on voice.md and values.md to address
  simplicity failure mode (cutting for symmetry, compound entries
  hurting agent word-filtering).

Mid-eval correction: aspirational partners (Zefr, brand launch
cohort) moved to claims.md aspirational with state_as and
verification_trigger fields. Hard_no added against naming any
party as partner until signed and approved.

License: CC BY 4.0."
```

**Commit 2: the eval record**

```bash
git add eval/2026-05-07-baseline.md
git commit -m "eval: 2026-05-07 baseline review of Encoded Brands BCP

Full critique, score progression across three passes, encoder
questions to add to encoder-v1.md, texture repair notes.

Disposition: keep. Final score 25/25."
```

**Push:**

```bash
git push
```

### Step 6: Verify

```bash
gh repo view Encoded-Brands/bcp --web
```

Confirm:
- Six BCP files render correctly at `.well-known/brand.md` and `.well-known/brand/*.md`
- Eval record is present at `eval/2026-05-07-baseline.md`
- Two commits with the messages above appear in history
- TSV row is appended to `Encoded-Brands/encoder/eval/results.tsv` (separate repo)

## What NOT to do

- Do not edit the content of any BCP file. They are at v1.2.1 final.
- Do not overwrite `results.tsv` — append only.
- Do not commit a single monolithic commit. The two-commit structure (BCP tree, then eval record) keeps history clean.
- Do not push to `main` directly if the repo has branch protection; open a PR instead with the same commit structure.

## If the repo has branch protection

```bash
git checkout -b bcp-v1.2.1-baseline
# ... commits as above ...
git push -u origin bcp-v1.2.1-baseline
gh pr create --title "BCP v1.2.1 baseline + 2026-05-07 eval record" \
  --body "Three-pass evaluator review, final score 25/25. See eval/2026-05-07-baseline.md for full record."
```

## Confirmation

When done, post a confirmation message back to the user containing:
- The commit SHAs for both commits in `Encoded-Brands/bcp`
- The commit SHA for the TSV append in `Encoded-Brands/encoder`
- The PR URL if a PR was opened

Format:

```
Pushed v1.2.1 to Encoded-Brands/bcp:
- BCP tree:  <sha1>
- Eval record: <sha2>

Appended TSV row to Encoded-Brands/encoder:
- <sha3>

PR (if applicable): <url>
```
