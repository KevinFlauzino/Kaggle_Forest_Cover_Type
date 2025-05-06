# Forest Cover Type Prediction

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Pandas](https://img.shields.io/badge/Pandas-1.3.0-%23007ACC)
![Kaggle](https://img.shields.io/badge/Kaggle-Challenge-%2320BEFF)

Projeto desenvolvido para o desafio **Forest Cover Type Prediction** do Kaggle, com o objetivo de prever o tipo de cobertura florestal em áreas de 30x30m na Floresta Nacional Roosevelt (Colorado, EUA). Utiliza um modelo de Árvore de Decisão para classificação, alcançando uma pontuação de **0.70962** no leaderboard do Kaggle.

---

## 📋 Conteúdo
- [Dataset](#dataset)
- [Metodologia](#metodologia)
- [Tecnologias](#tecnologias)


---

## Dataset
O dataset contém informações sobre características geográficas e ambientais de áreas florestais. Está disponível no [Kaggle](https://www.kaggle.com/c/forest-cover-type-prediction/data) e divide-se em:
- **train.csv**: Dados de treino com a classe de cobertura florestal (7 tipos).
- **test.csv**: Dados para previsão (sem a classe).

**Tipos de Cobertura Florestal:**
1. Spruce/Fir  
2. Lodgepole Pine  
3. Ponderosa Pine  
4. Cottonwood/Willow  
5. Aspen  
6. Douglas-fir  
7. Krummholz  

---

## Metodologia

### 🔍 Análise e Seleção de Variáveis
Foram selecionadas variáveis com base em:
1. **Correlação positiva** com a classe alvo.
2. **Distância horizontal/vertical de recursos hídricos**.
3. **Índice de sombra às 15h** (pico único por tipo de vegetação).
4. **Distância de pontos de incêndio** (ex: Abetos são mais suscetíveis).
5. **Distância de estradas** (influência na construção e acesso).

### 🌳 Modelo de Árvore de Decisão
- **Configuração**: 500 folhas (ramos finais de decisão).
- **Treinamento**: Aplicado ao dataset `train.csv`.
- **Previsão**: Utilizado no dataset `test.csv` para gerar o arquivo de submissão.

---

## Tecnologias
- **Python 3.8+**
- **Pandas**: Manipulação de dados.
- **Scikit-learn**: Implementação do modelo de Árvore de Decisão.
- **Matplotlib/Seaborn**: Visualização de dados.
