**Python - Estatística II** 
>**Teste de Tukey**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;



## Teste de Tukey (ou Procedimento de Tukey)

O teste de Tukey, também conhecido como Procedimento de Tukey, é uma técnica estatística utilizada após a realização do teste ANOVA para identificar quais pares específicos de grupos têm diferenças significativas nas médias. Ele é aplicado quando há três ou mais grupos e o teste ANOVA rejeita a hipótese nula, indicando que pelo menos um grupo é significativamente diferente dos outros. Aqui estão alguns conceitos-chave e o procedimento associado ao teste de Tukey:

### Procedimento de Tukey:

1. **Diferenças Entre Pares de Médias:**
   $ \text{Diferença Entre Médias} = \bar{X}_i - \bar{X}_j $
   - **Variáveis:**
     - $ \bar{X}_i $ e $ \bar{X}_j $: Médias dos grupos a serem comparados.

2. **Intervalo de Confiança para Diferenças Entre Médias:**

   $ \text{Intervalo de Confiança} = \bar{X}_i - \bar{X}_j \pm q \cdot \sqrt{\frac{2 \cdot \text{MSE}}{n}} $
   - **Variáveis:**
     - $ \text{MSE} $: Média dos quadrados dos erros (residuals) do teste ANOVA.
     - $ n $: Número de observações em cada grupo.

3. **Estatística de Teste para Cada Par de Médias:**

   $ q = \displaystyle\frac{\bar{X}_i - \bar{X}_j}{\sqrt{\displaystyle\frac{MSE}{n}}} $
   
   - **Variáveis:**
     - $ \bar{X}_i $ e $ \bar{X}_j $: Médias dos grupos a serem comparados.
     - $ \text{MSE} $: Média dos quadrados dos erros (residuals) do teste ANOVA.
     - $ n $: Número de observações em cada grupo.

### Testes de Hipótese:

1. **Teste de Hipótese para Diferenças Entre Médias:**
   - **Hipóteses:**
     - $ H_0 $: $ \bar{X}_i = \bar{X}_j $ (Não há diferença significativa)
     - $ H_1 $: $ \bar{X}_i \neq \bar{X}_j $ (Há diferença significativa)

### Procedimento Geral:

1. **Cálculo das Diferenças Entre Médias:**
   - Calcular todas as possíveis diferenças entre as médias dos grupos.

2. **Intervalos de Confiança:**
   - Calcular os intervalos de confiança para cada diferença entre médias.

3. **Comparação com Zero:**
   - Se o intervalo de confiança incluir zero, as médias não são consideradas significativamente diferentes.

4. **Teste de Hipótese para Cada Par:**
   - Realizar testes de hipótese para cada par de médias, comparando com o valor crítico.

### Quando Usar o Teste de Tukey:

1. **Após o Teste ANOVA:**
   - Quando o teste ANOVA indica diferenças significativas entre pelo menos um par de grupos.

2. **Identificar Pares com Diferenças Significativas:**
   - Para identificar quais grupos específicos têm médias significativamente diferentes.

O teste de Tukey é uma ferramenta valiosa para realizar comparações múltiplas entre as médias de grupos, controlando o erro global do experimento. Ele é frequentemente utilizado em experimentos científicos e estudos de pesquisa para identificar diferenças específicas entre grupos após a detecção de diferenças globais pelo teste ANOVA.


### Exercício 1:

#### TESTE DE TUKEY

Num estudo sobre o comportamento de cinco populações de amendoim, foi adotado um delineamento em blocos casualizados com quatro repetições. O Quadrado Médio do Erro, calculado, foi igual a 𝟑, 𝟒𝟔𝟒𝟐. Foram coletadas médias de peso de 100 sementes (em gramas) para cada população, após serem testadas e submetidas a uma adubação de 40kg/ha de P2O5. Os tratamentos e suas respectivas médias são apresentados abaixo:

| Tratamentos        | Médias (g) |
|--------------------|------------|
| Cultivar Tatu      | 41         |
| Cultivar Oirã      | 55         |
| Cultivar Tupã      | 56         |
| Linhagem FCA 170   | 43         |
| Linhagem FCA 265   | 43         |

Os dados acima são essenciais para realizar o teste de Tukey, uma ferramenta estatística usada para comparar médias de tratamentos quando se realiza uma análise de variância (ANOVA). O objetivo é determinar se há diferenças significativas entre as médias dos tratamentos. O Quadrado Médio do Erro (Resíduo) (𝟑, 𝟒𝟔𝟒𝟐) é uma medida da variabilidade não explicada pelos tratamentos. O resultado do teste de Tukey permitirá identificar quais tratamentos apresentam diferenças significativas entre si.

$s^2 (variância) = QM_{\displaystyle\text{resíduo}} = 3.4642$




### Solução:



#### TUKEY

#### ANOVA

| FV (FONTES DE VAR)                   | GL | SQ     | QM ou $S^2$| 
|-----------------------------------   |----|--------|------------|
| TRATAMENTO (trat - 1) + (bloco - 1)  | 7  | 42,24  | 6,034285714
| RESÍDUOS                             | 12 | -      | 3,4642     |
| TOTAL (5 populações com 4 repetições)| 19 | -      | -        



## Teste de Tukey

| tratamentos        | médias (g) |
|------------------- |------------|
| C - Cultivar Tupã  | 56       |
| B - Cultivar Oirã  | 55       |
| D - Linhagem FCA 170| 43       |
| E - Linhagem FCA 265| 43       |
| A - Cultivar Tatu  | 41       |

## DMS (DIFERENÇA MÍNIMA SIGNIFICATIVA)

- $ \Delta = q \cdot \displaystyle\frac{S}{\displaystyle\sqrt{r}} $

- Valor de q (tabela) (5; 12; 0.05): 4,51

- $ \displaystyle S = \sqrt{\text{quadrado médio do resíduo}}: 1,861236148$

- $ \displaystyle r = \sqrt{\text{número de repetições (4)}}: 2$

- $ \Delta $: 4,197087515

- DMS, UNIDADE GRAMAS

**Observação:** Devemos ter uma diferença acima de 4,19 g para dizer que esta diferença é em função do tratamento.



![Alt text](/assets/15-1.png)

## CONTRASTES |Y| intervalo


Obtenção das estimativas dos contrastes:

Para obter estimativas de contrastes positivas, é conveniente colocar as médias em ordem decrescente.






```

| CONTRASTES | |Y| | Intervalo                  |
|------------|-----|----------------------------|
| C-B        | -1  | -5,197087515, 3,197087515  |
| C-D        | -13 | -17,19708751, -8,802912485 |
| C-E        | -13 | -17,19708751, -8,802912485 |
| C-A        | -15 | -19,19708751, -10,80291249 |
|            |     |                            |
| B-D        | -12 | -16,19708751, -7,802912485 |
| B-E        | -12 | -16,19708751, -7,802912485 |
| B-A        | -14 | -18,19708751, -9,802912485 |
|            |     |                            |
| D-E        | 0   | -4,197087515, 4,197087515  |
| D-A        | -2  | -6,197087515, 2,197087515  |
|            |     |                            |
| E-A        | -2  | -6,197087515, 2,197087515  |

```

Se 𝒀 ≥ ∆(= 𝟒, 𝟏𝟗𝟕𝟎), o contraste é significativo ao nível de 5% de probabilidade.


- Médias seguidas de pelo menos uma letra em comum não diferem entre si no teste de Tukey, ao nível de significância de 5%.



| Tratamentos        | Médias (g) |            |
|--------------------|------------|------------|
| Cultivar Tupã      | 56         | a          |
| Cultivar Oirã      | 55         | a          |
| Linhagem FCA 170   | 43         | b          |
| Linhagem FCA 265   | 43         | b          |
| Cultivar Tatu      | 41         | b          |


