# Análise Preditiva para Manutenção Industrial (Indústria 4.0)

Sistema de **Machine Learning para predição de falhas mecânicas** em equipamentos industriais, desenvolvido como projeto avaliativo do **Módulo 1 do curso Desenvolvedor(a) em IA para Análise Preditiva (SCTEC)**.

O projeto implementa um pipeline completo de Ciência de Dados, contemplando desde a obtenção e preparação dos dados até o treinamento e avaliação de modelos preditivos, simulando um cenário real de **Manutenção Preditiva na Indústria 4.0**.

---

## Objetivo

Desenvolver um modelo capaz de identificar, antecipadamente, possíveis falhas em máquinas industriais a partir de dados coletados por sensores.

A utilização desse tipo de solução permite:

- Reduzir paradas não programadas;
- Diminuir custos com manutenção corretiva;
- Aumentar a disponibilidade dos equipamentos;
- Prolongar a vida útil dos ativos industriais;
- Apoiar a tomada de decisão baseada em dados.

O pipeline foi desenvolvido para execução em **modo batch**, utilizando dados históricos, podendo futuramente ser adaptado para processamento em tempo real.

---

## Desafio problema do projeto:

Na indústria moderna, uma falha inesperada pode gerar elevados custos de produção.

O objetivo deste projeto é prever se determinado equipamento apresentará falha mecânica com base nas informações provenientes de sensores industriais.

### Variável Alvo

- **Falha = 1** → Equipamento apresentou falha.
- **Falha = 0** → Equipamento operando normalmente.

---

## Base de Dados

O conjunto contém aproximadamente **10.000 registros** de sensores industriais, incluindo:

- Temperatura do ar
- Temperatura do processo
- Velocidade de rotação
- Torque
- Desgaste da ferramenta

---

## Tecnologias Utilizadas

- Python 3.10+
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Imbalanced-Learn (SMOTE)
- Google Sheets API (gspread)

---

## Pipeline Desenvolvido

O projeto contempla todas as etapas de um pipeline de Machine Learning:

1. Coleta dos dados
2. Limpeza e tratamento dos dados
3. Análise Exploratória (EDA)
4. Engenharia de Atributos
5. Balanceamento das Classes
6. Treinamento dos Modelos
7. Avaliação dos Resultados

---

## Estrutura do Projeto

```text
Mini-projeto-SCTEC/
│
├── README.md
├── requirements.txt
├── Projeto_avaliativo_Módulo_1.ipynb
├── manutencao_preditiva.csv
├── anotacoes do Departamento de Engenharia.pdf
├── grafico_eda_fase1.png
├── grafico_boxplots_fase2.png
├── pipeline_preditivo_fluxograma.png
└── roteiro_projeto_preditivo.png
```

---

## Como Executar

Clone o repositório:

```bash
git clone https://github.com/thaysfaleiro-a11y/Mini-projeto-SCTEC.git

cd Mini-projeto-SCTEC
```

Instale as dependências:

```bash
pip install -r requirements.txt
```

Abra o notebook:

```bash
Projeto_avaliativo_Módulo_1.ipynb
```

---

## Resultados

| Modelo | Acurácia |
|---------|---------:|
| KNN (k = 5) | **89,65%** |
| Árvore de Decisão (max_depth = 5) | **90,20%** |

### Observação Importante

O conjunto de dados apresenta forte desbalanceamento (**aproximadamente 96,6% dos registros pertencem à classe "sem falha"**).

Por esse motivo, **a acurácia isoladamente não representa o verdadeiro desempenho do modelo**, pois um classificador que sempre previsse "sem falha" já alcançaria uma acurácia elevada.

Em aplicações reais de manutenção preditiva, recomenda-se utilizar também métricas como:

- Recall
- Precision
- F1-Score
- Matriz de Confusão
- Curva ROC-AUC

Essas métricas permitem avaliar melhor a capacidade do modelo em identificar corretamente as falhas e reduzir falsos negativos.

---

## Sugestões futuras:

- Implementar Random Forest
- Aplicar Cross Validation
- Desenvolver pipeline para inferência em tempo real
- Integrar o modelo a sistemas SCADA/IIoT

---

## Assista ao vídeo do projeto:

https://drive.google.com/file/d/1GRGWp3bc6IDFTmRHYYHE1oFZUIbKYTRf/view?usp=sharing

---

## Aluna

**Thays Faleiro**

GitHub:
[![GitHub](https://img.shields.io/badge/GitHub-thaysfaleiro--a11y-181717?logo=github)](https://github.com/thaysfaleiro-a11y)


