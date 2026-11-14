<a href="https://sunilmehta.si">
  <img src="assets/banner.png" width="100%" alt="Sunil Mehta. I build and scale the infrastructure AI platforms run on. 300+ TDX GPU nodes, 100M+ LLM requests a month, 99.95% uptime, 55% lower cloud cost." />
</a>

<p align="center">
  <a href="https://sunilmehta.si"><strong>sunilmehta.si</strong></a>
  &nbsp;·&nbsp;
  <a href="https://sunilmehta.si/#projects">Projects</a>
  &nbsp;·&nbsp;
  <a href="https://sunilmehta.si/#experience">Experience</a>
  &nbsp;·&nbsp;
  <a href="https://sunilmehta.si/Sunil_Mehta_Resume.pdf">Resume</a>
  &nbsp;·&nbsp;
  <a href="https://www.linkedin.com/in/sunilmehta-si/">LinkedIn</a>
  &nbsp;·&nbsp;
  <a href="https://x.com/sunilmehta_si">X</a>
  &nbsp;·&nbsp;
  <a href="mailto:sunilmehta695@gmail.com">Email</a>
</p>

I'm **Sunil Mehta**, Founding Lead DevOps & MLOps Engineer at **[ORGN](https://orgn.com)**, based in Gurugram and open to remote roles. For 9+ years I have built and run the platforms AI products depend on, from multi-cloud Kubernetes and confidential GPU compute to secure delivery and cost governance.

In the open I build benchmarks and tools that answer questions a platform team has to answer, and I send the fixes I find upstream.

## Measured in the open

