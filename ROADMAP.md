# Station roadmap
[English](ROADMAP.md) · [Français](ROADMAP.fr.md) · [Start here](START_HERE.md)

Direction agreed on 25 October 2026. This page describes work to do, not released capabilities or delivery dates.

| Priority | Workstream | Completion evidence |
|---|---|---|
| 1 | Organize GitHub around Station | Bilingual organization profile, public documentation paths, consistent links from integration and evidence repositories. |
| 2 | Align documentation with actual architecture | Versioned flow map tracing actual client payloads, service destinations, internal storage and consumer exports for each supported mode. |
| 3 | Consolidate MCP: REST and SSE | Both measurement interaction modes tested; tools, endpoint versions, authentication, errors, interruption and terminal results documented. MCP client transport is documented separately from downstream measurement transport. |
| 3 | Consolidate Python SDK: REST and SSE | Tested request-response and streaming interfaces, version compatibility, preserved states and nulls, explicit timeout and retry behavior. |
| 4 | Qualify releases and usage rights | Licence decisions, reproducible installation, compatibility matrix and release notes. |
| 5 | Publish Station experiments progressively | Each published result has an approved protocol, execution regime, provenance, versions, coverage and limits. |
| 6 | Connect observation programs and business stations | Validated exports, explicit series boundaries, profession-specific protocols and acceptance criteria. |

## How we will check it works
- REST and SSE preserve the same applicable measurement semantics; streaming chunks remain distinct from the final result.
- Partial measurements and null values remain visible; transport errors are not invented measurement states.
- Interruptions, cancellation, timeouts and retries have explicit behavior; retries must not silently duplicate a paid generation.
- Requested and served model information and applicable versions are preserved when supplied.
- Authentication and per-client access boundaries are tested before wider distribution.
- Payload minimization follows verified implementation. A metrics-only mode requires evidence of local calculation and sufficient provenance for the claimed metrics.
- Documentation distinguishes replay, synthetic tests and actual provider executions.

## Simplify GitHub
Migrate unique material and verify consumers, CI, Pages, citations and links before archiving a superseded repository.
Preserve historical studies and their provenance. No repository is scheduled for deletion by this roadmap.

## What is available
Station's [current access conditions](README.md#access-to-the-station) remain applicable.
The planned dashboard and business stations must be described as planned until their behavior has been demonstrated.
