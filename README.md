# 🤖 Sistema de Recomendação de Produtos — Olist E-Commerce

> Avaliação N1 · Disciplina de Machine Learning · BCC · FMU 2026

---

## 📋 Descrição do Projeto

Este projeto desenvolve um **motor de recomendação baseado em propensão de satisfação**, utilizando o dataset público de e-commerce brasileiro da Olist. O modelo prevê se um cliente dará uma avaliação positiva (nota ≥ 4) a um produto com base em 6 características do item — produtos com alta probabilidade de satisfação são então "recomendados" ao usuário.

A abordagem utiliza **Machine Learning Supervisionado** com o algoritmo Random Forest, otimizado via GridSearchCV e validado com técnicas de validação cruzada e curvas de aprendizado.

---

## 🗂️ Estrutura do Repositório

```
📦 repositorio/
├── 📓 assignment_n1_machine_learning.ipynb   # Notebook principal (Google Colab)
├── 📄 README.md                              # Este arquivo
└── 👥 integrantes.txt                        # Nomes e RAs do grupo
```

---

## 🎯 Artefatos Entregues

| # | Artefato | Descrição |
|---|---|---|
| 1 | **Coleta e Limpeza de Dados** | Download do dataset Olist (Kaggle), merge de 3 tabelas, tratamento de nulos e padronização com StandardScaler |
| 2 | **Desenvolvimento do Modelo** | Comparação de algoritmos (RF × Logistic Reg. × KNN), treinamento do Random Forest com validação cruzada K-Fold=5 |
| 3 | **Avaliação e Aprimoramento** | GridSearchCV para otimização de hiperparâmetros, curvas de aprendizado, análise de overfitting/underfitting |
| 4 | **Visualização dos Resultados** | Matriz de Confusão, Curva ROC/AUC, Distribuição de Probabilidades, Feature Importance, Heatmap de Correlações, Top-10 Recomendações |
| 5 | **Apresentação Final e Relatório** | Relatório crítico com decisões técnicas, descobertas de negócio, limitações e reflexão sobre o aprendizado |

---

## 🛠️ Tecnologias Utilizadas

- **Python 3.10+**
- **pandas** — manipulação e limpeza de dados
- **numpy** — operações numéricas
- **scikit-learn** — modelos de ML, validação cruzada, GridSearchCV
- **matplotlib** — visualizações
- **seaborn** — visualizações estatísticas
- **kagglehub** — download do dataset diretamente no Colab

---

## 📊 Dataset

**Olist Brazilian E-Commerce Dataset** — disponível no Kaggle:  
🔗 https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

Tabelas utilizadas:
- `olist_order_items_dataset.csv`
- `olist_products_dataset.csv`
- `olist_order_reviews_dataset.csv`

---

## ⚙️ Como Executar

1. Acesse o notebook pelo link do Google Colab abaixo
2. Vá em **Arquivo → Salvar uma cópia no Drive**
3. Execute as células em ordem (Runtime → Run all)
4. Nenhuma configuração adicional é necessária — o dataset é baixado automaticamente

> 🔗 **Google Colab:** _[inserir link do Colab aqui]_

---

## 📈 Resultados Obtidos

| Métrica | Valor |
|---|---|
| Acurácia (teste) | ~74% |
| AUC-ROC | > 0.75 |
| Validação Cruzada (5-Fold) | ~73% ± 1% |
| Algoritmo final | Random Forest (otimizado via GridSearchCV) |

**Principal descoberta:** Preço e Valor do Frete são os fatores mais determinantes para a satisfação do cliente — um sistema de recomendação eficiente deve priorizar a relação preço/frete para o CEP do usuário.

---

## 👥 Integrantes do Grupo

| Nome | RA |
|---|---|
| _Gustavo Diniz Rodrigues_ | _2025102891_ |

---

## 📅 Entrega

- **Data limite:** 22/05/2026
- **Formato:** GitHub + Google Colab
- **Disciplina:** Machine Learning — FMU 2026

