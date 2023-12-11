**Python - Estatística II** 
>**Teste do Qui-Quadrado**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;

## Teste do Qui-Quadrado

O teste do Qui-Quadrado é uma técnica estatística utilizada para avaliar se existe uma diferença significativa entre as frequências observadas e as frequências esperadas em um conjunto de dados categorizados. Aqui estão alguns conceitos-chave e fórmulas associadas ao teste do Qui-Quadrado:

### Fórmulas Principais:

1. **Estatística do Qui-Quadrado ($X^2$):**

   $X^2 =\displaystyle \sum \frac{(O_i - E_i)^2}{E_i}$

   - **Variáveis:**
     - $O_i$: Frequência observada em cada categoria
     - $E_i$: Frequência esperada em cada categoria (calculada com base em uma distribuição ou modelo)
   - **Descrição:**
     - Calcula a diferença entre as frequências observadas e esperadas, ponderada pelo inverso da expectativa.

2. **Graus de Liberdade ($df$):**

   $df = (\text{Número de categorias} - 1)$
   - **Variáveis:**
     - $\text{Número de categorias}$: Número de categorias ou grupos no conjunto de dados
   - **Descrição:**
     - Indica o número de graus de liberdade associados ao teste.

### Testes de Hipótese:

1. **Teste de Independência (Qui-Quadrado de Independência):**
2. 
   - **Hipóteses:**
     - $H_0$: As variáveis são independentes.
     - $H_1$: Há uma associação entre as variáveis.
     - 
   - **Estatística de Teste:**

     $X^2 = \sum \frac{(O_i - E_i)^2}{E_i}$
     
   - **Graus de Liberdade:**

     $df = (\text{Número de linhas} - 1) \times (\text{Número de colunas} - 1)$

3. **Teste de Adequação (Qui-Quadrado de Adequação):**

   - **Hipóteses:**
     - $H_0$: Os dados seguem a distribuição especificada.
     - $H_1$: Os dados não seguem a distribuição especificada.

   - **Estatística de Teste:**

     $X^2 = \sum \frac{(O_i - E_i)^2}{E_i}$


   - **Graus de Liberdade:**
   
     $df = (\text{Número de categorias ou grupos} - \text{Número de parâmetros estimados})$

### Quando Usar o Teste do Qui-Quadrado:

1. **Dados Categóricos:**
   - Quando os dados podem ser organizados em categorias ou grupos.

2. **Associação ou Independência:**
   - Para testar se há uma associação entre duas variáveis categóricas (Qui-Quadrado de Independência).

3. **Adequação a uma Distribuição:**
   - Para testar se os dados seguem uma distribuição de probabilidade específica (Qui-Quadrado de Adequação).

O teste do Qui-Quadrado é uma ferramenta versátil usada em várias áreas, incluindo pesquisa de mercado, biologia, ciências sociais e epidemiologia, para avaliar se há uma relação significativa entre variáveis categóricas ou se os dados seguem uma distribuição esperada.



### Exercício 1:

Deseja-se verificar, a um nível de 5% de significância, se o comportamento aleatório expresso pelo número de termostatos vendidos por uma indústria mensalmente segue uma distribuição normal com média 250 e desvio padrão 50. Para isso, a amostra de 65 observações relativas à demanda mensal de termostatos é dada abaixo.

158 222 248 216 226 239 206 178 169 177 290 245 318 158 274 255 191 244 149 195 247 233 156 203 182 272 256 184 299 246 184 224 316 285 251 248 222 135 337 235 225 282 302 391 261 315 231 231 263 177 270 169 172 243 278 283 200 324 266 214 240 239 224 262 200

### Solução:

#### Organizando a lista em ordem crescente:

```
# Lista de números
numeros = [158, 222, 248, 216, 226, 239, 206, 178, 169, 177, 290, 245, 318, 158, 274, 255, 191, 244, 149, 195, 247, 233, 156, 203,
           182, 272, 256, 184, 299, 246, 184, 224, 316, 285, 251, 248, 222, 135, 337, 235, 225, 282, 302, 391, 261, 315, 231, 231,
           263, 177, 270, 169, 172, 243, 278, 283, 200, 324, 266, 214, 240, 239, 224, 262, 200]

# Organizando a lista em ordem crescente
numeros_ordenados = sorted(numeros)

# Exibindo a lista ordenada
print(numeros_ordenados)

```

