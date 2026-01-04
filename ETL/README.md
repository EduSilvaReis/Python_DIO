# 🚀 ETL Pipeline - Santander Dev Week 2023

## 📋 Sobre o Projeto
Este projeto consiste em um script Python que implementa um pipeline **ETL (Extract, Transform, Load)**. O objetivo é simular uma campanha de marketing bancário, gerando mensagens personalizadas de investimento para uma lista de clientes e exportando os resultados em formatos compatíveis com outros sistemas.

## ⚙️ Arquitetura do Pipeline

### 1. Extract (Extração)
O script inicia verificando a existência da base de dados.
- **Fonte de Dados:** Arquivo `SDW2023.csv`.
- **Ação:** Caso o arquivo não exista, o script gera uma massa de dados fictícia (Mock Data) com personagens de anime para fins de teste.
- **Tecnologia:** `pandas.read_csv`.

### 2. Transform (Transformação)
Nesta etapa, aplicamos a lógica de negócio para enriquecer os dados.
- **Lógica:** Uma função simuladora de IA (`generate_ai_message`) cria frases de marketing personalizadas inserindo o nome do usuário na comunicação.
- **Estrutura:** Os dados são reorganizados em uma estrutura de lista de dicionários (`news`), preparando o formato para APIs ou JSON.

### 3. Load (Carregamento)
A etapa final foca na persistência dos dados tratados, com atenção especial à codificação.
- **Saída JSON:** Arquivo `SDW2023_output.json` salvo com `utf-8` para interoperabilidade web.
- **Saída CSV:** Arquivo `SDW2023_final.csv`.
- **Destaque Técnico:** Utilização do encoding **`utf-8-sig`**. Isso garante que caracteres latinos (acentos, cedilha) sejam exibidos corretamente ao abrir o arquivo no Microsoft Excel.

## 🛠️ Tecnologias Utilizadas
* **Python 3**
* **Pandas:** Manipulação de DataFrames e leitura/escrita de CSV.
* **JSON:** Manipulação de estruturas de objetos.
* **OS:** Verificação de sistema de arquivos.
* **Google Colab Files:** (Opcional) Para download automático no ambiente nuvem.
