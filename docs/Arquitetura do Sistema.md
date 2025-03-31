# PROJETO DESKDATA
## Arquitetura e Desenvolvimento do Sistema

**Equipe:**  
- Augusto Henrique Buin  
- Caio Vitor Dias  
- Felipe Augusto Graciano  
- Júlio de Paula Machado  
- Valderi Douglas Camargo  

**Instituição:** Fatec Jessen Vidal  
**Grupo:** DeskData - 6º Semestre  
**Curso:** Desenvolvimento de Software Multiplataforma  
**Ano:** 2025

---

## ARQUITETURA E FUNCIONAMENTO DOS SISTEMAS

### I. Sobre o Sistema

Esse sistema foi elaborado com base na problemática de que, na presença de grandes volumes de dados gerados por interações de usuários em sistemas de atendimento, é necessária uma análise eficiente e automatizada para extrair informações relevantes e formar insights de interesse ao negócio. Tendo isso em vista, o sistema foi construído para receber um conjunto de dados no formato CSV, processá-lo, tratá-lo e manipulá-lo, exibindo os resultados de forma gráfica e intuitiva.

Na Sprint 1 (concluída em 30/03/2025), foram entregues:
- Tratamento de dados via serviço de IA.
- Interface web com dashboards de insights diários.
- API backend para suporte aos dashboards.

Funcionalidades como Processamento de Linguagem Natural (PLN), análise de sentimentos e busca semântica estão planejadas para a Sprint 2 (07/04/2025 - 27/04/2025).

---

### II. Visão Geral

O sistema DeskData é composto por três microsserviços principais:
- **Serviço de IA** (Python): Processa e trata os dados de entrada.
- **Backend** (TypeScript): Aplica regras de negócio e disponibiliza os dados via API.
- **Frontend** (TypeScript/React): Exibe os dados em uma interface gráfica.

---

### III. Funcionamento do Serviço de IA

O serviço de IA foi desenvolvido em Python, utilizando a biblioteca **Pandas** para manipulação de dados. Ele é responsável por:
1. Receber um arquivo CSV de chamados na pasta `data/` (ex.: `data/chamados.csv`).
2. Processar e tratar os dados através de uma pipeline que inclui:
   - Normalização de campos.
   - Limpeza de conjuntos irrelevantes.
   - Padronização de formatos.
3. Armazenar os dados tratados no banco de dados PostgreSQL.

Na Sprint 1, o tratamento de dados foi concluído, mas o suporte a PLN ainda está em desenvolvimento (Sprint 2).

---

### IV. Funcionamento do Serviço Banco de Dados

O banco de dados escolhido foi o **PostgreSQL**, executado em um container Docker. Ele possui uma tabela principal para armazenar os dados de chamados técnicos.

#### Estrutura da Tabela Chamados

| **Coluna**             | **Descrição**                   |
| ---------------------- | ------------------------------- |
| id                     | Identificador único             |
| titulo                 | Título do chamado               |
| entidade               | Entidade relacionada (opcional) |
| categoria              | Categoria do chamado (opcional) |
| localizacao            | Localização (opcional)          |
| elementos_associados   | Elementos associados (opcional) |
| data_abertura          | Data de abertura                |
| data_fechamento        | Data de fechamento (opcional)   |
| tempo_interno_excedido | Tempo excedido (opcional)       |
| tempo_resposta         | Tempo de resposta (opcional)    |
| tempo_interno_resposta | Tempo interno (opcional)        |
| descricao              | Descrição do chamado            |
| plugins                | Plugins usados (opcional)       |
| solucao                | Solução aplicada (opcional)     |
| status                 | Status atual                    |
| tipo                   | Tipo do chamado (opcional)      |
| tecnico_atribuido      | Técnico responsável (opcional)  |
| fornecedor_atribuido   | Fornecedor (opcional)           |
| ultima_atualizacao     | Última atualização (opcional)   |

---

### V. Funcionamento do Serviço Backend

O serviço backend foi construído em **TypeScript** com **Express** e **Prisma** como ORM. Ele:
1. Coleta os dados tratados do PostgreSQL via consultas.
2. Aplica regras de negócio, como filtragens e categorizações.
3. Disponibiliza os dados manipulados em rotas HTTP.

#### Rotas Implementadas (Sprint 1)
- **GET /chamados/dashboard**: Retorna estatísticas para dashboards (total, abertos, fechados, tempo médio, top categorias, etc.).
- **GET /chamados/abertos**: Lista chamados com status "Processando".
- **GET /chamados/:id**: Retorna detalhes de um chamado específico.

---

### VI. Funcionamento do Serviço Frontend

O frontend foi desenvolvido em **TypeScript** com **React**, **Vite** e **Tailwind CSS**, utilizando **ApexCharts** para gráficos. Ele:
1. Consome os dados das rotas do backend.
2. Exibe uma interface simples, clara e intuitiva com dashboards interativos.

Na Sprint 1, foram entregues a interface web e os dashboards com insights diários.

---

## DESENVOLVIMENTO DO PROJETO

### VII. Metodologias e Técnicas

O projeto segue os princípios da metodologia ágil **Scrum**, com sprints de 3 semanas. Ferramentas utilizadas:
- **Discord**: Comunicação interna do time.
- **Figma**: Prototipação da interface.
- **Whimsical**: Documentação inicial.
- **Jira**: Planejamento de escopo e tarefas.
- **Slack**: Comunicação com o cliente.
- **Git/GitHub**: Controle de versão e repositório.

Tecnologias práticas:
- **Docker**: Containerização.
- **AWS**: Infraestrutura em rede.
- **Visual Studio Code**: Desenvolvimento.
- **PostgreSQL**: Banco de dados.

---

### VIII. Padronização de Branches e Commits

- **Branches**: Nomeadas conforme as tarefas do Jira (ex.: `feature/tratamento-dados`).
- **Commits**: Seguem o padrão `<tipo>: <descrição>`:
  - `feat`: Nova funcionalidade.
  - `fix`: Correção crítica.
  - `refactor`: Melhoria de código.
  - `docs`: Atualização de documentação.

---

### IX. Andamento do Projeto

A Sprint 1 (10/03/2025 - 30/03/2025) teve um início instável devido a um escopo inicial complexo, que foi ajustado ao longo do período. Alterações incluíram:
- Abandono de um serviço mobile.
- Adiamento de funcionalidades de login.

Comunicação constante com o cliente, professores e o time via Slack e Discord permitiu contornar obstáculos e entregar:
- Tratamento de dados (Python-Services).
- Interface web e dashboards (Frontend-Web).
- API para suporte aos dashboards (Backend).

Pendências como PLN, análise de sentimentos e busca semântica foram movidas para a Sprint 2 (07/04/2025 - 27/04/2025).

---

### X. Fluxo Simplificado (Resumo)

1. O serviço de IA processa um CSV de chamados e realiza o tratamento (limpeza, normalização).
2. O campo "descrição" é o mais relevante para análise.
3. Os dados tratados são armazenados no banco.
4. O backend coleta os dados, aplica regras de negócio e os disponibiliza em rotas.
5. O frontend busca as rotas e exibe os dados em gráficos.

---

**[Nota Final]**  
Este documento será atualizado ao fim de cada sprint para refletir o progresso do sistema DeskData. Versão atual: 30/03/2025 (pós-Sprint 1).