```
[135, 149, 156, 158, 158, 169, 169, 172, 177, 177, 178, 182, 184, 184, 191, 195, 200, 200, 203, 206, 214, 216, 222, 222, 224, 224, 225, 226, 231, 231, 233, 235, 239, 239, 240, 243, 244, 245, 246, 247, 248, 248, 251, 255, 256, 261, 262, 263, 266, 270, 272, 274, 278, 282, 283, 285, 290, 299, 302, 315, 316, 318, 324, 337, 391]

```

- Número de intervalos (Regra de Sturges)

$k = 1 + 3.31 \log_{10} n$   

$k = 1 + 3.31 \log_{10} 65 \approx 7$

- Amplitude de cada intervalo:

$h = \displaystyle \frac{A}{k} = \frac{x(n) - x(1)}{k} = \displaystyle \frac{391 - 135}{7} \approx 36.57$


- Construindo a tabela de frequências

| INTERVALO            | AMPLITUDE              |
|----------------------|------------------------|
| 1                    | $\text{min}(x)$ - $\text{min}(x) + h$   |
| 2                    | $\text{min}(x) + h$ - $\text{min}(x) + 2h$ |
| 3                    | $\text{min}(x) + 2h$ - $\text{min}(x) + 3h$|
| 4                    | $\text{min}(x) + 3h$ - $\text{min}(x) + 4h$|
| 5                    | $\text{min}(x) + 4h$ - $\text{min}(x) + 5h$|
| 6                    | $\text{min}(x) + 5h$ - $\text{min}(x) + 6h$|
| 7                    | $\geq \text{min}(x) + 6h$                    |



- Construindo a tabela de frequências

| INTERVALO | AMPLITUDE               |
|-----------|-------------------------|
| 1         | 135.00 - 171.57         |
| 2         | 171.57 - 208.14         |
| 3         | 208.14 - 244.71         |
| 4         | 244.71 - 281.28         |
| 5         | 281.28 - 317.85         |
| 6         | 317.85 - 354.42         |
| 7         | $\geq$ 354.42       |


### Calculo da probabilidade para cada intervalo:



Vamos calcular os valores numéricos usando $\mu_0 = 250$ e $\sigma_0 = 50$. 

1. **Intervalo 1 (135.00 a 171.57):**
$p_1 = P(135 < X < 171.57) = P\left(\frac{135 - 250}{50} < Z < \frac{171.57 - 250}{50}\right)$ 

$p_1 = P(z) = 0.0476$

2. **Intervalo 2 (171.57 a 208.14):**
$p_2 = P(171.57 < X < 208.14) = P\left(\frac{171.57 - 250}{50} < Z < \frac{208.14 - 250}{50}\right)$

$p_2 = P(z) = 0.1429$

3. **Intervalo 3 (208.14 a 244.71):**
$p_3 = P(208.14 < X < 244.71) = P\left(\frac{208.14 - 250}{50} < Z < \frac{244.71 - 250}{50}\right)$

$p_3 = P(z) = 0.2566$

4. **Intervalo 4 (244.71 a 281.28):**
$p_4 = P(244.71 < X < 281.28) = P\left(\frac{244.71 - 250}{50} < Z < \frac{281.28 - 250}{50}\right)$

$p_4 = P(z) = 0.2763$

5. **Intervalo 5 (281.28 a 317.85):**
$p_5 = P(281.28 < X < 317.85) = P\left(\frac{281.28 - 250}{50} < Z < \frac{317.85 - 250}{50}\right)$

$p_5 = P(z) = 0.17846$

6. **Intervalo 6 (317.85 a 354.42):**
$p_6 = P(317.85 < X < 354.42) = P\left(\frac{317.85 - 250}{50} < Z < \frac{354.42 - 250}{50}\right)$

$p_6 = P(z) = 0.0690$

7. **Intervalo 7 ($ \geq 354.42$):**
$p_7 = P(X \geq 354.42) = P(Z \geq \frac{354.42 - 250}{50})$

$p_7 = P(z) = 0.0184$


```python
from scipy.stats import norm

# Parâmetros da distribuição normal
media = 250
desvio_padrao = 50

# Limites dos intervalos
limites = [(135, 171.57), (171.57, 208.14), (208.14, 244.71), (244.71, 281.28), (281.28, 317.85), (317.85, 354.42), (354.42, float('inf'))]

# Calculando p para cada intervalo
for i, (limite_inf, limite_sup) in enumerate(limites):
    z_inf = (limite_inf - media) / desvio_padrao
    z_sup = (limite_sup - media) / desvio_padrao
    p_intervalo = norm.cdf(z_sup) - norm.cdf(z_inf)
    print(f"p{i+1} para o intervalo {i+1}: {p_intervalo:.4f}")

# Calculando p(Z >= 354.42)
z_7 = (354.42 - media) / desvio_padrao
p_7 = 1 - norm.cdf(z_7)
print(f"p7 para o intervalo 7: {p_7:.4f}")
```

