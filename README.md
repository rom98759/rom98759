<div align="center">

<img src="assets/header.svg" width="100%" alt="Romain Caillier - Software, Security, Infrastructure" />

<p>
  <a href="https://caillier-romain.fr"><img src="https://img.shields.io/badge/Portfolio-caillier--romain.fr-172337?style=for-the-badge" alt="Portfolio" /></a>
  <a href="https://www.linkedin.com/in/romain-caillier/"><img src="https://img.shields.io/badge/LinkedIn-172337?style=for-the-badge&logo=linkedin" alt="LinkedIn" /></a>
  <a href="https://github.com/rom98759"><img src="https://img.shields.io/badge/GitHub-172337?style=for-the-badge&logo=github" alt="GitHub" /></a>
</p>

</div>

<p align="center">
  <img src="assets/status.svg" width="100%" alt="Current focus: backend, security, infrastructure and automation" />
</p>

## `whoami`

I'm a software developer student at [42 Angoulême](https://42angouleme.fr/), interested in the point where **software engineering, infrastructure and security** meet.

I like understanding the whole system: the application, its APIs, the Linux host, the network and the controls that keep everything observable and resilient.

> Build it. Break it. Understand why. Automate the lesson.

<table>
<tr>
<td width="33%" valign="top">

### DEVELOPMENT

Systems programming, backend services and APIs.

`C` `C++` `Python` `TypeScript`

</td>
<td width="33%" valign="top">

### SECURITY

Application security, API auditing and attack analysis.

`AppSec` `OpenAPI` `Pentest` `Monitoring`

</td>
<td width="33%" valign="top">

### INFRASTRUCTURE

Linux systems, containers and reproducible deployments.

`Docker` `Kubernetes` `Nginx` `Cloudflare`

</td>
</tr>
</table>

## System map

This is how I connect the different parts of a project:

<p align="center">
  <img src="assets/skill-map.svg" width="100%" alt="Map connecting backend, infrastructure, security and automation" />
</p>

```mermaid
flowchart LR
  Client[Client] --> API[API]
  API --> Backend[Backend]
  Backend --> Data[(Database)]
  Backend --> Queue[(Redis)]
  Backend --> Host[Linux host]
  Host --> Observability[Logs and monitoring]
  Observability --> Security[Security feedback]
  Security --> Backend

  classDef app fill:#164E63,stroke:#67E8F9,color:#ECFEFF,stroke-width:2px
  classDef data fill:#312E81,stroke:#C4B5FD,color:#EDE9FE,stroke-width:2px
  classDef infra fill:#14532D,stroke:#A7F3D0,color:#DCFCE7,stroke-width:2px
  classDef security fill:#713F12,stroke:#FDE68A,color:#FEF3C7,stroke-width:2px

  class Client,API,Backend app
  class Data,Queue data
  class Host,Observability infra
  class Security security
```

## Featured projects

The projects below are representative of the questions I like to explore. Each one starts with a system, a failure mode or an assumption worth testing.

### API audit scanner

