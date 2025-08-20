# Challenge Telecom X: análise de evasão de clientes - parte 2 (Oracle + Alura)

## 🔖 Sobre

O projeto **Challenge Telecom X** foi elaborado como critério avaliativo do programa **ONE** _(Oracle Next Education)_, em parceria com a **Alura**, e o objetivo desta segunda parte foi construir e avaliar uma solução preditiva de churn. Para isso, preparei os dados para Machine Learning (limpeza, encoding e, quando necessário, normalização), realizei o split estratificado em treino/teste e treinei ao menos dois modelos complementares (um linear com normalização, como Regressão Logística, e um baseado em árvore, como Random Forest). Em seguida, avaliei desempenho com acurácia, precisão, recall, F1, ROC/PR-AUC e matriz de confusão, e interpretei a relevância das variáveis (coeficientes/importâncias). Por fim, sintetizei os fatores-chave de evasão e propus estratégias de retenção acionáveis com base nos resultados.

##  :hammer_and_wrench: Tecnologias

- `Python`
- `Google Colab`
- `Pandas`
- `NumPy`
- `Matplotlib`
- `Joblib / CSV` 
- `Jupyter Notebook`  
- `scikit-learn`

## 📊 Resultados

- Preparei os dados (limpeza, one-hot, criação de `Contas_Diarias`) e confirmei desbalanceamento moderado da base (\~26,5% de churn).
- Dividi em treino/teste (80/20) com estratificação.
- **Regressão Logística (com normalização)** teve melhor generalização: ROC-AUC ≈ 0,843; PR-AUC ≈ 0,660; F1 ≈ 0,640.
- **Random Forest (sem normalização)** ficou próximo, porém com sinais de overfitting (treino muito acima de teste): ROC-AUC ≈ 0,838; PR-AUC ≈ 0,648; F1 ≈ 0,628.
- Principais fatores associados à evasão: contrato **month-to-month** (+), **tenure** baixo (– relação com churn), **electronic check** (+), **mensalidade** alta sem benefícios (+), ausência de **suporte técnico**/**segurança online** (+).
- Recomendei retenção focada em clientes novos e de contrato mensal (incentivo a planos anuais), bundles de valor (segurança/suporte), migração de método de pagamento e ajustes de preço/valor percebido.

## 📌 Conclusão

Os principais determinantes de evasão convergem para perfil contratual (especialmente “Month-to-month”), tenure baixo, método de pagamento com maior fricção e mensalidade alta sem contrapartida de valor. Ao endereçar esses pontos com fidelização contratual, bundles de valor, onboarding estruturado e migração de método de pagamento, a empresa tende a reduzir o churn de forma mensurável. Do ponto de vista de modelagem, mantenho a Regressão Logística como baseline interpretável e recomendo aplicar regularização adicional no Random Forest (e/ou testar Gradient Boosting com tuning) para elevar desempenho sem perder generalização.

## :computer: Desenvolvedor

| [<img loading="lazy" src="https://avatars.githubusercontent.com/u/201506724?s=400&u=835afcab83b5653fec0f8f8fb53e6b99207e9b00&v=4" width=115><br><sub>Vinicius Areias</sub>](https://github.com/Vinicius-Areias) |   
| :---: |