```
p1 para o intervalo 1: 0.0476
p2 para o intervalo 2: 0.1429
p3 para o intervalo 3: 0.2566
p4 para o intervalo 4: 0.2763
p5 para o intervalo 5: 0.1784
p6 para o intervalo 6: 0.0690
p7 para o intervalo 7: 0.0184
p7 para o intervalo 7: 0.0184

```

### Construindo a tabela de frequências com valores esperados - Ei = n × pi


| Ii | AMPLITUDE          | Oi | pi   | Ei = n × pi |
|----|--------------------|----|------|-------------|
| 1  | 135.00 - 171.57    | 7  | 0.05 | 3.25        |
| 2  | 171.57 - 208.14    | 13 | 0.14 | 9.10        |
| 3  | 208.14 - 244.71    | 17 | 0.26 | 16.90       |
| 4  | 244.71 - 281.28    | 16 | 0.28 | 18.20       |
| 5  | 281.28 - 317.85    | 8  | 0.18 | 11.70       |
| 6  | 317.85 - 354.42    | 3  | 0.07 | 4.55        |
| 7  | ≥ 354.42           | 1  | 0.02 | 1.30        |
| **SOMA** | -           | 65 | 1    | 65          |



### Estatística de Teste:


1. **Intervalo 1 (135.00 a 171.57):**
   
$Q_1 = \frac{(7 - 3.25)^2}{3.25} \approx 4,32692307692308$

3. **Intervalo 2 (171.57 a 208.14):**
   
$Q_2 = \frac{(13 - 9.10)^2}{9.10} \approx 1,67142857142857$

5. **Intervalo 3 (208.14 a 244.71):**
   
$Q_3 = \frac{(17 - 16.90)^2}{16.90} \approx 0,000591715976331378$

7. **Intervalo 4 (244.71 a 281.28):**
   
$Q_4 = \frac{(16 - 18.20)^2}{18.20} \approx 0,265934065934066$

9. **Intervalo 5 (281.28 a 317.85):**
    
$Q_5 = \frac{(8 - 11.70)^2}{11.70} \approx 1,17008547008547$

11. **Intervalo 6 (317.85 a 354.42):**
    
$Q_6 = \frac{(3 - 4.55)^2}{4.55} \approx 0,528021978021978$

13. **Intervalo 7 ($ \geq 354.42$):**
    
$Q_7 = \displaystyle \frac{(1 - 1.3)^2}{1.3} \approx 0,0692307692307692$

Somando todos os $Q_i$:

$Q = Q_1 + Q_2 + Q_3 + Q_4 + Q_5 + Q_6 + Q_7 \approx 8.03$

$X^2 = \sum \frac{(O_i - E_i)^2}{E_i} \approx 8.03$


```
import numpy as np

# Dados fornecidos
intervalos = [
    (135.00, 171.57),
    (171.57, 208.14),
    (208.14, 244.71),
    (244.71, 281.28),
    (281.28, 317.85),
    (317.85, 354.42),
    (354.42, float('inf'))
]

Oi = [7, 13, 17, 16, 8, 3, 1]
pi = [0.05, 0.14, 0.26, 0.28, 0.18, 0.07, 0.02]
Ei = [65 * p for p in pi]

# Cálculo dos Qi
Qi = [(oi - ei)**2 / ei for oi, ei in zip(Oi, Ei)]

# Cálculo do Q
Q = np.sum(Qi)

print("Qi:", Qi)
print("Q:", Q)


```

```
Qi: [4.326923076923077, 1.67142857142857, 0.0005917159763313356, 0.26593406593406654, 1.1700854700854697, 0.5280219780219784, 0.06923076923076925]
Q: 8.032215647600262

```


### Tabela - Distribuição Qui-Quadrado 


![Alt text](/assets/12-1.png)


### Conclusão:


$H_0: \text{A demanda mensal de termostatos segue uma distribuição normal com média } \mu = 250 \text{ e desvio padrão } \sigma = 50$

Como $Q$ < $\huge\chi^2_{6;(0.05)}$, ou seja, $8.03 < 12.59$, não rejeitamos $H_0$ à 5% de significância. A demanda mensal de termostatos possui, estatisticamente, uma distribuição normal com média 250 e desvio padrão 50.


