**Python - Estatística II** 
>>**Teste de Análise de Variância (ANOVA) & Teste-F**  
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;


## ANOVA e Teste-F


Análise da Variância (ANOVA) é um método para
testar a igualdade de três ou mais médias populacionais,
baseado na análise das variâncias amostrais.

Os dados amostrais são separados em grupos segundo
uma característica (fator).

Fator (ou tratamento): é uma característica que
permite distinguir diferentes populações umas das
outras. Cada fator contém dois ou mais grupos
(classificações).

---

### Exemplo 1:

Amostras do consumo de combustível para 3 tipos de
carros, de fábricas (marcas) diferentes.

Neste caso temos amostras de 3 populações de carros.

- Temos um único fator: A marca. Este fator se separa em 3
tratamentos, cada uma das marcas.

### Exemplo 2:

(2) Amostras do consumo de combustível para 3 tamanhos
de motor (1,5 L, 2,2 L e 2,5 L) e tipo de transmissão (manual
ou automática).

Temos dois fatores:

- O fator tamanho do motor, que contém três categorias: 1,5
L, 2,2 L e 2,5 L.
- O fator tipo de transmissão, que contém duas categorias:
manual e automática.

---

## ANOVA de um critério (um fator)


• Populações normalmente distribuida

• Populações tem mesma variância (ou mesmo desvio
padrão).

• Amostras são aleatórias e mutuamente independentes.

• As diferentes amostras são obtidas de populações
classificadas em apenas uma categoria.


### Hipóteses do ANOVA de um critério

HIPÓTESE NULA: a média de todas as populações são iguais,ou
seja, o tratamento (fator) não tem efeito (nenhuma variação em média
entre os grupos).

HIPÓTES ALTERNATIVA: nem todas a médias populacionais são
iguais, ou seja:
Pelo menos uma média é diferente, isto é, existe efeito do
tratamento.
Não quer dizer que todas as médias são diferentes (alguns pares
podem ser iguais)



![Alt text](/assets/14-1.png)


### Todas as médias populacionais são iguais


![Alt text](/assets/14-2.png)

![Alt text](/assets/14-3.png)


### Nem todas as médias populacionais são iguais

![Alt text](/assets/14-4.png)

![Alt text](/assets/14-5.png)

&nbsp;

![Alt text](/assets/14-6.png)


### Para amostras de tamanhos diferentes:

![Alt text](/assets/14-7.png)


### Para amostras de tamanhos iguais:

![Alt text](/assets/14-8.png)


### A ideia básica de ANOVA: partição da variabilidade



### Variabilidade total:

$\displaystyle\frac{\text{Variabilidade dos grupos (entre grupos)}}{\text{Variabilidade devido a outros fatores (dentro dos grupos)}} $

&nbsp;

### Decomposição das observações em contribuições de diferentes fontes:


![Alt text](/assets/14-9.png)

---

### Exemplo 3:

![Alt text](/assets/14-10.png)

![Alt text](/assets/14-11.png)

![Alt text](/assets/14-12.png)


---

### Medida de variação: variância amostral 

![Alt text](/assets/14-13.png)

Variação total = variação entre as amostras + variação dentro das amostras

Em símbolos: SQ(total) = SQ(entre amostras)+SQ(dentro das
amostras)



### Variação total

SQ(total) = SQ(dentro) + SQ(entre)

![Alt text](/assets/14-14.png)



### Variação entre amostras

SQ(total) = SQ(entre) + S(dentro)

![Alt text](/assets/14-15.png)


### Variação dentro das amostras

SQ(total) = SQ(entre) + SQ(dentro)

![Alt text](/assets/14-16.png)


### Tabela ANOVA 1- fator

![Alt text](/assets/14-17.png)

k = número de amostras (grupos)\
n = soma do número de elementos de todas as amostras\
gl = graus de liberdade

## Teste F:

![Alt text](/assets/14-18.png)

### Valores críticos são obtidos da tabela da distribuição F

![Alt text](/assets/14-19.png)


---


### Exercício 4:


Um experimento foi realizado para avaliar as notas atribuídas a uma mesma comida em três restaurantes diferentes, designados como A, B e C. As notas dadas por diferentes indivíduos foram registradas conforme a tabela abaixo:

$
\begin{array}{ccc}
\text{Restaurante A} & \text{Restaurante B} & \text{Restaurante C} \\
3 & 5 & 5 \\
2 & 3 & 6 \\
1 & 4 & 7 \\
\end{array}
$

