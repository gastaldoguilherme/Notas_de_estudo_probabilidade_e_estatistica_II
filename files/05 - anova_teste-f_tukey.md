**Python - Estatística II** 
>**Anova_Teste-F_Tukey**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;

## Anova

### Exercício 1:

- Compra de remédio para órgão público (grande quantidade, gastos de milhões);
- 3 opções: remédios comprovadamente eficientes:
- Tempo de cura é muito importante;

- remédio A: R$100,00 
- remédio B: R$120,00
- remédio C: R$130,00 (Cura mais rápida em relação ao remédio A e B)

- o que está variando? (eficácia no medicamento ou efeito nas pessoas?)
- o tempo de tratamento, e o sexo do paciente, podem influenciar para cada pessoa em relação aos 3 medicamentos;
- eficácia do medicamento;
- Não há diferença significativa entre os tempos de cura para os 3 medicamentos



### Solução:

Vamos testar os medicamentos:
- compra-se pequenos lotes de remédio A, B e C;
- aplicamos os 3 medicammentos entre homens e mulheres, totalizando 6 grupos de pacientes;


| Sexo | Remedio | Horas |
|------|---------|-------|
| F    | A       | 5     |
| F    | A       | 10    |
| F    | A       | 7     |
| F    | A       | 7     |
| M    | A       | 7     |
| M    | A       | 6     |
| M    | A       | 9     |
| M    | A       | 9     |
| F    | B       | 5     |
| F    | B       | 5     |
| F    | B       | 5     |
| F    | B       | 8     |
| M    | B       | 7     |
| M    | B       | 8     |
| M    | B       | 10    |
| M    | B       | 7     |
| F    | C       | 10    |
| F    | C       | 10    |
| F    | C       | 6     |
| F    | C       | 6     |
| M    | C       | 10    |
| M    | C       | 6     |
| M    | C       | 10    |
| M    | C       | 5     |

&nbsp;

### Teste de hipótese da ANOVA 

O teste de hipótese da ANOVA (Análise de Variância) é usado quando você tem três ou mais grupos independentes para comparar as médias entre eles. Portanto, a ANOVA é apropriada quando você está lidando com mais de dois grupos.

Para dois grupos, o teste t de Student pode ser mais apropriado. No entanto, se você estiver lidando com três ou mais grupos, a ANOVA pode fornecer informações sobre se há diferenças significativas entre as médias desses grupos.

Em resumo, a regra geral é usar a ANOVA quando você tem três ou mais grupos independentes e o teste t de Student quando tem apenas dois grupos.

```
# Importação das bibliotecas
import pandas as pd
from scipy import stats
import statsmodels.api as sm
from statsmodels.formula.api import ols
from statsmodels.stats.multicomp import MultiComparison
```

```
# Carregamento da base de dados
tratamento = pd.read_csv('anova.csv', sep = ';')
tratamento.head()
```



```
# Carregamento da base de dados
tratamento = pd.read_csv('anova.csv', sep = ';')
tratamento.head()
```


```
# Carregamento da base de dados
tratamento = pd.read_csv('anova.csv', sep = ';')
tratamento.head()
```


### Geramos um gráfico Bloxplot para comparar as horas x remédio
Verificamos como esta a distribuição dos remédios pelo temo

```
# Boxplot agrupando os dados pelo remédio

tratamento.boxplot(by = 'Remedio', grid = False)
```
```
<Axes: title={'center': 'Horas'}, xlabel='[Remedio]'>
```
![Alt text](/assets/05-1.png)

Análise do gráfico:
- a variação entre os 3 boxplot estão entre 5 e 10 horas;
- a mediana do remédio A e B é 7 horas;
- a mediana do remédio C 8 horas;
- os dados do remédio A estão mais centralizados entre 6.5 e 9 horas;
- os dados do remédio B estão mais baixos entre 5 e 8 horas;
- os dados do remédio c estão mais altos entre 6 e 10 horas;

- Conclusão: os tempos são diferentes. 

### As diferenças entre os tempos são Estatísticamente significativas?


```
# Criação do modelo de regressão linear e execução do teste

modelo1 = ols('Horas ~ Remedio', data = tratamento).fit()
resultados1 = sm.stats.anova_lm(modelo1)

# Observar valor de p maior que 0,05 (Pr(>F)) Hipótese nula de que não há diferença significativa

resultados1

```
|         | df  | sum_sq     | mean_sq   | F        | PR(>F)    |
|---------|---- |------------|-----------|----------|----------|
| Remedio | 2.0 | 4.083333   | 2.041667  | 0.537618 | 0.591966 |
| Residual| 21.0| 79.750000  | 3.797619  | NaN      | NaN      |


Conclusão: 

p-value = 0.591966 > Nível de significância (alpha) =0.05

H0: não rejeitar

Hipótese nula: não há diferenças significativas nas médias entre os grupos de remédios



```
# Criação do segundo modelo utilizando mais atributos e execução do teste

modelo2 = ols('Horas ~ Remedio * Sexo', data = tratamento).fit()
resultados2 = sm.stats.anova_lm(modelo2)

#Nenhum valor de P mostra diferença significativa

resultados2
```

|           | df  | sum_sq     | mean_sq   | F        | PR(>F)    |
|-----------|-----|------------|-----------|----------|----------|
| Remedio   | 2.0 | 4.083333   | 2.041667  | 0.532609 | 0.596042 |
| Sexo      | 1.0 | 4.166667   | 4.166667  | 1.086957 | 0.310948 |
| Remedio:Sexo| 2.0| 6.583333   | 3.291667  | 0.858696 | 0.440360 |
| Residual  | 18.0| 69.000000  | 3.833333  | NaN      | NaN      |


