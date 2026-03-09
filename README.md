# OCI IaC Pipeline with Drift Detection

Automated infrastructure provisioning pipeline using OCI DevOps,
Terraform, and Resource Manager — running entirely within OCI Always Free tier.

## Architecture
- OCI DevOps Build Pipeline → validates and scans Terraform code
- OCI Resource Manager → runs terraform apply (no local runner needed)
- OCI Vault → encrypts state and stores secrets
- OCI Object Storage → remote Terraform state backend
- Python drift detector → blocks deployments on infrastructure divergence

## Stack
- Terraform 1.7+
- OCI Provider 6.x
- Python 3 + OCI SDK
- tfsec (policy scanning)

## Projects Status
- [x] Project structure
- [ ] Terraform modules
- [ ] OCI DevOps pipeline
- [ ] Drift detection script
- [ ] Hardening
