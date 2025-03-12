# Detecção de Defeitos em Impressões 3D Utilizando Aprendizado de Máquina

Este projeto foi desenvolvido como parte da disciplina de Inteligência Artificial. O objetivo é comparar diferentes modelos de aprendizado de máquina para detectar erros em impressões 3D a partir de imagens, utilizando um dataset do Kaggle
## Descrição do Projeto

O projeto consiste em:
1. **Extrator de caracteristicas**: Para extrair caracteristicas das imagens e criar uma tabela.
2. **Pré-processamento dos dados**: Tratamento de valores faltantes, normalização e redução de dimensionalidade com PCA.
3. **Seleção de features**: Utilização de PCA para selecionar as features mais relevantes para serem analisadas nos gráficos.
4. **Balanceamento de classes**: Aplicação da técnica NearMiss para balancear as classes do dataset.
5. **Treinamento de modelos**: Comparação de quatro modelos de classificação:
   - K-Nearest Neighbors (KNN)
   - Support Vector Machine (SVM)
   - Random Forest (RF)
   - Gradient Boosting (GB)
6. **Validação cruzada**: Uso de K-Fold com 10 folds para avaliar os modelos.
7. **Teste de Wilcoxon**: Comparação estatística dos modelos para verificar diferenças significativas.

## Resultados

Os modelos foram avaliados com base em quatro métricas:
- Acurácia
- Precisão
- Recall
- F1-score

### Métricas Médias por Modelo

| Modelo           | Acurácia | Precisão | Recall | F1-score |
|------------------|----------|----------|--------|----------|
| KNN              | 0.9440   | 0.9523   | 0.9348 | 0.9434   |
| SVM              | 0.9768   | 0.9800   | 0.9734 | 0.9767   |
| Random Forest    | 0.9545   | 0.9392   | 0.9723 | 0.9553   |
| Gradient Boosting| 0.9555   | 0.9462   | 0.9665 | 0.9562   |

### Teste de Wilcoxon

O teste de Wilcoxon foi aplicado para comparar os modelos dois a dois. Abaixo estão os resultados para cada métrica:

| Comparação           | Acurácia | Precisão | Recall | F1-score |
|------------------|----------|----------|--------|----------|
| KNN vs SVM              | 0.002   | 0.002   | 0.002 | 0.002   |
| KNN vs Random Forest              | 0.017   | 0.009   | 0.002 | 0.019   |
| KNN vs Gradient Boosting    | 0.003   | 0.0845   | 0.002 | 0.002   |
| SVM vs Random Forest| 0.002   | 0.002   | 0.812 | 0.002   |
| SVM vs Gradient Boosting| 0.002   | 0.002   | 0.128 | 0.002   |
| Random Forest vs Gradient Boosting | 0.062   | 0.0137 | 0.296   | 0.105   |

### Dependências
- Python
- Bibliotecas:
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- imbalanced-learn
- scipy

### Dataset
O dataset utilizado neste projeto foi obtido do Kaggle. Para mais detalhes, consulte o link: : https://www.kaggle.com/datasets/nimbus200/3d-printing-errors.

