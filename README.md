# cloud-audit-scripts

Read-only audit scripts for cloud infrastructure. Designed for security reviews, compliance checks, and cost optimization.

All scripts are **read-only** — no resources are created, modified, or deleted.

## Setup

```bash
git clone https://github.com/dhayv/cloud-audit-scripts.git
cd cloud-audit-scripts
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

Configure AWS credentials via `aws configure` or environment variables. Scripts use the default profile and region unless flags are added later.

## Scripts

| Script | Purpose | Status |
|---|---|---|
| `s3_audit.py` | Reports public S3 buckets, missing encryption, missing versioning | In progress |

## Requirements

- Python 3.10+
- AWS credentials with read-only permissions on the services being audited
