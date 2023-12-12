**Python - Estatística II** 
>**Distribuição t de Student**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;

## Distribuição t de Student

A distribuição t de Student é uma distribuição de probabilidade contínua que surge em situações em que a amostra é pequena e o desvio padrão populacional é desconhecido. Ela é utilizada para realizar inferências estatísticas sobre a média populacional quando trabalhamos com amostras pequenas. Aqui estão alguns conceitos-chave e fórmulas associadas à distribuição t de Student:



### Principais critérios para o uso da distribuição t de Student


1. **Amostra Aleatória:**
   - Os dados devem ser obtidos por meio de uma amostra aleatória ou um processo que simule uma amostra aleatória.

2. **Distribuição Normal ou Amostra Grande:**
   - A distribuição da população subjacente dos dados deve ser aproximadamente normal ou a amostra deve ser grande o suficiente para garantir que a média amostral se aproxime de uma distribuição normal de acordo com o Teorema do Limite Central.

3. **Desconhecimento do Desvio Padrão Populacional:**
   - O desvio padrão populacional é desconhecido e precisa ser estimado a partir da amostra.

4. **Variáveis Contínuas:**
   - A variável de interesse deve ser contínua.

5. **Intervalo de Confiança ou Teste de Hipóteses para Médias:**
   - A distribuição t é comumente usada para intervalos de confiança ou testes de hipóteses envolvendo a média populacional, especialmente quando o desvio padrão populacional não é conhecido.

6. **Amostras Pequenas:**
   - Quando o tamanho da amostra é pequeno (geralmente $ n \leq 30 $).
   - É especialmente útil em situações com amostras pequenas, onde a distribuição t de Student se aproxima mais da distribuição normal do que a distribuição normal padrão (z) devido à incerteza introduzida pela estimativa do desvio padrão populacional.

7. **Pressuposto da Homocedasticidade (para testes de médias):**
   - Para testes de médias, assume-se que as variabilidades nas diferentes amostras são aproximadamente iguais (homocedasticidade).

8. **Pressuposto da Independência:**
   - As observações dentro da amostra devem ser independentes.

A distribuição t de Student é especialmente útil em situações em que a amostra é pequena e o desvio padrão populacional é desconhecido. Se a amostra for grande, a distribuição t se aproxima da distribuição normal padrão (z).


### Fórmulas Principais:

1. **Intervalo de Confiança para a Média ($\mu$) com Amostra Pequena:**

   $\huge\bar{X} \pm t \left( \frac{s}{\sqrt{n}} \right)$
   
   - **Variáveis:**
     - $\bar{X}$: Média da amostra
     - $t$: Valor crítico da distribuição t de Student com $ n-1 $ graus de liberdade
     - $s$: Desvio padrão da amostra
     - $n$: Tamanho da amostra
     - 
   - **Descrição:**
     - Usado para estimar um intervalo de confiança para a média populacional quando o desvio padrão populacional é desconhecido.

3. **Estatística de Teste t para a Média ($ \mu $):**

   $\huge t =\displaystyle \frac{\bar{X} - \mu_0}{\displaystyle\frac{s}{\sqrt{n}}}$
   - **Variáveis:**
     - $\bar{X}$: Média da amostra
     - $\mu_0$: Valor sob a hipótese nula
     - $s$: Desvio padrão da amostra
     - $n$: Tamanho da amostra
     - 
   - **Descrição:**
     - Usado para realizar testes de hipótese sobre a média populacional quando o desvio padrão populacional é desconhecido.




### Erro padrão


A distribuição t de Student é frequentemente utilizada em inferência estatística quando estamos lidando com médias de amostras pequenas e a variância populacional é desconhecida. O erro padrão, nesse contexto, está relacionado à precisão da estimativa da média amostral em relação à média populacional.

O erro padrão da média (também conhecido como erro padrão da amostra ou desvio padrão padrão) é calculado usando a fórmula:

$\huge SE = \displaystyle \frac{s}{\sqrt{n}}$

onde:
- $s$ é o desvio padrão amostral,
- $n$ é o tamanho da amostra.

Esse valor é utilizado para calcular intervalos de confiança para a média ou para realizar testes de hipóteses sobre a média populacional quando a variância populacional é desconhecida.

