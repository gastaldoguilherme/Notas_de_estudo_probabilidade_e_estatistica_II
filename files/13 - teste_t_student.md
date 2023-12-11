**Python - Estatística II** 
>**Teste t de Student**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;


## Teste t de Student

O teste t de Student é uma técnica estatística utilizada para testar se há diferenças significativas entre as médias de duas amostras independentes ou se uma única amostra difere significativamente de uma população com uma média conhecida. Aqui estão alguns conceitos-chave e fórmulas associadas ao teste t de Student:

### Fórmulas Principais:

1. **Teste t para uma Amostra (Média Populacional Conhecida):**

   $t = \displaystyle\frac{\bar{X} - \mu_0}{\displaystyle \frac{s}{\displaystyle \sqrt{n}}}$
   
   - **Variáveis:**
     - $\bar{X}$: Média da amostra
     - $\mu_0$: Média populacional sob a hipótese nula
     - $s$: Desvio padrão da amostra
     - $n$: Tamanho da amostra
       
   - **Descrição:**
     - Usado quando a média populacional é conhecida e queremos testar se uma amostra difere significativamente.

3. **Teste t para uma Amostra (Média Populacional Desconhecida):**

   $t = \displaystyle\frac{\bar{X} - \mu_0}{\displaystyle\frac{s}{\sqrt{n}}}$
   
   - **Variáveis:**
     - $\bar{X}$: Média da amostra
     - $\mu_0$: Média populacional sob a hipótese nula
     - $s$: Desvio padrão da amostra
     - $n$: Tamanho da amostra
      
   - **Descrição:**
     - Usado quando a média populacional é desconhecida e queremos testar se uma amostra difere significativamente.

5. **Teste t para Duas Amostras (Amostras Independentes):**

   $t = \displaystyle\frac{\bar{X}_1 - \bar{X}_2}{\sqrt{\displaystyle\frac{s_1^2}{n_1} + \frac{s_2^2}{n_2}}}$
   
   - **Variáveis:**
     - $\bar{X}_1$ e $\bar{X}_2$: Médias das amostras 1 e 2
     - $s_1$ e $s_2$: Desvios padrões das amostras 1 e 2
     - $n_1$ e $n_2$: Tamanhos das amostras 1 e 2
     - 
   - **Descrição:**
     - Usado para testar se as médias de duas amostras independentes são significativamente diferentes.

### Testes de Hipótese:

1. **Teste t para uma Amostra:**
   
   - **Hipóteses:**
     - $H_0$: $\mu = \mu_0$ (Média populacional é igual a $\mu_0$)
     - $H_1$: $\mu \neq \mu_0$ (Média populacional é diferente de $\mu_0$)

3. **Teste t para Duas Amostras (Amostras Independentes):**
   
   - **Hipóteses:**
     - $H_0$: $\mu_1 = \mu_2$ (Médias populacionais são iguais)
     - $H_1$: $\mu_1 \neq \mu_2$ (Médias populacionais são diferentes)

### Quando Usar o Teste t de Student:

1. **Amostras Pequenas:**
   - Quando o tamanho da amostra é pequeno e as condições para a aplicação do teste t são atendidas.

2. **População Normalmente Distribuída:**
   - Quando as amostras são provenientes de uma população que segue uma distribuição normal (ou se o tamanho da amostra é grande o suficiente de acordo com o Teorema do Limite Central).

3. **Variância Conhecida ou Desconhecida:**
   - Pode ser aplicado tanto quando a variância populacional é conhecida quanto quando é desconhecida.

O teste t de Student é amplamente utilizado em diversas áreas, especialmente quando se trabalha com amostras pequenas e é necessário realizar inferências sobre as médias populacionais.




#### Exercício 1:

**Questão: Teste t para Comparação de Tempo e Custo entre Dois Produtos**

Você é responsável por decidir qual é a melhor opção de compra para uma grande quantidade de 1000 unidades entre dois produtos, A e B. Para tomar essa decisão, você deseja avaliar tanto o tempo médio necessário para agir o produto quanto o custo associado. Os dados de tempo (em horas) e custo (em reais) para cada unidade dos dois produtos são apresentados abaixo:

**Dados:**
- Produto A (Custo): R$100,00 por unidade
- Produto B (Custo): R$120,00 por unidade

**Tempo (em horas) para agir o produto:**
```
Produto A: 10, 5, 5, 9, 10, 5, 9, 9
Produto B: 5, 5, 5, 8, 7, 8, 10, 7
```

Assumindo que as amostras são independentes, você decide realizar um Teste t para Duas Amostras (Amostras Independentes) para comparar as médias dos tempos de ação entre os dois produtos. Além disso, você deseja verificar se há uma diferença significativa nos custos.

