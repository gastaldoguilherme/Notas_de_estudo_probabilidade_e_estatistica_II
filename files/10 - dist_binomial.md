**Python - Estatística II** 
>**Distribuição Binomial**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;


## Distribuição Binomial

A distribuição binomial é um modelo de probabilidade discreta que descreve o número de sucessos em um número fixo de tentativas independentes, cada uma com a mesma probabilidade de sucesso. Aqui estão alguns conceitos-chave e fórmulas associadas à distribuição binomial:

### Principais critérios para o uso da distribuição binomial:



1. **Número Fixo de Tentativas (Ensaio Binomial):**
   - O experimento consiste em um número fixo de tentativas ou ensaios. Cada tentativa é independente das outras.

2. **Resultados Discretos:**
   - Os resultados de cada tentativa são mutuamente exclusivos e discretos, geralmente representados por sucesso ou fracasso, sim ou não, 1 ou 0.

3. **Probabilidade de Sucesso Constante:**
   - A probabilidade de sucesso (ou falha) é constante para cada tentativa. Isso significa que a probabilidade de sucesso, $ p $, não muda de tentativa para tentativa.

4. **Independência das Tentativas:**
   - Cada tentativa é independente das outras. O resultado de uma tentativa não afeta o resultado das outras tentativas.

5. **Número Fixo de Categorias (Dois Resultados Possíveis):**
   - Cada tentativa tem apenas dois resultados possíveis, geralmente rotulados como "sucesso" e "fracasso" (ou 1 e 0).

6. **Probabilidade do Complemento:**
   - A probabilidade de falha ($1 - p$) é facilmente calculada a partir da probabilidade de sucesso ($p$), e vice-versa.

7. **Ordem dos Resultados Não Importa:**
   - A ordem em que os resultados são observados não é relevante.

8. **Repetição do Experimento:**
   - O experimento é repetido um número fixo de vezes sob condições idênticas.



### Fórmulas Principais:

1. **Função de Probabilidade (PMF):**

   $ P(X = k) = \displaystyle\binom{n}{k} \cdot p^k \cdot (1 - p)^{n - k} $
   - **Variáveis:**
     - $ X $: Número de sucessos
     - $ n $: Número total de tentativas
     - $ k $: Número específico de sucessos desejados
     - $ p $: Probabilidade de sucesso em uma única tentativa
   - **Descrição:**
     - A PMF fornece a probabilidade de obter exatamente $ k $ sucessos em $ n $ tentativas.



2. **Função de Distribuição Cumulativa (CDF):**

   $ P(X \leq k) = \displaystyle\sum_{i=0}^{k} \displaystyle\binom{n}{i} \cdot p^i \cdot (1 - p)^{n - i} $
   - **Variáveis:**
     - $ X $: Número de sucessos
     - $ n $: Número total de tentativas
     - $ k $: Número de sucessos desejados
     - $ p $: Probabilidade de sucesso em uma única tentativa
   - **Descrição:**
     - A CDF fornece a probabilidade de obter no máximo $ k $ sucessos em $ n $ tentativas.



3. **Coeficiente binomial $\displaystyle\binom{n}{k}$**

Coeficiente binomial e é lido como "n escolha k". Representa o número de maneiras diferentes de escolher $ k $ elementos de um conjunto de $ n $ elementos. A fórmula é dada por:

   $\displaystyle\binom{n}{k} = \displaystyle\frac{n!}{k!(n-k)!} $

   onde $ n! $ (lê-se "n fatorial") é o produto de todos os números inteiros de 1 a $ n $. Isso leva em consideração as diferentes maneiras de escolher $ k $ sucessos em $ n $ tentativas, sem levar em conta a ordem em que ocorrem.




### Média da Distribuição Binomial:

A média ($ \mu $) de uma distribuição binomial é o número esperado de sucessos em $ n $ ensaios independentes. Matematicamente, é dado por:

$ \mu = n \cdot p $