Utilize a análise de variância (ANOVA) para determinar se existe alguma diferença significativa nas notas médias atribuídas aos restaurantes. Realize o teste-F para avaliar a hipótese nula de que as médias são iguais em todos os restaurantes.


### Solução:


### 1) Para amostras de tamanhos iguais:

![Alt text](/assets/14-8.png)

$\bar{\bar{X}} = \displaystyle \frac{3+2+1+ ... + 5+6+7}{9} = 4$



### 2) Variação total

SQ(total) = SQ(dentro) + SQ(entre)

![Alt text](/assets/14-14.png)


$SQT = (3-4)^2 +(2-4)^2 + ... +(7-4)^2 = 30$

SQT = 30

gl = n-1 = 8






### 3) Variação entre amostras


![Alt text](/assets/14-15.png)

$\bar{X}_jA = \displaystyle \frac{3+2+1}{3} = 2$

$\bar{X}_jB = \displaystyle \frac{5+3+4}{3} = 4$

$\bar{X}_jC = \displaystyle \frac{5+6+7}{3} = 6$

$\bar{\bar{X}} = 4$



$SQ(entre) =3.(2-4)^2 + 3. (4-4)^2 + 3.(6-4)^2 = 24$

SQ(entre) = 24

gl = k-1 = 2



### 4) Variação dentro das amostras


![Alt text](/assets/14-16.png)

$SQ(dentro) = (3-2)^2+...+(5-4)^2+... +(7-6)^2 = 6$

SQ(dentro) = 6

gl = n-k = 6


### 5) Tabela ANOVA 1- fator


| FV (Fontes de Variação) | SQ  | gl | QM   | Fcalc  | Ftab, 5% |
|-------------------------|-----|----|------|--------|----------|
| Tratamento              | 24  | 2  | 12   | 12     | 5,14     |
| Resíduos                | 6   | 6  | 1    |        |          |
| Total                   | 30  | 8  |      |        |          |

- Se Fcalc ≥ Ftab, 5%, existe efeito do fator, no caso restaurante
- Os restaurantes influenciam na notas das comidas.


#### Ftab(2,6, 0.05)

gl-tratamento: 2

gl-Resíduo: 6

![Alt text](/assets/14-20.png)



### 6) Hipóteses do ANOVA de um critério


Com base nas condições estabelecidas, podemos concluir o seguinte:

1. **Teste-F:**
   - $F_{\displaystyle \text{estatístico}} > F_{\displaystyle \text{crítico}}$
     - $12.00 > 5,14$
     - Condição atendida.
     - Portanto, rejeitamos $H_0$ ao nível de significância de $0.05$.

2. **Valor-p:**
   - $p$-value < $\alpha$
     - $0.0080 < 0.05$
     - Condição atendida.
     - Portanto, rejeitamos $H_0$ ao nível de significância de $0.05$.

Em ambas as abordagens, tanto pelo teste-F quanto pelo valor-p, as condições para rejeitar a hipótese nula $H_0$ são satisfeitas. Portanto, há evidências estatísticas para afirmar que existe uma diferença significativa nas notas médias atribuídas aos restaurantes A, B e C.

Essa conclusão sugere que, com base nos dados coletados, pelo menos uma das médias das notas dos restaurantes é diferente das outras. É importante considerar que a análise de variância (ANOVA) não fornece informações específicas sobre quais médias são diferentes entre si. Para identificar quais grupos são significativamente diferentes, seria necessário realizar testes de comparação múltipla, como o teste de Tukey.

```
import scipy.stats as stats

# Dados
restaurante_A = [3, 2, 1]
restaurante_B = [5, 3, 4]
restaurante_C = [5, 6, 7]

# Realizar a ANOVA
statistic, p_value = stats.f_oneway(restaurante_A, restaurante_B, restaurante_C)

# Nível de significância
alpha = 0.05

# Imprimir os resultados
print(f'Estatística do teste-F: {statistic:.4f}')
print(f'Valor-p: {p_value:.4f}')

# Verificar se rejeitamos H0
if p_value < alpha:
    print(f'Rejeitar H0. Existe uma diferença significativa nas notas médias.')
else:
    print(f'Não rejeitar H0. Não há evidências suficientes para indicar diferença nas notas médias.')

```


