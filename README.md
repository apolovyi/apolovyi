# Artem Polovyi

**Software engineer and architect.** I design and build systems across business workflows, application boundaries, external integrations and operational delivery.

## System architecture and end-to-end delivery

### YMart: from supplier files to reviewed storefront updates

Operators can turn supplier files into reviewed storefront updates, see which changes succeeded and handle partial failures. I designed and built YMart across backend integrations, the YourMix operations workspace, asynchronous ingestion, infrastructure and delivery.

The architecture connects Acumatica ERP and CS-Cart through one modular workflow application, while isolating file parsing as a separate workload. Local catalogue projections support operational queries; approval is separate from application. Item-level results, retries and compensating reverts support recovery from partial writes.

OpenAPI compatibility checks help prevent breaking API changes; GitHub Actions uses AWS OIDC for backend delivery without stored AWS deployment keys. CloudWatch and Grafana/Loki support diagnosis. The application uses Kotlin/Spring Modulith, PostgreSQL and React, with Terraform-managed AWS.

[Project and implementation](https://github.com/apolovyi/yourmix-showcase) · [Architectural decisions and trade-offs](https://github.com/apolovyi/yourmix-showcase/blob/main/ARCHITECTURE.md)

## Engineering tools and runtime reliability

I maintain these developer-tool forks:

- **[Pi MCP Adapter](https://github.com/apolovyi/pi-mcp-adapter):** unhandled tool failures stop dependent operations instead of allowing a broken workflow to continue; arguments that fail schema validation are rejected before reaching the remote tool.
- **[Pi](https://github.com/apolovyi/pi):** long-running coding sessions can recover from compaction failures rather than remain stuck, with earlier summaries retained during split-turn compaction. Extensions can observe the compaction lifecycle.

## Health history and device pairing

In my **[OpenStrap Edge fork](https://github.com/apolovyi/openstrap-src)**, incomplete device data does not prematurely replace imported health records in SQLite. The Dart/Swift pairing flow waits for iOS accessory authorization rather than treating picker presentation as success.

## Other projects

[Personal website](https://github.com/apolovyi/apolovyi-web) · [Turkey travel blog](https://github.com/apolovyi/turkeynomad-blog)