onde:
- $ n $ é o número de ensaios (número de tentativas),
- $ p $ é a probabilidade de sucesso em cada ensaio.

A média fornece uma medida de centralidade na distribuição binomial, indicando o valor médio que se espera observar ao realizar o experimento várias vezes.

### Variância e Desvio Padrão da Distribuição Binomial:

A variância ($ \sigma^2 $) e o desvio padrão ($ \sigma $) são medidas de dispersão que indicam quão longe os valores da distribuição estão da média.

$ \sigma^2 = n \cdot p \cdot (1 - p) $

$ \sigma = \sqrt{n \cdot p \cdot (1 - p)} $

onde:
- $ n $ é o número de ensaios,
- $ p $ é a probabilidade de sucesso.

A variância é o quadrado do desvio padrão. Ambos os valores aumentam à medida que a probabilidade de sucesso ($ p $) se afasta de 0,5. Quando $ p = 0,5 $, a distribuição é mais dispersa, e quando $ p $ se afasta de 0,5, a distribuição fica mais concentrada em torno da média.

Essas medidas são cruciais para entender a forma e a dispersão da distribuição binomial, sendo particularmente úteis em prever resultados e avaliar a consistência dos dados em experimentos onde o número de ensaios é fixo e os ensaios são independentes.


### Testes de Hipótese:

1. **Teste de Hipótese para uma Proporção ($ p $):**

   $ Z = \displaystyle\frac{\hat{p} - p_0}{\displaystyle\sqrt{\frac{p_0 \cdot (1 - p_0)}{n}}} $
   
   - **Variáveis:**
     - $ \hat{p} $: Proporção amostral de sucessos
     - $ p_0 $: Valor sob a hipótese nula
     - $ n $: Número total de tentativas
   - **Descrição:**
     - Usado para testar hipóteses sobre a proporção de sucessos em um experimento binomial.


---

### Exercícios:


### 1) Peças defeituosas: Probabilidade e Valor Esperado

Num determinado processo de fabricação, 10% das peças são consideradas defeituosas. As peças são acondicionadas em caixas com 5 unidades cada uma. Então:

a) Qual a probabilidade de haver exatamente 3 peças defeituosas numa caixa?

b) Qual a probabilidade de haver duas ou mais peças defeituosas numa caixa?

c) Se a empresa paga uma multa de R$10,00 por caixa em que houver alguma peça defeituosa, qual o valor esperado da multa num total de 1000 caixas?


Para resolver essas questões, podemos usar a distribuição de probabilidade binomial, já que cada peça pode ser considerada defeituosa ou não, e estamos interessados no número total de peças defeituosas em uma caixa.

A fórmula para a distribuição binomial é dada por:

$ P(X = k) = \displaystyle\binom{n}{k} \cdot p^k \cdot (1 - p)^{n - k} $

onde:
- $ n $ é o número total de ensaios (número de peças na caixa),
- $ k $ é o número de eventos desejados (número de peças defeituosas),
- $ p $ é a probabilidade de um evento (probabilidade de uma peça ser defeituosa),
- $ (1 - p) $ é a probabilidade do evento oposto (probabilidade de uma peça não ser defeituosa).

Vamos calcular cada parte:

a) Probabilidade de exatamente 3 peças defeituosas em uma caixa:

$ P(X = 3) = \binom{5}{3} \cdot (0.10)^3 \cdot (0.90)^2 $

```
Probabilidade de exatamente 3 peças defeituosas: 0.0081

```

![Alt text](/assets/10-1.png)


b) Probabilidade de duas ou mais peças defeituosas em uma caixa:

$ P(X < 2) = P(X = 0) + P(X = 1)$

$ P(X \geq 2) = P(X = 2) + P(X = 3) + P(X = 4) + P(X = 5) $

$ 1 - P(X < 2) = 1- 0.9185 = 0,0815 $

```
Probabilidade de duas ou mais peças defeituosas: 0.0815

```

