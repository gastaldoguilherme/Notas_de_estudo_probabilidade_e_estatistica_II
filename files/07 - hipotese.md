**Python - Estatística II** 
>**Teste de Hipótese**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;



### Teste de Hipótese

Um teste de hipótese é uma abordagem estatística utilizada para tomar decisões sobre afirmações ou hipóteses em relação a uma população com base em dados amostrais. Existem dois tipos principais de hipóteses em um teste de hipóteses:

1. **Hipótese Nula ($H_0$):**
   - Afirmação inicial ou hipótese que assume que não há efeito, diferença ou relação significativa. É geralmente a hipótese a ser testada.

2. **Hipótese Alternativa ($H_1$ ou $H_a$):**
   - Afirmação que contradiz a hipótese nula, sugerindo que há um efeito, diferença ou relação significativa.



### Teste de Hipótese - Etapas


O processo geral de um teste de hipótese envolve as seguintes etapas:

### 1. Formulação das Hipóteses:

- **Hipótese Nula ($H_0$):** Não há efeito observável; a situação é como esperada ou não há diferença.
- **Hipótese Alternativa ($H_1$ ou $H_a$):** Há um efeito observável; existe uma diferença.

### 2. Escolha do Nível de Significância ($\alpha$):

- O nível de significância ($\alpha$) é a probabilidade de cometer um erro tipo I (rejeitar erroneamente a hipótese nula quando ela é verdadeira). Valores comuns são 0,05, 0,01 ou 0,10.

### 3. Coleta de Dados e Cálculo da Estatística de Teste:

- Com base nos dados amostrais, calcula-se uma estatística de teste, como o valor-z ou o valor-t, dependendo da distribuição e do tipo de teste.

### 4. Tomada de Decisão:

- Compara-se o valor da estatística de teste com o valor crítico ou p-valor associado ao nível de significância escolhido.
- Se o valor de p for menor que $\alpha$, rejeita-se a hipótese nula em favor da hipótese alternativa. Caso contrário, não há evidência suficiente para rejeitar a hipótese nula.

### 5. Conclusões e Interpretação:

- Com base na decisão tomada, fazem-se conclusões sobre a presença ou ausência de efeitos significativos na população.

Existem vários tipos de testes de hipóteses, incluindo testes para média, proporção, diferença entre médias, correlação, entre outros. A escolha do teste depende da natureza dos dados e das questões específicas sendo investigadas.



### Níveis de significância 


Os níveis de significância são valores que determinam quão improvável um resultado deve ser para que possamos rejeitar a hipótese nula em um teste estatístico. Geralmente, são representados por $\alpha$ e indicam a probabilidade de cometer um erro do Tipo I (rejeitar erroneamente a hipótese nula quando é verdadeira).

Aqui estão as etapas básicas para calcular os níveis de significância:

1. **Defina a Hipótese Nula ($H_0$) e a Hipótese Alternativa ($H_1$):**
   - $H_0$: Declaração de igualdade ou ausência de efeito.
   - $H_1$: Declaração de diferença, efeito, ou relação.

2. **Escolha o Nível de Significância ($\alpha$):**
   - O nível de significância é o limiar que você define para determinar se os resultados são estatisticamente significativos. Um valor comum é $\alpha = 0,05$, mas pode variar dependendo do contexto.

3. **Escolha a Distribuição de Probabilidade e a Estatística de Teste:**
   - Dependendo do tipo de teste estatístico (por exemplo, teste Z, teste t, qui-quadrado), você escolherá a distribuição de probabilidade apropriada.

4. **Calcule a Estatística de Teste:**
   - Com base nos dados da amostra, calcule a estatística de teste apropriada para o seu teste estatístico específico.

5. **Determine a Região Crítica ou Valor Crítico:**
   - A região crítica é a área da distribuição de probabilidade em que você rejeitará a hipótese nula se a estatística de teste cair dentro dessa região. Para alguns testes, você pode usar valores críticos específicos.

