**Python - Estatística II** 
>**Distribuição de Poisson**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;



## Distribuição de Poisson

### Exercício 1:

Média de acidentes de carro é 2 por dia


```
# Importação da função
from scipy.stats import poisson
```


```
# Qual a probabilidade de ocorrerem 3 acidentes no dia?
poisson.pmf(3, 2)
```


```
0.18044704431548356
```

&nbsp;

```
# Qual a probabilidade de ocorrerem 3 ou menos acidentes no dia?
poisson.cdf(3, 2)
```




```
0.857123460498547
```

&nbsp;


```
# Qual a probabilidade de ocorrerem mais de 3 acidentes no dia?
poisson.sf(3, 2)
```



```
0.14287653950145296
```

&nbsp;

```
# Probabilidade acumulativa
poisson.cdf(3, 2) + poisson.sf(3, 2)
```



```
1.0
```








&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>