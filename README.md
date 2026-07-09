<h1 align="center">Said Sef</h1>

<p align="center">
Cloud architect &amp; platform engineer - AWS, GCP, Kubernetes, and AI platforms.<br/>
10+ years delivering cloud-native platforms for finance, food-delivery, retail, and media.<br/>
I consult through <a href="https://ai.saidsef.co.uk/home"><strong>Said Sef Associates</strong></a> - London-based, remote-first.
</p>

![Amazon AWS](https://img.shields.io/badge/Amazon%20AWS-FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Google Cloud](https://img.shields.io/badge/Google%20Cloud-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white)
![Kubernetes](https://img.shields.io/badge/-Kubernetes-326CE5?style=for-the-badge&logo=Kubernetes&logoColor=white)
![HELM](https://img.shields.io/badge/-HELM-FFFFFF?style=for-the-badge&logo=HELM&logoColor=0F1689)
![ArgoCD](https://img.shields.io/badge/-ArgoCD-EF7B4D?style=for-the-badge&logo=argo&logoColor=FFFFFF)
![Cilium](https://img.shields.io/badge/-Cilium-F8C517?style=for-the-badge&logo=cilium&logoColor=black)
![Terraform / Cloud](https://img.shields.io/badge/-Terraform&nbsp;&#47;&nbsp;Cloud-623CE4?style=for-the-badge&logo=Terraform&logoColor=white)
![OpenTofu](https://img.shields.io/badge/-OpenTofu-FFDA18?style=for-the-badge&logo=opentofu&logoColor=black)
![Vault](https://img.shields.io/badge/-Vault-000000?style=for-the-badge&logo=Vault&logoColor=white)
![Consul](https://img.shields.io/badge/-Consul-CA2171?style=for-the-badge&logo=Consul&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/-GitHub&nbsp;Actions-2088FF?style=for-the-badge&logo=GitHub-Actions&logoColor=white)
![GitLab](https://img.shields.io/badge/-GitLab-FCA121?style=for-the-badge&logo=gitlab&logoColor=white)
![Tekton](https://img.shields.io/badge/-Tekton-0D9FEA?style=for-the-badge&logo=Tekton&logoColor=white)
![Jenkins](https://img.shields.io/badge/-Jenkins-D24939?style=for-the-badge&logo=Jenkins&logoColor=white)
![DroneCI](https://img.shields.io/badge/-DroneCI-212121?style=for-the-badge&logo=Drone&logoColor=white)
![Docker](https://img.shields.io/badge/-Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Kaniko](https://img.shields.io/badge/-Kaniko-FFFFFF?style=for-the-badge&logo=kaniko&logoColor=FFA500)
![Prometheus](https://img.shields.io/badge/-Prometheus-E6522C?style=for-the-badge&logo=Prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/-Grafana-F46800?style=for-the-badge&logo=Grafana&logoColor=white)
![OpenTelemetry](https://img.shields.io/badge/-OpenTelemetry-425CC7?style=for-the-badge&logo=opentelemetry&logoColor=white)
![DataDog](https://img.shields.io/badge/-DataDog-632CA6?style=for-the-badge&logo=datadog&logoColor=white)
![Splunk](https://img.shields.io/badge/-Splunk-000000?style=for-the-badge&logo=Splunk&logoColor=white)
![Anthropic](https://img.shields.io/badge/-Anthropic-FF1744?style=for-the-badge&logo=Anthropic&logoColor=white)
![OpenAI](https://img.shields.io/badge/-OpenAI-412991?style=for-the-badge&logo=OpenAI&logoColor=white)
![Hugging Face](https://img.shields.io/badge/-Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)
![MCP](https://img.shields.io/badge/-MCP-000000?style=for-the-badge&logo=modelcontextprotocol&logoColor=white)
![scikit-learn](https://img.shields.io/badge/-scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/-Pandas-FFFFFF?style=for-the-badge&logo=Pandas&logoColor=000000)
![Jupyter](https://img.shields.io/badge/-Jupyter-F7931E?style=for-the-badge&logo=Jupyter&logoColor=FFFFFF)
![PostgreSql](https://img.shields.io/badge/-PostgreSQL-4169E1?style=for-the-badge&logo=PostgreSQL&logoColor=white)
![Redis](https://img.shields.io/badge/-Redis-DC382D?style=for-the-badge&logo=Redis&logoColor=white)
![ElasticSearch](https://img.shields.io/badge/-ElasticSearch-005571?style=for-the-badge&logo=ElasticSearch&logoColor=white)
![Python](https://img.shields.io/badge/-Python-3776AB?style=for-the-badge&logo=Python&logoColor=white)
![Golang](https://img.shields.io/badge/-Golang-00ADD8?style=for-the-badge&logo=go&logoColor=white)
![NodeJS](https://img.shields.io/badge/-NodeJS-339933?style=for-the-badge&logo=node.js&logoColor=white)
![TypeScript](https://img.shields.io/badge/-TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Bash](https://img.shields.io/badge/-Bash-4EAA25?style=for-the-badge&logo=gnu-bash&logoColor=white)
![Linux](https://img.shields.io/badge/-Linux-FFFFFF?style=for-the-badge&logo=Linux&logoColor=black)
![Git](https://img.shields.io/badge/-Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/-GitHub-181717?style=for-the-badge&logo=github&logoColor=white)

## Resume MCP Server

My CV runs as a live [Model Context Protocol](https://modelcontextprotocol.io) server. Connect any MCP client and ask about my experience, clients, certifications, and open-source work.

```text
https://ai.saidsef.co.uk/mcp
```

**Claude Code**

```bash
claude mcp add --transport http saidsef https://ai.saidsef.co.uk/mcp
```

**Claude Desktop / claude.ai** - Settings → Connectors → Add custom connector → paste the URL above.

<details>
<summary><strong>Other MCP clients</strong> (Cursor, VS Code, and any Streamable HTTP client)</summary>

```json
{
  "mcpServers": {
    "saidsef": {
      "type": "http",
      "url": "https://ai.saidsef.co.uk/mcp"
    }
  }
}
```

</details>

Example prompts: "What has Said shipped on EKS?", "Which observability stacks has he run at scale?", "What Terraform modules does he maintain?"

## Featured Open Source

| Project | What it does |
|---|---|
| [grafana-loki-on-k8s](https://github.com/saidsef/grafana-loki-on-k8s) | LGTM observability stack - Grafana, Loki, Tempo, Mimir, Alloy, Beyla - on Kubernetes |
| [k8s-nifi-cluster](https://github.com/saidsef/k8s-nifi-cluster) | Apache NiFi data-flow cluster on Kubernetes |
| [OIDC Terraform modules](https://registry.terraform.io/namespaces/saidsef) | Keyless CI/CD authentication to AWS &amp; GCP for GitHub Actions, GitLab, and Terraform Cloud |
| [mcp-github-pr-issue-analyser](https://github.com/saidsef/mcp-github-pr-issue-analyser) | MCP server for GitHub PR analysis, issue management, and releases |
| [argocd-applicationsets-services](https://github.com/saidsef/argocd-applicationsets-services) | PR preview environments via ArgoCD ApplicationSets |
| [Reusable GitHub Actions workflows](./docs/reusable-workflows.md) | Terraform/OpenTofu multi-version validation, Checkov security scanning, and semantic tag-and-release - hosted in this repo |

<p align="center"><img align="center" src="https://stats.saidsef.co.uk/github/stats" alt="saidsef" /></p>

<p align="center">
  <a href="https://www.credly.com/users/saidsef/" target="blank"> <img  align="center" src="https://img.shields.io/badge/-Credly-FF6B00?style=for-the-badge&logo=credly&logoColor=white" alt="saidsef" /></a>
  <a href="https://www.linkedin.com/in/saidsef/" target="blank"><img align="center" src="https://img.shields.io/badge/-linkedin-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="saidsef"/></a>
  <a href="https://twitter.com/saidsef" target="blank"><img align="center" src="https://img.shields.io/badge/-twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white" alt="saidsef"/></a>
  <a href="https://registry.terraform.io/namespaces/saidsef" target="blank"><img align="center" src="https://img.shields.io/badge/-Terraform-7B42BC?style=for-the-badge&logo=Terraform&logoColor=white" alt="saidsef" /></a>
  <a href="https://artifacthub.io/packages/search?org=saidsef&sort=relevance&page=1" target="blank"><img align="center" src="https://img.shields.io/badge/-artifacthub-4181C2?style=for-the-badge&logo=artifacthub&logoColor=white" alt="saidsef" /></a>
  <a href="https://hub.docker.com/u/saidsef" target="blank"><img align="center" src="https://img.shields.io/badge/-Docker%20Hub-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="saidsef" /></a>
</p>

<p align="center">For consulting engagements, visit <a href="https://ai.saidsef.co.uk/home"><strong>Said Sef Associates</strong></a>.</p>