```
Estatística do teste-F: 12.0000
Valor-p: 0.0080
Rejeitar H0. Existe uma diferença significativa nas notas médias.
```



---

### Exercício 5:


Avaliação da Efetividade de Inseticidas em uma Cultura de vegetais

Um experimento foi conduzido em um delineamento inteiramente casualizado (DIC) para avaliar o efeito de quatro inseticidas (A, B, C e D) e uma testemunha (sem inseticida) sobre o número de insetos coletados 36 horas após a pulverização em uma cultura específica de vegetais. Cada tratamento foi repetido seis vezes. Os dados obtidos estão apresentados na tabela abaixo:


|      | Rep1 | Rep2 | Rep3 | Rep4 | Rep5 | Rep6 |
|------|------|------|------|------|------|------|
| A    | 2370 | 2687 | 2592 | 2483 | 2910 | 3020 |
| B    |  682 |  927 |  871 |  725 |  805 |  920 |
| C    |  562 |  702 |  636 |  487 |  485 |  892 |
| D    |  349 |  271 |  582 |  610 |  496 |  619 |






### Solução:


### 1) Para amostras de tamanhos iguais:

![Alt text](/assets/14-8.png)

$\bar{\bar{X}} = \displaystyle \frac{2370 + ... + 619}{24} = 1153,458$



### 2) Variação total

SQ(total) = SQ(dentro) + SQ(entre)

![Alt text](/assets/14-14.png)


$SQT = (2370-1153,46)^2 + ... +(619-1153,46)^2 = 19497523,96$

SQT = 19497523,96

gl = n-1 = 24-1=23






### 3) Variação entre amostras


![Alt text](/assets/14-15.png)

$\bar{X}_jA = \displaystyle \frac{2370 + ... +3020}{6} = 2677$

$\bar{X}_jB = \displaystyle \frac{682 + ... + 920}{6} = 821,66$

$\bar{X}_jC = \displaystyle \frac{562 + ... + 892}{6} = 627,33$

$\bar{X}_jD = \displaystyle \frac{349 + ... + 619}{6} = 487,83$

$\bar{\bar{X}} = 1153,458$



$SQ(entre) =3.(2677-1153,458)^2 + 3.(821,66-1153,458)^2 + 3.(627,33-1153,458)^2 + 3.(487,83-1153,458)^2 = 6302258,153$

SQ(entre) = 6302258,153

gl = k-1 = 4-1=3



### 4) Variação dentro das amostras


![Alt text](/assets/14-16.png)

$SQ(dentro) = (2370-2677)^2+...+(682-821,66)^2 +... +(562-627,33)^2 +... +(349-487,83)^2 = 590749,50$

SQ(dentro) = 590749,50

gl = n-k = 24-4=20


### 5) Tabela ANOVA 1- fator


| FV (Fontes de Variação) | SQ             | gl | QM              | Fcalc        | Ftab, 5% |
|-------------------------|----------------|----|-----------------|--------------|----------|
| Tratamento              | 18,906,774.46  | 3  | 6,302,258.153   | 213.3648239  | 3.1      |
| Resíduos                | 590,749.5      | 20 | 29,537.475      |              |          |
| Total                   | 19,497,523.96  | 23 |                 |              |          |

- Se Fcalc ≥ Ftab, 5%, existe efeito de tratamento.
- Os inseticidas alteram os números de insetos.


#### Ftab(3,20, 0.05)

gl-tratamento: 3

gl-Resíduo: 20

![Alt text](/assets/14-21.png)



### 6) Hipóteses do ANOVA de um critério


Com base nas condições estabelecidas, podemos concluir o seguinte:

1. **Teste-F:**
   - $F_{\displaystyle \text{estatístico}} > F_{\displaystyle \text{crítico}}$
     - $213.36 > 3.10$
     - Condição atendida.
     - Portanto, rejeitamos $H_0$ ao nível de significância de $0.05$.

2. **Valor-p:**
   - $p$-value < $\alpha$
     - $2.38 e-15 < 0.05$
     - Condição atendida.
     - Portanto, rejeitamos $H_0$ ao nível de significância de $0.05$.

