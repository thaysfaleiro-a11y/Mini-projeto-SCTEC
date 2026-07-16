# 🛠️ Predicta-Industry: Pipeline Preditivo para a Indústria 4.0

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Data Science](https://img.shields.io/badge/Data%20Science-Scientific%20Computing-blue?style=for-the-badge)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Classifiers-green?style=for-the-badge)

## 📌 Sobre o Projeto
Este repositório contém o desenvolvimento de um **Pipeline Preditivo de Machine Learning ponta a ponta** aplicado ao monitoramento de sensores em um parque fabril. O objetivo do sistema é antecipar falhas mecânicas em equipamentos antes que elas gerem interrupções indesejadas na linha de produção, otimizando os custos de manutenção preventiva e corretiva.

---

## ⚙️ Técnicas e Tecnologias Utilizadas
* **Linguagem:** Python
* **Manipulação e Análise de Dados:** `Pandas` e `NumPy`
* **Visualização de Dados:** `Matplotlib` e `Seaborn`
* **Machine Learning:** `Scikit-Learn` (modelos KNN e Árvore de Decisão)
* **Tratamento de Desbalanceamento:** `Imbalanced-Learn` (técnica SMOTE)
* **Conectividade:** Integração direta com dados em nuvem via API do Google Sheets (`gspread`, `google.auth`)

---

## 🚀 Como Executar o Projeto

1. **Acesso Direto (Google Colab):**
   * Basta clicar no botão **"Open in Colab"** presente no topo do arquivo [`Projeto_avaliativo_Módulo_1.ipynb`](./Projeto_avaliativo_Módulo_1.ipynb).

2. **Execução Local:**
   * Clone este repositório em sua máquina:
     ```bash
     git clone [https://github.com/thaysfaleiro-a11y/Mini-Projeto-SCTEC.git](https://github.com/thaysfaleiro-a11y/Mini-Projeto-SCTEC.git)
     ```
   * Instale as dependências necessárias utilizando o arquivo `requirements.txt`:
     ```bash
     pip install -r requirements.txt
     ```
   * Execute o arquivo de Notebook Jupyter em seu ambiente preferido.

---

## 📈 Melhorias Futuras Propostas
* **Métricas de Negócio:** Substituição da Acurácia por análise detalhada de **Recall e F1-Score** para mapeamento real do impacto financeiro de falsos negativos.
* **Algoritmos Avançados:** Implementação de algoritmos de *Ensemble* (como Random Forest ou XGBoost) para ganho de robustez frente a ruídos de sensores.
* **Dados Temporais:** Construção de janelas e médias móveis para avaliar o desgaste gradual do maquinário ao longo do tempo.
