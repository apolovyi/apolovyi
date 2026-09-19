# Artem Polovyi

**Software engineer and architect.** I design and build systems across business workflows, application boundaries, external integrations and operational delivery. My focus is explicit ownership and recoverable failure, with complexity proportionate to the problem.

## System architecture and end-to-end delivery

### YMart: from supplier files to reviewed storefront updates

Operators can turn supplier files into reviewed price proposals, apply approved changes and inspect individual write outcomes. I designed and built YMart across backend integrations, the YourMix operations workspace, asynchronous ingestion, infrastructure and delivery.

The architecture connects Acumatica ERP and CS-Cart through one modular workflow application, while isolating file parsing as a separate workload. Local catalogue projections support operational queries; approval is separate from application so an operator's decision is not confused with a successful external write.

OpenAPI compatibility checks help prevent breaking API changes; GitHub Actions uses AWS OIDC for backend delivery without stored AWS deployment keys. CloudWatch and Grafana/Loki support diagnosis. The application uses Kotlin/Spring Modulith, PostgreSQL and React, with Terraform-managed AWS.

[Project and implementation](https://github.com/apolovyi/yourmix-showcase) · [Architectural decisions and trade-offs](https://github.com/apolovyi/yourmix-showcase/blob/main/ARCHITECTURE.md)

## Engineering tools and runtime reliability

I maintain forks of developer tools, working on the execution and lifecycle contracts around coding agents:

- **[Pi MCP Adapter](https://github.com/apolovyi/pi-mcp-adapter):** failed calls stop dependent execution unless explicitly handled; invalid arguments are rejected before approval or dispatch. My changes also address helper-process cleanup without losing buffered output.
- **[Pi](https://github.com/apolovyi/pi):** my changes help long-running agent sessions recover from failed compaction and make that lifecycle visible to extensions. I restored automatic retries after cooldown and exposed typed lifecycle events, while separating compaction trigger and summary budgets and retaining prior summaries during split-turn compaction.

Each fork's overview links the design decisions to implementing changes and regression tests.

## Data integrity and asynchronous state

In my **[OpenStrap Edge fork](https://github.com/apolovyi/openstrap-src)**, I preserve imported records until measured replacements are complete and settled, and make iOS pairing wait for accessory authorization rather than picker presentation. The changes exercise data ownership and device lifecycle across Dart, SQLite and Swift.

## Other projects

[Personal website](https://github.com/apolovyi/apolovyi-web) · [Turkey travel blog](https://github.com/apolovyi/turkeynomad-blog)
