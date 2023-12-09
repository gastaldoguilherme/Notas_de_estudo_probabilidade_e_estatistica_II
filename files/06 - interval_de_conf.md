**Python - Estatística II** 
>**Intervalos de Confiança**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;



## Intervalos de Confiança

Um **intervalo de confiança (IC)** é uma estimativa estatística usada para quantificar a incerteza em torno de uma estimativa de parâmetro. Ele fornece uma faixa de valores dentro da qual é razoável supor que o verdadeiro valor do parâmetro populacional esteja com uma certa probabilidade.

Existem diferentes níveis de confiança, comummente expressos em termos de porcentagem, como 95% de confiança. Um intervalo de confiança de 95%, por exemplo, indica que se o experimento ou a amostragem fossem repetidos 100 vezes, esperaríamos que o intervalo incluísse o verdadeiro valor do parâmetro em cerca de 95 experimentos ou 95%.

### Fórmula Geral:

$\text{IC} = \text{Estimativa Pontual} \pm \text{Margem de Erro}$

A margem de erro é calculada com base no desvio padrão da amostra e no tamanho da amostra, juntamente com um valor crítico associado ao nível de confiança desejado.

### Exemplo 1:

A média populacional está estimada em $\mu = 50$ com um desvio padrão amostral de $\sigma = 10$. Com uma amostra de tamanho $n = 30$ e um nível de confiança de 95%, o intervalo de confiança para a média é:

```
Na tabela Z, você procuraria o valor que corresponde a uma área acumulada de 0.975 (considerando 2.5% de cada cauda para obter 95% no meio). Este valor é aproximadamente 1.96.

Portanto, para um intervalo de confiança de 95%, você usaria $Z = 1.96$ para calcular a margem de erro em torno da sua estimativa pontual.
```

$\bar{x} \pm Z \left( \frac{\sigma}{\sqrt{n}} \right)$

Substituindo os valores conhecidos:

$50 \pm 1.96 \left( \frac{10}{\sqrt{30}} \right)$


Esse é um exemplo básico, e os cálculos específicos podem variar dependendo do tipo de intervalo de confiança (por exemplo, para proporções ou desvios padrão) e da distribuição subjacente dos dados.


### Nível de Confiança:

| Nível de Confiança | Valor Crítico (Z) |
|---------------------|-------------------|
| 80%                 | 1.28              |
| 90%                 | 1.64              |
| 95%                 | 1.96              |
| 98%                 | 2.33              |
| 99%                 | 2.58              |



### Relações

1. **Nível de Confiança (NC) x Erro Padrão (EP):**
   - O nível de confiança está relacionado à probabilidade de que o intervalo de confiança construído contenha o verdadeiro parâmetro da população.
   - Aumentar o nível de confiança geralmente resulta em um intervalo de confiança mais amplo, pois você está exigindo uma maior certeza de que o parâmetro está contido no intervalo.
   - O erro padrão influencia a largura do intervalo de confiança; um erro padrão menor levará a um intervalo mais estreito.

2. **Tamanho da Amostra x Erro Padrão:**
   - O erro padrão é inversamente proporcional ao tamanho da amostra. Isso significa que, em geral, um aumento no tamanho da amostra leva a uma diminuição do erro padrão.
   - Quanto maior o tamanho da amostra, mais precisa é a estimativa da média populacional ou de outros parâmetros, resultando em uma redução do erro padrão.
   - Um tamanho de amostra grande tende a produzir estimativas mais confiáveis e intervalos de confiança mais estreitos.

3. **Nível de Confiança x Tamanho da Amostra:**
   - Existe uma relação indireta entre o nível de confiança e o tamanho da amostra. Se você deseja aumentar o nível de confiança, muitas vezes precisa aumentar o tamanho da amostra para manter a largura do intervalo de confiança aceitável.
   - Aumentar o tamanho da amostra pode ser necessário para atender a requisitos específicos de precisão quando se trabalha com intervalos de confiança mais elevados.



4. **Variabilidade dos Dados:**
   - Quanto maior a variabilidade dos dados na amostra, maior será o erro padrão e, consequentemente, mais amplo será o intervalo de confiança, mantendo os outros fatores constantes.

5. **Distribuição dos Dados:**
   - Em certas situações, quando a distribuição dos dados é desconhecida ou não é normal, os intervalos de confiança podem ser ajustados usando métodos diferentes, como intervalos de confiança bootstrap.

6. **Assimetria da Distribuição:**
   - Em distribuições assimétricas, os intervalos de confiança podem não ser simétricos. Métodos como o intervalo de confiança assimétrico podem ser aplicados nessas situações.

