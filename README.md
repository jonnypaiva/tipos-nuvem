# ☁️ Tipos de Serviços em Nuvem no Azure

## 📘 Introdução

A computação em nuvem oferece diferentes modelos de serviço para atender às necessidades de negócios, desenvolvimento e operação de sistemas. No Microsoft Azure, os três principais modelos são:

- **IaaS** (Infrastructure as a Service)
- **PaaS** (Platform as a Service)
- **SaaS** (Software as a Service)

Cada modelo oferece um nível diferente de controle, flexibilidade e responsabilidade.

---

## 🧱 1. IaaS – Infrastructure as a Service

### 📌 O que é?
É a forma mais básica de serviço em nuvem, onde você aluga infraestrutura de TI: servidores, VMs, redes e armazenamento.

### 📦 O que você gerencia?
Você gerencia o sistema operacional, middleware, runtime e suas aplicações.

### 🔧 Exemplo no Azure:
- Azure Virtual Machines
- Azure Virtual Network
- Azure Load Balancer

### 📊 Casos de uso:
- Migração lift-and-shift de aplicações
- Ambientes de testes e desenvolvimento
- Hospedagem de servidores web ou banco de dados

![IaaS](https://learn.microsoft.com/pt-br/azure/cloud-adoption-framework/media/ready/azure-best-practices/iaas.png)
*Fonte: Microsoft Learn*

---

## 🧰 2. PaaS – Platform as a Service

### 📌 O que é?
Fornece um ambiente com ferramentas e serviços completos para desenvolver, testar, entregar e gerenciar aplicações.

### 📦 O que você gerencia?
Você gerencia apenas sua aplicação e dados — o restante (infraestrutura, sistema operacional, runtime) é responsabilidade do provedor.

### 🔧 Exemplo no Azure:
- Azure App Service
- Azure SQL Database
- Azure Functions

### 📊 Casos de uso:
- Desenvolvimento web e mobile
- APIs e microserviços
- Aplicações com escalabilidade automática

![PaaS](https://learn.microsoft.com/pt-br/azure/architecture/data-guide/images/paas-diagram.png)
*Fonte: Microsoft Learn*

---

## 🧑‍💻 3. SaaS – Software as a Service

### 📌 O que é?
Modelo onde o usuário consome uma aplicação pronta, hospedada e gerenciada pelo provedor.

### 📦 O que você gerencia?
Nada. Você apenas usa o software via navegador ou aplicativo.

### 🔧 Exemplo no Azure:
- Microsoft 365
- Power BI
- Dynamics 365

### 📊 Casos de uso:
- Colaboração e produtividade
- BI e dashboards
- ERP e CRM online

![SaaS](https://learn.microsoft.com/pt-br/dotnet/architecture/cloud-native/media/saas.png)
*Fonte: Microsoft Learn*

---

## ⚖️ Comparativo Geral

| Recurso                         | IaaS         | PaaS         | SaaS         |
|---------------------------------|--------------|--------------|--------------|
| Controle do Usuário             | Alto         | Médio        | Baixo        |
| Custo Inicial                   | Médio        | Baixo        | Baixo        |
| Escalabilidade                  | Manual       | Automática   | Automática   |
| Tempo de Deploy                | Horas/Dias   | Minutos      | Imediato     |
| Exemplo Azure                   | VM           | App Service  | Microsoft 365|

---

## 🧩 Diagrama Comparativo

```mermaid
graph LR
    A[Infraestrutura (Datacenter)]
    B[Sistema Operacional]
    C[Middleware / Runtime]
    D[Aplicações]
    E[Dados]

    subgraph IaaS
        A
        B
        C
        D
        E
    end

    subgraph PaaS
        C
        D
        E
    end

    subgraph SaaS
        D
        E
    end
