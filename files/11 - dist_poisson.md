**Python - Estatística II** 
>**Distribuição de Poisson**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;

## Distribuição de Poisson

A distribuição de Poisson é um modelo de probabilidade discreta que descreve o número de eventos raros que ocorrem em um intervalo fixo de tempo ou espaço. Aqui estão alguns conceitos-chave e fórmulas associadas à distribuição de Poisson:



### Principais critérios para o uso da distribuição de Poisson


1. **Número Fixo de Eventos:**
   - A distribuição de Poisson é aplicável quando estamos interessados no número de eventos que ocorrem em um intervalo fixo de tempo ou espaço. O número total de eventos, $n$, deve ser fixo.

2. **Eventos Independentes:**
   - Os eventos devem ser independentes uns dos outros, o que significa que a ocorrência de um evento não influencia a ocorrência de outro. Isso é um requisito fundamental para aplicar a distribuição de Poisson.

3. **Taxa Média de Ocorrência Constante:**
   - A taxa média de ocorrência de eventos, $\lambda$, deve ser constante ao longo do tempo ou espaço. A taxa $\lambda$ representa o número médio de eventos em um intervalo unitário (um segundo, um metro, etc.).

4. **Probabilidade de Ocorrência Constante:**
   - A probabilidade de mais de um evento ocorrer em um intervalo extremamente curto deve ser praticamente zero. Isso implica que a taxa de ocorrência $\lambda$ deve ser baixa.

5. **Eventos Mutuamente Exclusivos:**
   - A distribuição de Poisson é apropriada quando a ocorrência de dois ou mais eventos no mesmo intervalo é praticamente impossível (eventos mutuamente exclusivos).

6. **Eventos Contáveis e Discretos:**
   - A distribuição de Poisson é mais apropriada para eventos contáveis e discretos, como o número de telefonemas recebidos em uma central telefônica em uma hora ou o número de acidentes em um cruzamento em um dia.

7. **Amostra Aleatória:**
   - Os eventos devem ser observados em uma amostra aleatória, o que significa que a probabilidade de observar um evento é a mesma em todas as partes do intervalo de interesse.



### Fórmulas Principais:

1. **Função de Probabilidade (PMF):**

   $P(X = k) = \displaystyle\frac{e^{-\lambda} \cdot \lambda^k}{k!}$
   - **Variáveis:**
     - $X$: Número de eventos raros
     - $k$: Número específico de eventos desejados
     - $\lambda$: Taxa média de ocorrência de eventos por unidade de tempo ou espaço
   - **Descrição:**
     - A PMF fornece a probabilidade de ocorrer exatamente $k$ eventos raros em um intervalo específico.

2. **Função de Distribuição Cumulativa (CDF):**

   $P(X \leq k) = \displaystyle\sum_{i=0}^{k} \frac{e^{-\lambda} \cdot \lambda^i}{i!}$
   - **Variáveis:**
     - $X$: Número de eventos raros
     - $k$: Número de eventos desejados
     - $\lambda$: Taxa média de ocorrência de eventos por unidade de tempo ou espaço
   - **Descrição:**
     - A CDF fornece a probabilidade de ocorrer no máximo $k$ eventos raros em um intervalo específico.

### Testes de Hipótese:

1. **Teste de Ajuste para a Distribuição de Poisson:**

   $X^2 = \displaystyle\sum_{i=1}^{k} \frac{(O_i - E_i)^2}{E_i}$
   
   - **Variáveis:**
     - $O_i$: Frequência observada de eventos em uma categoria específica
     - $E_i$: Frequência esperada de eventos em uma categoria específica (calculada usando a distribuição de Poisson)
   - **Descrição:**
     - Usado para testar se a distribuição observada de eventos raros se ajusta à distribuição de Poisson esperada.

### Exercício 1:

O número de vezes que um indivíduo tem gripe em determinado ano é uma
variável aleatória de Poisson com λ = 5. Suponha que um novo medicamento reduza
o parâmetro λ para 3 em 75% da população. Para os 25% restantes a droga não tem
um efeito significativo. Se um indivíduo toma o medicamento durante um ano e tem
duas gripes, qual a probabilidade de que o medicamento seja benéfico para ele ?

Com base nesse resultado, se o indivíduo soubesse essa probabilidade a
priori, você acha que ele deveria continuar tomando o medicamento?

**SOLUÇÃO:**

