# Relatório DeskData - Sprint 2: de 07/04/2025 à 27/04/2025

<p align="center">
  <a href="#objetivo">Objetivo da sprint</a> |
  <a href="#backlog">Sprint Backlog</a> |
  <a href="#funcionalidades">Funcionalidades adicionadas</a>
</p>

---

## 📍 Objetivo da sprint

A Sprint 2 teve como objetivo avançar nas funcionalidades de **Processamento de Linguagem Natural (PLN)** do sistema DeskData, com foco no **pré-processamento de dados não estruturados** e na **geração de gráficos de similaridades entre chamados**. Também foram realizadas **padronizações visuais** no frontend e a implementação de um **histórico de processamento de chamados**, utilizando dados mockados devido a pendências no backend.

---

## 📋 Sprint Backlog

| Sprint |                           Requisito                           | Status |
| :----: | :-----------------------------------------------------------: | :----: |
|   2    |    Funcionalidade de Classificação de Tipo de Atendimento     |   ✔️    |
|   2    | Serviço de Processamento de Informações com Linguagem Natural |   ✔️    |
|   2    |          Pré-processamento de Dados Não Estruturados          |   ✔️    |
|   2    |           Gráficos de Similaridades entre Chamados            |   ✔️    |
|   2    |            Histórico de Processamento de Chamados             |   ⚠️    |
|   2    |                 Padronizações Visuais (UX/UI)                 |   ✔️    |

**Legenda:**
- ✔️ Concluído
- ⚠️ Parcialmente Concluído (ex.: Frontend concluído, Backend pendente)

---

## 🚀 Funcionalidades adicionadas

### ✅ Pré-processamento de Dados Não Estruturados
- Implementado no microsserviço de IA em **Python** utilizando **Pandas**.
- Limpeza e normalização de textos (remoção de caracteres especiais, formatação de textos) para preparação para PLN.

### ✅ Funcionalidade de Classificação de Tipo de Atendimento
- Desenvolvida no **Backend (TypeScript/Prisma)**.
- Classifica chamados com base em títulos e descrições utilizando PLN.
- Integrada à rota `/chamados/dashboard` para exibir métricas de categorizacão.

### ✅ Gráficos de Similaridades entre Chamados
- Implementados no **Frontend (React/ApexCharts)**.
- Utiliza embeddings de PLN (provavelmente **BERTimbau**) para calcular similaridades entre chamados.
- Exibição de mapas de calor e redes de similaridade no dashboard.

### ✅ Padronizações Visuais (UX/UI)
- Melhorias no **Frontend** utilizando **Tailwind CSS**:
  - Padronização de fontes (ex.: Roboto) e tamanhos.
  - Adição de ícones e melhoria na consistência de cores.

### ⚠️ Histórico de Processamento de Chamados
- Desenvolvido no **Frontend** como uma nova seção para exibição de histórico.
- Atualmente utilizando **dados mockados** devido à falta de integração com o backend.

---

## ⏳ Pendências

### 🔄 Funcionalidade de Busca Semântica
- Parcialmente iniciada nos gráficos de similaridades.
- Endpoint `/chamados/busca-semantica` ainda pendente de implementação completa.

### 🔄 Funcionalidade de Sumarização Automática
- Em andamento, dependente da utilização de modelos mais robustos de PLN.

### 🔄 Integração do Histórico de Chamados com o Backend
- O frontend está pronto para consumir, aguardando a geração dos dados de histórico e sumarização via backend.

---

## 🗓️ Próxima Sprint
- Foco na finalização da **busca semântica**, **sumarização automática**, **integração do histórico de chamados**.
- Implementação de **cadastro de usuários** e **conformidade com a LGPD**.

---

**📓 Sobre a Equipe:**  
Para documentação do processo da equipe, o resumo da Retrospectiva da Sprint 2, com foco no desempenho da equipe, estará disponível [aqui](/docs/SCRUM-Retrospective_Sprint2-DeskData.pdf) após a reunião de retrospectiva.

---