A distribuição t de Student é utilizada para calcular valores críticos (t crítico) para determinado nível de confiança e graus de liberdade (n-1, onde $n$ é o tamanho da amostra). Esses valores críticos são utilizados para construir intervalos de confiança e realizar testes de hipóteses.

Por exemplo, para um intervalo de confiança de 95% e uma amostra com $n$ graus de liberdade, aproximadamente 95% das médias amostrais estarão dentro do intervalo $\bar{X} \pm t_{\alpha/2} \times SE$, onde $ \bar{X}$ é a média amostral, $t_{\alpha/2}$ é o valor crítico da distribuição t e $SE$ é o erro padrão da média.

A fórmula geral para um intervalo de confiança é:

$\huge \bar{X} \pm t_{\alpha/2} \times SE$

   
---


### Intervalo de confiança para a diferença de médias de duas amostras independentes, SEM variâncias populacionais iguais 


O intervalo de confiança para a diferença de médias de duas amostras independentes, quando as populações não têm variâncias iguais e a distribuição amostral segue uma distribuição t de Student, pode ser expresso da seguinte forma:

$\huge\displaystyle \bar{X}_1 - \bar{X}_2 \pm t \times \sqrt{\left(\frac{s_1^2}{n_1}\right) + \left(\frac{s_2^2}{n_2}\right)}$

Onde:

- $\bar{X}_1$ e $\bar{X}_2$ são as médias das duas amostras.
- $s_1$ e $s_2$ são os desvios padrão das amostras.
- $n_1$ e $n_2$ são os tamanhos das amostras.
- $t$ é o valor crítico da distribuição t de Student com graus de liberdade $df$ calculados usando a fórmula:

$df = \displaystyle  \frac{\left(\displaystyle \frac{s_1^2}{n_1} + \displaystyle \frac{s_2^2}{n_2}\right)^2}{\displaystyle \frac{\left(\displaystyle  \frac{\displaystyle \frac{s_1^2}{n_1}}{n_1-1}\right)^2}{n_1-1} + \displaystyle  \frac{\left(\displaystyle  \frac{\displaystyle  \frac{s_2^2}{n_2}}{n_2-1}\right)^2}{n_2-1}}$

O intervalo de confiança é construído em torno da estimativa pontual da diferença das médias, $\bar{X}_1 - \bar{X}_2$, com a margem de erro determinada pelo desvio padrão padrão (erro padrão) multiplicado pelo valor crítico t. O valor crítico t é escolhido com base no nível de confiança desejado e nos graus de liberdade associados.

Lembrando que essas fórmulas assumem que as amostras são independentes e que as populações não têm variâncias iguais. Se as variâncias populacionais forem assumidas iguais (homocedasticidade), você pode usar uma versão simplificada da fórmula.

### Exemplo


Graus de liberdade $df$ calculados usando a fórmula:


```
def calculate_df(n1, s1, n2, s2):
    numerator = ((s1**2 / n1) + (s2**2 / n2))**2
    denominator = (1 / (n1 - 1)) + (1 / (n2 - 1))
    denominator *= ((1 / (n1 - 1)) * ((s1**2 / n1)**2) + (1 / (n2 - 1)) * ((s2**2 / n2)**2))
    denominator *= ((n1 * s1**2 + n2 * s2**2)**2) / (n1**2 * (n1 - 1) + n2**2 * (n2 - 1))
    
    df = numerator / denominator
    return df

# Dados da amostra
n1 = 20
s1 = 4

n2 = 25
s2 = 5

# Calcular df
df = calculate_df(n1, s1, n2, s2)

print("O valor do grau de liberdade (df) é:", df)


```
```
O valor do grau de liberdade (df) é: 11.53979003410661

```
O valor calculado para o grau de liberdade ($df$) é aproximadamente 11.54. Lembre-se de que, na prática, os graus de liberdade são geralmente arredondados para o inteiro mais próximo ao usar a distribuição t de Student em análises estatísticas. Portanto, você pode arredondar esse valor para o número inteiro mais próximo, dependendo das convenções do seu contexto específico.

Este valor de $df$ seria utilizado ao realizar um teste de hipóteses para a diferença de médias entre as duas amostras, assumindo variâncias populacionais diferentes e seguindo uma distribuição t de Student.

