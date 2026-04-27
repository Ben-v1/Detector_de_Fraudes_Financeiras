# **Detector de Fraude**

<div align="justify">

No mundo real, as transações financeiras são, em sua esmagadora maioria, legítimas. A fraude é uma anomalia (geralmente representando menos de 1% do volume total).

**O Dilema do Negócio:**

*    Falsos Negativos (Deixar a fraude passar): Custo direto para a empresa, que muitas vezes precisa reembolsar o cliente fraudado, além de gerar multas regulatórias e perda de confiança.

*   Falsos Positivos (Bloquear uma transação legítima): Atrito imenso. Se você bloqueia o cartão de um bom cliente no meio de um jantar, ele pode cancelar a conta e ir para o concorrente.

</div>
<div align="justify">

**A Armadilha do Desbalanceamento:**

Se 99,9% das transações são legítimas, um modelo "preguiçoso" que simplesmente diz que nenhuma transação é fraude terá 99,9% de acurácia. Para o negócio, porém, a utilidade desse modelo é zero. É por isso que não usamos a "Acurácia" como métrica principal aqui, mas sim o Recall (capacidade de encontrar as fraudes) e a Precisão (quando diz que é fraude, acertar).

**A Solução com SMOTE:**

O SMOTE (Synthetic Minority Over-sampling Technique) resolve esse desbalanceamento criando "clones inteligentes" (dados sintéticos) da classe minoritária (as fraudes) usando vizinhos mais próximos. Assim, o modelo tem exemplos suficientes para aprender os padrões criminosos sem ficar enviesado pela maioria de transações boas.

</div>

<div align="justify">
A detecção de fraudes em transações financeiras representa um dos maiores desafios e necessidades críticas para instituições bancárias e empresas de pagamento na atualidade. Como abordado no projeto, a fraude é uma anomalia, geralmente representando menos de 1% do volume total de transações. A importância de desenvolver um modelo preditivo eficaz reside na resolução do chamado "Dilema do Negócio", que consiste em equilibrar o impacto dos falsos negativos (deixar a fraude passar, o que gera custos diretos de reembolso e possíveis multas) e dos falsos positivos (bloquear uma transação legítima, causando um imenso atrito e perda de confiança do cliente).
<br><br>
Para superar a armadilha do desbalanceamento dos dados, onde focar apenas na Acurácia entregaria resultados enganosos, o projeto obteve sucesso ao priorizar as métricas de Recall e Precisão. Resultados consistentes foram alcançados graças à aplicação da técnica SMOTE, que criou "clones inteligentes" da classe minoritária (fraudes), permitindo que os modelos aprendessem os padrões criminosos de forma justa e sem o viés da maioria de transações legítimas. A utilização de algoritmos avançados, como Random Forest e XGBoost, provou-se altamente capaz de lidar com essa complexidade. Além disso, a estratégia de definir um threshold (ponto de corte) customizado de 0.70 mostrou-se um excelente refinamento, garantindo que o sistema só sinalize uma fraude quando tiver 70% ou mais de certeza, mitigando fortemente o bloqueio indevido de bons clientes.
<br><br>
A utilidade prática deste desenvolvimento no mundo corporativo é imensa. Ao ser implementado em um ambiente de produção, este modelo atua como uma poderosa camada de defesa em tempo real, capaz de processar e avaliar o risco de milhares de transações por segundo. Para o negócio, isso se traduz em uma diminuição significativa de perdas financeiras por golpes e na otimização do trabalho das equipes de análise de fraude, que passam a investigar apenas os alertas mais críticos e precisos. Em suma, o projeto entrega uma solução tecnológica robusta que protege o patrimônio da empresa e, simultaneamente, preserva a experiência de uso do cliente legítimo, fator vital para a competitividade no mercado financeiro moderno.
</div>