--- 


### Exercício 2:



**Exercício: Avaliação da Efetividade de Inseticidas em uma Cultura de Vegetal**

Um experimento foi conduzido em um delineamento inteiramente casualizado (DIC) para avaliar o efeito de quatro inseticidas (A, B, C e D) e uma testemunha (sem inseticida) sobre o número de insetos coletados 36 horas após a pulverização em uma cultura específica de vegetal. Cada tratamento foi repetido seis vezes. Os dados obtidos estão apresentados na tabela abaixo:

```
          Rep1  Rep2  Rep3  Rep4  Rep5  Rep6
A        2370  2687  2592  2483  2910  3020
B         682   927   871   725   805   920
C         562   702   636   487   485   892
D         349   271   582   610   496   619
```

### Solução:

## Tabela ANOVA:

| FV (FONTES DE VAR) | GL |        SQ       |    QM ou S^2    |   Fcalc   | Ftab, 5%  |
|---------------------|----|-----------------|------------------|-----------|-----------|
|    TRATAMENTO      |  3 | 18.906.774,46   | 6.302.258,153    | 213,3648239|     3,1   |
|    RESÍDUOS        | 20 |    590.749,5    |    29.537,475    |           |           |
|      TOTAL         | 23 | 19.497.524,0    |                 |           |           |


- Se Fcalc ≥ Ftab, 5%, existe efeito de tratamento.
- Os inseticidas alteram os números de insetos.


#### Ftab(3,20, 0.05)

GL-tratamento: 3

GL-Resíduo: 20

![Alt text](/assets/15-2.png)



## TUKEY

**Número de combinações:**

$ C(n, k) = \displaystyle \frac{n!}{k! \cdot (n-k)!} $

- $ n $ ou $ I = 4 $
- $ k = 2 $
- $ C(n, k) = 6 $

**Diferença Mínima Significativa (DMS):**

$ \Delta = q \cdot \displaystyle \frac{S}{r^{0,5}} $

- $ q $ - valor crítico da tabela
- $ n_1 $ (número de médias) = 4
- $ n_2 $ (gl denominador ou resíduo ou tratamento) = 20
- $ \alpha = 0,05 $
- $ \text{tab } q(n_1, n_2, \alpha) = 3,96 $


#### q-tab(4,20, 0.05)

![Alt text](/assets/15-3.png)




$ \Delta = q \cdot \displaystyle\frac{S}{r^{0,5}} $

- $\text{tab } q(n_1, n_2, \alpha) = 3,96$
- $S = \sqrt{S^2}$ desvio padrão (raiz do quadrado médio ou variância resíduo) = 171,8646997
- $r^{0,5}$ (repetições) = 2,449489743
- $\Delta$ = 277,8473406


|        |   A   |     B  |     C  |      D    |
|------- |-------|--------|--------|-----------|
|        | 2370  |    682 |    562 |     349   |
|        | 2687  |    927 |    702 |     271   |
|        | 2592  |    871 |    636 |     582   |
|        | 2483  |    725 |    487 |     610   |
|        | 2910  |    805 |    485 |     496   |
|        |       |        |        |           |
| $m̂_i$  | 2677  | 821.67 | 627.33 | 487.83    |


&nbsp;




| Ordenar |       |                |                  |
|---------|-------|----------------|------------------|
| 4       | $m̂_4$ | 487,8333333    | a                |
| 3       | $m̂_3$ | 627,3333333    | ac               |
| 2       | $m̂_2$ | 821,6666667    | bce              |
| 1       | $m̂_1$ | 2677           | bdf              |


&nbsp;



