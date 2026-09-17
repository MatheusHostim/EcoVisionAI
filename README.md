# EcoVisionAI

Sistema de classificação de risco ambiental utilizando dados simulados inspirados em informações de monitoramento por satélites.

## 👥 Equipe

| Nome                  | RM       |
| --------------------- | -------- |
| Eduardo da Silva Lima | RM554804 |
| Estevam Melo          | RM555124 |
| Enzo Bonacasatta      | RM555372 |
| Guilherme Ulacco      | RM558418 |
| Matheus Hostim        | RM556517 |

---

## 🌱 Definição do Problema

Mudanças climáticas e impactos ambientais representam desafios para governos e organizações responsáveis pelo monitoramento e preservação do meio ambiente.

Eventos como queimadas, degradação da vegetação e condições climáticas extremas podem causar impactos significativos tanto no meio ambiente quanto na população.

O **EcoVisionAI** propõe a utilização de dados ambientais para classificar regiões de acordo com seu nível de risco, utilizando Machine Learning como ferramenta de apoio à análise.

O objetivo do modelo é classificar uma determinada região em três categorias:

* Baixo risco ambiental
* Médio risco ambiental
* Alto risco ambiental

> **Observação:** os dados utilizados no projeto são sintéticos e foram criados para fins acadêmicos.

---

## 🛠️ Tecnologias Utilizadas

| Tecnologia                                | Utilização                                            |
| ----------------------------------------- | ----------------------------------------------------- |
| [Python](https://www.python.org/)         | Linguagem principal do projeto                        |
| [Pandas](https://pandas.pydata.org/)      | Manipulação e análise dos dados                       |
| [Scikit-learn](https://scikit-learn.org/) | Treinamento e avaliação do modelo de Machine Learning |
| Random Forest                             | Algoritmo utilizado para classificação                |
| Jupyter Notebook                          | Desenvolvimento e análise do modelo                   |

---

## 📊 Dataset Utilizado

Foi desenvolvido um dataset sintético contendo **500 registros**, simulando dados ambientais que poderiam ser obtidos por sensores embarcados em satélites.

As variáveis utilizadas foram:

| Variável          | Descrição                               |
| ----------------- | --------------------------------------- |
| `temperatura`     | Temperatura média da região (°C)        |
| `umidade`         | Umidade relativa do ar (%)              |
| `chuva_mm`        | Volume de chuva (mm)                    |
| `vegetacao`       | Índice de vegetação da região           |
| `focos_calor`     | Quantidade de focos de calor detectados |
| `risco_ambiental` | Classificação do risco ambiental        |

### Distribuição das classes

| Classe | Registros |
| ------ | --------: |
| Baixo  |       300 |
| Médio  |       140 |
| Alto   |        60 |

O dataset foi criado artificialmente para representar diferentes cenários ambientais e permitir o treinamento e avaliação do modelo.

---

## 🧹 Tratamento e Preparação dos Dados

Inicialmente, foi realizada uma análise da estrutura do dataset para verificar a integridade dos dados.

Foram identificados os seguintes pontos:

* 500 registros;
* ausência de valores nulos;
* variáveis numéricas estruturadas adequadamente;
* `risco_ambiental` definida como variável alvo.

### Variáveis de entrada

As features utilizadas pelo modelo foram:

* `temperatura`
* `umidade`
* `chuva_mm`
* `vegetacao`
* `focos_calor`

### Variável alvo

* `risco_ambiental`

Os dados também foram divididos em conjuntos de treinamento e teste:

| Conjunto    | Registros |
| ----------- | --------: |
| Treinamento |       400 |
| Teste       |       100 |

---

## 🤖 Treinamento do Modelo

O algoritmo utilizado foi o **Random Forest Classifier**.

A escolha desse algoritmo ocorreu por sua aplicação em problemas de classificação e pela capacidade de combinar múltiplas árvores de decisão para realizar as previsões.

O modelo foi treinado utilizando os **400 registros do conjunto de treinamento** e posteriormente avaliado utilizando os **100 registros do conjunto de teste**.

---

## 📈 Avaliação do Modelo

O modelo foi avaliado utilizando métricas de classificação.

### Acurácia

**94%**

### Relatório de Classificação

| Classe | Precision | Recall | F1-Score |
| ------ | --------: | -----: | -------: |
| Alto   |      1.00 |   0.73 |     0.85 |
| Baixo  |      0.96 |   1.00 |     0.98 |
| Médio  |      0.88 |   0.93 |     0.90 |

Os resultados indicam que, no conjunto de teste utilizado, o modelo classificou corretamente a maior parte das amostras.

Por se tratar de um dataset sintético e de um projeto acadêmico, os resultados representam o desempenho do modelo dentro das condições definidas para o experimento e não devem ser interpretados como uma validação de desempenho sobre dados ambientais reais.

---

## 🔲 Matriz de Confusão

<img width="501" height="393" alt="Matriz de confusão do modelo" src="https://github.com/user-attachments/assets/d9ac9351-7480-410f-aaaa-78c3d889c74e" />

A matriz de confusão permite visualizar a quantidade de classificações corretas e incorretas realizadas pelo modelo para cada categoria de risco.

No conjunto de teste, a classe **Baixo** apresentou maior número de classificações corretas, enquanto também foram observados erros de classificação entre as categorias **Médio** e **Alto**.

---

## 🌿 Importância das Variáveis

<img width="700" height="509" alt="Importância das variáveis do modelo" src="https://github.com/user-attachments/assets/a5647ed9-52af-4ee9-815b-780a86be1bf8" />

O gráfico de importância das variáveis apresenta a contribuição relativa de cada feature para as decisões realizadas pelo modelo.

Entre as variáveis analisadas, o **índice de vegetação** apresentou a maior importância no modelo utilizado. Temperatura, umidade e quantidade de focos de calor também contribuíram para as classificações realizadas.

---

## ✅ Conclusão

O **EcoVisionAI** permitiu aplicar conceitos de Machine Learning a um problema de classificação de risco ambiental utilizando Python e dados sintéticos inspirados em informações que poderiam ser obtidas por sistemas de monitoramento por satélite.

Durante o desenvolvimento, foram realizadas etapas de preparação dos dados, treinamento do modelo e avaliação utilizando métricas de classificação.

No conjunto de teste utilizado no projeto, o modelo alcançou **94% de acurácia**, além dos resultados apresentados nas métricas de Precision, Recall e F1-Score.

O projeto demonstra, em contexto acadêmico, como técnicas de Machine Learning podem ser utilizadas para analisar dados ambientais e apoiar processos de classificação e tomada de decisão.

---

## 🎓 Contexto Acadêmico

Projeto desenvolvido em equipe durante a graduação em **Engenharia de Software na FIAP**.