Sejam os eventos:
- G2: indivíduo tem duas gripes no ano
- M: Medicamento é benéfico para ele (a)
- Mc: Medicamento não é benéfico para ele (a)

E sejam as variáveis aleatórias:
- T: Indivíduo tem duas gripes no ano quando o medicamento é benéfico para ele.
- N: Indivíduo tem duas gripes no ano quando o medicamento não é benéfico para ele.

$T \sim \text{P}(3)$

$N \sim \text{P}(5)$

Queremos saber $P(M|G2):$ Probabilidade condicional do medicamento ser benéfico para um indivíduo que tomou o medicamento durante um ano, dado que ele teve duas gripes no ano?


Vamos calcular a probabilidade condicional $P(M|G2)$, que representa a probabilidade de o medicamento ser benéfico dado que o indivíduo teve duas gripes no ano.

Usaremos o Teorema de Bayes para isso:

$\huge P(M|G2) = \frac{P(G2|M) \cdot P(M)}{P(G2)}$

Podemos calcular cada uma das probabilidades no numerador e denominador usando as informações dadas:

1. $P(G2|M)$ = $T \sim \text{P}(3)$: A probabilidade de ter duas gripes dado que o medicamento é benéfico. Podemos usar a distribuição de Poisson com $\lambda = 3$ para isso.

$P(G2|M) = \displaystyle\frac{e^{-3} \cdot 3^2}{2!} = 0.2240$


![Alt text](/assets/11-1.png)




2. $P(M)$: A probabilidade de o medicamento ser benéfico. Isso corresponde a 75% da população, então $ P(M) = 0.75$.


3. $P(G2|M_c)$ = $N \sim \text{P}(5)$ é a probabilidade de ter duas gripes dado que o medicamento não é benéfico. Podemos usar a distribuição de Poisson com $\lambda = 5$ para isso.

$P(G2|M_c) = \displaystyle\frac{e^{-5} \cdot 5^2}{2!} = 0.0842$


![Alt text](/assets/11-2.png)





4. $P(M_c)$ é a probabilidade de o medicamento não ser benéfico, ou seja, 25% da população, então $P(M_c) = 0.25$.


5. $P(G2)$: A probabilidade marginal de ter duas gripes. Podemos usar a lei da probabilidade total:

$P(G2) = P(G2|M) \cdot P(M) + P(G2|M_c) \cdot P(M_c)$


### Resolvendo a expressão:


$\huge P(G2) = \frac{e^{-3} \cdot 3^2}{2!} \cdot 0.75 + \frac{e^{-5} \cdot 5^2}{2!} \cdot 0.25$

#### Primeiro, vamos calcular cada parte separadamente.

Para a primeira parte:

$\huge \frac{e^{-3} \cdot 3^2}{2!} \cdot 0.75$

Calculando $e^{-3}$ ou $\displaystyle \frac{1}{e^{3}}$

$e^{-3} \approx 0.04979$

Agora, substituímos isso de volta na expressão:

$\huge \frac{0.04979 \cdot 3^2}{2!} \cdot 0.75$


$0.16766$

#### Agora, para a segunda parte:

$\huge\frac{e^{-5} \cdot 5^2}{2!} \cdot 0.25$

Calculando $e^{-5}$ ou $ \displaystyle \frac{1}{e^{5}}$

$e^{-5} \approx 0.00674$

Substituindo de volta na expressão:

$\huge\frac{0.00674 \cdot 5^2}{2!} \cdot 0.25$


$0.02106$

#### Agora, somamos as duas partes:

$0.16766 + 0.02106 = 0.18872$

$P(G2) = \huge \frac{e^{-3} \cdot 3^2}{2!} \cdot 0.75 + \frac{e^{-5} \cdot 5^2}{2!} \cdot 0.25 = 0.18872$



#### Usaremos o Teorema de Bayes para isso:

$P(M|G2) = \displaystyle \frac{P(G2|M) \cdot P(M)}{P(G2)}$

$P(G2|M) = \displaystyle\frac{e^{-3} \cdot 3^2}{2!}$

$P(M) = 0.75$

$P(G2) = 0.18872$

$P(M|G2) = 0.8886$

#### Conclusão:

A probabilidade condicional $P(M|G2)$ foi calculada como 0.8886, isso significa que, dado o fato de que o indivíduo teve duas gripes, a probabilidade de o medicamento ser benéfico para ele é bastante alta.

