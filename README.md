# CloudOps Action Hub — GitOps Repository

**Owner: Hafiz (`HafizMohammadSunasara`)**. Private repo target `cloudops-action-hub-gitops`.

This is a GitOps *foundation*, not a deployed cluster. Phase 2 allows an AWS ECS/Fargate pilot; adopting Kubernetes + Argo CD later should be a deliberate decision, not assumed in Phase 3. The repository keeps environment policy and placeholders under `environments/` so the deployment model can be implemented cleanly after approval.

## Environment structure

- `environments/dev/README.md`: development deployment promotion contract.
- `environments/staging/README.md`: validation gates before release.
- `environments/prod/README.md`: two-person release approval and rollback requirements.

No cluster credentials, application secrets, unreviewed production Kustomize manifests or AWS policy trust grants are stored here. When the production platform is chosen, introduce the correct ECS deployment GitOps flow **or** ArgoCD/Kustomize workloads, with immutable image digests and traceable release tags.