![Alt text](/assets/10-2.png)



c) Valor esperado da multa em 1000 caixas:

$ \text{Valor Esperado} = \text{Probabilidade de peça defeituosa em uma caixa} \times \text{Multa por caixa} \times \text{Número total de caixas} $

$ \text{Valor Esperado} =$ 0,3281 x R$10,00 x 1000 = R$3.281,00

```
Valor esperado da multa em 1000 caixas: R$3280.50

```

![Alt text](/assets/10-3.png)



```python
from math import comb

def probabilidade_defeituosas(k, n, p):
    return comb(n, k) * (p ** k) * ((1 - p) ** (n - k))

# a) Probabilidade de exatamente 3 peças defeituosas em uma caixa

probabilidade_3_defeituosas = probabilidade_defeituosas(3, 5, 0.10)
print(f"a) Probabilidade de exatamente 3 peças defeituosas: {probabilidade_3_defeituosas:.4f}")

# b) Probabilidade de duas ou mais peças defeituosas em uma caixa
probabilidade_2_ou_mais_defeituosas = sum(probabilidade_defeituosas(k, 5, 0.10) for k in range(2, 6))
print(f"b) Probabilidade de duas ou mais peças defeituosas: {probabilidade_2_ou_mais_defeituosas:.4f}")

# c) Valor esperado da multa em 1000 caixas
multa_por_caixa = 10.00
numero_total_caixas = 1000
valor_esperado_multa = probabilidade_defeituosas(1, 5, 0.10) * multa_por_caixa * numero_total_caixas
print(f"c) Valor esperado da multa em 1000 caixas: R${valor_esperado_multa:.2f}")
```
```

a) Probabilidade de exatamente 3 peças defeituosas: 0.0081
b) Probabilidade de duas ou mais peças defeituosas: 0.0815
c) Valor esperado da multa em 1000 caixas: R$3280.50
```


### 2) Reação nociva, resultante da injeção de um determinado soro:



Se a probabilidade de um certo gado sofrer uma dada reação nociva, resultante da injeção de um determinado soro, é 0,001. Determinar a probabilidade de, entre 2.000 animais:

**a) Exatamente 3 sofrerem aquela reação;**

A probabilidade de exatamente 3 animais sofrerem a reação pode ser calculada utilizando a fórmula da distribuição binomial:

$ P(X = 3) = \binom{2000}{3} \cdot (0,001)^3 \cdot (1 - 0,001)^{2000 - 3} $

Substituindo os valores:

$ P(X = 3) = \binom{2000}{3} \cdot (0,001)^3 \cdot (0,999)^{1997} $

**Resultado:**

$ P(X = 3) \approx 0.180537 $

**b) Mais do que 2 sofrerem aquela reação;**

A probabilidade de mais do que 2 animais sofrerem a reação pode ser calculada somando as probabilidades para $ k = 3, 4, \ldots, 2000 $:

$ P(X > 2) = P(X = 3) + P(X = 4) + \ldots + P(X = 2000) $

**Resultado:**

$ P(X > 2) \approx 0.323324 $

```
from math import comb

# Função para calcular a probabilidade binomial
def probabilidade_binomial(n, k, p):
    return comb(n, k) * (p ** k) * ((1 - p) ** (n - k))

# a) Probabilidade de exatamente 3 animais sofrerem a reação
prob_3 = probabilidade_binomial(2000, 3, 0.001)
print(f"a) Probabilidade de exatamente 3 animais sofrerem a reação: {prob_3:.6f}")

# b) Probabilidade de mais do que 2 animais sofrerem a reação
prob_mais_que_2 = sum(probabilidade_binomial(2000, k, 0.001) for k in range(3, 100))
print(f"b) Probabilidade de mais do que 2 animais sofrerem a reação: {prob_mais_que_2:.6f}")

```

```
a) Probabilidade de exatamente 3 animais sofrerem a reação: 0.180537
b) Probabilidade de mais do que 2 animais sofrerem a reação: 0.323324

```

