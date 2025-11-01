# 🚀 Projeto de Análise de Dados: Turmas da UFRN (2023-2024)

Este projeto é uma análise detalhada dos dados de turmas da **Universidade Federal do Rio Grande do Norte (UFRN)**, focado nos anos de 2023 e 2024. O trabalho foi desenvolvido no contexto do **Programa de Educação Tutorial (PET)** do curso de Ciência da Computação da UFRN, sob a docência de Célio Felipe Bezerra Santiago.

## 🎯 Objetivo

O objetivo principal foi analisar a distribuição das turmas da UFRN, explorando variáveis como capacidade, número de solicitações, local (campus) e modalidade (presencial ou a distância). Além da análise exploratória, foram aplicadas técnicas de Machine Learning (clustering) para identificar padrões e perfis de turmas, com o intuito de gerar insights para o planejamento acadêmico.

## 📊 Fonte dos Dados

Os dados brutos foram obtidos através do [Portal de Dados Abertos da UFRN](https://dados.ufrn.br/dataset). A base final consolidada contém cerca de 50.000 registros, abrangendo os períodos de 2023.1, 2023.2, 2024.1 e 2024.2.

## 🛠️ Metodologia

O projeto seguiu um pipeline clássico de Ciência de Dados, dividido nas seguintes etapas:

1.  **Limpeza de Dados:**
    * Remoção de colunas completamente nulas (ex: `observação`, `matricula_docente_externo`).
    * Remoção de registros duplicados.
    * Tratamento de valores ausentes (preenchimento com mediana, moda ou valores específicos).

2.  **Análise Exploratória de Dados (AED):**
    * Visualização da distribuição de turmas por nível de ensino (Graduação, Stricto Sensu, etc.) e por campus.
    * Identificação de outliers.
    * Comparação entre capacidade, solicitações e carga horária.
    * Análise da oferta de turmas ao longo dos semestres.

3.  **Clustering (Machine Learning):**
    * Aplicação do **Método do Cotovelo (Elbow Method)** para determinar o número ótimo de clusters (definido como k=4).
    * Uso do algoritmo **K-Means** para agrupar as turmas em quatro perfis distintos.

4.  **Testes Estatísticos:**
    * Uso dos testes **ANOVA**, **Mann-Whitney U** e **Kruskal-Wallis** para validar hipóteses e avaliar se as diferenças observadas (ex: capacidade por nível de ensino) eram estatisticamente significativas.

## 💡 Principais Insights

A análise dos dados revelou diversos padrões importantes:

* **Concentração Acadêmica:** A vasta maioria das turmas é de **Graduação** (mais de 47 mil) e está concentrada no **Campus Central** (mais de 50 mil).
* **Modalidade EAD:** Turmas a distância, embora menos numerosas, tendem a ter **maior capacidade** e, em média, recebem **mais solicitações**.
* **Perfis de Turmas:** O clustering com K-Means (k=4) permitiu segmentar as turmas em perfis claros, como:
    1.  Turmas pequenas com baixa carga horária.
    2.  Turmas com alta capacidade e alta demanda.
    3.  Turmas com carga horária elevada.
* **Validação Estatística:** Testes confirmaram que a **capacidade média** e a **carga horária** variam de forma estatisticamente significativa entre os diferentes níveis de ensino (Graduação, Lato Sensu, Stricto Sensu).

## 🚀 Recomendações

Com base nos resultados, as seguintes ações são sugeridas para a UFRN:

1.  **Otimizar a Alocação:** Focar em grupos de turmas com alta demanda ou baixa capacidade para investigar gargalos (falta de professores, infraestrutura) e realocar recursos.
2.  **Expandir EAD:** Dado que turmas a distância apresentam alta capacidade e demanda, a universidade pode estudar a expansão desta modalidade.
3.  **Analisar Exclusões:** Investigar os motivos por trás do cancelamento ou exclusão de turmas do sistema para melhorar o planejamento futuro.

## 💻 Tecnologias Utilizadas

* **Python**
* **Google Colab**
* **Pandas** (para manipulação e limpeza de dados)
* **Numpy** (para operações numéricas)
* **Matplotlib** e **Seaborn** (para visualização de dados)
* **Scikit-learn (Sklearn)** (para clustering com K-Means)
* **Scipy.stats** (para os testes estatísticos)
