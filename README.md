# 📊 Microsoft Fabric e Integração com Azure DevOps

## 🧭 Visão Geral

O **Microsoft Fabric** é uma plataforma unificada de análise de dados criada para facilitar o trabalho de engenheiros de dados, analistas e cientistas de dados. Ele centraliza recursos que antes estavam separados no Azure Synapse, Power BI, Azure Data Factory, Azure Data Lake, entre outros — oferecendo **tudo em um só lugar** com uma interface SaaS moderna e pronta para uso.

---

## 🏗️ Recursos Principais do Microsoft Fabric

O Fabric é dividido em experiências (workloads) específicas para diferentes perfis profissionais:

| Workload           | Função Principal                                                                 |
|--------------------|----------------------------------------------------------------------------------|
| Data Engineering   | Desenvolvimento de pipelines, notebooks Spark e processamento em larga escala   |
| Data Factory       | Pipelines de movimentação e orquestração de dados (ADF dentro do Fabric)         |
| Data Science       | Treinamento de modelos e rastreamento de experimentos                           |
| Data Warehouse     | Armazenamento relacional em formato MPP e consultas SQL                          |
| Real-Time Analytics| Processamento de eventos em tempo real com KQL                                  |
| Power BI           | Visualização e modelagem de dados integrada                                     |
| Data Activator     | Detecção e reação a eventos de dados automatizados                              |

---

## 🔁 Microsoft Fabric vs Azure Synapse

| Comparativo         | Microsoft Fabric                         | Azure Synapse                                 |
|---------------------|------------------------------------------|-----------------------------------------------|
| Interface           | SaaS, moderna e integrada                | Portal Azure com componentes separados        |
| Integração          | Totalmente integrada (Power BI, ADF etc) | Integração parcial com recursos externos      |
| Orquestração        | Pipelines no Data Factory (Fabric)       | Pipelines no Synapse Studio                   |
| Data Lake           | OneLake integrado                        | Armazenamento externo no ADLS Gen2            |
| Pricing             | Capacidade por Unidade de Processamento  | Billing por recurso isolado                   |
| Escalabilidade      | Alta e automática via Capacidades        | Manual ou elástica com Synapse Pools          |

---

## 💰 Precificação do Microsoft Fabric

O Fabric utiliza **capacidades de computação** (F SKUs), parecidas com as do Power BI Premium:

- **Exemplo de SKU**: F2, F4, F8 etc.
- **Baseado em tempo ativo**: você paga apenas quando a capacidade está ligada.
- **Utilização sob demanda**: possível escalar de forma elástica.

---

## ⚙️ Azure DevOps + Microsoft Fabric

O Azure DevOps permite versionar, automatizar e gerenciar projetos de dados, inclusive no contexto do Microsoft Fabric e Azure Data Factory.

### 🧩 Principais Extensões do Azure DevOps

| Extensão                  | Descrição                                                           |
|---------------------------|---------------------------------------------------------------------|
| Azure Repos               | Controle de versão com Git (repositórios privados)                  |
| Azure Pipelines           | CI/CD para deploy de artefatos em ambientes diferentes              |
| ARM Template Deploy       | Automação de infraestrutura Azure por código (IaC)                  |
| Dataverse Deployment Tool | Deploy de soluções Power Platform / Fabric via DevOps               |
| ADF Tools for DevOps      | Extensão específica para versionamento de Azure Data Factory        |

---

## 🏗️ Criando um Azure Data Factory com Azure DevOps

### 1. Criar o Repositório Git

1. Acesse o **Azure DevOps**.
2. Crie um **novo projeto** e adicione um **Azure Repo Git**.
3. Estruture o repositório.

### 2. Publicar Data Factory no Azure

1. No portal do Azure, crie um **Azure Data Factory**.
2. Vá até a aba de gerenciamento do ADF e clique em **Git Configuration**.
3. Configure com:
- Tipo: Azure DevOps Git
- Conta: Sua organização do DevOps
- Projeto: Nome do projeto DevOps
- Repositório: Nome do repositório Git
- Branch: main ou dev
- Root Folder: `/`

### 3. Versionar com Git

- O ADF criará arquivos `.json` para cada pipeline, linked service e dataset.
- Você poderá criar **pull requests**, trabalhar com **branches** e automatizar deploys com **Pipelines do DevOps**.

---

## 📌 Conclusão

Com o **Microsoft Fabric** você tem uma plataforma completa e moderna para engenharia de dados, substituindo o antigo ecossistema separado (Synapse, Power BI, ADF etc). Integrar isso com o **Azure DevOps** garante versionamento, automação e governança do ciclo de vida dos seus projetos de dados.