```
import numpy as np
import pandas as pd
from scipy.stats import f_oneway
from statsmodels.stats.multicomp import pairwise_tukeyhsd

# Dados fornecidos
data = {
    'A': [2370, 2687, 2592, 2483, 2910, 3020],
    'B': [682, 927, 871, 725, 805, 920],
    'C': [562, 702, 636, 487, 485, 892],
    'D': [349, 271, 582, 610, 496, 619]
}

# Criando um DataFrame
df = pd.DataFrame(data)

# Aplicando ANOVA
f_statistic, p_value = f_oneway(df['A'], df['B'], df['C'], df['D'])

# Imprimindo resultados da ANOVA
print(f"ANOVA F-statistic: {f_statistic}")
print(f"ANOVA p-value: {p_value}")

```


```
ANOVA F-statistic: 213.3648239322331
ANOVA p-value: 2.378983837269639e-15
```

### Exercício 6:

**Outro modo de calcular:**


Um estudo foi conduzido para analisar possíveis diferenças entre três amostras em relação às médias de um determinado conjunto de dados. As amostras, representadas pelos conjuntos de valores abaixo, referem-se a diferentes grupos:

$ \text{Amostra 1:} \quad 64, \, 66, \, 59, \, 65, \, 62 $

$ \text{Amostra 2:} \quad 71, \, 73, \, 66, \, 70, \, 68 $

$ \text{Amostra 3:} \quad 52, \, 57, \, 53, \, 56, \, 53 $

Para determinar se há alguma diferença significativa entre as médias dessas amostras, realize um teste de comparação de médias com um nível de significância de 5%. Apresente os resultados e conclusões relevantes.

### Solução:

| Amostra | Valores                   | Ti  | Ti^2   | (Ti^2)/n   | Qi   |
|---------|---------------------------|-----|--------|------------|------|
| 1       | 64 66 59 65 62            | 316 | 99856  | 19971,2    | 20002|
| 2       | 71 73 66 70 68            | 348 | 121104 | 24220,8    | 24250|
| 3       | 52 57 53 56 53            | 271 | 73441  | 14688,2    | 14707|
|   SOMA  |                           | 935 |        | 58880,2    | 58959|

---

- n = 5; 
- k = 3;
- N = n . k = 15;
- i = 1 até k;
- j = 1 até n;
---
$
\displaystyle\sum_{i,k}\left(\displaystyle\frac{T_i^2}{n}\right) = 58880,2
$


$
\displaystyle \frac{T^2}{n \cdot k} = 58281,66667
$

---
**Soma dos quadrados ENTRE os grupos ou Soma dos quadrados dos Tratamentos:**

$SQE = \displaystyle\sum_{i,k} \left(\frac{T_i^2}{n}\right) - \left(\frac{T^2}{n \cdot k}\right) = 598,5333333$ ; $gl = k-1 = 2$

$MQE = \frac{SQE}{k-1} = 299,2666667$

---
**Soma dos quadrados TOTAL**

$SQT = Q - \left(\displaystyle\frac{T^2}{n \cdot k}\right) = 677,3333333$ ; $gl = n \cdot k - 1 = 14$

$MQT = \displaystyle\frac{SQT}{n \cdot k - 1} = 48,38095238$

---
**Soma dos quadrados de DENTRO dos grupos ou Soma dos quadrados dos Resíduos**

$ SQD = SQT - SQE = 78,8 $ ; $ gl = N - k = 12 $

$ MQD = \displaystyle\frac{SQD}{N - k} = 6,566666667 $

---






$F_{\text{calc}} = \displaystyle\frac{S^2_{\displaystyle\text{tratamento}}}{S^2_{\displaystyle\text{resíduo}}} = 45,57360406$


| FV (Fontes de Variação) | gl  | SQ         | QM ou S^2      | Fcalc         | Ftab (2,12,5%) |
|--------------------------|-----|------------|----------------|---------------|----------------|
| TRATAMENTO               | 2   | 598,5333333| 299,2666667    | 45,57360406   | 3,89           |
| RESÍDUOS                 | 12  | 78,8       | 6,566666667    |               |                |
| TOTAL                    | 14  | 677,3      |                |               |                |

Fcalc > Ftab (2,12,5%)

Como Fcalc é maior do que Ftab, concluímos que há diferença estatisticamente significativa entre as médias das amostras.



---


## ANOVA de dois critérios (dois fatores)


### ANOVA 2 FATORES - Sem repetição

### Exercício 7: 



Um estudo foi conduzido em uma empresa agrícola para avaliar a influência de seis diferentes fertilizantes em duas variedades de milho. Cada fertilizante foi aplicado a ambas as variedades, resultando em uma matriz de dados de 2 linhas (variedades) por 6 colunas (fertilizantes). O nível de significância adotado para este estudo é $ \alpha = 1\%$.