--- 

### Intervalo de confiança para a diferença de médias de duas amostras independentes, COM variâncias populacionais iguais 



Se assumirmos variâncias populacionais iguais (homocedasticidade), a fórmula do intervalo de confiança para a diferença de médias de duas amostras independentes é simplificada. Nesse caso, utilizamos a variância combinada ponderada. A fórmula do intervalo de confiança é dada por:

$\bar{X}_1 - \bar{X}_2 \pm t \times \sqrt{\displaystyle\left(\displaystyle \frac{s_p^2}{n_1}\right) + \left(\displaystyle \frac{s_p^2}{n_2}\right)}$

onde:

- $\bar{X}_1$ e $\bar{X}_2$ são as médias das duas amostras.
- $s_p^2$ é a variância combinada ponderada, calculada por:

$s_p^2 = \displaystyle\frac{(n_1 - 1)s_1^2 + (n_2 - 1)s_2^2}{n_1 + n_2 - 2}$

- $n_1$ e $n_2$ são os tamanhos das amostras.
- $t$ é o valor crítico da distribuição t de Student com graus de liberdade $df = n_1 + n_2 - 2$, com base no nível de confiança desejado.

A principal diferença em relação à fórmula anterior é o uso da variância combinada ponderada $s_p^2$ em vez de calcular os graus de liberdade separadamente para cada amostra. Essa versão é apropriada quando se pode assumir que as variâncias populacionais são iguais.

--- 





### Exercícios:


### 1) Diâmetro de esferas de rolamento

Os dados fornecidos representam o diâmetro, em milímetros, de 30 esferas de rolamento produzidas por uma máquina:

|   |   |   |   |   |   |   |   |   |   |
|---|---|---|---|---|---|---|---|---|---|
|137|154|159|155|167|159|158|159|152|169|
|154|158|140|149|145|157|160|155|155|143|
|157|139|159|139|129|162|151|150|134|151|


#### a) Intervalo de Confiança para a Média

Construa um intervalo de confiança, a 95%, para a média da população de todas as esferas produzidas pela máquina.


```
import numpy as np
from scipy import stats

# Dados fornecidos
dados = np.array([137, 154, 159, 155, 167, 159, 158, 159, 152, 169,
                  154, 158, 140, 149, 145, 157, 160, 155, 155, 143,
                  157, 139, 159, 139, 129, 162, 151, 150, 134, 151])

# Nível de confiança desejado
confianca = 0.95

# Calculando o intervalo de confiança para a média
media_amostral = np.mean(dados)
desvio_padrao_amostral = np.std(dados, ddof=1)  # Usando ddof=1 para ajuste do desvio padrão amostral
erro_padrao = stats.sem(dados)

# Obtendo o intervalo de confiança para a média
intervalo_confianca_media = stats.t.interval(confianca, len(dados) - 1, loc=media_amostral, scale=erro_padrao)

print("media_amostral:", media_amostral)
print("desvio_padrao_amostral:", desvio_padrao_amostral)
print("erro_padrao:", erro_padrao)
print("Valor Crítico t_0,975:", valor_critico)
print("Intervalo de Confiança para a Média:", intervalo_confianca_media)


```

```
media_amostral: 151.86666666666667
desvio_padrao_amostral: 9.712179816169446
erro_padrao: 1.7731933226207943
Valor Crítico t_0,975: 2.045229642132703
Intervalo de Confiança para a Média: (148.24007912201085, 155.4932542113225)

```



#### b) Intervalo de Confiança para a Proporção

Suponha que, para satisfazer as especificações do consumidor, as peças devem ter diâmetro entre 140 e 160 mm. Determine um intervalo de confiança de 98% para a verdadeira proporção de peças fabricadas pela máquina que satisfazem essas especificações.