7. **Precisão vs. Custo:**
   - Aumentar a precisão do intervalo de confiança geralmente requer um aumento no tamanho da amostra, o que pode aumentar os custos. Existirá, portanto, um equilíbrio entre a precisão desejada e os recursos disponíveis.

8. **Estimativas Pontuais:**
   - O ponto estimado (média, proporção, etc.) também influencia a largura do intervalo de confiança. Estimativas menos precisas tendem a resultar em intervalos de confiança mais amplos.

9. **Aplicação Prática:**
   - Em muitos casos, a escolha do nível de confiança e do tamanho da amostra é uma decisão prática e depende das implicações do erro, da variabilidade dos dados e dos recursos disponíveis.

1. **Relação com Testes de Hipóteses:**
   - Intervalos de confiança estão intrinsecamente relacionados a testes de hipóteses. Se um intervalo de confiança não incluir um valor específico, pode-se rejeitar uma hipótese nula associada.

&nbsp;

### Tipos de intervalos de confiança


Existem diferentes tipos de intervalos de confiança, e a escolha do tipo de intervalo de confiança depende do parâmetro que está sendo estimado e das características dos dados. Aqui estão alguns tipos comuns:

1. **Intervalo de Confiança para a Média:**
   - Usado para estimar a média populacional com base em uma amostra. Geralmente utiliza a distribuição normal ou a distribuição t de Student, dependendo do tamanho da amostra.

2. **Intervalo de Confiança para a Proporção:**
   - Utilizado quando se está estimando a proporção de uma característica em uma população com base em uma amostra. Usa a distribuição normal ou a distribuição binomial, dependendo do tamanho da amostra.

3. **Intervalo de Confiança para a Diferença de Médias:**
   - Aplicado quando se compara a média de duas amostras independentes. A distribuição normal ou a distribuição t de Student são comumente usadas.

4. **Intervalo de Confiança para a Diferença de Proporções:**
   - Utilizado ao comparar duas proporções em amostras independentes. A distribuição normal ou a distribuição binomial podem ser aplicadas.

5. **Intervalo de Confiança para a Variância e Desvio Padrão:**
   - Usado para estimar a variabilidade ou a dispersão dos dados. Normalmente envolve a distribuição qui-quadrado.

6. **Intervalo de Confiança para a Mediana:**
   - Aplicado quando a mediana é de interesse em vez da média. Pode ser construído usando métodos como o intervalo de confiança bootstrap.

7. **Intervalo de Confiança para a Razão de Chances (Odds Ratio):**
   - Usado em estudos de caso-controle para estimar a associação entre duas variáveis categóricas. Envolve a distribuição log-normal.

8. **Intervalo de Confiança para a Correlação:**
   - Aplicado quando se deseja estimar a força e a direção da relação linear entre duas variáveis. Geralmente usa a distribuição t de Student.

Estes são apenas alguns exemplos e a escolha do intervalo de confiança depende da natureza específica da análise estatística e do parâmetro de interesse. Em muitos casos, a distribuição normal é utilizada para tamanhos de amostra grandes, enquanto a distribuição t de Student é mais apropriada para tamanhos de amostra menores. O intervalo de confiança bootstrap é uma abordagem mais flexível que não depende de suposições específicas sobre a distribuição dos dados.


---

### Intervalo de Confiança para a Média:

#### Fórmula Geral:

$\bar{x} \pm Z \left(\displaystyle \frac{s}{\sqrt{n}} \right)$

- $\bar{x}$: média da amostra
- $Z$: valor crítico da distribuição normal ou t de Student (dependendo do tamanho da amostra e do nível de confiança)
- $s$: desvio padrão da amostra
- $n$: tamanho da amostra

### Exemplo 2:


**Exemplo de Intervalo de Confiança para Média:**

Suponha que um pesquisador coletou dados sobre os salários de 100 Vendedores. O desvio padrão populacional é conhecido e é de R$1.100,00. A média amostral desses salários é de R$5.800,00.

**Dados:**
- Tamanho da amostra ($n$): 100 pesquisados
- Intervalo de Confiança ($IC$): 95%
- Desvio Padrão Populacional ($\sigma$): R$1.100,00
- Média Amostral ($\bar{x}$): R$5.800,00

**1. Fórmula do Intervalo de Confiança para Média:**

$\text{Intervalo de Confiança} = \bar{x} \pm Z \left(\frac{\sigma}{\sqrt{n}}\right)$

Onde $Z$ é o valor crítico da distribuição normal padrão associado ao nível de confiança escolhido.

**2. Valor Crítico ($Z$):**

Para um intervalo de confiança de 95%, o valor crítico é $Z = 1,96$.

**3. Substituindo Valores:**

$\text{Intervalo de Confiança} = 5.800 \pm 1,96 \left(\frac{1.100}{\sqrt{100}}\right)$