**Hipóteses:**
- $H_0$: As médias populacionais dos tempos de ação são iguais para os dois produtos ( $\mu_A = \mu_B$ ).
- $H_1$: As médias populacionais dos tempos de ação são diferentes para os dois produtos ( $\mu_A \neq \mu_B$ ).

**Nível de Significância:**
- $\alpha = 0,05$

**Teste Estatístico:**
- Teste t para Duas Amostras (Amostras Independentes)

**Variáveis:**
- $\bar{X}_A$ e $\bar{X}_B$: Médias dos tempos de ação para os produtos A e B, respectivamente.
- $s_A$ e $s_B$: Desvios padrões dos tempos de ação para os produtos A e B, respectivamente.
- $n_A$ e $n_B$: Tamanhos das amostras para os produtos A e B, respectivamente.

**Tomando uma Decisão:**
- Rejeitar $H_0$ se o valor p for menor que $\alpha$.

**Pergunta:**
Considerando os resultados do teste t, qual produto você recomendaria para a compra de 1000 unidades com base nos critérios de tempo e custo? Justifique sua resposta.


### Solução:


Para realizar o teste t para duas amostras independentes, precisamos seguir alguns passos:

#### Formular as hipóteses estatísticas:

- $H_0$: As médias populacionais dos tempos de ação são iguais para os dois produtos ( $\mu_A = \mu_B$ ).
- $H_1$: As médias populacionais dos tempos de ação são diferentes para os dois produtos ( $\mu_A \neq \mu_B$ ).

#### Definir o nível de significância:

- $\alpha = 0,05$

#### Identificar o teste estatístico apropriado:

- Teste t para Duas Amostras (Amostras Independentes)

#### Coletar e organizar os dados:

Dados de tempo para o produto A:
```
10, 5, 5, 9, 10, 5, 9, 9
```

Dados de tempo para o produto B:
```
5, 5, 5, 8, 7, 8, 10, 7
```

#### Calcular as estatísticas amostrais necessárias:

- $\bar{X}_A$: Média dos tempos de ação para o produto A.
- $\bar{X}_B$: Média dos tempos de ação para o produto B.
- $s_A$: Desvio padrão dos tempos de ação para o produto A.
- $s_B$: Desvio padrão dos tempos de ação para o produto B.
- $n_A$: Tamanho da amostra para o produto A.
- $n_B$: Tamanho da amostra para o produto B.


**Produto A:**
- Média ($\bar{X}_A$): 7,75
- Desvio Padrão ($s_A$): 2,314550249
- Tamanho da Amostra ($n_A$): 8

**Produto B:**
- Média ($\bar{X}_B$): 6,875
- Desvio Padrão ($s_B$): 1,807721534
- Tamanho da Amostra ($n_B$): 8



### t-estatístico:

$t_{\huge\text{estatístico}} = 0.8427009716003844$

#### Calcular o valor p usando o teste t para duas amostras independentes.



$t_{\text{stat}} = \displaystyle \frac{\bar{X}_A - \bar{X}_B}{\sqrt{\displaystyle \frac{s_A^2}{n_A} + \displaystyle \frac{s_B^2}{n_B}}}$


$t_{\displaystyle\text{stat}} = \displaystyle\frac{7,75 - 6,875}{\sqrt{\displaystyle\frac{(2,314550249)^2}{8} + \frac{(1,807721534)^2}{8}}} \approx 0.8427009716003844$


#### Calcular os graus de liberdade para o teste t para duas amostras independentes 

$\text{Graus de Liberdade} = \displaystyle\frac{\left(\displaystyle\frac{s_1^2}{n_1} + \displaystyle\frac{s_2^2}{n_2}\right)^2}{\displaystyle\frac{\left(\displaystyle\frac{\left(\displaystyle\frac{s_1^2}{n_1}\right)^2}{n_1-1}\right)}{n_1-1} + \displaystyle\frac{\left(\displaystyle\frac{\left(\displaystyle\frac{s_2^2}{n_2}\right)^2}{n_2-1}\right)}{n_2-1}}$

Substituindo com os valores fornecidos:

$\text{Graus de Liberdade} = \displaystyle\frac{\left(\displaystyle\frac{(2.314550249)^2}{8} + \displaystyle\frac{(1.807721534)^2}{8}\right)^2}{\displaystyle\frac{\left(\displaystyle\frac{\left(\displaystyle\frac{(2.314550249)^2}{8}\right)^2}{8-1}\right)}{8-1} + \displaystyle\frac{\left(\displaystyle\frac{\left(\displaystyle\frac{(1.807721534)^2}{8}\right)^2}{8-1}\right)}{8-1}}$



$\huge\text{Graus de Liberdade} \approx \frac{1.154902828}{0.023983662}$

$\huge\text{Graus de Liberdade} \approx 48.14565154$

