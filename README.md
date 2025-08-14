# 📊 Projeto: Integração com API da CVM e BrasilAPI com Tratamento e Armazenamento no Databricks

Projeto Prático — Pipeline Python para Dados via APIs (Compass)

Este projeto realiza a ingestão de dados públicos da **CVM (Comissão de Valores Mobiliários)** e da **BrasilAPI** diretamente no Databricks, com tratamento das informações e armazenamento em tabelas Delta para análises posteriores.

---

## 📌 Fontes de Dados

- **CVM** — Disponibiliza arquivos CSV com informações atualizadas sobre fundos de investimento.
- **BrasilAPI** — Permite a consulta de dados de empresas a partir do CNPJ informado.

**Endpoints utilizados:**

- CVM: https://dados.cvm.gov.br/dados/FI/CAD/DADOS/cad_fi.csv
- BrasilAPI: https://brasilapi.com.br/api/cnpj/v1/{cnpj}

**Documentações:**

- CVM: https://dados.cvm.gov.br/dados/FI/CAD/DADOS/
- BrasilAPI: https://brasilapi.com.br/docs#tag/CNPJ

---

## ⚙️ Pré-requisitos

- **Databricks** configurado
- **Runtime com PySpark** habilitado

**Bibliotecas necessárias:**

- pandas
- requests
- pyspark
- io

🚀 Execução

- Criar um Notebook no Databricks.
- Copiar o código do projeto para o Notebook.
- Executar o arquivo Bronze_cvm para ingestão e tratamento dos dados da CVM.
- Executar o arquivo Bronze_brasil para enriquecimento dos dados com informações da BrasilAPI.
- Consultar os dados no Databricks com:
  SELECT * FROM cvm_bronze;
  SELECT * FROM brasil_bronze;

📄 Licença
Este projeto utiliza dados públicos disponibilizados sob licença aberta.
O uso é livre, respeitando as condições dos endpoints consultados.