$\text{Intervalo de Confiança} = 5.800 \pm 1,96 \times 110$

**4. Calculando o Intervalo:**

$\text{Intervalo de Confiança} =\$  [R$5.584.40 ;  R$6.015,60] 

**Interpretação:**
Com 95% de confiança, podemos afirmar que a média salarial dos Vendedores está estimada para estar entre R$5.584.40 e R$6.015,60. Isso significa que se coletássemos várias amostras e calculássemos intervalos de confiança para a média, esperaríamos que 95% desses intervalos incluíssem a verdadeira média salarial da população de Vendedores.

```
from scipy.stats import norm
import numpy as np

# Dados do problema
media_amostral = 5800
desvio_padrao = 1100
tamanho_amostra = 100
nivel_confianca = 0.95

# Calculando o erro padrão da média
erro_padrao_media = desvio_padrao / np.sqrt(tamanho_amostra)

# Calculando o intervalo de confiança
z_score = norm.ppf((1 + nivel_confianca) / 2)  # Valor crítico baseado no nível de confiança
intervalo_confianca = (
    media_amostral - z_score * erro_padrao_media,
    media_amostral + z_score * erro_padrao_media
)

# Imprimindo o resultado
print(f"Intervalo de Confiança (95%): {intervalo_confianca}")

```

```

Intervalo de Confiança (95%): (5584.403961700594, 6015.596038299406)
```


---



### Intervalo de Confiança para a Proporção:

#### Fórmula Geral:

$\hat{p} \pm Z \sqrt{\displaystyle \frac{\hat{p}(1-\hat{p})}{n}}$

- $\hat{p}$: proporção da amostra
- $Z$: valor crítico da distribuição normal
- $n$: tamanho da amostra

### Exemplo 3:

**Exercício: Intervalo de Confiança para a Proporção de Apoio ao Candidato A**

Suponha que uma pesquisa eleitoral tenha sido realizada para uma eleição de candidatos, e os resultados foram os seguintes:

- Tamanho da amostra ($n$): 1000 pesquisados
- Intervalo de Confiança ($IC$): 95%
- Candidato A: 650 votos
- Candidato B: 330 votos
- Não sabem: 20 votos

**1. Proporção de Apoio ao Candidato A:**

$\text{Proporção} (\hat{p}) =\displaystyle  \frac{\text{Número de votos para o Candidato A}}{\text{Tamanho da amostra total}}$

$\hat{p} = \displaystyle \frac{650}{1000} = 0,65$




**2. Erro Padrão da Proporção:**

$SE(\hat{p}) = \sqrt{\displaystyle \frac{\hat{p}(1 - \hat{p})}{n}}$

$SE(\hat{p}) = \sqrt{\displaystyle \frac{0,65 \times (1 - 0,65)}{1000}}$

**3. Valor Crítico Z para um Intervalo de Confiança de 95%:**

Para um intervalo de confiança de 95%, o valor crítico Z é aproximadamente 1,96.

**4. Intervalo de Confiança para a Proporção:**

$\text{Intervalo de Confiança} = \hat{p} \pm Z \times SE(\hat{p})$

Substituindo os valores conhecidos:

$\text{Intervalo de Confiança} = 0,65 \pm 1,96 \times \sqrt{\displaystyle \frac{0,65 \times (1 - 0,65)}{1000}}$

**5. Resolução em Python:**

```python
from math import sqrt
from scipy.stats import norm

# Dados do problema
votos_candidato_A = 650
tamanho_amostra = 1000
nivel_confianca = 0.95

# Proporção de apoio ao Candidato A
proporcao_A = votos_candidato_A / tamanho_amostra

# Erro padrão da proporção
erro_padrao_proporcao = sqrt((proporcao_A * (1 - proporcao_A)) / tamanho_amostra)

# Valor crítico Z para um intervalo de confiança de 95%
z_score = norm.ppf((1 + nivel_confianca) / 2)

# Intervalo de Confiança
intervalo_confianca = (proporcao_A - z_score * erro_padrao_proporcao,
                       proporcao_A + z_score * erro_padrao_proporcao)

# Imprimindo o resultado
print(f"Intervalo de Confiança para a Proporção de Apoio ao Candidato A: {intervalo_confianca}")
```

```

Intervalo de Confiança para a Proporção de Apoio ao Candidato A: (0.6204376610920599, 0.6795623389079402)

```
### Conclusão:

A conclusão a partir do resultado do intervalo de confiança para a proporção de apoio ao Candidato A é que, com 95% de confiança, a verdadeira proporção de votos para o Candidato A na população está estimada para estar entre aproximadamente 62,04% e 67,96%.




&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>