Então, os graus de liberdade para o teste t são aproximadamente $48.15$.

### t-crítico:

$\huge t_{\text{crítico}} = 2.0106347546964454$



```
from scipy.stats import t

# Nível de significância (alpha)
alpha = 0.05

# Graus de liberdade (gl)
gl = 48.14565154

# Calcula o valor crítico do t
t_critico = t.ppf(1 - alpha/2, df=int(gl))

print(f'O valor crítico do t para alpha = {alpha} e gl = {gl} é: {t_critico}')

```
```
O valor crítico do t para alpha = 0.05 e gl = 48.14565154 é: 2.0106347546964454

```




### p-value:


$\huge p_{\text{value}} = \text{P}(|t| > |t_{\text{stat ; gl = 0.8427 ;  48.15 }}|) \approx 0.4135613479392021$



``` 
import scipy.stats as stats
import numpy as np

# Dados de tempo para os produtos A e B
tempo_produto_A = np.array([10, 5, 5, 9, 10, 5, 9, 9])
tempo_produto_B = np.array([5, 5, 5, 8, 7, 8, 10, 7])

# Dados de custo por unidade
custo_produto_A = 100.00
custo_produto_B = 120.00

# Teste t para duas amostras independentes
t_stat, p_value = stats.ttest_ind(tempo_produto_A, tempo_produto_B)

print('t_stat =', t_stat, 'p_value =', p_value )

# Nível de significância
alpha = 0.05

# Tomar uma decisão com base no valor p
if p_value < alpha:
    print("Rejeitar H0: Há uma diferença significativa nas médias dos tempos de ação.")
else:
    print("Não rejeitar H0: Não há evidências suficientes de diferença nas médias dos tempos de ação.")

# Comparação de custo por unidade
if custo_produto_A < custo_produto_B:
    print("Recomendação: Produto A é mais econômico em termos de custo por unidade.")
else:
    print("Recomendação: Produto B pode ser mais caro por unidade.")

```
```
t_stat = 0.8427009716003844 p_value = 0.4135613479392021
Não rejeitar H0: Não há evidências suficientes de diferença nas médias dos tempos de ação.
Recomendação: Produto A é mais econômico em termos de custo por unidade.

```

### Conclusão:



1. **Teste-t:**

   - $\huge t_{\displaystyle \text{estatístico}} < \huge t_{\displaystyle \text{crítico}}$
   
     - $0.8427 < 2.011$
     - Condição NÃO atendida.
     - Portanto, NÃO rejeitamos $H_0$ ao nível de significância de $0.05$.

3. **Valor-p:**
   
   - $\huge p$-value > $\alpha$
     - $0.4135 > 0.05$
     - Condição NÃO atendida.
     - Portanto, NÃO rejeitamos $H_0$ ao nível de significância de $0.05$.


**Conclusão: Comparação de Tempo de Ação entre Produtos A e B**

Com base nos resultados do teste-t realizado para comparar o tempo de ação entre os produtos A e B, podemos tirar as seguintes conclusões:

1. **Teste-t:**
   
   - O valor do t-estatístico calculado ($0.8427$) é menor que o valor crítico do t ($2.011$) para um nível de significância de $0.05$ e $48$ graus de liberdade.
   - Portanto, a condição para rejeitar a hipótese nula não é atendida.
   - Consequentemente, NÃO rejeitamos $H_0$ ao nível de significância de $0.05$.

3. **Valor-p:**
   
   - O valor-p calculado ($0.4135$) é maior que o nível de significância ($0.05$).
   - Assim, a condição para rejeitar a hipótese nula não é atendida.
   - Concluímos que NÃO rejeitamos $H_0$ ao nível de significância de $0.05$.

**Resultado Final:**

Com base nas análises estatísticas realizadas, não há evidências estatísticas significativas para afirmar que há diferença no tempo de ação médio entre os produtos A e B. Portanto, ao nível de significância de $0.05$, não podemos concluir que um produto é superior ao outro em termos de tempo de ação. 


Portanto:



Recomendação: Produto A é mais econômico em termos de custo por unidade.

Essa recomendação é feita com base nos custos por unidade, independentemente das diferenças nos tempos de ação não serem estatisticamente significativas.




### O teste t-student pode ser aplicado para mais de duas populações?


O teste t-Student clássico, que é frequentemente usado para comparar as médias de duas amostras independentes, não é diretamente aplicável para comparar mais de duas populações de uma só vez. No entanto, existem extensões do teste t para comparações múltiplas, e uma delas é a Análise de Variância (ANOVA).

A ANOVA é um método estatístico projetado especificamente para lidar com a comparação de médias entre mais de dois grupos. Existem diferentes tipos de ANOVA, e a escolha do tipo depende da estrutura dos dados e das suposições subjacentes.


&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>
