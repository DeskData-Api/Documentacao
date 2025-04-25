# Relatório DeskData - Sprint 1: de 10/03/2025 à 30/03/2025

<p align="center">
  <a href="#objetivo">Objetivo da sprint</a> |
  <a href="#backlog">Sprint Backlog</a> |
  <a href="#funcionalidades">Funcionalidades adicionadas</a>
</p>

---

## 📌 Objetivo da sprint
A Sprint 1 teve como objetivo implementar as bases do sistema DeskData, focando na ingestão e tratamento de dados, construção da interface web e geração de dashboards com insights diários. Além disso, buscou-se iniciar o desenvolvimento de funcionalidades avançadas como processamento de linguagem natural (PLN), análise de sentimentos e busca semântica.

---

## 📋 Sprint Backlog

| Sprint |                          Requisito                          | Status |
| :----: | :---------------------------------------------------------: | :----: |
|   1    |              Serviço para Tratamento de dados               |   ✔️    |
|   1    |                        Interface web                        |   ✔️    |
|   1    | Funcionalidade de geração de dashboards de insights diários |   ✔️    |

---

## 🚀 Funcionalidades adicionadas

### ✅ Serviço para Tratamento de Dados
- Implementado no microsserviço de IA em **Python**, utilizando **Pandas** para processar arquivos CSV de chamados.
- Os dados são normalizados, limpos e armazenados no banco de dados **PostgreSQL**.
  
### ✅ Interface Web
- Desenvolvida em **TypeScript** com **React** e **Vite**, oferecendo uma interface simples e intuitiva para visualização de dados.
  
### ✅ Funcionalidade de Dashboards com Insights Diários
- Integrada ao frontend, exibindo gráficos gerados a partir dos dados processados pelo backend, como volume de chamados por dia.

---

## ⏳ Pendências

### 🔄 Serviço de Processamento de Informações com Linguagem Natural
- Iniciado, mas não concluído. A base para manipulação de dados está pronta, mas a integração com PLN ainda está em andamento.

### 🔄 Aplicar Análise de Sentimentos para Geração de Dashboards
- Parcialmente implementado no serviço de IA, porém sem finalização para exibição nos dashboards.

### 🔄 Funcionalidade de Busca Semântica e Prompt
- Planejada, mas não concluída devido à priorização das entregas básicas.

---

**📅 Próxima Sprint:** Foco na implementação completa das funcionalidades de PLN, análise de sentimentos e otimização dos dashboards.

--- 
** Sobre a Equipe: ** Para documentação do processo da equipe, o resumo da Retrospectiva da Sprint 1, com foco no desempenho da equipe está disponível [aqui](/docs/SCRUM-Retrospective_%20Sprint%201-DeskData.pdf)