6. **Calcule o P-Valor:**
   - Se você está usando o p-valor para tomar decisões, calcule o p-valor associado à sua estatística de teste. O p-valor é a probabilidade de obter uma estatística de teste tão extrema ou mais extrema do que a observada, sob a hipótese nula.

7. **Tome uma Decisão:**
   - Compare a estatística de teste com a região crítica ou compare o p-valor com o nível de significância ($\alpha$). Se a estatística de teste estiver na região crítica ou o p-valor for menor que $\alpha$, rejeite a hipótese nula.

Lembre-se de que a escolha do nível de significância ($\alpha$) é crucial e deve ser feita considerando o contexto específico do problema e as implicações práticas das decisões baseadas nos resultados do teste. O valor comum de $\alpha = 0,05$ implica uma probabilidade de 5% de cometer um erro do Tipo I. Escolher um $\alpha$ menor reduz a probabilidade de cometer um erro do Tipo I, mas aumenta a probabilidade de cometer um erro do Tipo II.


### Alpha ($\alpha$) e beta ($\beta$)


Alpha ($\alpha$) e beta ($\beta$) são termos associados a testes de hipóteses estatísticas e são usados para descrever os dois tipos de erros que podem ocorrer durante um teste.

1. **Alpha ($\alpha$):**
   - O alpha é o nível de significância do teste estatístico.
   - Representa a probabilidade de cometer um erro do Tipo I, ou seja, rejeitar erroneamente a hipótese nula quando ela é verdadeira.
   - O valor típico escolhido para $\alpha$ é 0,05, o que significa que há uma probabilidade de 5% de cometer um erro do Tipo I.

2. **Beta ($\beta$):**
   - O beta é a probabilidade de cometer um erro do Tipo II.
   - Representa a probabilidade de não rejeitar a hipótese nula quando ela é falsa.

---
### Exemplo 1:

**Exercício: Teste de Hipótese para Média de Salários de Vendedores**

Suponha que um novo pesquisador esteja interessado no salário médio de Vendedores e colete novamente dados de uma amostra de 100 profissionais. A análise inicial indica que a média amostral é de R$7.000,00, e o desvio padrão amostral é de R$1.100,00.

Dado que o desvio padrão populacional é conhecido e é de R$1.100,00, realize um teste de hipótese para determinar se há evidências para suportar a alegação de que o salário médio dos Vendedores é diferente de R$5.800,00, com um nível de confiança de 95%.

**Dados:**
- Tamanho da amostra ($n$): 100 pesquisados
- Intervalo de Confiança ($IC$): 95%
- Desvio Padrão Populacional ($\sigma$): R$1.100,00
- Média Amostral ($\bar{x}$): R$7.000,00
- Hipótese Nula ($H_0$): $ \mu = 5.800 $
- Hipótese Alternativa ($H_1$): $ \mu \neq 5.800 $
- Nível de Significância ($\alpha$): 0.05

**Perguntas:**
1. Formule as hipóteses nula e alternativa para este teste.
2. Calcule a estatística de teste Z.
3. Determine o p-valor associado ao teste.
4. Com base no p-valor e no nível de significância escolhido, decida se rejeita ou não a hipótese nula.
5. Interprete o resultado em termos do problema original.


**Solução:**

```

from scipy.stats import norm

# Dados do problema
media_amostral = 7000
media_hipotese_nula = 5800
desvio_padrao = 1100
tamanho_amostra = 100
nivel_significancia = 0.05  # Escolha o nível de significância desejado

# Calculando o teste Z
z_score = (media_amostral - media_hipotese_nula) / (desvio_padrao / (tamanho_amostra ** 0.5))

# Calculando o p-valor
p_valor = norm.sf(z_score)  

# Imprimindo os resultados
print(f"Teste Z: {z_score}")
print(f"P-valor: {p_valor}")

# Comparando o p-valor com o nível de significância
if p_valor < nivel_significancia:
    print("Rejeitar a hipótese nula")
else:
    print("Não rejeitar a hipótese nula")

```