| Project | What it asks | What held |
| :--- | :--- | :--- |
| **[k8s-gpu-scheduler-benchmark](https://github.com/sunilmehta-si/k8s-gpu-scheduler-benchmark)**<br/>`v0.5.0` | Which Kubernetes GPU scheduler should a platform run? | Out of the box only KAI bin-packs GPU pods by their GPUs. One setting made Volcano **26% faster and 26% cheaper** per useful GPU-hour on the same trace. |
| **[k8s-inference-routing-benchmark](https://github.com/sunilmehta-si/k8s-inference-routing-benchmark)**<br/>`v0.6.0` | How much does the router in front of LLM servers matter? | Prefix-aware routing lifts cache hits from **64% to 80%** and cuts median time to first token by 27%. Under load the router matters more and the routers differ less. |
| **[k8s-inference-autoscaling-benchmark](https://github.com/sunilmehta-si/k8s-inference-autoscaling-benchmark)**<br/>`v0.8.0` | What should an autoscaler follow when it scales LLM inference? | On a real cluster **no ramp from 30 seconds to 10 minutes** was slow enough for the default HPA to keep requests on time. Pod startup is the constraint, a small warm pool is the cheapest fix, and a forecast helps on slow ramps only. |
| **[k8s-gpu-cost-scanner](https://github.com/sunilmehta-si/k8s-gpu-cost-scanner)**<br/>`v0.1.0` | Which GPUs is the cluster paying for and not using? | A read-only Go tool on the metrics a cluster already has. On a synthetic fleet backfilled into a real Prometheus in CI it finds every planted problem: **221.4 wasted GPU-hours** in a day, each counted once, and the cost per million tokens of each model. |
| **[kube-diagnose](https://github.com/sunilmehta-si/kube-diagnose)**<br/>`v0.2.0` | Why is this Kubernetes workload broken? | A read-only kubectl plugin that names the root cause with the evidence and the kubectl command behind each fact. On a real cluster in CI it named the cause of **40 of 40** broken namespaces in its first finding; k8sgpt named 21. `record --redact` makes a snapshot safe to share. |
| **[kubernetes-secure-mlops-pipeline](https://github.com/sunilmehta-si/kubernetes-secure-mlops-pipeline)**<br/>`v0.8.0` | Can every model in production be reproducible, signed and verified? | A real kind cluster runs **24 checks** on every push, and the gate blocked a 0.909 challenger against the 0.938 champion. |
| **[agentic-code-review-tool](https://github.com/sunilmehta-si/agentic-code-review-tool)**<br/>`v0.11.1` | Scanner-grounded AI review for the whole pull request. | 128 rules, each swept over real repositories before release. One rule went from **1,556 findings to 101**. |

Also: **[ai-devsecops-cicd](https://github.com/sunilmehta-si/ai-devsecops-cicd)**, a secure delivery path for LLM and agent services · **[llm-inference-platform](https://github.com/sunilmehta-si/llm-inference-platform)**, LLM serving on Apple Silicon you can measure · **[jev-inference-router](https://github.com/sunilmehta-si/jev-inference-router)**, an observable routing layer for local inference.

### How the numbers are held

1. **One workload, every contender.** The same trace is replayed through each scheduler, router or policy, so a difference belongs to the component and not to the traffic.
2. **Real components, in CI.** Kueue, Volcano, KAI, the llm-d router, the HPA and KEDA run as released, on kind clusters in GitHub Actions. Anyone can run them again.
3. **Every number has a test.** The datasets are committed, and tests hold each figure a README quotes to the data behind it.
4. **Only what repeats is claimed.** A difference on a cluster counts when it holds over more than one run. One early reading reversed on the second run and was withdrawn in the open.

## Shipped lately

| When | What | |
| :--- | :--- | :--- |
| 14 Nov 2026 | **kube-diagnose** `v0.2.0` | [62 rules and redacted recordings](https://github.com/sunilmehta-si/kube-diagnose/releases/tag/v0.2.0): 40 of 40 faults named first on a real cluster; k8sgpt named 21. |
| 12 Nov 2026 | **k8s-gpu-cost-scanner** `v0.1.0` | [A new tool](https://github.com/sunilmehta-si/k8s-gpu-cost-scanner/releases/tag/v0.1.0): the GPUs an inference cluster pays for and does not use, and what each model costs per million tokens. |
| 11 Nov 2026 | **k8s-inference-autoscaling-benchmark** `v0.8.0` | [A predictive policy](https://github.com/sunilmehta-si/k8s-inference-autoscaling-benchmark/releases/tag/v0.8.0): scaling one pod startup ahead helps on slow ramps, and warm capacity still wins the fast ones. |
| 09 Nov 2026 | **kubernetes-secure-mlops-pipeline** `v0.8.0` | [Every pin is held back](https://github.com/sunilmehta-si/kubernetes-secure-mlops-pipeline/releases/tag/v0.8.0) until its release is 14 days old, and reported when it drifts. |
| 04 Nov 2026 | **agentic-code-review-tool** `v0.11.1` | [A false positive](https://github.com/sunilmehta-si/agentic-code-review-tool/releases/tag/v0.11.1) found by sweeping Inspect AI: 1,124 findings from one rule, down to 8. |

## The platform I run at ORGN

| Ship | Guard | Run | Watch & own |
| :--- | :--- | :--- | :--- |
| GitHub Actions, keyless through Workload Identity Federation | Secret, code, dependency, image and infrastructure-code scanning | 10+ GKE clusters for an engineering org of 50+ | 99.95% uptime across 200+ services |
| Artifact Registry, images signed with cosign | Kyverno and OPA at admission | 300+ Intel TDX confidential GPU nodes | Istio, Prometheus, Loki, OpenTelemetry, Grafana HA |
| Argo CD to every cluster | Falco at runtime | Rust LLM gateways, 100M+ requests a month | $70K–$90K of monthly cloud spend owned |
| Protected Terraform workflows | | OAuth 2.1 / OIDC sign-on, migrated with zero downtime | Infrastructure cost cut by 55% |

*This describes my professional work. Most of it lives in private organization repositories. The [full experience](https://sunilmehta.si/#experience), five roles since 2017, is on the site.*

## Upstream

| Project | Contribution | Status |
| :--- | :--- | :--- |
| [Argo CD](https://github.com/argoproj/argo-cd/pull/30374) | Documented OCI repositories over plain HTTP (`insecureOCIForceHttp`, `type: oci` secrets) | **Merged** |
| [MLflow](https://github.com/mlflow/mlflow/pull/27173) | Model downloads no longer modify signed model directories, which broke signature verification. [Reported](https://github.com/mlflow/mlflow/issues/27051), then fixed. | **Merged** |
| [NVIDIA KAI Scheduler](https://github.com/NVIDIA/KAI-Scheduler/pull/2498) | Corrected the GPU fractioning docs to the names the subchart and operator use | **Merged** |
| [KServe](https://github.com/kserve/kserve/pull/6472) | Security: every Python lock moved off the certifi that still trusted the compromised emSign roots | In review |
| [Tesla vehicle-command](https://github.com/teslamotors/vehicle-command/pull/529) | Fixed key storage rejecting valid P-256 keys whose scalar starts with a zero byte, about one key in 256 | In review |
| [xAI Python SDK](https://github.com/xai-org/xai-sdk-python/pull/241) | Shipped the missing `py.typed` marker, so type checkers use the SDK's annotations | In review |
| [X API CLI (xurl)](https://github.com/xdevplatform/xurl/pull/108) | The webhook server fails fast without an ngrok token instead of hanging | In review |
| [etcd-operator](https://github.com/etcd-io/etcd-operator/pull/544) | The operator no longer carries on without its TLS certificates when provisioning fails | In review |
| [KServe website](https://github.com/kserve/website/pull/766) | Install docs: create the `kserve` namespace before applying the manifest | In review |
| [Kubeflow Pipelines](https://github.com/kubeflow/pipelines/issues/15056) | A compiler bug: a multi-line default value makes the compiled pipeline YAML invalid. Fix ready. | Reported |

## Tools

**Infrastructure** &nbsp; Kubernetes · Terraform · Argo CD · Helm · GCP · AWS · DigitalOcean · Cloudflare<br/>
**MLOps & serving** &nbsp; Kubeflow Pipelines · MLflow · KServe · vLLM<br/>
**GPU scheduling** &nbsp; Kueue · Volcano · KAI Scheduler · kwok<br/>
**Security** &nbsp; Intel TDX · OAuth 2.1 / OIDC · Kyverno · OPA · cosign · SLSA · OpenSSF model signing<br/>
**Observability** &nbsp; Prometheus · Grafana · Loki · Tempo · OpenTelemetry · ClickHouse<br/>
**Languages & data** &nbsp; Go · Rust · TypeScript · Python · PostgreSQL · Redis

---

**Building AI platforms, developer tools or secure infrastructure?**<br/>
[sunilmehta.si](https://sunilmehta.si/#contact) · [LinkedIn](https://www.linkedin.com/in/sunilmehta-si/) · [X](https://x.com/sunilmehta_si) · [Email](mailto:sunilmehta695@gmail.com)