```python

# Definindo o intervalo especificado pelo consumidor
limite_inferior = 140
limite_superior = 160

# Calculando a proporção de peças que estão dentro das especificações
pecas_dentro_especificacoes = np.sum((dados >= limite_inferior) & (dados <= limite_superior))
proporcao_dentro_especificacoes = pecas_dentro_especificacoes / len(dados)

# Nível de confiança para a proporção
confianca_proporcao = 0.98

# Obtendo o valor crítico
z_score = norm.ppf((1 + 0.98) / 2)

# Calculando o intervalo de confiança para a proporção
erro_padrao_proporcao = np.sqrt((proporcao_dentro_especificacoes * (1 - proporcao_dentro_especificacoes)) / len(dados))


# Calculando Intervalo de confiança
intervalo_confianca_proporcao_inf = proporcao_dentro_especificacoes -(z_score * erro_padrao_proporcao )
intervalo_confianca_proporcao_sup = proporcao_dentro_especificacoes +(z_score * erro_padrao_proporcao )


intervalo_confianca_proporcao2 = stats.norm.interval(confianca_proporcao, loc=proporcao_dentro_especificacoes, scale=erro_padrao_proporcao)


print("pecas_dentro_especificacoes:", pecas_dentro_especificacoes)
print("proporcao_dentro_especificacoes:", proporcao_dentro_especificacoes)
print("z_score :", z_score )
print("erro_padrao_proporcao:", erro_padrao_proporcao)

print("intervalo_confianca_proporcao_inf:", intervalo_confianca_proporcao_inf)
print("intervalo_confianca_proporcao_sup:", intervalo_confianca_proporcao_sup)
print("Intervalo de Confiança para a Proporção 2:", intervalo_confianca_proporcao2)

```

```
pecas_dentro_especificacoes: 22
proporcao_dentro_especificacoes: 0.7333333333333333
z_score : 2.3263478740408408
erro_padrao_proporcao: 0.08073734277593311
intervalo_confianca_proporcao_inf: 0.5455101876108346
intervalo_confianca_proporcao_sup: 0.921156479055832
Intervalo de Confiança para a Proporção 2: (0.5455101876108346, 0.921156479055832)


```



### 2) Intervalo de Confiança para o Índice Cardíaco Médio

Foi conduzida uma pesquisa envolvendo uma amostra de 600 pacientes de um hospital específico. Cada um desses pacientes foi submetido a uma série de exames clínicos, incluindo a medição do Índice Cardíaco (em litros/min/m²). Os 600 pacientes foram aleatoriamente divididos em 40 grupos de 15 pacientes cada. Para um desses grupos, os valores medidos do Índice Cardíaco foram: 405, 348, 365, 291, 135, 260, 300, 155, 34, 294, 758, 472, 559, 143, 172.

#### (a) Intervalo de Confiança para a Média ($ \mu $) do Índice Cardíaco ao nível de 95%

```python

import numpy as np
from scipy import stats

# Dados fornecidos
indice_cardiaco_grupo = np.array([405, 348, 365, 291, 135, 260, 300, 155, 34, 294, 758, 472, 559, 143, 172])

# Nível de confiança desejado
confianca = 0.95

# Tamanho da amostra
n = len(indice_cardiaco_grupo)

# Média e desvio padrão amostral
media_amostral = np.mean(indice_cardiaco_grupo)
desvio_padrao_amostral = np.std(indice_cardiaco_grupo, ddof=1)

# Erro padrão da média
erro_padrao = desvio_padrao_amostral / np.sqrt(n)

# Calculando o intervalo de confiança para a média
intervalo_confianca = stats.t.interval(confianca, n - 1, loc=media_amostral, scale=erro_padrao)

print("Intervalo de Confiança para a Média do Índice Cardíaco:", intervalo_confianca)


```

```
Intervalo de Confiança para a Média do Índice Cardíaco: (209.84029996080437, 415.6263667058623)

```





O intervalo de confiança para a média do Índice Cardíaco é calculado com base nos valores fornecidos, utilizando a distribuição t de Student, com um nível de confiança de 95%.

#### (b) Quantidade de Intervalos que Não Contêm a Verdadeira Média Populacional

Ao construir um Intervalo de Confiança para $ \mu $ para cada um dos 40 grupos de 15 pacientes ao nível de 95%, espera-se que alguns desses intervalos não contenham a verdadeira média populacional. Isso ocorre devido à variabilidade amostral. O número esperado de intervalos que não contêm a verdadeira média é calculado teoricamente.


