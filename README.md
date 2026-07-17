# Pipeline Preditivo para a Indústria 4.0

Este projeto consiste em um pipeline preditivo completo para a previsão de falhas mecânicas em equipamentos industriais. Desenvolvido como o Projeto Avaliativo do Módulo 1 do curso de Desenvolvedor(a) em IA para Análise Preditiva (SCTEC), o sistema utiliza técnicas de preparação de dados, engenharia de atributos e modelagem estatística aplicada ao contexto de manufatura inteligente.

## Objetivo do Projeto

O objetivo principal consiste em analisar dados históricos de sensores de um parque fabril para prever quebras físicas em componentes mecânicos. Com isso, é possível reduzir paradas não planejadas na linha de produção, diminuir a depreciação precoce das máquinas e economizar custos operacionais. O pipeline aqui desenvolvido opera em modo batch (análise offline de dados históricos) e serve de base para uma futura solução de monitoramento em tempo real (ver seção "Próximos Passos").

**A Variável Alvo:**

- `Falha = 1`: Avaria detectada no maquinário.
- `Falha = 0`: Funcionamento operacional normal.

## Origem dos Dados

Dataset baseado no **AI4I 2020 Predictive Maintenance Dataset** (UCI Machine Learning Repository), contendo 10.000 registros de sensores industriais (temperatura, velocidade de rotação, torque, desgaste de ferramenta) e a variável alvo de falha de máquina.

## Tecnologias e Bibliotecas Utilizadas

- **Python 3.10+**
- **Pandas & NumPy** — limpeza, imputação estatística e manipulação dos dados brutos.
- **Matplotlib & Seaborn** — geração de gráficos para análise exploratória de dados (EDA) e mapeamento de outliers.
- **Scikit-Learn** — modelagem com classificadores (KNN e Árvore de Decisão), divisão estratificada e padronização escalar.
- **Imbalanced-Learn (SMOTE)** — balanceamento sintético de classes no conjunto de treinamento para evitar viés de dados minoritários.
- **Google API integration (`gspread`)** — conexão e carregamento dinâmico de dados hospedados em nuvem.

## Estrutura do Repositório

```
Mini-projeto-SCTEC/
│
├── README.md                           # Documentação principal do projeto
├── requirements.txt                    # Dependências e pacotes necessários
└── Projeto_avaliativo_Módulo_1.ipynb   # Notebook oficial contendo as 7 fases do pipeline
```

## Como Executar

1. Clone o repositório:
   ```bash
   git clone https://github.com/<thaysfaleiro>/Mini-projeto-SCTEC.git
   cd Mini-projeto-SCTEC
   ```

## Resultados

| Modelo | Acurácia (Teste) |
|---|---|
| KNN (k=5) | 89,65% |
| Árvore de Decisão (max_depth=5) | 90,20% |

> **Nota sobre a métrica:** o dataset é fortemente desbalanceado (~96,6% dos registros são "sem falha"), portanto a acurácia isolada não é a métrica mais adequada para decidir o modelo final — um classificador que sempre prevê "sem falha" atingiria acurácia próxima disso sem detectar nenhuma falha real. Recomenda-se complementar a avaliação com **Recall** e **F1-Score** da classe "falha" antes de declarar um modelo vencedor.

## Sugestões futuras

- Substituir a acurácia por métricas focadas em minimizar falsos negativos (Recall, F1-Score).
- Testar modelos de ensemble (Random Forest, XGBoost).
- Criar atributos temporais (médias e desvios móveis) a partir do histórico dos sensores.
- Integrar o pipeline a sistemas SCADA para inferência em tempo real.

## Autor

Desenvolvido por Thays Faleiro como projeto avaliativo do Módulo 1 do curso de Desenvolvimento em IA para Análise Preditiva — SCTEC.















