# ⚡ ResilienceLab

[![Build Status](https://img.shields.io/github/actions/workflow/status/<usuario>/infra-resiliencelab-fault-csharp/build.yml?branch=main)](https://github.com/<usuario>/infra-resiliencelab-fault-csharp/actions)
[![Coverage](https://img.shields.io/codecov/c/github/<usuario>/infra-resiliencelab-fault-csharp)](https://codecov.io/gh/<usuario>/infra-resiliencelab-fault-csharp)
[![License](https://img.shields.io/github/license/<usuario>/infra-resiliencelab-fault-csharp)](LICENSE)
[![.NET](https://img.shields.io/badge/.NET-9.0-blue)](https://dotnet.microsoft.com/)

---

## 🚀 Overview

**ResilienceLab** é um laboratório de **resiliência e fault injection** em C#, projetado para:

- Simular falhas em **sistemas distribuídos e microserviços**  
- Testar **circuit breakers, retries, timeouts e fallback patterns**  
- Avaliar **robustez de serviços e pipelines críticos**  
- Auxiliar na construção de **sistemas tolerantes a falhas**  

Este projeto serve como **base prática para engenheiros de nível sênior**, permitindo experimentos controlados e análises de comportamento em cenários críticos.

---

## 🏗 Architecture

```mermaid
graph TD
    App[Application / Microservice] -->|Requests| FaultInjector[Fault Injector]
    FaultInjector -->|Injects| Services[Target Services / Modules]
    Services -->|Responses| Monitor[Metrics & Logging]
    Monitor -->|Reports| Dashboard[Grafana / Custom UI]
