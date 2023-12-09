**Python - Estatística II** 
>**Distribuição T Student**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;

## Distribuição T Student

### Exercício 1: 

Média de salário dos cientistas de dados = R$ 75,00 por hora Amostra com 9 funcionários e desvio padrão = 10

```
# Importação da função para fazer o teste
from scipy.stats import t
```

&nbsp;

```
# Qual a probabilidade de selecionar um cientista de dados e o salário ser menor que R$ 80 por hora
t.cdf(1.5, 8)
```
```
0.9139983540240443
```
&nbsp;

```
# Qual a probabilidade do salário ser maior do que 80?
t.sf(1.5, 8)
```

```
0.08600164597595565
```
&nbsp;
```
# Somatório da execução dos dois códigos acima (lado esquerdo + lado direito da distribuição)
t.cdf(1.5, 8) + t.sf(1.5, 8)
```

```
0.9999999999999999
```




&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>