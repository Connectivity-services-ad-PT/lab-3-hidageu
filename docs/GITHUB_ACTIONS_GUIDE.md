# GitHub Actions Guide

Workflow nằm tại `.github/workflows/newman.yml`.

CI thực hiện:

1. Install dependencies
2. Lint OpenAPI contracts
3. Start Prism mock server
4. Wait until mock server ready
5. Run Newman
6. Upload reports
