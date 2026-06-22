
# progresssoft-k8s-assessment

A complete Kubernetes + Git + Helm environment built for the ProgressSoft Support & Implementation Engineer technical assessment.

## What's in this repo

| File | Task | Description |

|------|------|-------------|

| `nginx-deployment.yaml` | Task 2 | nginx Deployment — 2 replicas |

| `nginx-service.yaml` | Task 2 | NodePort Service on port 30080 |

| `configmap.yaml` | Task 3 | ConfigMap — APP_MODE, APP_NAME |

| `secret.yaml` | Task 3 | Secret — DB_USER, DB_PASSWORD |

| `nginx-with-config.yaml` | Task 3 | Deployment with env vars injected |

| `my-nginx-chart/` | Task 4 | Custom Helm chart |

## Quick start

```bash

minikube start --driver=docker

kubectl apply -f nginx-deployment.yaml

kubectl apply -f nginx-service.yaml

kubectl apply -f configmap.yaml

kubectl apply -f secret.yaml

kubectl apply -f nginx-with-config.yaml

kubectl get pods && kubectl get svc

```

## Helm

```bash

helm install my-nginx-release my-nginx-chart

helm history my-nginx-release

helm upgrade my-nginx-release my-nginx-chart --set replicaCount=3

helm rollback my-nginx-release 1

```

## Git workflow

Feature branch, pull request, merge, and a deliberate merge conflict resolved manually.

---

**Candidate:** Yaqeen Alasouli | Support & Implementation Engineer

