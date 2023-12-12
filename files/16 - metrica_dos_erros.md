**Python - Estatística II** 
>**Métricas de Erros**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;



 ## Métricas de Erro

As métricas de erro são utilizadas para avaliar o desempenho de modelos preditivos e a qualidade das previsões em relação aos valores reais. Aqui estão algumas métricas comuns, suas fórmulas e o contexto em que são aplicadas:

### 1. **Erro Absoluto Médio (MAE):**
   - **Fórmula:**
     $MAE = \displaystyle\frac{1}{n} \sum_{i=1}^{n} |y_i - \hat{y}_i|$
   - **Descrição:**
     - Média das diferenças absolutas entre os valores reais ($y_i$) e os valores previstos ($\hat{y}_i$).
     - Útil quando os erros positivos e negativos têm o mesmo impacto.

### 2. **Erro Quadrático Médio (MSE):**
   - **Fórmula:**
     $MSE = \displaystyle\frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2$
   - **Descrição:**
     - Média das diferenças quadráticas entre os valores reais ($y_i$) e os valores previstos ($\hat{y}_i$).
     - Penaliza mais os erros grandes.

### 3. **Raiz do Erro Quadrático Médio (RMSE):**
   - **Fórmula:**
     $RMSE = \sqrt{MSE}$
   - **Descrição:**
     - Raiz quadrada do MSE, proporcionando uma métrica na mesma escala dos valores originais.
     - Facilita a interpretação em termos das unidades da variável de resposta.

### 4. **Erro Percentual Absoluto Médio (MAPE):**

   - **Fórmula:**
     
     $MAPE = \displaystyle\frac{1}{n} \sum_{i=1}^{n} \left( \displaystyle\frac{|y_i - \hat{y}_i|}{|y_i|} \right) \times 100$
     
   - **Descrição:**
     
     - Média dos erros percentuais absolutos em relação aos valores reais.
     - Expressa os erros como uma porcentagem do valor real, útil para interpretar a precisão relativa.

### 5. **Coeficiente de Determinação ($R^2$):**
   - **Fórmula:**
   


![Alt text](/assets/16-1.png)




   - **Descrição:**
     - Mede a proporção da variabilidade na variável de resposta que é explicada pelo modelo.
     - $R^2$ próximo a 1 indica bom ajuste, enquanto próximo a 0 indica baixa capacidade de explicação.

### Testes de Hipótese:

- **H0 (Hipótese Nula):**
  - Não há diferença significativa entre os valores reais e os valores previstos.
- **H1 (Hipótese Alternativa):**
  - Existe diferença significativa entre os valores reais e os valores previstos.

### Quando Usar Cada Métrica:

1. **MAE e RMSE:**
   - Usados quando é importante avaliar a magnitude dos erros.
   - MAE é mais robusto a outliers, enquanto RMSE penaliza mais erros grandes.

2. **MAPE:**
   - Útil quando se deseja avaliar os erros como uma porcentagem dos valores reais.

3. **$R^2$:**
   - Indicado quando se busca entender o quanto a variabilidade do modelo explica a variabilidade dos dados.

A escolha da métrica depende do contexto específico do problema e das características desejadas na avaliação do modelo. Cada métrica fornece uma perspectiva única sobre o desempenho do modelo, e a escolha deve ser feita considerando os objetivos específicos da análise.








&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>