```
# Número de grupos
num_grupos = 40

# Probabilidade de não conter a verdadeira média populacional
prob_nao_conter = 1 - confianca

# Número esperado de intervalos que não contêm a verdadeira média
num_esperado_nao_conter = prob_nao_conter * num_grupos

print(f"Número esperado de intervalos que não contêm a verdadeira média: {num_esperado_nao_conter}")
```


```
Número esperado de intervalos que não contêm a verdadeira média: 2.0000000000000018
```



### 3) Comparando métodos de ensino de Matemática

Os 36 alunos de uma turma foram divididos aleatoriamente em dois grupos de 18 cada. No primeiro grupo, o ensino de Matemática é realizado utilizando elementos de multimídia, enquanto no segundo grupo é utilizado o método tradicional (quadro negro e giz). Ao final do período, é aplicado um teste comum aos dois grupos, resultando nos seguintes dados:

**Grupo 1:** 7,3 8,2 6,0 7,7 8,0 6,1 5,6 5,3 5,9 5,8 5,8 7,1 5,1 8,0 7,6 8,3 4,9 6,5

**Grupo 2:** 7,5 6,2 5,7 4,4 4,7 5,8 5,0 6,0 6,5 5,8 4,5 5,1 5,5 6,0 5,8 5,8 5,7 7,5

Considerando os dois grupos como amostras aleatórias de duas populações independentes e normalmente distribuídas, deseja-se determinar um intervalo de confiança de 95% para a verdadeira diferença das médias populacionais dos dois grupos. 

#### Solução:

Se assumirmos variâncias populacionais iguais (homocedasticidade), a fórmula do intervalo de confiança para a diferença de médias de duas amostras independentes é simplificada. Nesse caso, utilizamos a variância combinada ponderada. A fórmula do intervalo de confiança é dada por:

$\bar{X}_1 - \bar{X}_2 \pm t \times \sqrt{\displaystyle\left(\displaystyle \frac{s_p^2}{n_1}\right) + \left(\displaystyle \frac{s_p^2}{n_2}\right)}$

onde:

- $\bar{X}_1$ e $\bar{X}_2$ são as médias das duas amostras.
- $s_p^2$ é a variância combinada ponderada, calculada por:

$s_p^2 = \displaystyle\frac{(n_1 - 1)s_1^2 + (n_2 - 1)s_2^2}{n_1 + n_2 - 2}$




```
import numpy as np
from scipy import stats

# Dados fornecidos
grupo1 = np.array([7.3, 8.2, 6.0, 7.7, 8.0, 6.1, 5.6, 5.3, 5.9, 5.8, 5.8, 7.1, 5.1, 8.0, 7.6, 8.3, 4.9, 6.5])
grupo2 = np.array([7.5, 6.2, 5.7, 4.4, 4.7, 5.8, 5.0, 6.0, 6.5, 5.8, 4.5, 5.1, 5.5, 6.0, 5.8, 5.8, 5.7, 7.5])

# Nível de confiança desejado
confianca = 0.95

# Tamanho das amostras
n1 = len(grupo1)
n2 = len(grupo2)

# Médias e desvios padrão amostrais
media1 = np.mean(grupo1)
media2 = np.mean(grupo2)
desvio_padrao1 = np.std(grupo1, ddof=1)
desvio_padrao2 = np.std(grupo2, ddof=1)

# Diferença entre as médias
diferenca_medias = media1 - media2

# Erro padrão da diferença entre as médias
erro_padrao_diferenca = np.sqrt((desvio_padrao1**2 / n1) + (desvio_padrao2**2 / n2))

# Graus de liberdade
graus_de_liberdade = n1 + n2 - 2

# Obtendo o valor crítico da distribuição t de Student
valor_critico_t = stats.t.ppf((1 + confianca) / 2, graus_de_liberdade)

# Calculando o intervalo de confiança para a diferença das médias
intervalo_confianca_diferenca = (diferenca_medias - valor_critico_t * erro_padrao_diferenca,
                                  diferenca_medias + valor_critico_t * erro_padrao_diferenca)

print("Intervalo de Confiança para a Diferença das Médias:", intervalo_confianca_diferenca)
```


```
Intervalo de Confiança para a Diferença das Médias: (0.1839745617601024, 1.560469882684341)
```











&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>