Na prática, uma probabilidade próxima de 1 sugere forte evidência de que o medicamento é benéfico para o indivíduo que teve duas gripes. Com base nesse resultado, o indivíduo pode considerar continuar tomando o medicamento, pois a probabilidade de benefício é alta.

```
import math

# Função para calcular a probabilidade de uma distribuição de Poisson
def poisson_probability(k, lambd):
    return (math.exp(-lambd) * lambd**k) / math.factorial(k)

# Dados do problema
lambd_M = 3  # parâmetro lambda quando o medicamento é benéfico
lambd_Mc = 5  # parâmetro lambda quando o medicamento não é benéfico
P_M = 0.75  # probabilidade de o medicamento ser benéfico
P_Mc = 0.25  # probabilidade de o medicamento não ser benéfico

# Probabilidade de ter duas gripes dado que o medicamento é benéfico
P_G2_M = poisson_probability(2, lambd_M)

# Probabilidade de ter duas gripes dado que o medicamento não é benéfico
P_G2_Mc = poisson_probability(2, lambd_Mc)

# Probabilidade marginal de ter duas gripes
P_G2 = P_G2_M * P_M + P_G2_Mc * P_Mc

# Aplicação do Teorema de Bayes para calcular a probabilidade condicional
P_M_G2 = (P_G2_M * P_M) / P_G2

# Exibindo os resultados
print(f"A probabilidade de o medicamento ser benéfico dado que o indivíduo teve duas gripes é: {P_M_G2:.4f}")

```

```

A probabilidade de o medicamento ser benéfico dado que o indivíduo teve duas gripes é: 0.8886

```


### Exercício 2:

Suponha que $X_t$, o número de partículas emitidas em $t$ horas por uma fonte radioativa, tenha uma distribuição de Poisson com parâmetro $20t$. Qual será a probabilidade de que exatamente 5 partículas sejam emitidas durante um período de 15 minutos?


A distribuição de Poisson é frequentemente usada para modelar a probabilidade de um número de eventos ocorrer em um intervalo fixo de tempo ou espaço. A função de probabilidade de Poisson é dada por:

$P(X = k) = \displaystyle\frac{e^{-\lambda} \cdot \lambda^k}{k!}$

onde $X$ é a variável aleatória representando o número de eventos, $k$ é o número específico de eventos que estamos interessados, e $\lambda$ é o parâmetro da distribuição.

No seu caso, a variável aleatória $X_t$, o número de partículas emitidas em $t$ horas, segue uma distribuição de Poisson com parâmetro $\lambda = 20t$. Como você está interessado no número de partículas emitidas durante um período de 15 minutos ($t = \frac{1}{4}$ horas), o parâmetro é $\lambda = 20 \times \frac{1}{4} = 5$.

Agora, a probabilidade de exatamente 5 partículas serem emitidas durante esse período de 15 minutos é dada pela fórmula de Poisson:

$P(X_{1/4} = 5) = \displaystyle\frac{e^{-5} \cdot 5^5}{5!}$

Vamos calcular isso:

$P(X_{1/4} = 5) = \displaystyle\frac{e^{-5} \cdot 3125}{120}$

$P(X_{1/4} = 5) \approx 0.175467$

Portanto, a probabilidade de exatamente 5 partículas serem emitidas durante um período de 15 minutos é aproximadamente 0.175467, ou 17.55%.

![Alt text](/assets/11-3.png)



```

from scipy.stats import poisson

# Parâmetro da distribuição de Poisson
lmbda = 20 * (1/4)  # Convertendo 15 minutos para horas

# Número de partículas desejado
k = 5

# Calculando a probabilidade usando a distribuição de Poisson
probabilidade = poisson.pmf(k, lmbda)

print(f"A probabilidade de exatamente {k} partículas serem emitidas em 15 minutos é: {probabilidade:.4f}")


```

```
A probabilidade de exatamente 5 partículas serem emitidas em 15 minutos é: 0.1755


```


### Exercício 3:

Uma indústria de tintas recebe pedidos de seus vendedores através de fax, telefone e internet. A taxa média é de 5 pedidos por hora.

**a) Probabilidade de receber mais de dois pedidos por hora:**
Qual seria a probabilidade da indústria receber mais de dois pedidos por hora?
Digamos que, no horário do almoço, a indústria fica impossibilitada de atender a mais de dois pedidos por hora. Você acha que deveria aumentar o número de atendentes nesse período?

