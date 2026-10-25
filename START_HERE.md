# Start here
[English](START_HERE.md) · [Français](START_HERE.fr.md) · [Station](README.md)

Station is NeoMundi's product entry point: an instrument for observing AI responses under declared conditions and examining the associated measurements and evidence.

[**Explore all evidence →**](EVIDENCE.md)

## Choose your path
| Your goal | Read next |
|---|---|
| Understand the instrument | [Station overview](README.md#what-it-does-in-plain-terms) |
| Inspect the records | [Public JSON schemas](schemas/) |
| Understand the terms | [Glossary](GLOSSARY.md) |
| Integrate the measurement API | [API documentation](https://github.com/neomundi-io/neomundi-runtime-measurement) |
| Use a client or agent connector | [Python SDK](https://github.com/neomundi-io/neomundi-python-sdk) · [MCP](https://github.com/neomundi-io/neomundi-measurement-mcp) |
| Examine methods and previous pilots | [Validation](https://github.com/neomundi-io/neomundi-metrology-validation) · [Use cases](https://github.com/neomundi-io/neomundi-use-cases) |
| See the planned work | [Roadmap](ROADMAP.md) |
| Discuss your own pilot | [contact@neomundi.io](mailto:contact@neomundi.io) |

## What you can do today
Read the schemas and documentation without an account. Hosted Station access is granted case by case; see [access conditions](README.md#access-to-the-station).
This repository contains the public contracts and documentation, not a deployable implementation. SDK and MCP are experimental and retain their own installation and licence conditions.

## What happens to your data
Distinguish four flows: AI execution; submission for measurement; internal records; disclosure or export to a consumer. The read-only interface and the interoperability export do not describe every internal flow.
A field in a client interface does not prove that it is sent in every mode. Equally, an export without raw text does not prove that no text is processed upstream.
The planned architecture review will document actual payloads, destinations and retention per mode before making broader privacy claims. A metrics-only SDK mode is not announced as available.

## Public documentation and pilot material
The glossary, contracts, limits and integration guidance belong in public documentation.
Pilot data, credentials and recipient-specific results are shared through controlled channels. Selected deeper documentation may be shared under NDA according to its scope; an NDA is not permission to access secrets or another pilot's data.

Prior studies retain their own provenance. They are not evidence that Station produced those results.
