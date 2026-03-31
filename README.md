# 🚦 Dashboard: Acidentes de Trânsito no Brasil

Análise exploratória dos dados abertos de acidentes de trânsito fornecidos pelo **SENATRAN/RENAST**, cobrindo o período de **2018 a 2025**.

![Dashboard Acidentes de Trânsito](screenshots/dashboard.png)

## 📊 Visão Geral

Este projeto apresenta um relatório interativo desenvolvido em **Power BI**, com foco em identificar padrões, tendências e perfis de vítimas em acidentes de trânsito no Brasil.

## 🗂️ Fontes de Dados

| Tabela | Descrição |
|---|---|
| `Acidentes_DadosAbertos` | Registro de ocorrências por tipo, condição e localização |
| `Vitimas_DadosAbertos` | Perfil das vítimas (faixa etária, gênero, gravidade) |
| `Localidade_DadosAbertos` | Dados geográficos e municipais (IBGE) |
| `TipoVeiculo_DadosAbertos` | Frota circulante e tipo de veículo |
| `feriados_2018_2025` | Calendário de feriados nacionais e pontos facultativos |
| `dCalendario` | Tabela calendário (ano, trimestre, mês) |

## 📐 Modelo de Dados

Esquema estrela com `Acidentes` como tabela fato central, conectada às dimensões de localidade, vítimas, veículos e calendário.

## 📄 Páginas do Relatório

- **Visão Geral** — KPIs principais, tendência trimestral e distribuição por tipo de acidente e perfil demográfico

## 🧮 Principais Medidas DAX

- `Total Acidentes` — contagem de ocorrências
- `Total Envolvidos` / `Total Óbitos` — métricas de impacto
- `Δ Acidentes` e `Δ% Acidentes` — variação YoY com truncamento de período para anos incompletos

## 🛠️ Tecnologias

- Power BI Desktop
- DAX
- Dados Abertos Gov.br (SENATRAN)

## 🔗 Fonte dos Dados

[Dados Abertos — Ministério dos Transportes](https://dados.transportes.gov.br/dataset/renaest)
