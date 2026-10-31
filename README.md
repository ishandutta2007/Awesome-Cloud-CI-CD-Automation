# Awesome-Cloud-CI-CD-Automation

# Awesome-Cloud-CI-CD-Automation

# Awesome-Cloud-CI-CD-Automation
**Top Cloud CI CD Automation (Opensource) 🌟 Star if you like it! 🌟**

**Curated List of SaaS Products & Open-Source GitHub Projects**
*Focused on Pipeline Orchestration, Self-Hosted Runners, GitOps Delivery & Container-Native Builds*
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Cloud CI/CD Automation**. These tools enable teams to build, test, and deploy software automatically—from fully managed cloud pipelines with generous free tiers and deep Git integration to self-hosted runners and Kubernetes-native frameworks that give organizations complete control over their build infrastructure.

**Examples** include GitHub Actions, GitLab CI, CircleCI, Bitbucket Pipelines, Azure Pipelines, AWS CodePipeline, Buildkite, Semaphore, Travis CI, and Drone (the category leaders in commercial and open-source space).

**Open-source emphasis**: This section is expanded with every relevant project for self-hosted CI/CD, container-native pipelines, and open automation infrastructure. **Critical note**: The open-source CI/CD landscape is mature and deeply fragmented—**Jenkins** remains the most extensible with the largest plugin ecosystem, **Woodpecker CI** and **Gitea Actions** are the easiest self-hosted entry points, **Tekton** and **Argo CD** dominate Kubernetes-native workflows, and **Dagger** represents the programmable pipeline future. No single open-source tool matches GitHub Actions' marketplace ecosystem, but for self-hosted control, the options are production-proven at scale.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[GitHub Actions](https://github.com/features/actions)**
  **CI/CD integrated with GitHub** with a marketplace of reusable actions and a **CI/CD Catalog** for discovering community workflows. **Pricing**: Free for public repos; private repos get included minutes on Free plan, scaling with paid tiers. **Free tier**: Yes, generous for open source. **Best for**: teams already hosting code on GitHub wanting the tightest integration and largest action ecosystem—**trade-off**: vendor lock-in to GitHub; pin third-party actions to commit SHAs to reduce supply-chain risk .

