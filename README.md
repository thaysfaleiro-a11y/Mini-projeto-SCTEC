**Pipeline Preditivo para a Indústria 4.0**



Este projeto consiste em um pipeline preditivo completo de ponta a ponta para a previsão de falhas mecânicas em equipamentos industriais. Desenvolvido como o **Projeto Avaliativo do Módulo 1** do curso de **Desenvolvedor(a) em IA para Análise Preditiva (SCTEC)**, o sistema utiliza técnicas avançadas de preparação de dados, engenharia de atributos e modelagem estatística aplicada ao contexto de manufatura inteligente.

---

##  Objetivo do Projeto

O objetivo principal consiste em monitorar sensores de um parque fabril em tempo real para prever quebras físicas em componentes mecânicos. Com isso, é possível evitar paradas não planejadas na linha de produção, reduzir a depreciação precoce das máquinas e economizar custos operacionais.

**A Variável Alvo:**
* **Falha = 1:** Avaria detectada no maquinário.
* **Falha = 0:** Funcionamento operacional normal.

---

##Tecnologias e Bibliotecas Utilizadas

* **Python 3.10+**
* **Pandas & NumPy:** Limpeza, imputação estatística e manipulação dos dados brutos.
* **Matplotlib & Seaborn:** Geração de gráficos para análise exploratória de dados (EDA) e mapeamento de outliers.
* **Scikit-Learn:** Modelagem com classificadores (KNN e Árvore de Decisão), divisão estratificada e padronização escalar.
* **Imbalanced-Learn (SMOTE):** Balanceamento sintético de classes no conjunto de treinamento para evitar o viés de dados minoritários.
* **Google API integration (`gspread`):** Conexão e carregamento dinâmico de dados hospedados em nuvem.

---

## Estrutura do Repositório


O repositório está organizado de forma clara e profissional:

```text
Mini-projeto-SCTEC/
│
├── README.md                           # Documentação principal do projeto
├── requirements.txt                    # Dependências e pacotes necessários
└── Projeto_avaliativo_Módulo_1.ipynb   # Notebook oficial contendo as 7 fases do pipeline



git clone [https://github.com/thaysfaleiro-a11y/Mini-projeto-SCTEC.git](https://github.com/thaysfaleiro-a11y/Mini-projeto-SCTEC.git)





