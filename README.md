## Repository structure
```
gitops-repo/
├── bootstrap/                  # ArgoCD bootstrap resources
│   ├── kustomization.yaml
│   └── argocd-install.yaml
├── clusters/                   # Cluster-specific configurations
│   ├── production/
│   │   ├── apps.yaml           # References to apps for this cluster
│   │   └── infrastructure.yaml # References to infra components
│   └── staging/
│       ├── apps.yaml
│       └── infrastructure.yaml
└── apps/                       # Application definitions
    ├── monitoring/             # Monitoring stack
    │   ├── prometheus/
    │   │   ├── kustomization.yaml
    │   │   ├── values.yaml     # Helm values overrides
    │   │   └── release.yaml    # Helm release definition
    │   └── grafana/
    │       ├── kustomization.yaml
    │       ├── values.yaml
    │       └── release.yaml
    └── other-apps/
```