```
Teste Z: 10.909090909090908
P-valor: 5.214703332852256e-28
Rejeitar a hipótese nula

```


**1. Hipóteses:**

$ H_0: \mu = 5.800 $
$ H_1: \mu \neq 5.800 $

**2. Estatística de Teste Z:**

$ Z = \displaystyle \frac{\bar{x} - \mu_0}{\frac{\sigma}{\sqrt{n}}} $

Substituindo os valores conhecidos:

$ Z = \frac{7.000 - 5.800}{\frac{1.100}{\sqrt{100}}} $
$ Z = \frac{1.200}{110} $
$ Z \approx 10,91 $

**3. P-valor:**

### Estatística de Teste: Z = 10,91

$ p\text{-valor} = P(|10,91|) > 5.214703332852256e-28 $  

$ p\text{-valor} = 5.214703332852256e-28$


**4. Decisão:**

Comparando o $ p\text{-valor} = (5.214703332852256e-28) $ com o nível de significância ($\alpha = 0.05$):

$ p\text{-valor} > \alpha $

Portanto, REJEITAMOS a hipótese nula.



**5. Interpretação:**
Com base nos dados da amostra, há evidências estatísticas para afirmar que o salário médio dos Vendedores é diferente de R$5.800,00. O p-valor muito baixo sugere que a diferença observada na média salarial não pode ser explicada apenas por variações aleatórias e é estatisticamente significativa.


### Exercício 2:

Vamos realizar um teste de hipótese para verificar se a média amostral de peso de crianças de 6 anos, conforme observada pelo médico, é significativamente diferente da média afirmada pelos estudos.

**Hipóteses:**
- $H_0: \mu = 22$ (A média do estudo é correta)
- $H_1: \mu \neq 22$ (A média observada pelo médico é significativamente diferente)

**Dados:**
- Tamanho da amostra ($n$): 100
- Média amostral ($\bar{x}$): 23
- Desvio padrão amostral ($s$): 4
- Nível de significância ($\alpha$): 0,05

**Estatística de Teste ( Z ):**
$ Z = \displaystyle \frac{\bar{x} - \mu_0}{\frac{s}{\sqrt{n}}} $

Vamos calcular o valor crítico e o p-valor para tomar uma decisão.

```python

import scipy.stats as stats

# Dados do problema
n = 100
x_barra = 23
s = 4
media_estudo = 22
nivel_significancia = 0.05

# Estatística de Teste Z
z_score = (x_barra - media_estudo) / (s / (n ** 0.5))

# Valor Crítico para um teste bilateral
valor_critico = 2 * (stats.norm.sf(abs(1.96)))

# P-valor para um teste bilateral
p_valor = 2 * (1 - stats.norm.cdf(abs(z_score)))

# Decisão
if abs(z_score) > valor_critico:
    decisao = "Rejeitar H0"
else:
    decisao = "Não rejeitar H0"

# Resultados
print(f'Estatística de Teste Z: {z_score}')
print(f'P-valor  ou p(z_score): {p_valor}')
print(f'Valor Crítico Z =1,96 ~ p(z)= 0,05: {valor_critico}')
print(f'Decisão: {decisao}')
```

```
Estatística de Teste Z: 2.5
P-valor  ou p(z_score): 0.012419330651552318
Valor Crítico Z =1,96 ~ p(z)= 0,05: 0.04999579029644087
Decisão: Rejeitar H0

```


**Resultado:**
- Estatística de Teste Z: 2.5
- Valor Crítico Z (para $\alpha = 0.05$): $\pm1.96$ (aproximadamente)
- P-valor: 0.0122 (aproximadamente)
- Decisão: Rejeitar $H_0$ (pois $|2.5| > 1.96$)

