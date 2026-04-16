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