### 3) Doença em bovinos


Uma certa doença em bovinos pode ser curada por meio de procedimentos cirúrgicos em 50% dos casos. Dentre os que possuem essa doença, sorteamos 4 bovinos que serão submetidos à cirurgia. Fazendo alguma suposição adicional, que julgar necessária, responda:

**a) Variável em Estudo (X)**

Considerando a Distribuição de Probabilidades, a variável em estudo (X) representa o número de bovinos curados entre os 4 submetidos à cirurgia. A distribuição é apresentada na tabela abaixo:

| X | P(X=x)        |
|---|---------------|
| 0 | 0.0625000     |
| 1 | 0.2500000     |
| 2 | 0.3750000     |
| 3 | 0.2500000     |
| 4 | 0.0625000     |


![Alt text](/assets/10-4.JPG)


Justificativa: A variável X representa o número de sucessos em uma sequência de ensaios independentes (cura ou não cura), o que sugere uma distribuição binomial.

**b) Probabilidade de Todos Serem Curados**

A probabilidade de todos serem curados (X = 4) é dada por $ P(X = 4) = 0.06250003 $.

**c) Probabilidade de ao Menos Dois Não Serem Curados**

A probabilidade de ao menos dois não serem curados (X ≥ 2) é dada por:

 $ P(X \geq 2) = P(X = 2) + P(X = 3) + P(X = 4) $.

$ P(X < 2) = P(X = 0) + P(X = 1) $

$ P(X \geq 2) = 1 - P(X < 2) = $ 1 - 0.3125 = 0.6875

![Alt text](/assets/10-5.png)



**d) Número Esperado e Desvio Padrão**

O número esperado de animais curados:

  $ \mu = n \cdot p = 4 \cdot 0.5 = 2 $ animais. 
 
 O desvio padrão ($ \sigma $) é calculado como:
 
  $ \sigma = \sqrt{n \cdot p \cdot (1 - p)}  =  \sqrt{4 \cdot 0.5 \cdot (1 - 0.5)} =  1.00 $.



```
from math import comb, sqrt

# Função para calcular a probabilidade binomial
def probabilidade_binomial(n, k, p):
    return comb(n, k) * (p ** k) * ((1 - p) ** (n - k))

# a. Distribuição de Probabilidades
n = 4
p = 0.50

# Cálculos para a distribuição de probabilidades
probabilidades = [probabilidade_binomial(n, k, p) for k in range(n + 1)]

print("a. Distribuição de Probabilidades:")
print("X\tP(X=x)")
for k, prob in enumerate(probabilidades):
    print(f"{k}\t{prob:.7f}")

# b. Probabilidade de todos serem curados (X = 4)
prob_todos_curados = probabilidades[4]
print(f"\nb. Probabilidade de todos serem curados: {prob_todos_curados:.7f}")

# c. Probabilidade de ao menos dois não serem curados (X ≥ 2)
prob_ao_menos_dois_nao_curados = sum(probabilidades[2:])
print(f"\nc. Probabilidade de ao menos dois não serem curados: {prob_ao_menos_dois_nao_curados:.7f}")

# d. Número esperado de animais curados (μ) e Desvio padrão (σ)
mu = n * p
sigma_squared = n * p * (1 - p)
sigma = sqrt(sigma_squared)

print(f"\nd. Número esperado de animais curados (μ): {mu:.2f}")
print(f"   Desvio padrão (σ): {sigma:.2f}")

```

```
a. Distribuição de Probabilidades:
X	P(X=x)
0	0.0625000
1	0.2500000
2	0.3750000
3	0.2500000
4	0.0625000

b. Probabilidade de todos serem curados: 0.0625000

c. Probabilidade de ao menos dois não serem curados: 0.6875000

d. Número esperado de animais curados (μ): 2.00
   Desvio padrão (σ): 1.00

```
**e ) Nova Variável: Y**

