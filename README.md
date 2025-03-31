<h1 id="topo" align="center"> 🖥️ DeskData 🖥️ </h1>

## 📓  Sobre o Projeto

O projeto consiste num sistema cujo intuito é facilitar e automatizar a obtenção de informações em um Atendimento Inteligente, de modo a reduzir a carga de trabalho manual e aumentar a eficiência do atendimento, bem como possibilitar a tomada de decisões a partir da análise desses dados.

Serviços de atendimento inteligente geram grandes quantidades de dados devido às interações entre as entidades. Com esse sistema, será possível não só organizar essas infromações, mas também, analisá-las e torná-las úteis através de insights que garantirão uma melhor eficácia para a tomada de decisões do negócio.

A aplicação é montada por 3 microsserviços principais, o Backend construído em typescript, o Frontend, também em typescript e o serviço de IA construído em python.

<span id="entregas">
<br>
  
## 🔨 Entregas

| Sprint |   Início   |    Fim     |   Status    |                                  Relatório da Sprint                                   |
| :----: | :--------: | :--------: | :---------: | :------------------------------------------------------------------------------------: |
|   01   | 10/03/2025 | 30/03/2025 | ✅ Concluída | [Relatório](sprints/sprint1.md) |
|   02   | 07/04/2025 | 27/04/2025 | 🚧 Bloqueado |                                                                                        |
|   03   | 05/05/2025 | 25/05/202  | 🚧 Bloqueado |                                                                                        |


