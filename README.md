# 🖥️ DeskData 🖥️

## 📓 Sobre o Projeto

O projeto DeskData facilita e automatiza a obtenção de informações em Atendimentos Inteligentes, reduzindo a carga de trabalho manual e aumentando a eficiência do atendimento, além de possibilitar a tomada de decisões baseadas em dados. A aplicação é composta por três microsserviços principais:
- **Backend**: TypeScript
- **Frontend**: TypeScript
- **Serviço de IA**: Python

---

## 🔨 Entregas

| Sprint | Início     | Fim       | Status             | Relatório                     |
| :----: | :--------: | :-------: | :----------------: | :----------------------------: |
|   01   | 10/03/2025 | 30/03/2025 | ✅ Concluída       | [Relatório](sprints/sprint1.md) |
|   02   | 07/04/2025 | 27/04/2025 | ✅ Concluída       | [Relatório](sprints/sprint2.md) |
|   03   | 05/05/2025 | 25/05/2025 | ✅ Concluída       | [Relatório](sprints/sprint3.md) |

[Voltar ao topo](#topo)

---

## 📝 Backlog do Produto

| Sprint | Requisito                                                     | Status |
| :----: | :------------------------------------------------------------: | :----: |
|   1    | Serviço para Tratamento de Dados                               | ✔️ |
|   1    | Interface Web                                                  | ✔️ |
|   1    | Funcionalidade de Dashboards com Insights Diários              | ✔️ |
|   2    | Funcionalidade de Classificação de Tipo de Atendimento         | ✔️ |
|   2    | Serviço de Processamento de Informações com Linguagem Natural  | ✔️ |
|   2    | Pré-processamento de Dados Não Estruturados                    | ✔️ |
|   2    | Gráficos de Similaridades entre Chamados                       | ✔️ |
|   2    | Histórico de Processamento de Chamados                         |✔️ |
|   2    | Padronizações Visuais (UX/UI)                                  | ✔️ |
|   3    | Funcionalidade de Busca Semântica                              | ✔️ |
|   3    | Funcionalidade de Sumarização Automática                       | ✔️ |
|   3    | Cadastro de Usuários                                           | ✔️ |

**Legenda:**
- ✔️ Concluído
- ⚠️ Parcialmente Concluído
- ❗ Pendente

[Voltar ao topo](#topo)

---

## 📺 BPMN do Projeto

O BPMN atualizado até a Sprint 2:

**Participantes:**
- Usuário/Desenvolvedor
- Sistema DeskData

**Processo:**
1. Fornecimento de arquivos CSV.
2. Inserção dos CSVs na pasta `data/` do serviço de IA.
3. Processamento e pré-processamento de dados não estruturados.
4. Armazenamento no PostgreSQL.
5. Validação dos dados.
6. Backend aplica regras de negócio e classifica chamados via PLN.
7. Frontend exibe dashboards, gráficos de similaridades e histórico (mockado).
8. Usuário visualiza insights.

**Notas:**
- Sprint 1: Dashboards iniciais.
- Sprint 2: Gráficos de similaridades, pré-processamento, histórico.

[Voltar ao topo](#topo)

---

## 🚧 Fluxo do Sistema

**Componentes e Fluxo:**
- CSVs → Serviço de IA (Python/Pandas) → PostgreSQL (Docker) → Backend (Express/Prisma) → Frontend (React/Vite/ApexCharts).

**Notas:**
- Sprint 1: Tratamento de dados e dashboards.
- Sprint 2: Pré-processamento de dados não estruturados, similaridades e padronizações visuais.

[Voltar ao topo](#topo)

---

## 📡 Repositórios

- [Serviço Backend](https://github.com/DeskData-Api/Backend)
- [Serviço Frontend Web](https://github.com/DeskData-Api/Frontend-Web)
- [Serviço de IA](https://github.com/DeskData-Api/Python-Services)

[Voltar ao topo](#topo)

---

## 🛠️ Tecnologias Utilizadas

| Ferramenta       | Tipo de Tecnologia        |
| :--------------: | :-----------------------: |
| TypeScript       | 🔨 Desenvolvimento     |
| Python           | 🔨 Desenvolvimento     |
| React            | 🔨 Desenvolvimento     |
| Express          | 🔨 Desenvolvimento     |
| Prisma           | 🔧 ORM / Banco de Dados |
| Pandas           | 🔧 Processamento de Dados |
| Vite             | 🔧 Build Tool           |
| Tailwind CSS     | 🎨 Estilização         |
| ApexCharts       | 📊 Visualização         |
| Git & GitHub     | 🔧 Controle de Versão   |
| Docker           | 🐳 Containerização       |
| PostgreSQL       | 📄 Banco de Dados        |
| AWS              | ☁️ Infraestrutura na Nuvem |

[Voltar ao topo](#topo)

---

## 📁 Documentação Específica

- [Arquitetura do Sistema](docs/Arquitetura%20do%20Sistema.md)
- [Manual de Uso do Sistema](docs/Manual%20do%20Sistema.md)

[Voltar ao topo](#topo)

---

## 🧑‍💻 Colaboradores

| Função          | Nome                    | LinkedIn & GitHub |
| :--------------: | :---------------------- | :------------------------------------------------------------: |
| Product Owner    | Caio Vitor Dias          | [LinkedIn](https://www.linkedin.com/in/caio-vitor-c1/) - [GitHub](https://github.com/caiovitordias1) |
| Scrum Master     | Augusto Henrique Buin    | [LinkedIn](https://www.linkedin.com/in/augusto-henrique-buin) - [GitHub](https://github.com/AugustoBuin) |
| Dev Team         | Felipe Augusto Graciano  | [LinkedIn](https://www.linkedin.com/in/felipe-augusto-graciano-2b796026a/) - [GitHub](https://github.com/Yetgvg) |
| Dev Team         | Julio de Paula Machado   | [LinkedIn](https://www.linkedin.com/in/j%C3%BAlio-machado-7a07a4250) - [GitHub](https://github.com/JulioPm142) |
| Dev Team         | Valderi Douglas          | [LinkedIn](https://br.linkedin.com/in/valderidouglas) - [GitHub](https://github.com/ValderiDouglas) |

[Voltar ao topo](#topo)