**b) Probabilidade de haver 50 pedidos em um Dia de Trabalho:**
Em um dia de trabalho (8 horas), qual seria a probabilidade de haver 50 pedidos?
A indústria deveria aumentar o número de atendentes para receber mais de 50 pedidos por dia?

&nbsp;

#### Solução:

**a) Probabilidade de receber mais de dois pedidos por hora:**

Neste caso, a situação pode ser modelada usando a distribuição de Poisson, onde a variável aleatória é o número de pedidos por hora, e o parâmetro $ \lambda $ (lambda) é a taxa média de pedidos por hora.

Dado que a taxa média é de 5 pedidos por hora, temos $\lambda = 5$.

A probabilidade de receber exatamente $ k $ pedidos em uma hora é dada pela fórmula da distribuição de Poisson:

$P(X = k) = \displaystyle \frac{e^{-\lambda} \cdot \lambda^k}{k!}$

Agora, a probabilidade de receber mais de dois pedidos por hora $P(X > 2)$ pode ser calculada somando as probabilidades para $k = 3, 4, 5, \ldots$. 

$P(X > 2) = P(X = 3) + P(X = 4) + P(X = 5) ...$

$P(X <= 2) = P(X = 0) + P(X = 1) + P(X = 2) = 0.1247$

![Alt text](/assets/11-4.png)

$P(X > 2) = 1- P(X < = 2) = 1 - 0.1247 = 0.8753$


&nbsp;

**b) Probabilidade de haver 50 pedidos em um Dia de Trabalho:**



Dada a Situação:
- Taxa média de pedidos por hora ($\lambda$): 5
- Número de horas em um dia de trabalho: 8
- Número desejado de pedidos ($k$): 50

Calcular a Taxa Média Diária ($\lambda_{\text{dia}}$):
$\huge \lambda_{\text{dia}} = \lambda \times \text{número de horas}$

$\huge \lambda_{\text{dia}} = 5 \times 8 = 40$

Agora, temos a taxa média diária ($\lambda_{\text{dia}}$).

Usar a Distribuição de Poisson para Calcular a Probabilidade 

$P(X = 50)$:

$P(X = k) = \huge\frac{e^{\displaystyle -\lambda_{\text{dia}}} \cdot \lambda_{\text{dia}}^k}{k!}$

$P(X = 50) = \huge\frac{e^{-40} \cdot 40^{50}}{50!}$

Podemos calcular isso numericamente usando Python ou outras ferramentas, mas aqui vou fornecer o resultado:

$P(X = 50) \approx 0.0177$

Interpretar o Resultado:
A probabilidade de haver exatamente 50 pedidos em um dia de trabalho é muito baixa, indicando que é uma ocorrência extremamente rara. Portanto, com base nesta probabilidade, a indústria provavelmente não precisaria aumentar o número de atendentes para lidar com essa situação específica.



Vamos calcular isso em Python:


```python
from scipy.stats import poisson

# Taxa média de pedidos por hora
lambda_value = 5

# Probabilidade de receber mais de dois pedidos por hora
prob_less_than_2 = poisson.cdf(2, lambda_value)
prob_more_than_2 = 1 - prob_less_than_2

print(f"A probabilidade de receber mais de dois pedidos por hora é: {prob_more_than_2:.4f}")

# Número de horas em um dia de trabalho
horas_por_dia = 8

# Número desejado de pedidos
k = 50

# Lambda para um dia de trabalho
lambda_dia = lambda_value * horas_por_dia

# Probabilidade de haver 50 pedidos em um dia de trabalho
prob_50_pedidos = poisson.pmf(k, lambda_dia)

print(f"A probabilidade de haver 50 pedidos em um dia de trabalho é: {prob_50_pedidos:.4f}")
```

```
A probabilidade de receber mais de dois pedidos por hora é: 0.8753

A probabilidade de haver 50 pedidos em um dia de trabalho é: 0.0177
```

Este script usa a função `cdf` (Cumulative Distribution Function) da distribuição de Poisson para calcular a probabilidade acumulativa de receber até 2 pedidos e, em seguida, subtrai esse valor de 1 para obter a probabilidade de receber mais de dois pedidos por hora.

Se a probabilidade for alta, pode ser indicativo de que há uma demanda significativa no horário do almoço, e aumentar o número de atendentes pode ser considerado. No entanto, outras considerações, como a eficiência operacional e os custos associados, também devem ser levadas em conta ao tomar essa decisão.



&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>