Caso fossem feitas, agora, 8 cirurgias e observássemos que 2 foram curados,
quais seriam as possíveis conclusões a serem tomadas para esse experimento?
(Nova Variável: Y) 



Para avaliar as possíveis conclusões para esse experimento, onde foram realizadas 8 cirurgias e 2 animais foram curados, podemos realizar um teste de hipótese com a distribuição binomial. Vamos formular as hipóteses:

**Hipótese Nula ($H_0$):** A taxa de sucesso (probabilidade de cura) é igual a $p_0$.

**Hipótese Alternativa ($H_1$):** A taxa de sucesso é diferente de $p_0$.

Vamos definir os parâmetros do teste:

- $n = 8$ (número total de cirurgias)
- $k = 2$ (número de cirurgias bem-sucedidas)
- $p_0= 0.5$ (é a taxa de sucesso sob a hipótese nula) 

Vamos realizar o teste de hipótese e interpretar os resultados:

```python
import scipy.stats as stats

# Parâmetros
n = 8
k = 2
p_0 = 0.5  

# Teste de hipótese
result = stats.binomtest(k, n, p_0)

# Tomada de decisão
alpha = 0.05  # Nível de significância
if result.pvalue < alpha:
    print(f"Rejeitar a hipótese nula. p-value: {result.pvalue}")
else:
    print(f"Falha em rejeitar a hipótese nula. p-value: {result.pvalue}")
```

```
Falha em rejeitar a hipótese nula. p-value: 0.2890625

```


- Valor-p: 0.2891 (aproximadamente)


### Conclusão 1:

- $ \text{Valor-p} > \alpha $

Se o valor-p (p-value) associado ao teste de hipótese for 0.2890625, isso significa que a probabilidade de observar 2 sucessos em 8 cirurgias, assumindo uma taxa de sucesso de $p_0 = 0.5$, é relativamente alta.

Nesse contexto:

- **Valor-p Alto:** A probabilidade de obter os resultados observados (ou resultados mais extremos) sob a hipótese nula é alta. Isso sugere que os resultados não são estatisticamente significativos, e falhamos em rejeitar a hipótese nula.

- **Conclusão:** Não temos evidências suficientes para concluir que a taxa de sucesso é diferente de $p_0 = 0.5$ com base nos resultados observados. Em outras palavras, os dados não fornecem suporte estatístico para a ideia de que a taxa de cura é significativamente diferente da taxa assumida na hipótese nula.

Portanto, com um valor-p de 0.2890625, não rejeitamos a hipótese nula a um nível de significância padrão de 0.05 (ou qualquer outro nível de significância usual). Isso significa que, com base nos dados disponíveis, não temos razão para concluir que a taxa de cura é diferente da taxa assumida na hipótese nula.


### Conclusão 2:

Caso o valor-p fosse menor que $\alpha $
- $ Valor-p < \alpha $
- $p_0= 0.75$ (é a taxa de sucesso sob a hipótese nula) 
- Hipótese Nula ($H_0$): A taxa de sucesso (probabilidade de cura) é igual a $p_0$.
- Valor-p: 0.00423 (aproximadamente)

```
Rejeitar a hipótese nula. p-value: 0.0042266845703125

```



Nesse caso, como o valor-p é menor que o nível de significância ($ \alpha = 0.05 $), podemos rejeitar a hipótese nula ($ H_0 $) em favor da hipótese alternativa ($ H_1 $). Isso indica que a taxa de sucesso observada é significativamente diferente de 0.75.

Portanto, podemos concluir que, com base nos dados observados, há evidências estatísticas para suportar a ideia de que a taxa de sucesso é diferente de 0.75. O valor-p indica quão improvável seria observar os dados que você tem, sob a suposição de que a taxa de sucesso é realmente 0.75.

Lembre-se sempre de considerar o contexto específico do problema e a interpretação do valor-p, juntamente com a análise do tamanho da amostra e outras considerações relevantes.










































&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>