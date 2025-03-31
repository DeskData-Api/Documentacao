# PROJETO DESKDATA
## Manual de Uso do Sistema

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

## INSTALAÇÃO E USO DO SISTEMA

### I. Requisitos Mínimos

- **Docker** e **Docker Compose** (para PostgreSQL e containerização).  
- **Python 3.8+** (para o serviço de IA).  
- **Node.js** (versão LTS recomendada, para Backend e Frontend).  
- **Git** (para clonar os repositórios).  
- Arquivo CSV de chamados no formato especificado (ex.: colunas `id`, `titulo`, `data_abertura`, etc.).  

---

### II. Instalação do Sistema

O sistema DeskData é composto por três microsserviços. Siga os passos abaixo para instalar cada um.

#### Serviço Backend
1. Clone o repositório:  
   ```
   git clone https://github.com/DeskData-Api/Backend.git
   cd Backend
   ```
2. Instale as dependências:  
   ```
   npm install
   ```
3. Crie um arquivo `.env` na raiz do projeto com:  
   ```
   DATABASE_URL="postgresql://deskdata:deskdata@localhost:5432/chamados_db?schema=public"
   PORT=3003
   ```
4. Gere os arquivos do Prisma:  
   ```
   npx prisma generate
   ```

#### Serviço de IA
1. Clone o repositório:  
   ```
   git clone https://github.com/DeskData-Api/Python-Services.git
   cd Python-Services
   ```
2. Crie e ative um ambiente virtual:  
   ```
   python -m venv venv
   source venv/bin/activate  # Windows: venv\Scripts\activate
   ```
3. Instale as dependências:  
   ```
   pip install -r requirements.txt
   ```
4. Coloque o arquivo CSV de chamados na pasta `data/` (ex.: `data/chamados.csv`).  

#### Serviço Frontend
1. Clone o repositório:  
   ```
   git clone https://github.com/DeskData-Api/Frontend-Web.git
   cd Frontend-Web
   ```
2. Instale as dependências:  
   ```
   npm install
   ```

---

### III. Rodando a Aplicação

#### Serviço de IA
1. Inicie o container PostgreSQL:  
   ```
   docker-compose up -d
   ```
   - Verifique se o banco está rodando em `localhost:5432` com usuário/senha `deskdata:deskdata`.  
2. Execute o script principal:  
   ```
   python src/main.py
   ```
   - Isso processará o CSV de chamados e armazenará os dados no banco.  

#### Serviço Backend
1. Certifique-se de que o PostgreSQL (via Docker) está ativo e populado pelo serviço de IA.  
2. Inicie o servidor:  
   ```
   npm run dev
   ```
   - A API estará disponível em `http://localhost:3003`.  

#### Serviço Frontend
1. Inicie o servidor de desenvolvimento:  
   ```
   npm run dev
   ```
   - O frontend estará disponível em `http://localhost:5173`.  

#### Parando os Containers
- Para parar o PostgreSQL:  
   ```
   docker-compose down
   ```

---

### IV. Usando o Sistema

Após iniciar os três serviços:  
1. Acesse o frontend em `http://localhost:5173` no navegador.  
2. Na interface web, visualize os dashboards com insights diários:  
   - Gráficos de total de chamados, abertos, fechados, etc.  
   - Top categorias e elementos associados.  
3. Os dados exibidos são processados pelo serviço de IA e fornecidos pelo backend via rota `/chamados/dashboard`.  

**Nota:** Funcionalidades como busca semântica e análise de sentimentos estarão disponíveis em futuras sprints.  

---

**[Nota Final]**  
Este manual reflete o estado do sistema após a Sprint 1 (30/03/2025). Atualizações serão feitas conforme novas funcionalidades forem implementadas.