Os dados coletados, representados na tabela abaixo, indicam as médias de algum parâmetro relevante para cada combinação de variedade e fertilizante:

| Fertilizantes | a   | b   | c   | d   | e   | f   |
|---------------|-----|-----|-----|-----|-----|-----|
| Variedade 1   | 5,4 | 3,2 | 3,8 | 4,6 | 5   | 4,4 |
| Variedade 2   | 5,7 | 4   | 4,2 | 4,5 | 5,3 | 5   |


As hipóteses a serem testadas são as seguintes:

- **Hipóteses para as Linhas:**
  - $ H_{01} $: As médias em todas as linhas são iguais ($ M_1 = M_2 = \ldots = M_k $).
  - $ H_{11} $: Pelo menos uma das médias das linhas é diferente.

- **Hipóteses para as Colunas:**
  - $ H_{02} $: As médias em todas as colunas são iguais ($ M_1 = M_2 = \ldots = M_n $).
  - $ H_{21} $: Pelo menos uma das médias das colunas é diferente.



### Solução:

| Fertilizantes | a   | b   | c   | d   | e   | f   | Ti   | Ti^2   | (Ti^2)/ni       | Qi     |
|---------------|-----|-----|-----|-----|-----|-----|------|--------|-----------------|--------|
| Variedade 1   | 5,4 | 3,2 | 3,8 | 4,6 | 5   | 4,4 | 26,4 | 696,96 | 116,16          | 119,36 |
| Variedade 2   | 5,7 | 4   | 4,2 | 4,5 | 5,3 | 5   | 28,7 | 823,69 | 137,2816667     | 139,47 |
| Tj            | 11,1| 7,2 | 8   | 9,1 | 10,3| 9,4 | 55,1 |        | 253,4416667     | 258,83 |
| Tj^2          | 123,21| 51,84| 64  | 82,81| 106,09| 88,36 |       |                 |        |
| (Ti^2)/k      | 258,155 |     |     |     |     |     |      |                 |        |

---

- n = 6;
- k = 2;
- i = 1 até k;
- j = 1 até n;

---

$ Q = \displaystyle \sum_{i, k} \sum_{j, n} x_{ij}^2 = 258,83 $

$ \displaystyle \sum_{i, k} \left(\displaystyle \frac{T_i^2}{n_i}\right) = 253,4416667 $

$ \displaystyle  \sum_{j, n} \left(\displaystyle \frac{T_j^2}{k_j}\right) = 258,155 $

$ \displaystyle \frac{T^2}{n \cdot k} = 253,0008333 $

---

**Soma dos quadrados ENTRE LINHAS:**

$ SQL = \displaystyle \sum_{i, k} \left(\frac{T_i^2}{n_i}\right) - \left(\frac{T^2}{n \cdot k}\right) = 0,440833333 $ ;
$ gl = k - 1 = 1 $

$ MQL = \frac{SQL}{k-1} = 0,440833333 $

---

**Soma dos quadrados ENTRE COLUNAS:**

$ SQC = \displaystyle \sum_{j, n} \left(\frac{T_j^2}{k_j}\right) - \left(\frac{T^2}{n \cdot k}\right) = 5,154166667 $ ;
$ gl = n - 1 = 5 $

$ MQC = \displaystyle\frac{SQC}{n-1} = 1,030833333 $

---
**Soma dos quadrados TOTAL**

$ SQT = Q - \displaystyle\left(\frac{T^2}{n \cdot k}\right) = 5,829166667 $; 
$ gl = n \cdot k - 1 = 11 $

---

**Soma dos quadrados de DENTRO dos grupos ou Soma dos quadrados dos Resíduos**

$ SQD_{\text{resíduo}} = SQT - SQL - SQC = 0,234166667 $;
$ gl = (n-1) \cdot (k-1) = 5 $

$ MQD = \displaystyle\frac{SQD}{N-k} = 0,046833333 $

---

$ F_{\text{calc}} = \displaystyle\frac{S^2_{\displaystyle\text{tratamento - linha}}}{S^2_{\text{resíduo}}} = 9,412811388 $

$ F_{\text{calc}} = \displaystyle \frac{S^2_{\displaystyle\text{tratamento - coluna}}}{S^2_{\text{resíduo}}} = 22,01067616 $