→ [Voltar ao topo](#topo)

<br>

## 📝 Backlog do Produto

<div align="center">
  
| Sprint |                           Requisito                            | status |
| :----: | :------------------------------------------------------------: | :----: |
|   1    |                Serviço para Tratamento de dados                |   ✔️    |
|   1    |                         Interface web                          |   ✔️    |
|   1    |       Funcionalidade de dashboards com insights diarios        |   ✔️    |
|   2    | Serviço de processamento de informações com linguagem natural  |   ❗    |
|   2    |   Aplicar análise de sentimentos para geração de dashboards    |   ❗    |
|   2    |           Funcionalidade de busca semântica e prompt           |   ❗    |
|   2    |            Funcionalidade de sumarização automatica            |   ❗    |
|   2    |     Funcionalidade de classificação de tipo de atendimento     |   ❗    |
|   3    |                      Cadastro de Usuários                      |   ❗    |
|   3    |                    Banco de dados Usuários                     |   ❗    |
|   3    |                Não funcional - adequação à lgpd                |   ❗    |
|   3    | Não funcional - garantia de escalabilidade (através de testes) |   ❗    |
|   3    |       Não funcional - remoção correta de dados pessoais        |   ❗    |

</div>

<br>

## 🗺️ BPMN do Projeto

O BPMN descreve o processo de utilização do sistema DeskData conforme implementado na Sprint 1 (concluída em 30/03/2025):

- **Participantes**:
  - **Usuário/Desenvolvedor**: Inicia o sistema e fornece os dados.
  - **Sistema DeskData**: Executa as etapas automatizadas.
- **Processo**:
  1. **Início**: O usuário fornece arquivos CSV (chamados).
  2. **Tarefa (Usuário)**: Colocar os CSVs na pasta `data/` do serviço de IA.
  3. **Tarefa (Sistema)**: O serviço de IA (Python/Pandas) processa e trata os CSVs, realizando normalização, limpeza e padronização.
  4. **Tarefa (Sistema)**: Os dados tratados são armazenados no banco PostgreSQL.
  5. **Decisão**: "Dados estão corretos?" 
     - Se sim, prossegue.
     - Se não, retorna ao usuário para corrigir os CSVs.
  6. **Tarefa (Sistema)**: O backend (Express/Prisma) consulta os dados e gera estatísticas via rota `/chamados/dashboard`.
  7. **Tarefa (Sistema)**: O frontend (React/Vite) consome a API e exibe dashboards com insights diários.
  8. **Fim**: O usuário visualiza os insights nos gráficos.
- **Notas**: 
  - Este processo reflete a Sprint 1. Funcionalidades como PLN e busca semântica serão adicionadas na Sprint 2.

<br>

## 🪧 Fluxo do Sistema

O Fluxo do Sistema DeskData detalha a interação entre os microsserviços após a Sprint 1 (concluída em 30/03/2025):

- **Componentes e Fluxo**:
  1. **Fonte de Dados**: Arquivos CSV (chamados) são fornecidos como entrada.
  2. **Serviço de IA (Python)**: Processa os CSVs com Pandas, executando tratamento (normalização, limpeza, padronização) e envia os dados ao banco.
  3. **Banco de Dados (PostgreSQL)**: Armazena os dados tratados em tabelas "Chamados", acessíveis via Docker.
  4. **Serviço Backend (TypeScript)**: Consulta os dados no PostgreSQL com Prisma, aplica regras de negócio e os disponibiliza na API (ex.: `/chamados/dashboard`).
  5. **Serviço Frontend (React)**: Consome a API com Axios e exibe os dados em dashboards interativos usando ApexCharts.
- **Caminho dos Dados**: 
  - CSVs → Serviço de IA → PostgreSQL → Backend → Frontend.
- **Notas**: 
  - Este fluxo representa a arquitetura da Sprint 1. Expansões como PLN e análise de sentimentos estão planejadas para a Sprint 2.

<br>


## 📡 Repositórios

- → [Serviço Backend](https://github.com/DeskData-Api/Backend)
- → [Serviço Frontend Web](https://github.com/DeskData-Api/Frontend-Web)
- → [Serviço de IA](https://github.com/DeskData-Api/Python-Services)

→ [Voltar ao topo](#topo)

<br>

## 🛠️ Tecnologias utilizadas


|    Ferramenta    |    Tipo de Tecnologia     |
| :--------------: | :-----------------------: |
|  **TypeScript**  |     🔨 Desenvolvimento     |
|    **Python**    |     🔨 Desenvolvimento     |
|    **React**     |     🔨 Desenvolvimento     |
|   **Express**    |     🔨 Desenvolvimento     |
|    **Prisma**    |  🔧 ORM / Banco de Dados   |
|    **Pandas**    | 🔧 Processamento de Dados  |
|     **Vite**     |       🔧 Build Tool        |
| **Tailwind CSS** |       🎨 Estilização       |
|  **ApexCharts**  |      📊 Visualização       |
| **Git & GitHub** |   🔧 Controle de Versão    |
|    **Docker**    |     🐳 Containerização     |
|  **PostgreSQL**  |     🗄️ Banco de Dados      |
|     **AWS**      | ☁️ Infraestrutura na Nuvem |



→ [Voltar ao topo](#topo)

<br>

## 📑 Documentação específica:

 - [Arquitetura do Sistema](docs/Arquitetura%20do%20Sistema.md)

 - [Manual de Uso do Sistema](docs/Manual%20do%20Sistema.md)

→ [Voltar ao topo](#topo)
<br>
<span id="equipe">

<br>

## 🧑‍💻 Colaboradores

|    Função     | Nome                    |                                                                                                                                                   LinkedIn & GitHub                                                                                                                                                    |
| :-----------: | :---------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| Product Owner | Caio Vitor Dias         |       [![Linkedin Badge](https://img.shields.io/badge/Linkedin-blue?style=flat-square&logo=Linkedin&logoColor=white)](https://www.linkedin.com/in/caio-vitor-c1/) [![GitHub Badge](https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white)](https://github.com/caiovitordias1)       |
| Scrum Master  | Augusto Henrique Buin   |         [![Linkedin Badge](https://img.shields.io/badge/Linkedin-blue?style=flat-square&logo=Linkedin&logoColor=white)](www.linkedin.com/in/augusto-henrique-buin) [![GitHub Badge](https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white)](https://github.com/AugustoBuin)         |
|   Dev Team    | Felipe Augusto Graciano | [![Linkedin Badge](https://img.shields.io/badge/Linkedin-blue?style=flat-square&logo=Linkedin&logoColor=white)](https://www.linkedin.com/in/felipe-augusto-graciano-2b796026a/) [![GitHub Badge](https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white)](https://github.com/Yetgvg) |
|   Dev Team    | Julio de Paula Machado  |    [![Linkedin Badge](https://img.shields.io/badge/Linkedin-blue?style=flat-square&logo=Linkedin&logoColor=white)](https://www.linkedin.com/in/júlio-machado-7a07a4250) [![GitHub Badge](https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white)](https://github.com/JulioPm142)     |
|   Dev Team    | Valderi Douglas         |       [![Linkedin Badge](https://img.shields.io/badge/Linkedin-blue?style=flat-square&logo=Linkedin&logoColor=white)](https://br.linkedin.com/in/valderidouglas) [![GitHub Badge](https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white)](https://github.com/ValderiDouglas)        |


→ [Voltar ao topo](#topo)
