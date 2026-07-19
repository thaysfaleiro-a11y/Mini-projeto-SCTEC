# Pipeline Preditivo para a Indústria 4.0

Este projeto consiste em um pipeline preditivo completo para a previsão de falhas mecânicas em equipamentos industriais. Desenvolvido como o Projeto Avaliativo do Módulo 1 do curso de Desenvolvedor(a) em IA para Análise Preditiva (SCTEC), o sistema utiliza técnicas de preparação de dados, engenharia de atributos e modelagem estatística aplicada ao contexto de manufatura inteligente.

## Objetivo do Projeto

O objetivo principal consiste em analisar dados históricos de sensores de um parque fabril para prever quebras físicas em componentes mecânicos. Com isso, é possível reduzir paradas não planejadas na linha de produção, diminuir a depreciação precoce das máquinas e economizar custos operacionais. O pipeline aqui desenvolvido opera em modo batch (análise offline de dados históricos) e serve de base para uma futura solução de monitoramento em tempo real (ver seção "Próximos Passos").

### A Variável Alvo:
* **Falha = 1:** Avaria detectada no maquinário.
* **Falha = 0:** Funcionamento operacional normal.

## Origem dos Dados

Dataset baseado no *AI4I 2020 Predictive Maintenance Dataset* (UCI Machine Learning Repository), contendo 10.000 registros de sensores industriais (temperatura, velocidade de rotação, torque, desgaste de ferramenta) e a variável alvo de falha de máquina.

## Tecnologias e Bibliotecas Utilizadas

* **Python 3.10+**
* **Pandas & NumPy** — limpeza, imputação estatística e manipulação dos dados brutos.
* **Matplotlib & Seaborn** — geração de gráficos para análise exploratória de dados (EDA) e mapeamento de outliers.
* **Scikit-Learn** — modelagem com classificadores (KNN e Árvore de Decisão), divisão estratificada e padronização escalar.
* **Imbalanced-Learn (SMOTE)** — balanceamento sintético de classes no conjunto de treinamento para evitar viés de dados minoritários.
* **Google API integration (gspread)** — conexão e carregamento dinâmico de dados hospedados em nuvem.

## Estrutura do Repositório

```text
Mini-projeto-SCTEC/
├── README.md                          # Documentação principal do projeto
├── requirements.txt                   # Dependências e pacotes necessários
├── Projeto_avaliativo_Módulo_1.ipynb  # Notebook oficial contendo as 7 fases do pipeline
├── manutencao_preditiva.csv           # Base de dados utilizada no projeto
├── anotacoes do Departamento de E...  # Documento auxiliar com regras de negócio e anotações
├── grafico_boxplots_fase2.png         # Gráfico gerado na Análise Exploratória (Fase 2)
├── grafico_eda_fase1.png              # Gráfico gerado na Análise Exploratória (Fase 1)
├── pipeline_preditivo_fluxograma.png   # Fluxograma visual do modelo preditivo
└── roteiro_projeto_preditivo.png       # Imagem com o roteiro e planejamento do projeto








