# EcoVisionAI

Sistema Inteligente de Monitoramento Ambiental com Dados Satelitais

### Integrantes

Eduardo da Silva Lima (RM: 554804)

Estevam Melo (RM: 555124)

Enzo Bonacasatta (RM: 555372)

Guilherme Ulacco (RM: 558418)

Matheus Hostim (RM: 556517)

---

# Definição do Problema

As mudanças climáticas e os impactos ambientais representam desafios cada vez maiores para governos e organizações em todo o mundo. Eventos como queimadas, degradação da vegetação e condições climáticas extremas podem causar danos significativos ao meio ambiente e à população.

O projeto EcoVisionAI propõe a utilização de dados que podem ser obtidos por sensores embarcados em satélites para monitorar condições ambientais e classificar regiões de acordo com seu risco ambiental.

A solução busca auxiliar autoridades e órgãos responsáveis na tomada de decisões preventivas, reduzindo impactos ambientais e contribuindo para a preservação dos recursos naturais.

O objetivo do modelo de Machine Learning é classificar uma determinada região em três categorias:

* Baixo risco ambiental
* Médio risco ambiental
* Alto risco ambiental

---

# Dataset Utilizado

Foi desenvolvido um dataset sintético contendo 500 registros, simulando dados ambientais que poderiam ser coletados por satélites.

As variáveis utilizadas foram:

| Variável        | Descrição                               |
| --------------- | --------------------------------------- |
| temperatura     | Temperatura média da região (°C)        |
| umidade         | Umidade relativa do ar (%)              |
| chuva_mm        | Volume de chuva (mm)                    |
| vegetacao       | Índice de vegetação da região           |
| focos_calor     | Quantidade de focos de calor detectados |
| risco_ambiental | Classificação do risco ambiental        |

Distribuição das classes:

* Baixo: 300 registros
* Médio: 140 registros
* Alto: 60 registros

O dataset foi criado artificialmente para estar representando diferentes cenários ambientais e permitir o treinamento do modelo.

---

# Tratamento e Preparação dos Dados

Inicialmente foi realizada a verificação da estrutura do dataset para garantir a integridade dos dados.

Foi constatado que:

* O dataset possui 500 registros.
* Não existem valores nulos.
* Todas as variáveis numéricas estão adequadamente estruturadas.
* A variável alvo corresponde à classificação do risco ambiental.

Posteriormente os dados foram divididos em:

* Variáveis de entrada (features):

  * temperatura
  * umidade
  * chuva_mm
  * vegetacao
  * focos_calor

* Variável alvo (target):

  * risco_ambiental

Também foi realizada a divisão entre dados de treinamento e teste:

* Treinamento: 400 registros
* Teste: 100 registros

---

# O Treinamento

O algoritmo que usamos foi o Random Forest Classifier.

Escolhemos ele pela sua capacidade de poder lidar com problemas de classificação, apresentar boa precisão e reduzir problemas de sobreajuste.

O modelo foi treinado utilizando os 400 registros do conjunto de treinamento e avaliado com os 100 registros do conjunto de teste.

---

# Avaliação do Modelo

O desempenho do modelo foi analisado utilizando métricas de classificação.

Resultados obtidos:

* Accuracy (Acurácia): 94%

Relatório de classificação:

| Classe | Precision | Recall | F1-Score |
| ------ | --------: | -----: | -------: |
| Alto   |      1.00 |   0.73 |     0.85 |
| Baixo  |      0.96 |   1.00 |     0.98 |
| Médio  |      0.88 |   0.93 |     0.90 |

Os resultados demonstram que o modelo foi capaz de classificar corretamente a grande maioria das amostras, apresentando desempenho satisfatório para o problema proposto.

---

## Matriz de Confusão

<img width="501" height="393" alt="image" src="https://github.com/user-attachments/assets/d9ac9351-7480-410f-aaaa-78c3d889c74e" />

A matriz de confusão permite visualizar os acertos e erros do modelo durante a classificação dos níveis de risco ambiental. Analisando os resultados, é possível perceber que o modelo teve um bom desempenho geral, principalmente na identificação das regiões classificadas como Baixo Risco. As categorias Médio e Alto Risco também apresentaram resultados satisfatórios, demonstrando que o modelo conseguiu aprender os padrões presentes nos dados utilizados para o treinamento.



## Importância das Variáveis

<img width="700" height="509" alt="image" src="https://github.com/user-attachments/assets/a5647ed9-52af-4ee9-815b-780a86be1bf8" />

O gráfico de importância das variáveis mostra quais fatores tiveram maior peso na tomada de decisão do modelo. Entre todas as variáveis analisadas, o índice de vegetação foi o que mais influenciou a classificação do risco ambiental. Além dele, fatores como temperatura, umidade e quantidade de focos de calor também tiveram participação significativa nos resultados.



---

# Conclusão

Com o desenvolvimento de nossa solução, a EcoVisionAI, foi possível aplicar nele técnicas de Machine Learning pra classificar regiões de acordo com seu risco ambiental utilizando dados simulados inspirados em informações que poderiam ser coletadas por satélites.
O modelo treinado mostrou bons resultados, alcançando 94% de acurácia e demonstrando boa capacidade de estar identificando padrões relacionados às condições ambientais analisadas.
Dessa forma, o projeto atingiu o objetivo de mostrar como a IA pode auxiliar no monitoramento ambiental e na prevenção de possíveis problemas, servindo como uma ferramenta de apoio para a tomada de decisões baseada em dados.


---
