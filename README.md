# Análise de modelos de explicabilidade

Este notebook apresenta uma análise prática de diferentes métodos de explicabilidade de modelos de machine learning, com foco em técnicas locais e globais aplicadas a um modelo do tipo Random Forest Classifier. O objetivo é compreender como cada variável contribui para as previsões e demonstrar como gerar explicações interpretáveis para modelos de caixa-preta.

O notebook exemplifica o uso das bibliotecas `LIME`, `DiCE` e `InterpretML` para produzir explicações visuais e numéricas sobre decisões individuais e padrões globais do modelo. Para isso, foi usado um dataset de caráter biomédico que coleta informações acerca de diagnósticos para doenças cardiovasculares.

## Técnicas Utilizadas

### 1. LIME (Local Interpretable Model-agnostic Explanations)

Método de explicabilidade local que cria um modelo simples (geralmente linear) ao redor de uma predição específica, permitindo entender quais atributos mais influenciaram o resultado daquela instância.

### 2. SHAP (SHapley Additive exPlanations)

Método baseado na Teoria dos Valores de Shapley, originada da Teoria dos Jogos.
O SHAP calcula a contribuição média de cada atributo para a previsão final, considerando todas as possíveis combinações de características.
Ele fornece explicações consistentes e justas, tanto no nível local (instância específica) quanto global (modelo como um todo).
É amplamente usado por sua base matemática sólida e pela capacidade de interpretar modelos complexos, como Random Forests e redes neurais.

### 3. DiCE (Diverse Counterfactual Explanations)

Ferramenta voltada para gerar explicações contrafactuais — pequenas alterações nos atributos de entrada que fariam o modelo mudar sua predição.
Ideal para investigar fronteiras de decisão e a sensibilidade do modelo em relação às variáveis de entrada.

## Colaboradores

Esse notebook foi desenvolvido para a disciplina de Sistemas Baseados em Conhecimento, na Universidade Federal da Paraíba, pelos seguintes discentes de Ciência da Computação:

* [Davi de Lacerda Teixeira](https://github.com/DavideLacerdaT)
* [João Victor Fernandes da Silveira](https://github.com/oiotave)

## Instruções de execução

1. Clone o repositório em sua máquina com o seguinte comando.

```bash
git clone "https://github.com/oiotave/explainability-models"
```

2. Certifique-se de instalar todas as dependências necessárias para esse notebook.

```bash
pip install interpret lime shap dice_ml imblearn pandas seaborn scikit-learn kagglehub
```

3. Abra o notebook no Google Colab ou em um ambiente Jupyter.

4. Execute todas as células sequencialmente.

## Dataset

O dataset usado nesse notebook pode ser encontrado no link: https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction
