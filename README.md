<a href="https://x.com/sunilmehta_si">
  <img src="assets/hero.svg" width="100%" alt="Sunil Mehta — Lead DevOps, MLOps and Platform Engineer. The infrastructure behind AI platforms." />
</a>

<p align="center">
  <a href="https://sunilmehta.si"><strong>sunilmehta.si ↗</strong></a>
  &nbsp;&nbsp;·&nbsp;&nbsp;
  <a href="https://www.linkedin.com/in/sunilmehta-si/"><strong>LinkedIn ↗</strong></a>
  &nbsp;&nbsp;·&nbsp;&nbsp;
  <a href="https://orgn.com">Building at ORGN</a>
  &nbsp;&nbsp;·&nbsp;&nbsp;
  <a href="https://x.com/sunilmehta_si"><strong>Connect on X</strong></a>
</p>

## I build the infrastructure AI products run on.

I'm **Sunil Mehta**, a lead DevOps, MLOps and platform engineer and founding lead at **[ORGN](https://orgn.com)**. I work across cloud infrastructure, confidential computing, identity, and the systems that turn AI capabilities into dependable products.

My scope runs from `terraform plan` to production traffic: **Kubernetes and GitOps, confidential compute, and secure delivery pipelines**.

### Selected engineering work

| Area | What I've built and operated |
| :--- | :--- |
| **Confidential computing** | Hardware-isolated Kubernetes sandboxes on Intel TDX, with remote attestation and network policy. |
| **AI infrastructure** | An LLM gateway across providers, with metering, spend controls, and GitOps delivery. |
| **Cloud platforms** | Multi-cloud Kubernetes across GKE and DigitalOcean; Terraform across GCP and AWS; Argo CD reconciliation and keyless CI/CD. |
| **Identity & security** | An OAuth 2.1 / OIDC authorization server, and a zero-downtime migration onto GKE and Cloud SQL. |
| **Reliability & cost** | Prometheus, Grafana, OpenTelemetry, and ClickHouse; infrastructure cost reductions through right-sizing, consolidation, and scale-to-zero policies. |

*These highlights describe my professional experience. Most of the underlying work lives in private organization repositories.*

### Public engineering projects

**[Agentic Code Review Tool](https://github.com/sunilmehta-si/agentic-code-review-tool)** — Scanner-grounded AI review for the whole pull request: 58 rules across app code, Kubernetes, Docker, Terraform, GitHub Actions and AI/agent code (OWASP LLM Top 10, MCP configs, agent skills), only on changed lines, with an optional Claude or local-LLM agent that verifies findings using read-only, repository-confined tools.

Explore the [rule catalogue](https://github.com/sunilmehta-si/agentic-code-review-tool#built-in-rules), [GitHub Action](https://github.com/sunilmehta-si/agentic-code-review-tool#use-it-in-github-actions), and [threat model](https://github.com/sunilmehta-si/agentic-code-review-tool/blob/main/SECURITY.md).

**[AI DevSecOps CI/CD](https://github.com/sunilmehta-si/ai-devsecops-cicd)** — A reference pipeline for shipping LLM and AI-agent services safely: prompt-injection tests mapped to the OWASP LLM Top 10, SBOM and AI-BOM generation, Trivy and secret scanning, keyless cosign signing with attestations, and Kyverno admission policies with an offline validator mirroring them in CI.

Explore the [threat model](https://github.com/sunilmehta-si/ai-devsecops-cicd/blob/main/docs/threat-model.md), [AI security test corpus](https://github.com/sunilmehta-si/ai-devsecops-cicd/tree/main/tests/ai_security), and [workflows](https://github.com/sunilmehta-si/ai-devsecops-cicd/tree/main/.github/workflows).

**[Jev Inference Router](https://github.com/sunilmehta-si/jev-inference-router)** — An observable decision layer for local GPU inference: TypeSafe Jev chooses the handler, Python applies the policy, and local Qwen generates the answer, with visible probabilities, retrieval, Prometheus metrics, and reproducible evaluations against rule-based and classifier baselines.

Explore the [architecture](https://github.com/sunilmehta-si/jev-inference-router/blob/main/docs/architecture.md), [evaluations](https://github.com/sunilmehta-si/jev-inference-router/tree/main/evaluations), and [operations guide](https://github.com/sunilmehta-si/jev-inference-router/blob/main/docs/operations.md).

**[LLM Inference Platform](https://github.com/sunilmehta-si/llm-inference-platform)** — GPU-backed LLM serving on Apple Silicon with vLLM-Metal, a Python streaming gateway, Prometheus/Grafana monitoring, reproducible benchmarks, and Kubernetes deployment templates.

Explore the [architecture](https://github.com/sunilmehta-si/llm-inference-platform/blob/main/docs/architecture.md), [operational tests](https://github.com/sunilmehta-si/llm-inference-platform/tree/main/tests), and [benchmark evidence](https://github.com/sunilmehta-si/llm-inference-platform/tree/main/benchmarks).

### Tools I work with

**Infrastructure** &nbsp; Kubernetes · Terraform · Argo CD · Helm · GCP · AWS · DigitalOcean · Cloudflare<br/>
**Systems & services** &nbsp; Go · Rust · TypeScript · Python · PostgreSQL · Redis<br/>
**Security** &nbsp; Intel TDX · OAuth 2.1 / OIDC · Kyverno · OPA<br/>
**Observability** &nbsp; Prometheus · Grafana · Loki · Tempo · OpenTelemetry · ClickHouse

### How I work

- **Make changes reviewable.** Reproducible plans, GitOps reconciliation, and keyless delivery.
- **Make failures understandable.** Useful telemetry, explicit failure modes, and written runbooks.
- **Make correctness repeatable.** Regression tests for security fixes, billing paths, and migrations.
- **Own the whole path.** Design, delivery, operations, and the details between them.

---

**Building AI platforms, developer tools, or secure infrastructure?**<br/>
[sunilmehta.si](https://sunilmehta.si) · [Connect on LinkedIn](https://www.linkedin.com/in/sunilmehta-si/) · [Connect on X](https://x.com/sunilmehta_si) · [Email me](mailto:sunilmehta695@gmail.com)
