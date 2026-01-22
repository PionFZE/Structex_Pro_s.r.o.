# Structex_Pro_s.r.o.

# AI Core System Architecture Demo

Demonstration of Architecture and Engineering for AI Core Systems by Structex Pro

## Layers
- **Data Layer**: Kafka ingestion, Feast features [web:1]
- **Model Layer**: Kubeflow pipelines, MLflow registry
- **Serving Layer**: KServe inference

## Diagram (Mermaid)
```mermaid
graph TD
    A[Data Sources] --> B[Preprocessing]
    B --> C[Feature Store]
    C --> D[Training]
    D --> E[Registry]
    E --> F[Inference]

##Architecture Diagram
[Architecture](diagrams/architecture.mmd)
