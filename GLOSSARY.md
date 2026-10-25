# Glossary
[English](GLOSSARY.md) · [Français](GLOSSARY.fr.md) · [Start here](START_HERE.md)

A reading guide. Field names and allowed values remain defined by the versioned schemas and contracts.

| Term | Meaning here |
|---|---|
| Observation | A record of an AI execution under declared conditions. |
| Measurement | A result associated with a method, a version and an execution context. |
| Reference evaluation | Evaluation against a declared reference; kept separate from measurement signals. |
| Interpretation | The meaning a person or consuming system assigns to a result. |
| Coverage | Which expected measurement components were actually available, according to the applicable contract. |
| Complete / partial | Result states defined by the applicable contract; a successful HTTP response alone does not establish completeness. |
| Refusal | A result that cannot be qualified, recorded with its reason under Station's contract. It is not a zero. |
| Null | Absence of a value under the applicable field definition; distinct from a measured zero. |
| Provenance | Origin, versions and conditions that produced a record. |
| Comparability | Conditions under which results can be compared; shared labels alone are insufficient. |
| Requested / served model | The model requested and the model attested as actually responding. |
| Ledger | Station's add-only record structure; corrections are new records referring to previous ones. |
| Integrity | Evidence that an artefact has not changed relative to its verification reference; not proof that its content is true. |
| Interoperability contract | A versioned exchange format for consumers, distinct from internal ledger schemas. |
| REST / SSE | Request-response interaction and server-sent event streaming. Neither transport establishes measurement validity. |
| Business station | Planned profession-specific protocols and configuration on a shared foundation, not a claim of current availability. |

Sources: [Station record schemas](schemas/) · [Metric Contract](https://github.com/neomundi-io/neomundi-metric-contract) · [Exchange contract](https://github.com/neomundi-io/neomundi-measurement-interoperability)
