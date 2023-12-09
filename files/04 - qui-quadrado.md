**Python - Estatística II** 
>**Qui Quadrado**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;


## Qui Quadrado

### Exercício 1:

pvalue > alpha: 0,05

H0: Não existe diferença significativa além do acaso

### Não Rejeita H0

Pessoas que assistem novela:

|            | Assiste | Não Assiste | Proporção |
|------------|---------|-------------|-----------|
| Masculino  | 19      | 6           | 25        |
| Feminino   | 43      | 32          | 75        |
| Total      | 62      | 38          | 100       |


&nbsp;




```
# Importação das funções, chi2_contingency porque temos 2 categorias
import numpy as np
from scipy.stats import chi2_contingency
```


```
# Criação da matriz com os dados e execução do teste
novela = np.array([[19, 6], [43, 32]])
novela
```


```
array([[19,  6],
       [43, 32]])
```

&nbsp;


```
#segundo valor é o pvalue

#Valor de p é maior que 0,05 não há evidências de diferença significativa (hipótese nula): não há diferença significativa

chi2_contingency(novela)
```


```
Chi2ContingencyResult(
    statistic=2.037351443123939, 
    pvalue=0.15347667161786666, 
    dof=1, 
    expected_freq=array([[15.5,  9.5],
       [46.5, 28.5]]))
```

--- 

### Exercício 2:

pvalue < alpha: 0,05

H0: Não existe diferença significativa além do acaso

### Rejeita H0

Ha: Existe diferença significativa além do acaso



Pessoas que assistem novela:

|            | Assiste | Não Assiste | Proporção |
|------------|---------|-------------|-----------|
| Masculino  | 22      | 3           | 25        |
| Feminino   | 43      | 32          | 75        |
| Total      | 65      | 35          | 100       |


```
novela2 = np.array([[22, 3], [43, 32]])
novela2
```


```
array([[22,  3],
       [43, 32]])
```


```
#agora valor de p menor que 0,05, podemos rejeitar a hipótese nula em favor da hipótese alternativa: há diferença significativa
chi2_contingency(novela2)
```


```
Chi2ContingencyResult(
    statistic=6.461538461538461, 
    pvalue=0.011023416388221425, 
    dof=1, 
    expected_freq=array([[16.25,  8.75],
       [48.75, 26.25]]))
```








&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>