**Interpretação:**
Com base nos resultados do teste, a estatística de teste Z é significativamente maior que o valor crítico, e o p-valor é maior que o nível de significância ($\alpha$). Portanto, rejeitamos a hipótese nula. Há evidências estatísticas para concluir que a média observada pelo médico é significativamente diferente da média afirmada pelos estudos.

---


### Exemplo 3:

**Exercício: Teste de Significância para a Proporção de Apoio ao Candidato A**

Suponha que uma pesquisa inicial tenha sido realizada para uma eleição de candidatos, com os seguintes resultados:

- Tamanho da amostra ($n$): 1000 pesquisados
- Candidato A: 650 votos
- Candidato B: 330 votos
- Não sabem: 20 votos

A pesquisa inicial indicou que a proporção de apoio ao Candidato A foi de $ \displaystyle \frac{650}{1000} = 0,65 $.

No entanto, o Candidato B, desconfiado, refaz a pesquisa e descobre que a verdadeira proporção de votos para o Candidato A é de 0,67.

Vamos realizar um teste de significância para avaliar se a diferença entre a proporção observada e a proporção alegada pelo Candidato B é estatisticamente significativa com um nível de significância de $ \alpha = 0,05 $.

**Solução:**

**1. Hipóteses:**
- Hipótese Nula ($H_0$): A proporção de apoio ao Candidato A é igual a 0,65.
- Hipótese Alternativa ($H_1$): A proporção de apoio ao Candidato A é diferente de 0,65.

$H_0: p = 0,65 $
$H_1: p \neq 0,65 $

**2. Estatística de Teste:**

$Z = \displaystyle \frac{\hat{p} - p_0}{\sqrt{\frac{p_0 \cdot (1 - p_0)}{n}}} $

Substituindo os valores conhecidos:
$Z = \displaystyle \frac{0,67 - 0,65}{\sqrt{\frac{0,65 \cdot (1 - 0,65)}{1000}}} $


**3. P-valor:**

### Estatística de Teste: Z = 1,3260

$ p\text{-valor} = P(|1,3260|) > 1,8152 $  

$ p\text{-valor} = 1.8152$


**4. Decisão:**

Comparando o $ p\text{-valor} = (1.8152) $ com o nível de significância ($\alpha = 0.05$):

$ p\text{-valor} > \alpha $

Portanto, NÃO rejeitamos a hipótese nula.


```
from scipy.stats import norm
import numpy as np

# Dados do problema
proporcao_observada = 0.67
proporcao_alegada = 0.65
tamanho_amostra = 1000

# Estatística de teste Z
z_score = (proporcao_observada - proporcao_alegada) / np.sqrt((proporcao_alegada * (1 - proporcao_alegada)) / tamanho_amostra)

# P-valor
p_valor = 2 * norm.cdf(z_score)  # Multiplicado por 2 para um teste bilateral

# Imprimir resultados
print(f"Estatística de Teste Z: {z_score}")
print(f"P-valor: {p_valor}")

# Decisão
nivel_significancia = 0.05
if p_valor < nivel_significancia:
    decisao = "Rejeitar H0"
else:
    decisao = "Não rejeitar H0"

print(f"Decisão: {decisao}")

```

```
Estatística de Teste Z: 1.325987088263593
P-valor: 1.815156025772466
Decisão: Não rejeitar H0

```

### Conclusão:


A estatística de teste Z calculada é 1.325987088263593, e como seu valor absoluto é maior do que o valor crítico Z de ±1.96, não rejeitamos a hipótese nula ($H_0$). Isso sugere que, com um nível de significância de 0,05, não há evidências estatísticas suficientes para afirmar que a proporção real de apoio ao Candidato A difere significativamente da proporção alegada pelo Candidato B.
 Portanto, não há suporte estatístico para a alegação do Candidato B de que algo estava errado com a pesquisa inicial.




### Exemplo 4:

