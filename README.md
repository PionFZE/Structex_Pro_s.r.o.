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
    subgraph data_layer["Data Layer"]
        ds[(Джерела даних)]
        pp[Preprocessing]
        fs[Feature Store]
    end
    subgraph model_layer["Model Layer"]
        mt[Model Training]
        mr[Model Registry]
    end
    subgraph serving_layer["Serving Layer"]
        inf[Inference Engine]
        api[API Gateway]
    end
    ds --> pp --> fs
    fs --> mt --> mr
    mr --> inf --> api

## Workflow Model

+———––+     +––––––––+     +———––+ | Data Intake | –> | Preprocessing  | –> | Model Train | +———––+     +––––––––+     +———––+ |                 | v                 v +———–+     +–––––+ | Validate? | –> | Deploy   | +———–+     +–––––+ |                 | | No              | Yes v                 v +———–+     +–––––+ | Retrain   | <– | Monitor  | +———–+     +–––––+
