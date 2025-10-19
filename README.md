# 🧠 Desafio de Projeto — Integrando Dados com MySQL e Power BI

## 📋 Descrição Geral

Este projeto foi desenvolvido como parte do desafio **“Integrando Dados com MySQL Azure e Transformando com Power BI”**, da trilha **Formação Power BI Analyst (DIO)**.

O objetivo principal foi **integrar dados de um banco MySQL** hospedado na **Azure**, realizar **transformações e modelagem no Power BI** e, por fim, **criar dashboards analíticos** que relacionassem **funcionários, dependentes, gestores e departamentos**.

---

## ⚙️ Configuração do Ambiente

Devido à **indisponibilidade de créditos na Azure**, a integração foi feita por meio de uma **conexão direta entre o MySQL local e o Power BI Desktop**, sem uso de instância em nuvem.

- **Banco de dados utilizado:** `azure_company`
- **Ferramenta de visualização:** Power BI Desktop
- **Fonte de dados:** MySQL Workbench (conexão direta)
- **Modelagem de dados:** Power Query + relacionamentos no Power BI

---

## 🧱 Estrutura do Projeto

O projeto foi desenvolvido a partir das tabelas:

- `employee` — informações dos funcionários  
- `department` — departamentos e gerentes  
- `dependent` — dependentes dos funcionários  
- `project` — projetos e alocações  
- `works_on` — relação entre funcionários e projetos  

---

## 🔍 Etapas e Transformações Realizadas

As etapas seguiram as diretrizes do desafio, com pequenas adaptações devido ao ambiente local.

### 1️⃣ Verificação e limpeza dos dados
- Ajuste dos **tipos de dados** (numéricos, texto e double para valores monetários).  
- Remoção de colunas desnecessárias, mantendo apenas as essenciais para análise.  
- Tratamento de **valores nulos** nas colunas `Super_ssn` (indicando gerentes).  
- Padronização de campos de texto (nomes e cargos).

### 2️⃣ Mesclas e junções
- **Mescla de `employee` e `department`** → inclusão do nome do departamento de cada colaborador.  
- **Mescla de `employee` com ele mesmo (auto join)** → inclusão do **nome do supervisor** com base no `Super_ssn`.  

