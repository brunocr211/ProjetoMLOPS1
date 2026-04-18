# Desafio MLOps Playground: Previsão de rotatividade de clientes (40 pontos)

## Objetivo

Neste desafio, irá implementar um modelo de aprendizagem automática pré-treinado para prever a rotatividade de clientes utilizando o conjunto de dados «Bank Customer Churn Dataset». O modelo fornecido (`churn_model.pkl`) será integrado num pipeline para carregamento do modelo, recolha de dados de entrada e previsão. Também irá automatizar o processo utilizando o Docker e o GitHub Actions para CI/CD. O GitHub Codespaces irá ajudá-lo a configurar, executar e testar o projeto num ambiente consistente.

### Observe a estrutura do repositório 

Organize o seu projeto com a seguinte estrutura (Note que o diretório contém subdiretórios e ficheiros):

```
- models/              # Diretório para armazenar o modelo pré-treinado
  - churn_model.pkl    # Ficheiro pickle do modelo pré-treinado
- src/                 # Diretório para scripts de implementação
  - run_model.py       # Script para interagir com o modelo
- Dockerfile           # Ficheiro de configuração do Docker
- .github/workflows/   # Ficheiros de configuração de CI/CD
  - deploy.yml         # Ficheiro de fluxo de trabalho do GitHub Actions
- requirements.txt     # Dependências Python

```

## Descrição das tarefas

### Tarefa 1: Carregar o modelo pré-treinado (10 pontos)

- Escreva um script em Python (`load_model.py` no diretório `src/`) para carregar o modelo pré-treinado usando `pickle`.
- Certifique-se de que o modelo seja carregado corretamente do diretório `models/`, onde o arquivo `churn_model.pkl` está armazenado.

---

### Tarefa 2: Previsão interativa (10 pontos)
- Implemente um script em Python (`run_model.py`) para solicitar ao usuário os dados do cliente (por exemplo, pontuação de crédito, idade, saldo, número de produtos, etc.).
- Use o modelo pré-treinado para prever se o cliente irá cancelar o serviço com base nos valores inseridos.

---

### Tarefa 3: Dockerizar a aplicação (10 pontos)

- Crie um `Dockerfile` que:
  1. Use **Python 3.8 ou posterior** como imagem base.
  2. Copie os arquivos necessários (modelo, scripts, etc.) para o contêiner.
  3. Instale as dependências necessárias do `requirements.txt`.
  4. Execute o script `run_model.py` dentro do contêiner.
---

### Tarefa 4: Configurar o pipeline de CI/CD com o GitHub Actions (10 pontos)

- Configure um fluxo de trabalho do GitHub Actions que:
  1. Instale as dependências.
  2. Compile a imagem do Docker.
  3. Execute o contêiner para rodar o script `run_model.py`.
- O fluxo de trabalho deve ser acionado sempre que alterações forem enviadas para o branch `main`.

---

### Usando o GitHub Codespaces

Para desenvolver e testar o projeto, use o **GitHub Codespaces** como seu ambiente de desenvolvimento:

1. **Faça um fork do repositório** e clique no botão verde **Code** no seu repositório forkado.
2. Selecione **Codespaces** e escolha “Create codespace on main” para abrir seu ambiente de desenvolvimento.
3. Quando seu Codespace estiver pronto, vá até a pasta `src/` e comece a trabalhar nos scripts `load_model.py` e `run_model.py`.
4. Siga a estrutura do projeto para implementar cada tarefa e testar seu código diretamente no Codespace.

---
