# Challenge_Telecom_X2
Analise de evasão de clientes

# Análise Preditiva de Churn na Telecom X 🚀

## �� Visão Geral do Projeto

Este repositório contém a análise completa e o desenvolvimento de um modelo de Machine Learning para prever a evasão de clientes (churn) em uma empresa fictícia do setor de telecomunicações, a Telecom X. O objetivo principal é ir além da simples modelagem, construindo um pipeline de ponta a ponta, desde a limpeza dos dados até a interpretação estratégica dos resultados, transformando dados brutos em insights acionáveis para o negócio.

Este projeto foi desenvolvido como parte de um desafio prático para a posição de Analista de Machine Learning.

---

## 🎯 Objetivos do Desafio

O projeto foi estruturado para atender aos seguintes objetivos:

1.  **Preparação de Dados:** Realizar um tratamento robusto dos dados, incluindo limpeza, tratamento de valores ausentes, encoding de variáveis categóricas e normalização.
2.  **Análise Exploratória e Correlação:** Investigar as relações entre as variáveis para identificar os principais fatores correlacionados com o churn.
3.  **Modelagem Preditiva:** Treinar e comparar pelo menos dois modelos de classificação (Regressão Logística e Random Forest) para prever a probabilidade de um cliente evadir.
4.  **Avaliação de Performance:** Utilizar métricas adequadas (Acurácia, Precisão, Recall, F1-Score) para avaliar e comparar o desempenho dos modelos.
5.  **Interpretação e Estratégia:** Extrair a importância das variáveis (feature importance) do melhor modelo e traduzir os achados técnicos em uma conclusão estratégica com propostas de ações de retenção.

---

## Dataset

O dataset utilizado neste projeto contém informações demográficas dos clientes, os serviços contratados, informações de contrato e cobrança, e a variável alvo indicando se o cliente evadiu ou não.

*   **Fonte dos Dados:** [TelecomX_Data.json](https://raw.githubusercontent.com/ingridcristh/challenge2-data-science/refs/heads/main/TelecomX_Data.json)
*   **Tamanho:** Contém informações de mais de 7.000 clientes.

---

## 🛠️ Metodologia

O pipeline de Machine Learning foi construído seguindo as etapas abaixo:

1.  **Limpeza e Pré-processamento:**
    *   Remoção de colunas irrelevantes (`customerID`).
    *   Conversão da coluna `TotalCharges` para o tipo numérico e tratamento de valores nulos (substituídos por 0, representando clientes novos).
    *   Codificação da variável alvo `Churn` para formato binário (0/1).
    *   Aplicação da técnica **One-Hot Encoding** para as variáveis categóricas.
    *   Normalização das variáveis numéricas contínuas com **StandardScaler** para padronizar as escalas.

2.  **Modelagem e Treinamento:**
    *   **Divisão dos Dados:** Separação em conjuntos de treino (80%) e teste (20%).
    *   **Modelo Baseline:** Treinamento de um modelo de **Regressão Logística**.
    *   **Modelo Avançado:** Treinamento de um modelo de **Random Forest Classifier**, conhecido por sua robustez e capacidade de capturar relações complexas.

3.  **Avaliação e Interpretação:**
    *   O desempenho foi medido utilizando o `classification_report`, com foco especial no **F1-Score** e no **Recall** para a classe "Churn".
    *   A importância das variáveis foi extraída do modelo de Random Forest para identificar os principais drivers do churn.

---

## 📈 Principais Resultados e Conclusões

O modelo **Random Forest** apresentou um desempenho superior, demonstrando ser a ferramenta mais eficaz para prever o churn com um bom equilíbrio entre precisão e recall.

Os principais fatores que influenciam a evasão de clientes, em ordem de importância, são:

1.  **Tipo de Contrato (Mensal):** Clientes sem vínculo de longo prazo são extremamente propensos a cancelar.
2.  **Antiguidade (Tenure):** Clientes com pouco tempo de casa têm um risco de churn muito maior.
3.  **Serviço de Internet (Fibra Ótica):** Sugere um possível desalinhamento entre o custo/expectativa do serviço e a experiência real do cliente.
4.  **Cobrança Mensal (MonthlyCharges):** Valores mais altos estão associados a maior churn.

Com base nesses insights, foram propostas estratégias de retenção direcionadas, como campanhas para migração de contratos, programas de onboarding para novos clientes e uma investigação aprofundada sobre a satisfação dos usuários de fibra ótica.

---

## 🚀 Como Executar o Projeto

Para replicar esta análise, siga os passos abaixo:

1.  **Clone o repositório:**
    ```bash
    git clone https://github.com/lrfurst/Challenge_Telecom_X2.git
    ```

2.  **Navegue até o diretório do projeto:**
    ```bash
    cd Challenge_Telecom_X
    ```

3.  **Instale as dependências:**
    O projeto utiliza bibliotecas padrão de Data Science em Python. Recomenda-se criar um ambiente virtual.
    ```bash
    pip install pandas numpy scikit-learn seaborn matplotlib
    ```

4.  **Abra e execute o notebook:**
    O arquivo principal é um notebook Jupyter (`.ipynb`). Abra-o no Jupyter Notebook, JupyterLab ou Google Colab e execute as células em ordem.

---

## ��‍💻 Autor

*   **Luis Ricardo Furst**
*   **LinkedIn:** (https://www.https://www.linkedin.com/in/luisfurst/)
*   **GitHub:** (https://github.com/lrfurst)

---

## ⭐ Mostre seu apoio

Dê uma ⭐️ se este projeto te ajudou ou se você o achou interessante!