---

| FV (Fontes de Variação) | SQ               | gl   | QM ou S^2       | Fcalc             | Ftab     |
|--------------------------|------------------|------|-----------------|-------------------|---------|
| LINHA                    | 0,440833333      | 1    | 0,440833333     | 9,412811388       | 16,26   |
| COLUNA                   | 5,154166667      | 5    | 1,030833333     | 22,01067616       | 10,97   |
| RESÍDUOS                 | 0,234166667      | 5,0  | 0,046833333     |                   |         |
| TOTAL                    | 5,829166667      | 11,0 |                 |                   |         |



- $ F_{\text{calc\_linhas}} = 9,413 < F_{\text{tab (1, 5, 1\%)}} = 16,26 $
  - Não rejeitar $ H_{01} $, ou seja, média igual em todas as linhas com um nível de significância $ \alpha = 1\% $.

- $ F_{\text{calc\_colunas}} = 22,011 > F_{\text{tab (5, 5, 1\%)}} = 10,97 $
  - Rejeitar $ H_{02} $, ou seja, a média de pelo menos uma coluna é diferente.




---
### ANOVA 2 FATORES - Com repetição


### Exercício 8:


Resolva a seguinte questão utilizando ANOVA de dois fatores com repetição:

Foram registrados os tempos, em segundos, necessários para que quatro operários realizassem a montagem de uma peça, utilizando três métodos distintos. Cada operário executou a montagem de duas peças para cada método, resultando nos seguintes dados, conforme a tabela abaixo. Considera-se admissível a presença de interação entre operários e métodos. Realize uma análise de variância para verificar se há diferença significativa entre os métodos, operários, tratamentos, etc., utilizando um nível de significância de 5%.



| Método | Operário 1 | Operário 2 | Operário 3 | Operário 4 |
|--------|------------|------------|------------|------------|
| I      | 9, 7       | 1, 2       | 10, 9      | 6, 15      |
| II     | 9, 12      | 16, 10     | 14, 16     | 11, 12     |
| III    | 14, 17     | 18, 13     | 18, 16     | 14, 15     |



### Fórmulas:


#### Calcular as partes principais das seguintes fórmulas:



![Alt text](/assets/14-22.png)




### Variáveis:

---

$ \displaystyle\sum_{i,k} \displaystyle \frac{T_i^2}{n \cdot r} = \frac {59^2}{4\cdot  2} + ... + \frac {125^2}{4\cdot  2} = 3638.5 $

---

$ \displaystyle\sum_{j,n} \displaystyle\frac{T_j^2}{k \cdot r} = \frac {68^2}{3\cdot  2} + ... + \frac {73^2}{3\cdot  2} = 3407 $

---

$ \displaystyle\sum_{i,k} \displaystyle\sum_{j,n} \displaystyle\frac{T_{ij}^2}{r}  = \frac {(9+7)^2 + (1+2)^2  + ... + (18+16)^2 + (/assets/14+15)^2}{2} = 37.66 $

---

$\displaystyle \frac{T^2}{n \cdot k \cdot r}  = \frac {(59 + 100 +25)^2}{4\cdot  3\cdot 2 }  = 3360.67 $

---

$ Q = \displaystyle\sum_{i,k} \sum_{j,n} \sum_{1,r} X_{ijr}^2  = 9^2 + 7^2 + ... + 14^2 + 15^2  = 3854 $

---

#### Resolvendo e criando a Tabela ANOVA com 2 fatores com repetição:

1. Soma Total dos Quadrados (SQT):

$ SQT = Q - \displaystyle\frac{T^2}{nkr} = 493.3333333 $ ; $ \text{gl = } \ knr-1 = \ 23 $

3. Médias dos Quadrados para SQT (MQT):

$ MQT = \displaystyle \frac{SQT}{knr-1} = 21.44927536 $

---



4. Soma dos Quadrados para Linhas (SQL):

$ SQL = \sum_{i,k} \displaystyle\frac{Ti^2}{nir} - \frac{T^2}{nkr} = 277.5833333 $ ; $ \text{gl = } \ k-1 = \ 2 $

6. Médias dos Quadrados para SQL (MQL):

$ MQL = \displaystyle\frac{SQL}{k-1} = 138.7916667 $

---


7. Soma dos Quadrados para Colunas (SQC):

