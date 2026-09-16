This directory contains C4 diagrams (PlantUML) for MeterForge derived from the content in documentation/01-Problem_understanding.

Files:
- 01-context.puml    : System context diagram
- 02-containers.puml : Container-level architecture
- 03-components.puml : Component diagrams for Billing Engine and Ingestion

To render (requires PlantUML + Graphviz):
- plantuml Architecture/01-context.puml
- or use an editor/IDE plugin that supports PlantUML

Notes:
- Diagrams reference the C4 PlantUML library via includeurl. An internet connection is required to fetch the library when rendering.
- The diagrams encode concepts from the documentation: tenant management, multi-tenancy, usage ingestion, billing, reconciliation, analytics, and integrations.


