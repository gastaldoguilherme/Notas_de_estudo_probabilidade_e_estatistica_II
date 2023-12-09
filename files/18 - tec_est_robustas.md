**Python - Estatística II** 
>**Técnicas Estatísticas Robustas**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;



## Técnicas Estatísticas Robustas para dados que não seguem uma distribuição normal ou quando há preocupações com outliers

Quando os dados não seguem uma distribuição normal ou quando há preocupações com outliers, é possível recorrer a técnicas estatísticas mais robustas. Algumas dessas técnicas incluem:

1. **Mediana e Intervalo Interquartil (IQR):** Em vez da média e do desvio padrão, a mediana e o IQR (diferença entre o terceiro quartil e o primeiro quartil) são medidas mais robustas de tendência central e dispersão, respectivamente.

2. **Métodos Robustos de Estimação de Parâmetros:**
   - **Mínimos Quadrados Ponderados (WLS):** atribui pesos diferentes aos pontos de dados.
   - **Mínimos Quadrados Alternados (LAD):** minimiza a soma dos desvios absolutos.

3. **Testes Não Paramétricos:**
   - **Teste de Mann-Whitney:** uma alternativa não paramétrica ao teste t de Student.
   - **Teste de Wilcoxon:** um teste não paramétrico para amostras pareadas.

4. **Regressão Quantílica (Quantile Regression):** Analisa a relação entre variáveis independentes e a mediana (ou outros quantis) da variável dependente, sendo menos sensível a outliers.

5. **Bootstrap:** Uma técnica de reamostragem que é menos sensível à presença de outliers.

6. **Métodos de Trimmed Mean:** Calcula a média após remover uma porcentagem fixa dos valores extremos.

7. **Transformações Robustas:** Transformações como a transformação de Tukey, que reduz o impacto de valores extremos.

8. **Métodos de Estimação de Densidade Robusta:** Técnicas como o estimador de densidade robusta de kernel, que é menos sensível a outliers.

É importante observar que a escolha da técnica dependerá da natureza específica dos dados e dos objetivos da análise. Em casos de grandes desvios da normalidade ou presença de outliers, essas técnicas mais robustas podem oferecer resultados mais confiáveis.


#### Métodos não paramétricos

 Os métodos não paramétricos são chamados assim porque não fazem suposições sobre a forma específica da distribuição dos dados. Eles são mais flexíveis e robustos em relação à distribuição dos dados.

Alguns exemplos de métodos não paramétricos incluem:

1. **Teste de Mann-Whitney:** Um teste não paramétrico para comparar duas amostras independentes.
2. **Teste de Wilcoxon:** Um teste não paramétrico para comparar duas amostras pareadas.
3. **Teste de Kruskal-Wallis:** Uma extensão do teste de Mann-Whitney para mais de duas amostras independentes.
4. **Teste de Friedman:** Uma extensão do teste de Wilcoxon para mais de duas amostras pareadas.
5. **Correlação de Spearman:** Uma medida de correlação não paramétrica entre duas variáveis.
6. **Regressão de Theil-Sen:** Uma alternativa robusta à regressão linear.

Esses métodos não dependem da suposição de normalidade dos dados, tornando-os úteis em situações onde essa suposição não é atendida. Além disso, eles são menos sensíveis a outliers do que alguns métodos paramétricos, tornando-os robustos em ambientes com dados mais extremos.


&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>