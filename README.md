## 🩸 Modelo de Machine Learning: O paciente vai ou não desenvolver uma doença hepática? 

![alt text](<imagens/Imagem do WhatsApp de 2025-04-21 à(s) 13.53.20_1a970805.jpg>)

## 🩺Descrição do Problema

O projeto tem como objetivo desenvolver um modelo preditivo capaz de classificar a presença ou ausência de doença hepática em pacientes com base em dados clínicos e laboratoriais. Essa é uma tarefa de classificação supervisionada, na qual o algoritmo aprende a partir de exemplos rotulados (com ou sem doença hepática) para, posteriormente, realizar previsões em novos dados.
O conjunto de dados utilizado contém variáveis como idade, sexo, níveis de bilirrubina, enzimas hepáticas, albumina, entre outros indicadores clínicos. 
A ideia é que esse modelo possa ser uma ferramenta útil para médicos, hospitais ou governos, auxiliando no planejamento de gastos com saúde ou na criação de políticas de prevenção mais eficazes.  

Por se tratar de uma tarefa de previsão de classe (sim ou não), optei por usar aprendizado supervisionado para classificação. Durante o projeto, criei diferentes versões do modelo empregando diversos algoritmos de classificação, buscando identificar qual deles teria o melhor desempenho. O processo envolveu todas as etapas de Machine Learning, desde a pré-processamento de dados até a avaliação do modelo final.  

Os dados utilizados para treinar e testar o modelo foram obtidos a partir de um dataset público, disponível no seguinte link: [🔗 Dataset Utilizado](https://archive.ics.uci.edu/dataset/225/ilpd+indian+liver+patient+dataset)

Trabalhei cuidadosamente para garantir a integridade dos dados e realizar uma análise detalhada, ajustando o modelo para oferecer previsões confiáveis que possam contribuir para a tomada de decisões.

## ✅ Justificativa da Escolha

As doenças hepáticas são um problema de saúde pública mundial, podendo evoluir silenciosamente até estágios avançados. Um sistema preditivo automatizado pode auxiliar na triagem médica inicial, ajudando médicos e instituições de saúde a identificarem casos suspeitos de forma mais ágil e eficiente, especialmente em contextos de escassez de recursos.

Além disso, a base de dados é de domínio público e amplamente utilizada para estudos de classificação, permitindo uma comparação com abordagens já consolidadas e servindo como excelente exercício prático para aplicação de algoritmos de aprendizado de máquina.

## 🤖 Algoritmo com Melhor Desempenho

Foram testados diferentes algoritmos de classificação, incluindo:

Regressão Logística

K-Nearest Neighbors (KNN)

Árvore de Decisão

Random Forest

Suporte a Vetores de Máquinas (SVM)

XGBoost

Após realizar o pré-processamento dos dados, balanceamento das classes com SMOTE e ajuste de hiperparâmetros por meio de GridSearchCV, o algoritmo que apresentou melhor desempenho foi o Random Forest, com os seguintes resultados:

Acurácia: 86%

Precisão: 84%

Recall: 88%

F1-Score: 86%


## 📊 Análise dos Resultados

O modelo de Random Forest destacou-se com o melhor desempenho entre os algoritmos testados, apresentando um ótimo equilíbrio entre acurácia, precisão e recall. Esse equilíbrio é crucial no contexto clínico, pois reduz significativamente a ocorrência de falsos negativos — casos em que pacientes com a doença poderiam não ser identificados. Em cenários de triagem médica, esse aspecto é vital para evitar diagnósticos tardios e permitir intervenções mais eficazes.

Além do bom desempenho métrico, a análise de importância das variáveis indicou que atributos como Bilirrubina Direta, Aspartato Aminotransferase (SGOT), Albumina e Idade possuem maior influência sobre a predição. Essa descoberta está alinhada com evidências na literatura médica, reforçando a confiabilidade clínica do modelo ao refletir fatores biológicos relevantes no diagnóstico de disfunções hepáticas.

Outro ponto relevante foi a aplicação de técnicas de balanceamento de classes e validação cruzada, que contribuíram para a robustez do modelo. Essas estratégias minimizaram o impacto do desbalanceamento natural do conjunto de dados — onde há predominância de uma das classes — e garantiram uma generalização mais confiável do modelo em novos dados.