![Security](https://img.shields.io/badge/SECURITY-FDE68A?style=flat-square&labelColor=713F12)

> How different is the documented API from the application that actually runs?

An automation tool for comparing an OpenAPI surface with observed application behaviour and highlighting security-relevant gaps.

`OpenAPI` `REST` `Security` `Automation`

<details>
<summary><b>Architecture</b></summary>

```mermaid
flowchart LR
    Spec[OpenAPI spec] --> Scanner[Scanner]
    Target[Running API] --> Scanner
    Scanner --> Findings[Findings]
    Findings --> Report[Security report]

  classDef source fill:#164E63,stroke:#67E8F9,color:#ECFEFF,stroke-width:2px
  classDef process fill:#14532D,stroke:#A7F3D0,color:#DCFCE7,stroke-width:2px
  classDef result fill:#713F12,stroke:#FDE68A,color:#FEF3C7,stroke-width:2px

  class Spec,Target source
  class Scanner process
  class Findings,Report result
```

</details>

### Honeypot and monitoring

![Monitoring](https://img.shields.io/badge/MONITORING-A7F3D0?style=flat-square&labelColor=14532D)

> What does automated traffic reveal when a service is deliberately exposed?

A self-hosted environment for collecting, parsing and analysing suspicious activity around exposed services.

`Linux` `Docker` `Networking` `Python`

<details>
<summary><b>Architecture</b></summary>

```mermaid
flowchart LR
    Internet --> Gateway[Nginx]
    Gateway --> Honeypot[Honeypot service]
    Honeypot --> Logs[Raw logs]
    Logs --> Parser[Parser]
    Parser --> Store[(SQLite)]
    Store --> Dashboard[Analysis]

  classDef external fill:#312E81,stroke:#C4B5FD,color:#EDE9FE,stroke-width:2px
  classDef service fill:#14532D,stroke:#A7F3D0,color:#DCFCE7,stroke-width:2px
  classDef detection fill:#713F12,stroke:#FDE68A,color:#FEF3C7,stroke-width:2px
  classDef analysis fill:#164E63,stroke:#67E8F9,color:#ECFEFF,stroke-width:2px

  class Internet external
  class Gateway,Honeypot service
  class Logs,Parser detection
  class Store,Dashboard analysis
```

</details>

### Self-hosted infrastructure

![Infrastructure](https://img.shields.io/badge/INFRASTRUCTURE-A7F3D0?style=flat-square&labelColor=14532D)

> How can personal services stay simple, observable and reasonably protected?

Linux infrastructure for containers, reverse proxying, HTTPS, DNS and security controls.

`Linux` `Docker` `Nginx` `Cloudflare`

### Local AI playground

![Experiment](https://img.shields.io/badge/EXPERIMENT-C4B5FD?style=flat-square&labelColor=4C1D95)

> What changes when inference runs locally instead of behind an API?

Experiments with local inference, quantization, context size, memory usage and developer tooling.

`Ollama` `llama.cpp` `Open WebUI` `Linux`

## Lab

<p align="center">
  <img src="assets/lab.svg" width="100%" alt="Current experiments in local AI, security, infrastructure and hardware" />
</p>

## 42 projects

42 has been my foundation for systems programming, Unix environments, networking and collaborative development.

| Project | Focus |
| --- | --- |
| [Libft](https://github.com/rom98759/Libft) · [ft_printf](https://github.com/rom98759/ft_printf) · [get_next_line](https://github.com/rom98759/Get-Next-Line) | C, memory, file descriptors |
| [Minitalk](https://github.com/rom98759/Minitalk) · [push_swap](https://github.com/rom98759/push_swap) | Processes, signals, algorithms |
| [Philosophers](https://github.com/rom98759/Philosophers) · [minishell](https://github.com/rom98759/minishell) | Threads, synchronisation, Unix |
| [cub3d](https://github.com/rom98759/cub3d) · [NetPractice](https://github.com/rom98759/netpractice) | Graphics, networking, TCP/IP |
| [ft_irc](https://github.com/rom98759/ft_irc) · [Inception](https://github.com/rom98759/inception) | C++, Docker, services |

## Technical landscape

<p align="center">
  <img src="https://skillicons.dev/icons?i=c,cpp,python,bash,typescript,javascript,nodejs,react,postgresql,redis,linux,docker,kubernetes,nginx,gitlab,github" alt="C, C++, Python, Bash, TypeScript, JavaScript, Node.js, React, PostgreSQL, Redis, Linux, Docker, Kubernetes, Nginx, GitLab and GitHub" />
</p>

## Journey

| Period | Direction |
| --- | --- |
| Robotics | Programming robots and competing with RoboCup Junior teams |
| 42 | C, Unix, systems programming, networking and C++ |
| Projects | Backend development, Linux, Docker and self-hosting |
| Today | Security automation, DevSecOps and local AI |

## Contact

I'm interested in backend development, security engineering and infrastructure projects where understanding the system matters.

- Website: [caillier-romain.fr](https://caillier-romain.fr)
- LinkedIn: [romain-caillier](https://www.linkedin.com/in/romain-caillier/)
- GitHub: [rom98759](https://github.com/rom98759)
- Email: [rcaillie@student.42angouleme.fr](mailto:rcaillie@student.42angouleme.fr)
