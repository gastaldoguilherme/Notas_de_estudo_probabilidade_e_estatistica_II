**Python - Estatística II** 
>**Geraração de uma amostra com restrições específicas**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;




## Geraração de uma amostra com restrições específicas:


Para gerar uma amostra com restrições específicas, como valores mínimos e máximos, apenas valores positivos ou apenas valores inteiros, você pode ajustar a geração de números aleatórios no NumPy. Além disso, para reproduzir os mesmos resultados, você pode definir uma semente (seed). Aqui estão exemplos para cada caso:

### Gerando uma amostra entre 20 e 30:

```python
import numpy as np

np.random.seed(10)  # Definindo a semente para reproduzir os resultados
amostra_min_max = 20 + 10 * np.random.rand(20)  # Gera valores entre 20 e 30
print("Amostra com valores entre 20 e 30:", amostra_min_max)
```

```
Amostra com valores entre 20 e 30: [27.71320643 20.20751949 26.33648235 27.48803883 24.98507012 22.24796646
 21.98062865 27.60530712 21.69110837 20.88339814 26.85359818 29.53393346
 20.03948266 25.12192263 28.12620962 26.12526067 27.21755317 22.91876068
 29.17774123 27.14575783]

```




### Gerando uma amostra apenas com valores positivos:

```python
import numpy as np

np.random.seed(42)  # Definindo a semente para reproduzir os resultados
amostra_positiva = np.random.rand(20)  # Gera valores entre 0 e 1 (exclusivo)
print("Amostra com valores positivos:", amostra_positiva)
```

```
Amostra com valores positivos: [0.37454012 0.95071431 0.73199394 0.59865848 0.15601864 0.15599452
 0.05808361 0.86617615 0.60111501 0.70807258 0.02058449 0.96990985
 0.83244264 0.21233911 0.18182497 0.18340451 0.30424224 0.52475643
 0.43194502 0.29122914]

```



### Gerando uma amostra apenas com valores inteiros:

```python
import numpy as np

np.random.seed(42)  # Definindo a semente para reproduzir os resultados
amostra_inteira = np.random.randint(1, 11, size=20)  # Gera valores inteiros de 1 a 10
print("Amostra com valores inteiros:", amostra_inteira)
```

```
Amostra com valores inteiros: [ 7  4  8  5  7 10  3  7  8  5  4  8  8  3  6  5  2  8  6  2]

```



Lembre-se de que ao usar `randn` ou `randint`, a distribuição dos valores pode ser diferente do exemplo original com `rand`. A escolha entre esses métodos depende da natureza dos seus dados. Experimente e escolha a abordagem que melhor atenda às suas necessidades.


&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>