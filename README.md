# cloud-audit-scripts

Read-only audit scripts for cloud infrastructure. Designed for security reviews, compliance checks, and cost optimization.

All scripts are **read-only** — no resources are created, modified, or deleted.

## Setup

This project uses [uv](https://docs.astral.sh/uv/) for dependency and environment management.

```bash
git clone https://github.com/dhayv/cloud-audit-scripts.git
cd cloud-audit-scripts
uv sync
```

Run a script:

```bash
uv run python s3_audit.py
```

Add a dependency:

```bash
uv add <package>
```

Configure AWS credentials via `aws configure` or environment variables. Scripts use the default profile and region unless flags are added later.

## Scripts

| Script | Purpose | Status |
|---|---|---|
| `s3_audit.py` | Reports public S3 buckets, missing encryption, missing versioning | In progress |

## Requirements

- Python 3.13+
- [uv](https://docs.astral.sh/uv/getting-started/installation/)
- AWS credentials with read-only permissions on the services being audited