Neste trecho, $\chi^2_{\huge 6;(0.05)}$ representa a estatística de teste do qui-quadrado com 6 graus de liberdade a um nível de significância de 5%. O valor crítico é 12.59, e como o valor calculado $Q$ (8.03) é menor do que o valor crítico, não há evidências para rejeitar a hipótese nula $H_0$.


```
from scipy.stats import chi2

# Valor crítico do qui-quadrado para 6 graus de liberdade a 5% de significância
valor_critico = chi2.ppf(0.95, 6)

# Valor calculado Q
Q_calculado = 8.03

# Conclusão
if Q_calculado < valor_critico:
    conclusao = "Não rejeitamos H0 à 5% de significância. A demanda mensal de termostatos possui, estatisticamente, uma distribuição normal com média 250 e desvio padrão 50."
else:
    conclusao = "Rejeitamos H0 à 5% de significância. Não há evidências estatísticas de que a demanda mensal de termostatos siga uma distribuição normal com média 250 e desvio padrão 50."

print("Conclusão:", conclusao)

```

```
Conclusão: Não rejeitamos H0 à 5% de significância. A demanda mensal de termostatos possui, estatisticamente, uma distribuição normal com média 250 e desvio padrão 50.
```


### usando outro método: Teste de Shapiro-Wilk

Para verificar se a amostra segue uma distribuição normal, você pode usar o teste de Shapiro-Wilk. 



#### Teste de Shapiro-Wilk:

```python
from scipy.stats import shapiro

# Amostra de dados
amostra = [158, 222, 248, 216, 226, 239, 206, 178, 169, 177, 290, 245, 318, 158, 274, 255, 191, 244, 149, 195,
           247, 233, 156, 203, 182, 272, 256, 184, 299, 246, 184, 224, 316, 285, 251, 248, 222, 135, 337, 235,
           225, 282, 302, 391, 261, 315, 231, 231, 263, 177, 270, 169, 172, 243, 278, 283, 200, 324, 266, 214,
           240, 239, 224, 262, 200]

# Teste de Shapiro-Wilk
stat, p_value = shapiro(amostra)

# Conclusão do teste
alpha = 0.05
if p_value > alpha:
    conclusao = "A amostra parece ser normal (não rejeitamos H0)"
else:
    conclusao = "A amostra não parece ser normal (rejeitamos H0)"

# Exibindo resultados
print(f"Teste de Shapiro-Wilk: Estatística = {stat}, p-valor = {p_value}")
print(conclusao)
```


``` 
Teste de Shapiro-Wilk: Estatística = 0.9839334487915039, p-valor = 0.5611811876296997
A amostra parece ser normal (não rejeitamos H0)

```


### Exercício 2:


**Enunciado do Exercício: Teste Qui-Quadrado para Independência em Dados de Assistência à TV Aberta**

Um pesquisador deseja investigar se existe uma relação significativa entre o gênero (masculino ou feminino) e a preferência por assistir à televisão aberta. Para isso, ele coletou dados sobre a observação de 100 pessoas (62 masculinos e 38 femininos) e registrou se cada pessoa assiste ou não à televisão aberta.


$H_0: \text{Não há diferença significativa entre as frequências observadas e esperadas.}$

Isso significa que, se o teste qui-quadrado não rejeitar a hipótese nula, não teremos evidências estatísticas para afirmar que existe uma diferença significativa entre as frequências observadas e esperadas. Em outras palavras, os dados se encaixam bem com as expectativas teóricas, e qualquer diferença observada pode ser devida ao acaso.


A tabela abaixo resume os dados observados e esperados:


|         | Assiste     | Não Assiste  | Proporção|
|---------|-------------|--------------|----------|
| Obs_M   | 19          | 6            | 25%
| Esp_M   | -           | -            |
| Obs_F   | 43          | 32           | 75%
| Esp_F   | -           | -            |
| Total   | 62          | 38           | 100%





Onde:
- `Obs_M`: Número observado de homens que assistem à televisão aberta.
- `Esp_M`: Número esperado de homens que não assistem à televisão aberta.
- `Obs_F`: Número observado de mulheres que assistem à televisão aberta.
- `Esp_F`: Número esperado de mulheres que não assistem à televisão aberta.

Utilizando um teste qui-quadrado para independência, com um nível de significância de 95%, determine se há uma associação significativa entre o gênero e a preferência por assistir à televisão aberta. Apresente a tabela observada, a tabela esperada, a estatística de teste e a conclusão do teste.


#### Solução:


#### 1° Modo de solução em Python:

