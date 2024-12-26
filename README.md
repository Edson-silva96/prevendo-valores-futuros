# prevendo-valores-futuros
**Projeto de Ciência de Dados: Previsão de Arrecadação**

![imag ci 0](https://github.com/user-attachments/assets/4d5b6879-c50c-42aa-ae2b-f8432d1fef93)


Este projeto de Ciência de Dados visa a criação de um modelo de Machine Learning para prever os valores futuros de arrecadação, com base nos dados históricos de arrecadação e despesas dos diversos centros de custos de uma organização. O conjunto de dados disponível contém informações mensais sobre os valores planejados e realizados de cada centro de custo, incluindo áreas como Presidência, Diretoria, Comercial, Contabilidade, Financeiro, Recurso Humanos, Produção e TI, ao longo do ano de 2018.

O objetivo principal deste projeto é utilizar técnicas de Machine Learning para identificar padrões e relações entre os valores planejados e realizados, de modo a prever a arrecadação futura. Com isso, será possível oferecer insights valiosos para o planejamento financeiro e orçamentário da organização, permitindo uma gestão mais eficiente dos recursos e um melhor acompanhamento das metas de arrecadação.

A análise dos dados incluirá o pré-processamento, a escolha de variáveis relevantes, a divisão do conjunto de dados em treino e teste, além da aplicação de modelos de regressão e/ou séries temporais para alcançar as melhores previsões. A precisão do modelo será avaliada e ajustada para garantir que ele seja capaz de oferecer previsões úteis e confiáveis para os gestores da organização.

![imag ci](https://github.com/user-attachments/assets/9fe160b8-f31d-4997-ba29-3c928c041b75)

A análise descrita pelos métodos `describe()` dos dados fornecidos nos dá uma visão estatística sobre as colunas "Planejado" e "Realizado", e também fornece algumas informações sobre a coluna "Mês". Aqui está uma interpretação das principais métricas geradas:

1. **Mês (Data)**:
   - **count**: Existem 96 registros de meses (um por mês ao longo de 2018).
   - **mean**: A média dos meses está em torno de 2018-06-16. Isso indica que os dados estão distribuídos uniformemente ao longo de 2018.
   - **min**: O primeiro mês registrado é 2018-01-01 (janeiro de 2018).
   - **25%**: O primeiro quartil está em 2018-03-24, indicando que 25% dos dados estão antes dessa data.
   - **50%**: A mediana dos meses é em 2018-06-16, o que significa que metade dos dados está antes e metade está depois desta data.
   - **75%**: O terceiro quartil está em 2018-09-08, indicando que 75% dos dados estão antes desta data.
   - **max**: O último mês registrado é 2018-12-01 (dezembro de 2018).

2. **Planejado**:
   - **count**: Existem 96 valores de "Planejado".
   - **mean**: O valor médio de arrecadação planejada é de aproximadamente 30.600 unidades monetárias.
   - **min**: O valor mínimo de arrecadação planejada é 20.545,47 unidades monetárias.
   - **25%**: O valor do primeiro quartil de arrecadação planejada é 25.029,91 unidades monetárias, o que significa que 25% dos valores planejados estão abaixo desse valor.
   - **50%** (Mediana): O valor médio de arrecadação planejada no meio dos dados é 30.270,34 unidades monetárias.
   - **75%**: O valor do terceiro quartil de arrecadação planejada é 36.220,17 unidades monetárias, indicando que 75% dos valores planejados estão abaixo deste valor.
   - **max**: O valor máximo de arrecadação planejada é 40.985,65 unidades monetárias.
   - **std**: O desvio padrão de 6.127,08 unidades monetárias indica uma certa variabilidade nos valores planejados, ou seja, há uma diferença considerável entre o valor mínimo e máximo dos dados planejados.

3. **Realizado**:
   - **count**: Existem 96 valores de "Realizado".
   - **mean**: O valor médio de arrecadação realizada é de aproximadamente 28.850,28 unidades monetárias, ligeiramente inferior ao valor planejado.
   - **min**: O valor mínimo de arrecadação realizada é 19.638,40 unidades monetárias.
   - **25%**: O valor do primeiro quartil de arrecadação realizada é 23.681,13 unidades monetárias.
   - **50%** (Mediana): O valor médio de arrecadação realizada na mediana é 28.569,35 unidades monetárias.
   - **75%**: O valor do terceiro quartil de arrecadação realizada é 33.926,16 unidades monetárias.
   - **max**: O valor máximo de arrecadação realizada é 37.986,70 unidades monetárias.
   - **std**: O desvio padrão de 5.756,37 unidades monetárias indica uma variabilidade similar à de "Planejado", com valores consideráveis de dispersão.

Conclusões Gerais:
- A arrecadação "Realizada" é, em média, inferior à arrecadação "Planejada", o que pode indicar que a organização tem dificuldades em atingir suas metas de arrecadação.
- A diferença entre os valores mínimos e máximos, bem como os desvios padrão relativamente altos, sugerem que a organização experimenta flutuações consideráveis em ambos os valores planejados e realizados ao longo do ano.
- A análise de quartis sugere que, em média, os valores planejados e realizados aumentam ao longo do ano, com os meses de junho a setembro apresentando um aumento significativo nas metas de arrecadação.

- ![imag ci2](https://github.com/user-attachments/assets/2b25bf90-a2a8-4cc7-9ee7-d4da39d87c6a)

1. **Planejamento total: 2.937.630,53**  
   O valor total de arrecadação planejada ao longo de 2018 foi de 2.937.630,53 unidades monetárias.

2. **Arrecadação total: 2.769.627,15**  
   O valor total de arrecadação realizada ao longo do ano foi de 2.769.627,15 unidades monetárias.

3. **Total: -168.003,38**  
   A diferença entre a arrecadação realizada e a planejada foi negativa em 168.003,38 unidades monetárias, o que significa que a arrecadação real foi inferior à arrecadação planejada. Esse valor negativo indica que a organização não atingiu suas metas de arrecadação ao longo do ano.

Em resumo, a organização arrecadou 168.003,38 unidades monetárias a menos do que o valor previsto no planejamento. Isso pode refletir desafios no cumprimento das metas financeiras estabelecidas para 2018.

![imag ci 3](https://github.com/user-attachments/assets/d64e251b-8147-47fa-83fb-60649dc44a03)

![imag ci 4](https://github.com/user-attachments/assets/f5f2867c-aedd-4220-8a33-5c8a70ae04e7)

Entendendo o Gráfico

O gráfico apresentado compara os valores planejados e realizados ao longo de um ano (de janeiro a dezembro). Cada linha representa uma dessas métricas, e os pontos indicam os valores para cada mês.

Principais Observações:

Variação Mensal: Há uma considerável variação nos valores planejados e realizados ao longo dos meses, tanto para mais quanto para menos.
Tendência Geral: Não há uma tendência clara de crescimento ou decrescimento ao longo do ano, mas sim oscilações mês a mês.
Desvios: Em diversos meses, os valores realizados divergem significativamente dos valores planejados, indicando que, em alguns casos, as metas não foram alcançadas e, em outros, foram superadas.
Picos e Valas: É possível identificar meses com picos de valores, tanto planejados quanto realizados, e outros com valores mais baixos.

![imag ci 6](https://github.com/user-attachments/assets/846121de-f8c9-4897-b17b-d0b9cc99874b)

![imag c1 5](https://github.com/user-attachments/assets/f12b4337-9e90-4e22-b4ce-c76952c9704c)

Analisando o Gráfico 
O que o Gráfico Mostra?
O gráfico de barras apresentado compara os valores planejados e realizados ao longo de um ano, mês a mês. Ele permite visualizar de forma clara:

Desempenho Variável: Os valores planejados e realizados variam significativamente entre os meses, indicando que o desempenho pode ser influenciado por fatores sazonais, econômicos ou outros.
Desvios: Há meses em que os valores realizados estão bem acima ou abaixo dos valores planejados, sugerindo que as previsões podem não ser precisas em todos os casos.
Tendências: Observar a direção geral das barras pode indicar se há uma tendência de crescimento ou decrescimento nos valores ao longo do ano.
## treinando o modelo
![imag ci 7](https://github.com/user-attachments/assets/4e98b7c0-4e6b-48f9-99d9-2b5e96d271be)
![imag ci 8](https://github.com/user-attachments/assets/6d5bcc0e-2456-4c7d-a247-85e63b60d391)

O que o Código Faz?

O código apresentado realiza as seguintes etapas:

1. **Codificação Categorical:** Transforma a coluna 'Centro de Custos' em variáveis dummy (0 ou 1) para que possam ser utilizadas nos modelos de machine learning.
2. **Divisão dos Dados:** Separa os dados em features (X) e target (y), e depois em conjuntos de treino e teste para avaliar o desempenho dos modelos.
3. **Definição da Função de Avaliação:** Cria uma função para treinar um modelo, fazer previsões e calcular o erro absoluto médio (MAE) e o coeficiente de determinação (R²).
4. **Teste de Modelos:** Aplica a função de avaliação a diferentes modelos de regressão (Linear Regression, DecisionTreeRegressor, RandomForestRegressor e GradientBoostingRegressor).

### Interpretação dos Resultados

Os resultados obtidos para cada modelo são os seguintes:

* **Regressão Linear:** MAE: 367.23, R²: 0.99
* **Árvore de Decisão:** MAE: 457.05, R²: 0.99
* **Random Forest:** MAE: 420.22, R²: 0.99
* **Gradient Boosting:** MAE: 466.49, R²: 0.99

**Análise dos Métricas:**

* **MAE (Mean Absolute Error):** Representa o erro médio absoluto entre os valores reais e os valores previstos pelo modelo. Quanto menor o MAE, melhor o modelo.
* **R² (Coeficiente de Determinação):** Indica a proporção da variância dos dados que é explicada pelo modelo. Um valor de R² próximo a 1 indica que o modelo se ajusta bem aos dados.

**Conclusões:**

* **Alto R²:** Todos os modelos apresentaram um R² muito próximo de 1, o que indica que eles explicam quase toda a variância dos dados. Isso sugere que os modelos estão se ajustando muito bem aos dados de treinamento.
* **MAE Variável:** O MAE varia entre os modelos, indicando que alguns modelos podem ser mais precisos em termos de prever valores individuais. A Regressão Linear apresentou o menor MAE, sugerindo que ela pode ser a melhor opção para este conjunto de dados específico.
* **Overfitting:** O alto R² e a diferença nos valores de MAE podem indicar um possível caso de overfitting, especialmente para os modelos de árvore de decisão, random forest e gradient boosting. Esses modelos podem estar memorizando os dados de treinamento em vez de generalizar para novos dados.

## Por que a Regressão Linear Foi Escolhida?

**Analisando os Resultados**

Com base nos resultados apresentados, onde a Regressão Linear apresentou o menor MAE (Erro Absoluto Médio) entre os modelos testados, podemos inferir algumas razões para sua escolha:

* **Simplicidade e Interpretabilidade:** A Regressão Linear é um modelo estatístico linear que estabelece uma relação linear entre uma variável dependente e uma ou mais variáveis independentes. Essa simplicidade facilita a interpretação dos coeficientes do modelo, permitindo entender como cada variável independente influencia a variável dependente.
* **Menor Complexidade:** Em comparação com modelos como Árvore de Decisão, Random Forest e Gradient Boosting, a Regressão Linear é menos propensa a overfitting (superajuste), que ocorre quando o modelo se ajusta demais aos dados de treinamento e perde a capacidade de generalizar para novos dados.
* **Bom Desempenho:** Embora os outros modelos também tenham apresentado um alto R², a Regressão Linear obteve o menor MAE, indicando que, em média, suas previsões estão mais próximas dos valores reais.

## link para o codigo da matriz de confusao do modelo de regressao linear
https://colab.research.google.com/drive/1jalr5hcnEx13T6mb-8K-9smkl2W5ILpZ#scrollTo=Av4bnUsVhuuN&line=1&uniqifier=1
![imag ci 9](https://github.com/user-attachments/assets/c8758433-4614-4a6c-bff1-8a4128130d77)

Interpretando a Matriz
A matriz de confusão apresentada mostra que:

Todos os erros foram classificados como "Pequeno": Isso indica que a diferença entre os valores reais e os valores previstos foi sempre menor ou igual a 500.
Não houve erros classificados como "Médio" ou "Grande": Isso significa que nenhum erro ultrapassou os limiares definidos para essas categorias.


![imag 11](https://github.com/user-attachments/assets/e269e7e9-1315-4878-8915-fa465ee2f3cc)
**O que o Gráfico Mostra:**

O gráfico apresentado compara os valores reais de uma determinada variável (representados pela linha azul contínua e marcadores circulares) com os valores previstos por um modelo (representados pela linha vermelha tracejada e marcadores em "x"). A diferença entre as duas linhas indica a precisão do modelo em prever os valores.

**Interpretação:**

* **Ajuste do Modelo:** A proximidade entre as linhas azul e vermelha indica o quão bem o modelo se ajusta aos dados reais. Se as linhas estiverem muito próximas, o modelo está fazendo previsões precisas. Se as linhas estiverem distantes, o modelo não está capturando bem as tendências dos dados.
* **Tendências:** Ao analisar as formas das duas linhas, podemos identificar se o modelo consegue capturar as tendências dos dados. Se as duas linhas seguirem padrões semelhantes, o modelo está capturando as tendências de forma adequada.
* **Pontos de Desvio:** Os pontos onde as linhas se distanciam significativamente indicam que o modelo está tendo dificuldades em prever os valores corretamente nesses pontos específicos.

**Possíveis Cenários e Interpretações:**

* **Bom Ajuste:** Se as linhas estiverem muito próximas e seguirem padrões semelhantes, o modelo está fazendo previsões precisas e pode ser utilizado para fazer previsões futuras com confiança.
* **Sobreajuste:** Se a linha do modelo seguir os dados de treinamento muito de perto, mas não generalizar bem para novos dados, pode indicar um caso de overfitting (sobreajuste). Nesse caso, o modelo pode estar memorizando os dados de treinamento em vez de aprender as relações subjacentes.
* **Subajuste:** Se a linha do modelo estiver muito distante dos dados reais, o modelo pode estar subajustado, ou seja, não está capturando a complexidade dos dados.
* **Ruído:** Se houver muita variação aleatória nos dados, pode ser difícil para qualquer modelo fazer previsões precisas.

* ## testando com novos dados
![imag ci 12](https://github.com/user-attachments/assets/abed78a7-8afe-435d-a899-1ce89f94c86a)