**Contrastes |$Ŷ$|:**
| $Ŷ$      |       |              |              |               |   |
|----------|-------|--------------|--------------|---------------|---|
| $Ŷ_1$    | m4-m3 | -139,5       | -417,3473406 | 138,3473406   | ns|
| $Ŷ_2$    | m4-m2 | -333,8333333 | -611,6806739 | -55,98599277  | * |
| $Ŷ_3$    | m4-m1 | -2189,166667 | -2467,014007 | -1911,319326  | * |
| $Ŷ_4$    | m3-m2 | -194,3333333 | -472,1806739 | 83,51400723   | ns|
| $Ŷ_5$    | m3-m1 | -2049,666667 | -2327,514007 | -1771,819326  | * |
| $Ŷ_6$    | m2-m1 | -1855,333333 | -2133,180674 | -1577,485993  | * |

- ns : não significativo

- '*' : contraste significativo

- $\Delta$ = 277,85; Valores abaixo de 277,85 a um nível de significância, $\alpha$= 5%, não é estatisticamente significativa, portanto não há diferença entre as médias







&nbsp;

| Ordenar |       |                |                       |
|---------|-------|----------------|-----------------------|
| 4       | $m̂_4$ | 487,8333333    | a  (1° melhor opção)  |
| 3       | $m̂_3$ | 627,3333333    | ac (1° melhor opção)  |
| 2       | $m̂_2$ | 821,6666667    | bce                   |
| 1       | $m̂_1$ | 2677           | bdf                   |

&nbsp;

A conclusão dos contrastes para Tukey pode ser resumida da seguinte forma:

Os contrastes $Ŷ$ foram calculados para as combinações específicas entre diferentes médias $m$. Os resultados indicam:

- $Ŷ_1$: A diferença entre $m_4$ e $m_3$ não é estatisticamente significativa (ns).
- $Ŷ_2$: Existe uma diferença significativa entre $m_4$ e $m_2$ (*).
- $Ŷ_3$: Há uma diferença significativa entre $m_4$ e $m_1$ (*).
- $Ŷ_4$: A diferença entre $m_3$ e $m_2$ não é estatisticamente significativa (ns).
- $Ŷ_5$: Existe uma diferença significativa entre $m_3$ e $m_1$ (*).
- $Ŷ_6$: Há uma diferença significativa entre $m_2$ e $m_1$ (*).

As conclusões são baseadas nos valores dos contrastes e nos critérios de significância. Contrastes marcados com 'ns' indicam que a diferença não é significativa, enquanto aqueles marcados com '*' indicam diferenças estatisticamente significativas. Esses resultados fornecem insights sobre as relações entre as médias e ajudam a identificar quais comparações são estatisticamente diferentes em um estudo de análise de variância.


```
import pandas as pd
from statsmodels.stats.multicomp import pairwise_tukeyhsd

# Supondo que você já tenha as listas de notas
tratamento_A = [2370, 2687, 2592, 2483, 2910, 3020]
tratamento_B = [682, 927, 871, 725, 805, 920]
tratamento_C = [562, 702, 636, 487, 485, 892]
tratamento_D = [349, 271, 582, 610, 496, 619]

# Criar um DataFrame com os dados
data = pd.DataFrame({
    'num_insetos': tratamento_A + tratamento_B + tratamento_C + tratamento_D,
    'tratamento': ['A'] * 6 + ['B'] * 6 + ['C'] * 6 + ['D'] * 6
})

# Realizar o teste de Tukey
tukey_results = pairwise_tukeyhsd(data['num_insetos'], data['tratamento'])

# Imprimir os resultados
print(tukey_results)

```

```
    Multiple Comparison of Means - Tukey HSD, FWER=0.05     
============================================================
group1 group2  meandiff  p-adj    lower      upper    reject
------------------------------------------------------------
     A      B -1855.3333    0.0 -2133.0609 -1577.6057   True
     A      C -2049.6667    0.0 -2327.3943 -1771.9391   True
     A      D -2189.1667    0.0 -2466.8943 -1911.4391   True
     B      C  -194.3333 0.2366  -472.0609    83.3943  False
     B      D  -333.8333  0.015  -611.5609   -56.1057   True
     C      D     -139.5 0.5103  -417.2276   138.2276  False
------------------------------------------------------------

```





















&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>