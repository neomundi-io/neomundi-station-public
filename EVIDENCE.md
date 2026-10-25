<div align="center">

<sub><b>English</b> · <a href="EVIDENCE.fr.md">Français</a></sub>

# Explore Evidence

### Pilots. Observations. Methods. Historical work.

**The work behind NeoMundi, with its sources and limits.**

[![Pilots](https://img.shields.io/badge/Explore-Pilots-2563eb?style=flat-square)](#pilots)
[![Observatory](https://img.shields.io/badge/Explore-Observatory-0f766e?style=flat-square)](#observatory)
[![Methods](https://img.shields.io/badge/Explore-Methods-8b5cf6?style=flat-square)](#methods)
[![Archives](https://img.shields.io/badge/Explore-Archives-64748b?style=flat-square)](ARCHIVES.md)

[Station](README.md) · [Start here](START_HERE.md) · [Evidence catalogue](evidence/catalog.json)

</div>

---

## What you can examine

NeoMundi's evidence comes from pilot work, the Observatory's accumulated observations,
measurement qualification and external methodological critique.
These materials do not all establish the same thing. A protocol, a synthetic test,
a field report and a reproducible dataset have different roles.

**Station is the next product entry point. Earlier results keep their original
instrument, protocol and provenance; they are not relabelled as Station results.**
This library indexes sources rather than copying their data.

Reviewed on **25 October 2026**: repository documentation, file inventories and selected
manifests and reports. This review did not rerun the experiments, recompute all results,
or independently reproduce partner claims.

## Pilots

[**Open the pilot index →**](https://github.com/neomundi-io/neomundi-use-cases)

The existing index remains the detailed source for pilot descriptions. Its status labels
describe a stated scope; the public material available to inspect is identified below.

| Pilot | Public material | Scope and current limit |
|---|---|---|
| [OASSE](https://github.com/neomundi-io/use-case-oasse-runtime-governance/tree/main/public_evidence) | Sanitized evidence for 60-request and 1,000-request controlled runs | Measurement, policy and enforcement remain separate. The 1,000 measured calls and 996 locally sealed calls have different denominators. |
| [AI Business — controlled audit](https://github.com/neomundi-io/use-case-aibusiness-runtime-conformity/tree/main/evidence) | Execution journal, receipts, validator outputs and measurement bridge artifacts | Controlled fictional service environment; not an insurance outcome or general reliability guarantee. |
| [FactNotebook](https://github.com/neomundi-io/use-case-factnotebook-pubmedqa) | Five-generation PubMedQA export, summary and integration feedback | Bounded ingestion and evidence reconstruction; no general factual or medical validation. |
| [Kabbalah App — RAG](https://github.com/neomundi-io/neomundi-use-cases/tree/main/evidence/kabbalah-app-rag) | Public field report and explanatory note | 60 instrumented generations per reported round. Alerts are signals, not independently established factual error rates. |
| [OmarAGI / REVAS](https://github.com/effacermonexistence/omaragi-neomundi-pilot) | Partner documentation of five synthetic signal mappings | Synthetic pilot; the live follow-up is described as planned. |
| [ManChine / RiCo](https://github.com/neomundi-io/use-case-rico-observation-to-admissibility) | Architectural documentation | No completed machine-to-machine run established by these materials. Terminology requires alignment with the pilot index. |
| [VERITAS](https://github.com/veritasfuji-japan/veritas_os/blob/main/docs/en/architecture/neomundi-rgc-v02-real-observation-poc.md) | Adapter code/tests and real-observation intake procedure | A procedure and adapter do not establish that a real handoff was completed. |
| [DriftShield / HIC](https://github.com/neomundi-io/neomundi-use-cases) | One execution reported in the index | Detailed public evidence package not identified in the reviewed sources. |
| [SEILX](https://github.com/neomundi-io/neomundi-use-cases) | Evaluation described in the index | In progress; no final result established here. |
| [AI Business — insurance](https://github.com/neomundi-io/neomundi-use-cases) | Evaluation described; related controlled audit exists | In progress; the controlled audit does not establish underwriting results. |

A further **OGS technical pilot** has been reported. Its supplied repository URL returned
404 during this review; it remains pending source access and is not counted as a verified result.

## Observatory

[**Open the Observatory →**](https://github.com/neomundi-io/neomundi-ai-observatory)

The Observatory is the research umbrella for repeated observations and accumulated
datasets. Barometer, Cartography and AI Weather are parts of this history, not
independent datasets to add again to an Observatory total.

The new direction organizes future publication around Station. It does not erase
previous work or establish that historical measurements are comparable with current ones.

## Methods

| Material | What it contributes | What it does not establish |
|---|---|---|
| [Metrology and methodology](https://github.com/neomundi-io/neomundi-metrology-validation) | Definitions, control protocols, claims registry and experimental roadmap | A roadmap is not a completed validation program. |
| [EXP-001 human review](https://github.com/neomundi-io/neomundi-metrology-validation/blob/main/results/EXP-001/EXP-001_smoke_test_human_review_FR.md) · [Run manifest](https://github.com/neomundi-io/neomundi-metrology-validation/blob/main/experiments/EXP-001/EXP-001_smoke_test_run_manifest.json) | Closed technical smoke test on 20 controlled synthetic cases | No general performance or scientific-validity claim. The report template under experiments is not the completed report. |
| [External methodological audit](https://github.com/neomundi-io/neomundi-metrology-validation/tree/main/external-audits) | Published critique and recommendations for stronger tests | An audit is distinct from validation and independent replication. |
| [G-score reproducibility study](https://github.com/neomundi-io/G-score-reproducibility-study) | Exploratory analysis, notebook, figures and reports based on historical barometer material | Raw data are not public; general invariance and independent replication are not established. |

## Archives

[**Explore the historical programs →**](ARCHIVES.md)

Historical means **retained with its original context**, not discarded or necessarily
archived through GitHub's archive setting. Public sources remain in their repositories.
Recent activity in a legacy pipeline is documented separately from its role in the new product direction.

## What comes next

Future Station experiments will enter this library only with a declared protocol,
execution regime, versions, coverage, source artifacts and explicit limits.
See [Station experiments](README.md#experiments) and the [roadmap](ROADMAP.md).

Source availability and experimental outcome are separate: an unavailable public package
does not prove a test failed, and a success label does not replace inspectable evidence.
