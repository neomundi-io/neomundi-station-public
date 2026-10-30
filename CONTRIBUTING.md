**English** · [Français](CONTRIBUTING.fr.md)

# Contributing — what is possible here, and what is not

Thank you for your interest. **Read this file before opening anything**: this repository does not accept the kind of contribution normally associated with a public repository.

> **Legal notice.** No licence is declared for this repository: **all rights reserved**. A contribution is therefore **not** covered by an open-source licence, and no contribution agreement currently exists. **Before investing time, open an issue** — we do not want to accept work whose status would be ambiguous.

## What this repository is

**The public surface of a measurement instrument.** Not a library, not a product to install, and not a demonstration.

🔴 **It does not contain the implementation.** The implementation is private. There is therefore **no code to fix, test to write or dependency to update** here, and a pull request proposing one would be refused — not as a matter of principle, but because it would have nothing to modify.

## What is useful, in order of value

| | What you can report | Why it matters |
|---|---|---|
| **1** | 🔴 **A schema that inaccurately describes what the registry records** — a field marked required when it is not, a missing constraint, an ambiguous description | A third party verifying evidence relies on these contracts. **If they misrepresent the record, the verification is worthless** |
| **2** | **A scientific defect** — a measure that does not measure what it claims, a series that mixes two comparability keys, a zero treated as a measurement | These are the reports we value most |
| **3** | **An unsupported claim in the documentation** — an advertised capability established by nothing, a number without provenance | This repository requires every number to carry its provenance. Hold us to that rule |
| **4** | **An inconsistency between this repository and Station** — what is written here differs from what the instance does | Both must say the same thing |
| **5** | **A language error or dead link** | Useful and welcome, but the least critical category |

**NEVER report a security vulnerability through an issue:** see [SECURITY.md](SECURITY.md).

## How to report

Open an **issue** and state three things:

1. **what you read or called** — the file or route;
2. **what you expected**;
3. **what you observed**, with enough information to reproduce it.

If you write *“verified”*, **show the output.** We apply that rule to ourselves, and we apply it to you as well.

## What will be refused

- **a schema change without a demonstration.** A schema describes a real registry: changing it without showing what the registry actually writes would break the contract instead of correcting it;
- **an open-source licence proposal.** The legal regime is an open decision, and it will not be settled in a pull request;
- **a composite score, a model ranking, or an aggregation across a comparability key.** The instrument rejects all three by design;
- **a secret, key or token** — even a fake one if it looks plausible;
- **third-party dataset content.** Only manifests circulate, together with their fingerprints and declared licence;
- **a default value that hides an absence.** **null is not zero**;
- **a capability claim unsupported by an execution.**

## What we will not ask of you

Speed. This repository moves forward by showing its evidence, and a report that takes one extra day to establish a fact through execution rather than reading is a better report.