**Exercício: Intervalo de Confiança para a Proporção e Teste de Hipótese**

**Contexto:**
Suponha que você esteja conduzindo uma pesquisa sobre a preferência de métodos de pagamento online entre os consumidores. Deseja-se estimar a proporção de consumidores que preferem usar cartão de crédito. Além disso, você tem interesse em testar a hipótese de que mais de 60% dos consumidores preferem cartão de crédito.

**Dados:**
- Tamanho da amostra ($n$): 1000
- Proporção observada ($\hat{p}$): 0.65 (65% dos entrevistados preferem cartão de crédito)
- Nível de confiança ($IC$): 95%

**Parte 1: Intervalo de Confiança para a Proporção**

1. **Hipóteses:**
   - $H_0: p = 0.60$ (A proporção é igual a 60%)
   - $H_1: p > 0.60$ (A proporção é maior que 60%)

2. **Intervalo de Confiança:**
   - Utilize a fórmula do intervalo de confiança para a proporção:

     $ \text{Intervalo} = \hat{p} \pm Z \times \sqrt{\displaystyle \frac{\hat{p} \times (1 - \hat{p})}{n}} $
   - Calcule os limites inferior e superior do intervalo de confiança.

```python
import scipy.stats as stats
import math

# Dados do problema
n = 1000
proporcao_observada = 0.65
nivel_confianca = 0.95

# Z-score para um intervalo de confiança de 95%
z_score = stats.norm.ppf(1 - (1 - nivel_confianca) / 2)

# Intervalo de Confiança
erro_padrao = math.sqrt((proporcao_observada * (1 - proporcao_observada)) / n)
intervalo_inferior = proporcao_observada - z_score * erro_padrao
intervalo_superior = proporcao_observada + z_score * erro_padrao

# Resultados
print(f'Intervalo de Confiança: ({intervalo_inferior:.4f}, {intervalo_superior:.4f})')
```
```
Intervalo de Confiança: (0.6204, 0.6796)
```






**Parte 2: Teste de Hipótese**

1. **Estatística de Teste Z:**
   - Utilize a fórmula para a estatística de teste Z para proporções:
     $ Z =\displaystyle \frac{\hat{p} - p_0}{\sqrt{\frac{p_0 \times (1 - p_0)}{n}}} $
   - $p_0$ é a proporção sob a hipótese nula.

```python
# Hipóteses do teste
proporcao_nula = 0.60

# Estatística de Teste Z
z_teste = (proporcao_observada - proporcao_nula) / math.sqrt((proporcao_nula * (1 - proporcao_nula)) / n)

# P-valor para um teste unilateral à direita
p_valor_teste = 1 - stats.norm.cdf(z_teste)

# Resultados
print(f'Estatística de Teste Z: {z_teste:.4f}')
print(f'P-valor do Teste: {p_valor_teste:.4f}')
```

```
Estatística de Teste Z: 3.2275
P-valor do Teste: 0.0006
```



**Interpretação dos Resultados do Teste de Hipótese:**

1. **Estatística de Teste Z: 3.2275**
   - A estatística de teste Z é 3.2275, o que indica que a diferença entre a proporção observada ($\hat{p} = 0.65$) e a proporção sob a hipótese nula ($p_0 = 0.60$) é 3.2275 vezes o erro padrão.

2. **P-valor do Teste: 0.0006**
   - O p-valor é 0.0006, que é menor que o nível de significância $\alpha = 0.05$.
   - Como o p-valor é menor que $\alpha$, rejeitamos a hipótese nula.

**Conclusão:**
Com base nos resultados do teste de hipótese, há evidências estatísticas para concluir que a proporção de consumidores que preferem cartão de crédito é significativamente maior que 60%. O p-valor baixo sugere que a diferença observada na preferência de pagamento não pode ser atribuída apenas ao acaso, fornecendo suporte à hipótese alternativa de que mais de 60% dos consumidores preferem cartão de crédito.




























&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>