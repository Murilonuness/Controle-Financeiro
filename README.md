# Controle Financeiro com Google Sheets

Este projeto permite o gerenciamento de finanças pessoais utilizando uma planilha no Google Sheets. Ele é desenvolvido com **Streamlit**, **Google Sheets API** e **Plotly** para visualizações interativas. Com ele, você pode filtrar dados, gerar gráficos, importar/exportar arquivos CSV e muito mais.

## Funcionalidades

- **Controle financeiro**: Gerencie suas receitas e despesas de forma simples.
- **Resumo por categoria**: Veja seus gastos e ganhos agrupados por categoria.
- **Resumo mensal**: Acompanhe a evolução do seu saldo ao longo dos meses.
- **Filtragem**: Filtre por tipo (receita ou despesa), categoria e competência (mês/ano).
- **Geração de dados fictícios**: Adicione dados de teste aleatórios para simulações.
- **Importação/Exportação de CSV**: Importe dados de um CSV para a planilha ou exporte os dados atuais.
- **Limpeza de dados**: Exclua um número específico de linhas da planilha.
- **Exclusão da planilha**: Apague toda a planilha do Google Sheets.

## Você pode acessar o projeto em produção no seguinte link:

[Deploy: controlefinanceirosheets.streamlit.app](https://controlefinanceirosheets.streamlit.app)

## Você pode visualizar o modelo da planilha de controle financeiro que o projeto utiliza clicando no link abaixo:

[Planilha de Controle Financeiro](https://docs.google.com/spreadsheets/d/1GefKYSag0D-YgmCWWoPdLubdjoF-mfJMeYcia6Wy5eY/edit?gid=0#gid=0)


## 📂 Como Rodar o Projeto Localmente

### 1. Instalar as dependências

Certifique-se de que o Python e o `pip` estão instalados em sua máquina. Em seguida, instale os pacotes necessários:

```bash
pip install streamlit pandas plotly gspread oauth2client
```

### 2. Configurar o acesso ao Google Sheets

- Crie um projeto no [Google Cloud Console](https://console.cloud.google.com/).
- Ative as APIs **Google Sheets API** e **Google Drive API**.
- Crie credenciais do tipo **Conta de Serviço (Service Account)** e baixe o arquivo JSON.
- Renomeie o arquivo para `credenciais.json` e coloque-o na raiz do projeto.

### 3. Configurar variável de ambiente

Adicione o conteúdo do arquivo `credenciais.json` em uma variável de ambiente:

#### Linux/macOS:
```bash
export GOOGLE_CREDS_JSON='{"type": "service_account", ...}'
```

#### Windows (PowerShell):
```powershell
$env:GOOGLE_CREDS_JSON='{"type": "service_account", ...}'
```

### 4. Rodar o projeto

Execute o comando abaixo para iniciar o aplicativo:

```bash
streamlit run app.py
```

O navegador abrirá automaticamente com a interface da aplicação.

## 📁 Estrutura do Projeto

- `app.py`: Arquivo principal da aplicação com a interface em Streamlit.
- `crudPlanilha.py`: Contém a classe `GerenciarPlanilha`, que gerencia operações na planilha do Google Sheets.
- `planilhaFicticia.py`: Contém a classe `PlanilhaFicticia`, que insere dados fictícios na planilha.
- `requirements.txt`: Lista de dependências para instalação do projeto.

---

## 📷 Screenshot

![Screenshot do projeto](/media/project.png)

Desenvolvido com ❤️ usando Python e ferramentas de produtividade na nuvem.
👨‍💻 [GitHub: Murilonuness](https://github.com/Murilonuness)