$ SQC = \displaystyle\sum_{j,n} \displaystyle\frac{Tj^2}{kjr} - \frac{T^2}{nkr} = 46.33333333 $ ; $ \text{gl = } \ n-1 = \ 3 $

9. Médias dos Quadrados para SQC (MQC):

$ MQC = \displaystyle \frac{SQC}{n-1} = 15.44444444 $

---

10. Soma dos Quadrados para Tratamentos (SQtr):

$ SQtr = \displaystyle\sum_{i,k} \sum_{j,n} \displaystyle \frac{Tij^2}{r} - T^2  = 405.3333333 $ ; $ \text{gl = } \ n.k-1 = \ 11 $

12. Médias dos Quadrados para SQtr (MQtr):

$ MQtr = \displaystyle\frac{SQtr}{n.k-1} = 36.84848485 $

---



13. Soma dos Quadrados para a Interação (SQI):

$ SQI = SQtr - SQL - SQC = 81.41666667 $ ; $ \text{gl:} \ (k-1) \times (n-1) = \ 6 $

15. Médias dos Quadrados para SQI (MQI):

$ MQI = \displaystyle\frac{SQI}{(k-1) \times (n-1)} = 13.56944444 $

---


16. Soma dos Quadrados Residual (SQR):

$ SQR = SQT - SQtr = 88 $ ; $ \text{gl = } \ n.k.(r-1) = \ 12 $

18. Médias dos Quadrados para SQR (MQR):

$ MQR = \displaystyle\frac{SQR}{n.k.(r-1)} = 7.333333333 $

---


### Análise de Variância


| Fonte de Variaçãov | SQ            | gl | QM              | Fcalc               | Ftab (6,12,5%)  |
|--------------------|---------------|----|-----------------|---------------------|--------         |
| Entre Linhas       | 277.5833333   | 2  | 138.7916667     |                     |                 |
| Entre Colunas      | 46.33333333   | 3  | 15.44444444     |                     |                 |
| Entre Tratamentos  | 405.3333333   | 11 | 36.84848485     |                     |                 |
| Interação          | 81.41666667   | 6  | 13.56944444     | 1.850378788         |<3               |
| Residual           | 88            | 12 | 7.333333333     |                     |                 |
| Total              | 493.3333333   | 23 | 21.44927536     |                     |                 |










### Decisões

- $ F \text{ Interação} = 1.850378788 < 3 $: Não há interação significativa.
- Reorganizamos a tabela considerando apenas os efeitos principais (métodos e operários).
- Recalculamos:

$ \text{SQ Residual = SQI + SQR = 81.4167 + 88 = 169.4167  } $, 

$ \text{QM Residual = SQR / gl = 169.4167 / 12 = 14.1180} $ 

$ \text{Fcalc} $.



### Análise de Variância (Após Reorganização)


| Fonte de Variação | SQ            | gl | QM              | Fcalc               | Ftab, 5% |
|--------------------|---------------|----|-----------------|---------------------|---------|
| Entre Linhas       | 277.5833333   | 2  | 138.7916667     | 9.830791933         | 3.89    |
| Entre Colunas      | 46.33333333   | 3  | 15.44444444     | 1.093949828        | 3.49    |
| Entre Tratamentos  | 405.3333333   | 11 | 36.84848485     | 2.610025489        | 2.72    |
| Residual           | 169.4166667   | 12 | 14.11805556     |                     |         |
| Total              | 493.3333333   | 23 | 21.44927536     |                     |         |


### Decisões Finais

Conclusão sobre as respostas da ANOVA 2 fatores com repetição:

- $F \text{ Entre Linhas} = 9.830791933 > F \text{ tab, 5\%} = 3.89$: Indica que há diferença significativa entre os métodos. Rejeitamos a hipótese nula de igualdade entre os métodos.

- $F \text{ Entre Colunas} = 1.093949828 < F \text{ tab, 5\%} = 3.49$: Não há diferença significativa entre os operários. Não rejeitamos a hipótese nula de igualdade entre os operários.

- $F \text{ Entre Tratamentos} = 2.610025489 < F \text{ tab, 5\%} = 2.72$: Não há diferença significativa entre os tratamentos. Não rejeitamos a hipótese nula de igualdade entre os tratamentos.

Essas conclusões são baseadas nos resultados dos testes de hipóteses utilizando a análise de variância (ANOVA) com um nível de significância de 5%. 































&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>