- **[GitLab CI](https://about.gitlab.com/)**
  **Integrated CI/CD within GitLab** covering source control, pipelines, registry, and environments in one platform. **CI/CD Catalog** (GA in GitLab 17.0) enables versioned, parameterized component reuse across projects—moving teams from copy-paste to referenced components . **Pricing**: Free tier with limited compute minutes; paid tiers scale. **Free tier**: Yes, limited minutes. **Best for**: teams wanting a single tool for repo, CI, and deployment with strong component reuse—**trade-off**: complex YAML at scale; self-hosted management overhead.

- **[CircleCI](https://circleci.com/)**
  **Cloud CI/CD platform** known for speed and first-class Docker support. **Pricing**: Free tier with credits (expire monthly); **Performance** from $15/month plus credits; paid credits roll over . **Free tier**: Yes, 30,000 credits/month. **Best for**: teams prioritizing fast builds and Docker-native workflows—**trade-off**: credit model can become expensive at scale; SSO and config policies require Scale tier .

- **[Bitbucket Pipelines](https://bitbucket.org/product/features/pipelines)**
  **CI/CD integrated with Bitbucket** and the Atlassian ecosystem (Jira, Confluence). **Self-hosted runners V5** (2026) add Docker volume mounts, customizable CPU/memory (1x–16x presets), and S3/GCS storage control. **Free tier**: 50 minutes/month; **Standard** includes 2,500 pooled minutes . **Best for**: teams fully committed to Atlassian wanting zero-config Jira integration—**trade-off**: free tier is nearly useless for real projects; self-hosted runners have free tier (up to 100 runners) and premium tier with support .

- **[Azure Pipelines](https://azure.microsoft.com/en-us/products/devops/pipelines)**
  **CI/CD within Azure DevOps** with Microsoft-hosted and self-hosted agents. **Free tier**: 1 free parallel job with **1,800 minutes/month** for private projects (requires request form for new orgs) . **Free tier**: Yes, generous minutes. **Best for**: organizations deeply invested in Azure wanting native integration with App Service, AKS, and Azure Functions—**trade-off**: Microsoft is steering AI investment toward GitHub; Azure Pipelines is increasingly legacy.

- **[AWS CodePipeline](https://aws.amazon.com/codepipeline/)**
  **Managed CI/CD service** within AWS with integration to CodeBuild, CodeDeploy, and third-party tools like GitHub. **Pricing**: Pay-as-you-go; no upfront fees or long-term contracts . **Free tier**: AWS Free Tier applies to some usage. **Best for**: AWS-centric teams wanting native integration with IAM, S3, and other AWS services—**trade-off**: CodeBuild free tier is on the smallest instance; pipeline orchestration is basic compared to GitHub Actions or GitLab CI.

- **[Buildkite](https://buildkite.com/)**
  **Hybrid CI/CD** with managed orchestration and **free self-hosted agents**. **Pricing**: **Personal** (free) includes 1 user, 3 concurrent jobs, 1 self-hosted agent, 50k monthly test executions . **Free tier**: Yes, personal plan for individuals. **Best for**: teams with specific infrastructure requirements (GPU builds, custom hardware, air-gapped environments) wanting managed orchestration without giving up control—**trade-off**: self-hosted agent model adds operational complexity.

- **[Semaphore](https://semaphoreci.com/)**
  **Fast CI/CD** with Docker-native pipelines and self-hosted option. **Pricing**: **$15 free usage every month** for every account; direct per-minute pricing (not credit-based); **free Community Edition** for self-hosting . **Free tier**: Yes, $15/month usage. **Best for**: teams wanting speed and Docker-native workflows with transparent per-minute billing—**trade-off**: no traditional free cloud tier beyond the $15 credit.

- **[Travis CI](https://www.travis-ci.com/)**
  **Hosted CI** with simple `.travis.yml` configuration, historically popular in open source. **Pricing**: **OSS plan free** for open-source repos; **Usage Based** $15/month (35k Linux build credits, 80 concurrent jobs); **Unlimited** $78+/month . **Free tier**: Yes, for open source. **Best for**: simple open-source projects wanting minimal setup—**trade-off**: lost most mindshare after pricing changes; smaller ecosystem than GitHub Actions.

## Open-Source GitHub Projects

- **[Jenkins](https://github.com/jenkinsci/jenkins)**
  **Self-contained automation server with the largest plugin ecosystem** (MIT) — **the most extensible open-source CI/CD tool**, with 1,800+ plugins covering virtually every integration imaginable. **Features**: Pipeline-as-code via Jenkinsfile (Groovy DSL); distributed builds with controller/agent architecture; extensive plugin ecosystem for SCM, build tools, deployment, and notifications; mature RBAC and authentication integrations. **Tech stack**: Java. **Deploy**: Self-hosted (WAR file, Docker, Kubernetes). **Trade-off**: **UI and architecture are aging**; plugin management becomes a maintenance burden; not Kubernetes-native without plugins. **Best for**: teams needing maximum flexibility and existing Jenkins expertise—or organizations with complex legacy workflows that no modern tool handles out of the box.

- **[Woodpecker CI](https://github.com/woodpecker-ci/woodpecker)**
  **Lightweight, Docker-native CI** (Apache 2.0) — **the easiest self-hosted CI to set up**, created as a community fork of Drone CI after license changes. **Features**: Simple `.woodpecker.yml` configuration—each step runs in a Docker container; **single binary** server and agents; multi-platform agents (Linux, macOS, Windows, ARM); works with **Gitea, GitHub, GitLab, Bitbucket, and Forgejo**; v3.0 shipped with redesigned UI and native multi-architecture builds. **Tech stack**: Go. **Deploy**: Self-hosted (Docker, single binary). **Trade-off**: **Smaller ecosystem than Jenkins**—fewer plugins; no built-in artifact storage or advanced caching. **Best for**: small teams using Gitea/Forgejo wanting simple, Docker-native CI with minimal overhead—the easiest entry point for self-hosted pipelines.

- **[Gitea Actions](https://github.com/go-gitea/gitea)**
  **GitHub Actions-compatible CI built into Gitea** (MIT) — **the simplest path to GitHub Actions compatibility on self-hosted Git**. **Features**: **GitHub Actions workflow compatibility**—reuse existing workflows and many marketplace actions; **no separate CI service to deploy**—Actions is built into Gitea; Act runner based on the `act` project; lightweight runners easy to deploy. **Tech stack**: Go. **Deploy**: Gitea 1.21+ with Actions enabled. **Trade-off**: **Not all GitHub Actions features are supported**—complex workflows may need adjustments; newer and less mature than Woodpecker or Jenkins. **Best for**: teams already using Gitea wanting GitHub Actions-style CI without running a separate CI system.

- **[Tekton](https://github.com/tektoncd/pipeline)**
  **Kubernetes-native CI/CD framework** (Apache 2.0) — **the vendor-neutral standard for cloud-native pipelines**. **Features**: **Kubernetes CRDs** for Tasks, Pipelines, and PipelineRuns; highly composable and reusable; event-driven architecture with Triggers; multi-cloud portability; **MCP server support** for agentic workflows; backed by CD Foundation. **Tech stack**: Go, Kubernetes. **Deploy**: Self-hosted (Kubernetes required). **Trade-off**: **Steep learning curve**—requires building pipelines from scratch; fewer out-of-the-box integrations; less opinionated means more configuration. **Best for**: teams building custom cloud-native pipelines on Kubernetes—especially those in the Red Hat/OpenShift ecosystem or needing vendor-neutral portability.

- **[Argo CD](https://github.com/argoproj/argo-cd)**
  **Declarative GitOps continuous delivery for Kubernetes** (Apache 2.0) — **the standard for Kubernetes GitOps delivery**. **Features**: **Git as source of truth** with automatic sync and drift detection; multi-cluster management; built-in RBAC and audit trails; web UI for visualization; supports Helm, Kustomize, and Jsonnet; SSO integration (SAML, OIDC); canary and blue/green deployments via Argo Rollouts. **Tech stack**: Go, Kubernetes. **Deploy**: Self-hosted (runs in Kubernetes cluster). **Trade-off**: **CD only—needs a separate CI tool** for build and test; steeper learning curve for GitOps concepts; resource-intensive at scale. **Best for**: teams adopting GitOps for Kubernetes deployments—the most mature open-source CD tool for cloud-native environments.

- **[Dagger](https://github.com/dagger/dagger)**
  **Programmable CI/CD engine with container-native pipelines** (Apache 2.0) — **the most forward-looking open-source CI/CD project**, positioning pipelines as code in real programming languages. **Features**: **Pipelines in Go, Python, TypeScript, and Java**—not YAML; **native LLM integration** and MCP server for agentic workflows; container isolation for every step; runs locally or in any CI system; no Kubernetes requirement; medium setup complexity. **Tech stack**: Go (core), multi-language SDKs. **Deploy**: Self-hosted (CLI, container runtime). **Trade-off**: **Different mental model**—not a traditional CI server; requires programming knowledge; smaller community than Jenkins or GitHub Actions. **Best for**: development teams wanting programmable, testable pipelines in real languages—especially those building agentic or AI-integrated CI workflows.

- **[Concourse](https://github.com/concourse/concourse)**
  **Container-based automation system** (Apache 2.0) — **the most opinionated open-source CI/CD** with pipelines as resources and jobs. **Features**: Every step runs in a container; pipelines declared as resources and jobs; no plugins—built-in resource types; strong isolation; visual pipeline UI; actively maintained. **Tech stack**: Go. **Deploy**: Self-hosted. **Trade-off**: **Opinionated model**—less flexible than Jenkins; smaller community; requires learning its specific abstractions. **Best for**: teams wanting a clean, container-first CI/CD model without plugin sprawl.

- **[GoCD](https://github.com/gocd/gocd)**
  **Continuous delivery server with built-in value-stream maps** (Apache 2.0) — **the most CD-focused open-source tool**. **Features**: **Pipelines and value-stream maps built in**—no plugins needed for CD visualization; modeling complex workflows; active development. **Tech stack**: Java. **Deploy**: Self-hosted. **Trade-off**: **CI capabilities are secondary**—best suited for CD orchestration; UI is functional but dated. **Best for**: teams needing strong CD visualization and dependency management—especially those modeling complex deployment pipelines.

### Additional Strong Open-Source Options

- **Drone CI** — Container-native CI (Apache 2.0). Lightest footprint (256 MB RAM); Docker-native pipelines. **Note**: License changed to source-available for newer versions; Woodpecker is the community fork. **Best for**: teams wanting Drone's original model via the Woodpecker fork.
- **OneDev** — Git server with built-in CI/CD (MIT). All-in-one Git hosting, issue tracking, and CI. **Best for**: small teams wanting a single self-hosted platform.
- **Earthly** — Container-native build automation (Apache 2.0). Reproducible builds with Docker and Earthfile syntax. **Best for**: teams wanting reproducible container builds.
- **Agola** — Lightweight CI/CD (Apache 2.0). Simple setup, Docker-native. **Best for**: small teams wanting minimal CI overhead.

**Frameworks for building custom systems**: Combine **Jenkins** for maximum integration flexibility with **Woodpecker CI** or **Gitea Actions** for simple Docker-native pipelines, **Tekton** for Kubernetes-native CI, **Argo CD** for GitOps delivery, and **Dagger** for programmable pipelines—creating a CI/CD stack matched to each team's infrastructure and language preferences. **None of these match GitHub Actions' marketplace ecosystem**, but for self-hosted control, the open-source options are production-proven at scale.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, license (for open-source), and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- CI/CD platforms handling code and deployment credentials must comply with data protection regulations (GDPR, CCPA, etc.) and implement appropriate access controls and secret management.
- **The "SaaS platform" vs. "self-hosted CI" vs. "GitOps CD" vs. "programmable engine" distinction is critical.** **GitHub Actions, GitLab CI, CircleCI, Bitbucket Pipelines, Azure Pipelines, AWS CodePipeline, Buildkite, Semaphore, and Travis CI** are **managed SaaS platforms**—they provide hosted runners and orchestration. **Jenkins, Woodpecker CI, Gitea Actions, Tekton, Concourse, and GoCD** are **self-hosted CI/CD tools**—you own the infrastructure and maintenance. **Argo CD** is **GitOps CD**—it handles deployment, not build/test. **Dagger** is a **programmable engine**—it runs anywhere but is not a server. **Choose based on whether you want managed convenience, full control, or GitOps delivery.**
- **GitHub Actions is the pragmatic default for teams already on GitHub**—the action marketplace and tight integration make fighting the platform rarely worth it. **Pin third-party actions to commit SHAs** to reduce supply-chain risk . **GitLab CI's CI/CD Catalog** (GA 17.0) now provides versioned component reuse, closing a key gap versus GitHub Actions .
- **Bitbucket's free tier (50 minutes/month) is nearly useless for real projects** . **Azure Pipelines has the best free tier** (1,800 minutes, though new orgs must request it) . **Semaphore offers $15 free usage monthly with transparent per-minute billing** . **Buildkite's free Personal plan** is limited but viable for individuals .
- **Woodpecker CI and Gitea Actions are the easiest self-hosted entry points**—Docker-native, simple YAML, single binary deployment. **Jenkins remains the most extensible** with 1,800+ plugins, but plugin management and aging architecture are real burdens.
- **Tekton and Argo CD are the Kubernetes-native standards**—Tekton for CI, Argo CD for CD. **The trade-off**: both require Kubernetes expertise and have steeper learning curves than Docker-native tools.
- **Dagger represents the future of programmable pipelines**—real languages, native LLM integration, MCP server, and no Kubernetes requirement. **The trade-off**: different mental model; requires programming knowledge.
- Self-hosted open-source solutions require proper infrastructure (servers, runners, databases), security hardening for build credentials, and ongoing maintenance. **CI/CD pipelines handle code and deployment secrets**—ensure your deployment meets your organization's security standards and includes secret management before automating production deployments.

---

**Made for developers, DevOps teams, and organizations building transparent CI/CD automation solutions.**
Let's make Cloud CI/CD Automation more open, data-driven, and pipeline-friendly.