```
from scipy.stats import chi2

# Dados observados
obs_assiste11m = 19
obs_assiste21f = 43
obs_n_assiste12m = 6
obs_n_assiste22f = 32


total_assiste = 62
total_n_assiste = 38

# Proporções esperadas
prop_m = 0.25
prop_f = 0.75

# Dados esperados
esp_assiste11m = total_assiste * prop_m
esp_assiste21f = total_assiste  * prop_f
esp_n_assiste12m = total_n_assiste * prop_m
esp_n_assiste22f = total_n_assiste * prop_f


# Cálculo da estatística de teste Q
Q = (((obs_assiste11m - esp_assiste11m)**2) / (esp_assiste11m)) +\
    (((obs_assiste21f - esp_assiste21f)**2) / (esp_assiste21f)) +\
    (((obs_n_assiste12m - esp_n_assiste12m)**2) / (esp_n_assiste12m)) +\
    (((obs_n_assiste22f - esp_n_assiste22f)**2) / (esp_n_assiste22f)) 


# Graus de liberdade
graus_liberdade = 1

# Valor crítico
valor_critico = chi2.ppf(0.95, graus_liberdade)

# Comparação com o valor crítico
resultado = "Rejeitar H0" if Q > valor_critico else "Não rejeitar H0"

Q, valor_critico, resultado

```
```
(2.77306168647425, 3.841458820694124, 'Não rejeitar H0')

```




#### 2° Modo de solução em Python:

```
import pandas as pd

# Dados observados
obs_assiste11m = 19
obs_assiste21f = 43
obs_n_assiste12m = 6
obs_n_assiste22f = 32

total_assiste = 62
total_n_assiste = 38
total = 100

# Proporções esperadas
prop_m = 0.25
prop_f = 0.75

# Dados esperados
esp_assiste11m = total_assiste * prop_m
esp_assiste21f = total_assiste * prop_f
esp_n_assiste12m = total_n_assiste * prop_m
esp_n_assiste22f = total_n_assiste * prop_f

data = {
    'Assiste': [obs_assiste11m, esp_assiste11m, obs_assiste21f, esp_assiste21f],
    'Não Assiste': [obs_n_assiste12m, esp_n_assiste12m, obs_n_assiste22f, esp_n_assiste22f],
    'Proporção': [((obs_assiste11m + obs_n_assiste12m )/ total), ((esp_assiste11m  + esp_n_assiste12m )/ total),
                  ((obs_assiste21f + obs_n_assiste22f )/ total), ((esp_assiste21f  + esp_n_assiste22f )/ total)]
}

index = ['Obs_M', 'Esp_M', 'Obs_F', 'Esp_F']


df = pd.DataFrame(data, index=index)

# Cálculo da estatística de teste Q
Q = (((df.loc['Obs_M', 'Assiste'] - df.loc['Esp_M', 'Assiste'])**2) / df.loc['Esp_M', 'Assiste'] +
     ((df.loc['Obs_F', 'Assiste'] - df.loc['Esp_F', 'Assiste'])**2) / df.loc['Esp_F', 'Assiste'] +
     ((df.loc['Obs_M', 'Não Assiste'] - df.loc['Esp_M', 'Não Assiste'])**2) / df.loc['Esp_M', 'Não Assiste'] +
     ((df.loc['Obs_F', 'Não Assiste'] - df.loc['Esp_F', 'Não Assiste'])**2) / df.loc['Esp_F', 'Não Assiste'])

# Graus de liberdade
graus_liberdade = 1

# Valor crítico
valor_critico = chi2.ppf(0.95, graus_liberdade)

# Comparação com o valor crítico
resultado = "Rejeitar H0" if Q > valor_critico else "Não rejeitar H0"

df, Q, valor_critico, resultado

```
```
(       Assiste  Não Assiste  Proporção
 Obs_M     19.0          6.0       0.25
 Esp_M     15.5          9.5       0.25
 Obs_F     43.0         32.0       0.75
 Esp_F     46.5         28.5       0.75,
 2.77306168647425,
 3.841458820694124,
 'Não rejeitar H0')

```

#### Tabela Qui-Quadrado:


![Alt text](/assets/12-2.png)



#### Resposta:

Com base nos resultados apresentados:


A interpretação é que, com um nível de significância de 5%, não há evidências estatísticas suficientes para rejeitar a hipótese nula ($H_0$), indicando que não há diferença significativa entre as frequências observadas e esperadas. Portanto, os dados não fornecem suporte estatístico para concluir que há uma discrepância significativa entre as observações e as expectativas teóricas.




&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>
