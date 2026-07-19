# 🚀 Pipeline Preditivo para Manutenção Industrial (Indústria 4.0)

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![Status](https://img.shields.io/badge/status-em%20desenvolvimento-yellow)
![License](https://img.shields.io/badge/license-MIT-green)

Sistema de **Machine Learning para predição de falhas mecânicas** em equipamentos industriais, desenvolvido como projeto avaliativo do **Módulo 1 do curso Desenvolvedor(a) em IA para Análise Preditiva (SCTEC)**.

O projeto implementa um pipeline completo de Ciência de Dados — da obtenção e preparação dos dados ao treinamento e avaliação de modelos preditivos — simulando um cenário real de **Manutenção Preditiva na Indústria 4.0**.

---

## 📌 Objetivo

Desenvolver um modelo capaz de identificar, antecipadamente, possíveis falhas em máquinas industriais a partir de dados coletados por sensores.

Esse tipo de solução permite:

- Reduzir paradas não programadas
- Diminuir custos com manutenção corretiva
- Aumentar a disponibilidade dos equipamentos
- Prolongar a vida útil dos ativos industriais
- Apoiar a tomada de decisão baseada em dados

O pipeline foi desenvolvido para execução em **modo batch**, utilizando dados históricos, com possibilidade de adaptação futura para processamento em tempo real.

---

## 🎯 Problema de Negócio

Na indústria moderna, uma falha inesperada pode gerar elevados custos de produção e parada de linha.

O objetivo é prever se um equipamento apresentará falha mecânica com base em informações de sensores industriais.

### Variável Alvo

| Valor | Significado |
|:-----:|:------------|
| `1` | Equipamento apresentou falha |
| `0` | Equipamento operando normalmente |

---

## 📊 Base de Dados

O projeto utiliza o **[AI4I 2020 Predictive Maintenance Dataset](https://archive.ics.uci.edu/dataset/601/ai4i+2020+predictive+maintenance+dataset)**, disponibilizado pela UCI Machine Learning Repository.

O conjunto contém aproximadamente **10.000 registros** de sensores industriais, incluindo:

| Sensor | Descrição |
|--------|-----------|
| 🌡️ Temperatura do ar | Temperatura ambiente medida em [K] |
| 🔥 Temperatura do processo | Temperatura do processo produtivo [K] |
| ⚙️ Velocidade de rotação | Rotação do equipamento [rpm] |
| 🔩 Torque | Torque aplicado [Nm] |
| 🛠️ Desgaste da ferramenta | Tempo de uso da ferramenta [min] |

---

## 🛠 Tecnologias Utilizadas

- **Python 3.10+**
- **Pandas** / **NumPy** — manipulação e tratamento de dados
- **Matplotlib** / **Seaborn** — visualização e EDA
- **Scikit-Learn** — modelagem e avaliação
- **Imbalanced-Learn (SMOTE)** — balanceamento de classes
- **Google Sheets API (gspread)** — integração de dados

---

## ⚙️ Pipeline Desenvolvido

1. **Coleta dos dados**
2. **Limpeza e tratamento dos dados**
3. **Análise Exploratória (EDA)**
4. **Engenharia de Atributos**
5. **Balanceamento das Classes (SMOTE)**
6. **Treinamento dos Modelos**
7. **Avaliação dos Resultados**

---

## 📂 Estrutura do Projeto

```text
Mini-projeto-SCTEC/
│
├── README.md
├── requirements.txt
├── Projeto_avaliativo_Modulo_1.ipynb
├── manutencao_preditiva.csv
├── anotacoes_departamento_engenharia.pdf
├── grafico_eda_fase1.png
├── grafico_boxplots_fase2.png
├── pipeline_preditivo_fluxograma.png
└── roteiro_projeto_preditivo.png
```

---

## ▶️ Como Executar

**1. Clone o repositório**

```bash
git clone https://github.com/thaysfaleiro-a11y/Mini-projeto-SCTEC.git
cd Mini-projeto-SCTEC
```

**2. Crie um ambiente virtual (opcional, mas recomendado)**

```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
```

**3. Instale as dependências**

```bash
pip install -r requirements.txt
```

**4. Abra o notebook**

```bash
jupyter notebook Projeto_avaliativo_Modulo_1.ipynb
```

---

## 📈 Resultados

| Modelo | Acurácia |
|--------|---------:|
| KNN (k = 5) | **89,65%** |
| Árvore de Decisão (max_depth = 5) | **90,20%** |

### 📌 Como interpretar esses números

O conjunto de dados apresenta forte desbalanceamento: **cerca de 96,6% dos registros pertencem à classe "sem falha"**.

Isso significa que **a acurácia isoladamente não representa o real desempenho do modelo** — um classificador ingênuo, que sempre previsse "sem falha", já atingiria acurácia elevada sem detectar nenhuma falha de fato.

Por isso, os próximos passos deste projeto incluem a análise de métricas mais adequadas a cenários desbalanceados:

- **Recall** — capacidade de identificar as falhas reais
- **Precision** — confiabilidade das previsões positivas
- **F1-Score** — equilíbrio entre recall e precision
- **Matriz de Confusão** — visão detalhada dos acertos e erros
- **Curva ROC-AUC** — desempenho geral do classificador

> 💡 Em manutenção preditiva, um falso negativo (não detectar uma falha real) costuma ser muito mais custoso que um falso positivo — por isso o recall tende a ser a métrica prioritária nesse tipo de aplicação.

---

## 🔮 Próximos Passos

- [ ] Implementar Random Forest
- [ ] Implementar XGBoost
- [ ] Avaliar LightGBM
- [ ] Aplicar Cross Validation
- [ ] Otimização de hiperparâmetros (Grid Search)
- [ ] Criar atributos temporais (Rolling Window)
- [ ] Desenvolver pipeline para inferência em tempo real
- [ ] Integrar o modelo a sistemas SCADA/IIoT

---

## 🎥 Demonstração

👉 [Assista ao vídeo do projeto](https://drive.google.com/file/d/1GRGWp3bc6IDFTmRHYYHE1oFZUIbKYTRf/view?usp=sharing)

---

## 👩‍💻 Autora
**Thays Faleiro** 
🤖 Estudante de Inteligência Artificial aplicada à Análise Preditiva

[![GitHub](https://img.shields.io/badge/GitHub-thaysfaleiro--a11y-181717?logo=github)](https://github.com/thaysfaleiro-a11y)


Considere deixar uma **⭐ Star** no repositório. Isso ajuda a divulgar o projeto e incentiva o desenvolvimento de novas soluções em Ciência de Dados e Inteligência Artificial.