#### Conclusão:

A tabela é um resumo dos resultados de uma análise de variância (ANOVA) para um modelo de regressão linear que inclui as variáveis categóricas `Remedio` e `Sexo`, bem como a interação entre essas variáveis. Vamos analisar cada parte da tabela:

1. **Remedio:**
   - **df (graus de liberdade):** 2.0
   - **sum_sq (soma dos quadrados):** 4.083333
   - **mean_sq (média dos quadrados):** 2.041667
   - **F (estatística F):** 0.532609
   - **PR(>F) (valor p):** 0.596042

   Neste caso, a variável `Remedio` não mostra diferença significativa nas médias das horas, já que o valor p (0.596042) é maior que 0.05.

2. **Sexo:**
   - **df (graus de liberdade):** 1.0
   - **sum_sq (soma dos quadrados):** 4.166667
   - **mean_sq (média dos quadrados):** 4.166667
   - **F (estatística F):** 1.086957
   - **PR(>F) (valor p):** 0.310948

   Da mesma forma, a variável `Sexo` não mostra diferença significativa nas médias das horas, pois o valor p (0.310948) é maior que 0.05.

3. **Remedio:Sexo (interação entre Remedio e Sexo):**
   - **df (graus de liberdade):** 2.0
   - **sum_sq (soma dos quadrados):** 6.583333
   - **mean_sq (média dos quadrados):** 3.291667
   - **F (estatística F):** 0.858696
   - **PR(>F) (valor p):** 0.440360

   A interação entre `Remedio` e `Sexo` também não mostra diferença significativa nas médias das horas, pois o valor p (0.440360) é maior que 0.05.

4. **Residual:**
   - **df (graus de liberdade):** 18.0
   - **sum_sq (soma dos quadrados):** 69.000000
   - **mean_sq (média dos quadrados):** 3.833333
   - **F (estatística F):** NaN
   - **PR(>F) (valor p):** NaN

   A última linha representa a variabilidade não explicada pelo modelo (residual). Neste caso, o valor F e o valor p são indefinidos (NaN), pois não há um teste explícito para a variabilidade residual em um modelo de regressão linear.

Em resumo, nenhum dos fatores (Remedio, Sexo, ou a interação entre eles) mostra diferença significativa nas médias das horas, conforme indicado pelos valores p maiores que 0.05. Isso significa que, com base na análise de variância, não há evidências suficientes para rejeitar a hipótese nula de que não há diferenças significativas nas médias das horas entre os diferentes níveis de `Remedio` e `Sexo`.

### Qual medicamento comprar?

Resposta: Remédio A


1. **Diferença nos Preços:**
   - O preço dos medicamentos é diferente: A (R$100,00), B (R$120,00), C (R$130,00).

2. **Influência do Tempo de Cura:**
   - Não há diferença significativa nos tempos de cura entre os três medicamentos.
   - Isso sugere que, estatisticamente, os medicamentos A, B e C têm tempos de cura semelhantes.

3. **Fatores a Considerar na Escolha:**
   - Considerando apenas o tempo de cura e o preço, não há uma diferença estatisticamente significativa.
   - Se a prioridade é a eficácia do tratamento e não há diferença significativa nos tempos de cura, o remédio mais barato (A) pode ser uma escolha econômica.



### Se houver diferença, o teste de Tukey é executado


```

# Execução do teste de Tukey e visualização dos gráficos com os resultados

mc = MultiComparison(tratamento['Horas'], tratamento['Remedio'])

resultado_teste = mc.tukeyhsd()

print(resultado_teste)

```

| group1 | group2 | meandiff | p-adj  | lower  | upper  | reject |
|--------|---------|----------|--------|--------|--------|--------|
| A      | B       | -0.625   | 0.7991 | -3.081 | 1.831  | False  |
| A      | C       | 0.375    | 0.9219 | -2.081 | 2.831  | False  |
| B      | C       | 1.0      | 0.5689 | -1.456 | 3.456  | False  |


Esta tabela é um resultado de um teste de comparação múltipla de médias usando o método de comparação de Tukey. Esse teste é frequentemente utilizado após a realização de uma ANOVA (Análise de Variância) para identificar quais grupos específicos são significativamente diferentes entre si. Vamos explicar cada coluna da tabela:

1. **group1 e group2:**
   - Essas colunas indicam os grupos que estão sendo comparados. Neste caso, A, B e C representam diferentes níveis ou categorias de uma variável.

2. **meandiff (diferença média):**
   - Esta coluna mostra a diferença média estimada entre os grupos comparados. Por exemplo, entre os grupos A e B, a diferença média estimada é -0.625.

3. **p-adj (valor p ajustado):**
   - Este é o valor p ajustado, que leva em consideração o problema da multiplicidade quando você faz várias comparações. Ele ajuda a controlar o erro global de tipo I. Valores p ajustados são usados para determinar se a diferença entre os grupos é estatisticamente significativa. Neste caso, todos os valores p estão acima de 0.05.

4. **lower e upper:**
   - Essas colunas fornecem os limites inferior e superior do intervalo de confiança para a diferença média. No exemplo, para a comparação entre A e B, o intervalo de confiança para a diferença média vai de -3.081 a 1.831.

5. **reject:**
   - Esta coluna indica se a hipótese nula de igualdade das médias é rejeitada ou não. Se "False", não há evidência estatística para rejeitar a hipótese nula, o que significa que não há diferença significativa entre os grupos comparados.

Resumidamente, esta tabela mostra que não há diferenças estatisticamente significativas entre os grupos A, B e C, com base no teste de comparação de Tukey. Isso significa que as médias desses grupos não são estatisticamente diferentes entre si, considerando um nível de significância de 0.05.





&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>