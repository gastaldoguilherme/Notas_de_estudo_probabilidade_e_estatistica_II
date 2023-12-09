**Python - Estatística II** 
>**Distribuição Binomial**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;


## Distribuição Binomial




Em estatística, CDF (Função de Distribuição Cumulativa) e PMF (Função de Massa de Probabilidade) são conceitos relacionados que descrevem a distribuição de probabilidade de uma variável aleatória discreta.

1. **Função de Distribuição Cumulativa (CDF):**
   - A CDF de uma variável aleatória X, denotada por F(x), é uma função que fornece a probabilidade de X ser menor ou igual a um determinado valor x.
   - Matematicamente, para todos os valores reais x, a CDF é dada por F(x) = P(X ≤ x).
   - A CDF é não decrescente e limitada entre 0 e 1.

2. **Função de Massa de Probabilidade (PMF):**
   - A PMF é uma função que associa a cada possível valor da variável aleatória discreta a sua probabilidade de ocorrência.
   - Para uma variável aleatória discreta X, a PMF é muitas vezes denotada por P(X = x), representando a probabilidade de X ser igual a um valor específico x.
   - A PMF deve satisfazer duas propriedades: ser não negativa para todos os valores possíveis e a soma de todas as probabilidades deve ser igual a 1.

Em resumo, a CDF fornece a probabilidade acumulada de uma variável aleatória ser menor ou igual a um determinado valor, enquanto a PMF fornece a probabilidade exata de a variável aleatória assumir um valor específico.




### Exercício 1:

Jogar uma moeda 5 vezes, qual a probabilidade de dar cara 3 vezes?

```
# Importação da função binom
from scipy.stats import binom
```


```
# eventos , experimentos, probabilidades
prob = binom.pmf(3, 5, 0.5)
prob
```

```
0.31249999999999983
```

![Alt text](/assets/02-1.png)




---

### Exercício 2:

Passar por 4 sinais de 4 tempos, qual a probabilidade de pegar o sinal verde, nos seguintes casos:

```
Número de vezes de pegar o sinal verde em 4 sinaleiras:

a)nenhuma; 
b)1; 
c)2; 
d)3;  
e)4;
```

![Alt text](/assets/02-2.JPG)



a)nenhuma; 
```
binom.pmf(0, 4, 0.25)
```
```
0.3164062500000001
```


b)1; 
```
binom.pmf(1, 4, 0.25)
```
```
0.4218750000000001
```


c)2; 
```
binom.pmf(2, 4, 0.25)
```
```
0.21093750000000006
```

d)3; 
```
binom.pmf(3, 4, 0.25)
```
```
0.046875000000000014
```


e)4;
```
binom.pmf(4, 4, 0.25)
```
```
0.00390625
```

&nbsp;


```
#Passar por 4 sinais de 2 tempos, qual a probabilidade de pegar sinal verde nos 4 sinais?

binom.pmf(4, 4, 0.5)
```

```
0.0625
```


![Alt text](/assets/02-3.png)


&nbsp;


```
# Probabilidade acumulativa
#Passar por 4 sinais de 4 tempos, qual a probabilidade de pegar sinal verde até 4 sinais?

binom.cdf(4, 4, 0.25)
```
```
1.0
```

![Alt text](/assets/02-4.png)


```
# Probabilidade acumulativa
binom.pmf(0, 4, 0.25) + binom.pmf(1, 4, 0.25) + binom.pmf(2, 4, 0.25) + binom.pmf(3, 4, 0.25) + binom.pmf(4, 4, 0.25)
```

```
1.0000000000000002
```

![Alt text](</assets/02-5.JPG>)





---

### Exercício 3:

Concurso com 12 questões, qual a probabilidade de acertar 7 questões considerando que cada questão tem 4 alternativas?

```
binom.pmf(7, 12, 0.25) 
```

```
0.011471271514892587
```
![Alt text](/assets/02-6.png)



&nbsp;

```
# Probabilidade de acertar as 12 questões
binom.pmf(12, 12, 0.25) 
```


```
5.960464477539063e-08
```

![Alt text](/assets/02-7.png)



&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>