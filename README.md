# Artem Polovyi

**Software engineer and architect.** I design and build systems across business workflows, application boundaries, external integrations and operational delivery.

## System architecture and end-to-end delivery

### YMart: from supplier files to reviewed storefront updates

Operators can turn supplier files into reviewed price proposals, apply approved changes and inspect individual write outcomes. I designed and built YMart across backend integrations, the YourMix operations workspace, asynchronous ingestion, infrastructure and delivery.

The architecture connects Acumatica ERP and CS-Cart through one modular workflow application, while isolating file parsing as a separate workload. Local catalogue projections support operational queries; approval is separate from application.

OpenAPI compatibility checks help prevent breaking API changes; GitHub Actions uses AWS OIDC for backend delivery without stored AWS deployment keys. CloudWatch and Grafana/Loki support diagnosis. The application uses Kotlin/Spring Modulith, PostgreSQL and React, with Terraform-managed AWS.

[Project and implementation](https://github.com/apolovyi/yourmix-showcase) · [Architectural decisions and trade-offs](https://github.com/apolovyi/yourmix-showcase/blob/main/ARCHITECTURE.md)

## Engineering tools and runtime reliability

I maintain these developer-tool forks:

- **[Pi MCP Adapter](https://github.com/apolovyi/pi-mcp-adapter):** failed calls stop dependent execution unless explicitly handled; invalid arguments are rejected before approval or dispatch.
- **[Pi](https://github.com/apolovyi/pi):** my changes help long-running agent sessions recover from failed compaction, retain prior summaries during split-turn compaction, and expose lifecycle state to extensions.

## Data integrity and asynchronous state

In my **[OpenStrap Edge fork](https://github.com/apolovyi/openstrap-src)**, imported records in SQLite remain intact until measured replacements are complete and settled. My Dart/Swift changes make pairing wait for iOS accessory authorization rather than picker presentation.

## Other projects

[Personal website](https://github.com/apolovyi/apolovyi-web) · [Turkey travel blog](https://github.com/apolovyi/turkeynomad-blog)
