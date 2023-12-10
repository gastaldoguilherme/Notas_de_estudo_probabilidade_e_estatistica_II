**Python - Estatística II** 
>**Distribuição Normal**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;


## Distribuição Normal

A distribuição normal, também conhecida como a distribuição de Gauss ou distribuição gaussiana, é uma distribuição contínua que desempenha um papel fundamental em estatísticas e probabilidade. Ela é simétrica em torno da média e possui a forma de sino. Aqui estão alguns conceitos-chave e fórmulas associadas à distribuição normal:



### Principais critérios para o uso da distribuição normal


1. **Distribuição da População:**
   - Os dados ou variáveis em estudo devem seguir uma distribuição normal na população. Isso significa que a forma da distribuição dos dados deve ser simétrica e em forma de sino.

2. **Média, Mediana e Moda Iguais:**
   - Na distribuição normal, a média, a mediana e a moda são todas iguais. Isso contribui para a simetria da distribuição.

3. **Parâmetros da Distribuição:**
   - A distribuição normal é totalmente caracterizada por dois parâmetros: a média (\(\mu\)) e o desvio padrão (\(\sigma\)). Portanto, esses parâmetros precisam ser conhecidos ou estimados a partir da amostra.

4. **Padronização (Z):**
   - Os cálculos envolvendo a distribuição normal frequentemente envolvem a padronização dos valores usando a variável padronizada \(Z\), que é obtida subtraindo a média e dividindo pelo desvio padrão (\(Z = \frac{(X - \mu)}{\sigma}\)). Isso facilita a comparação entre diferentes distribuições normais.

5. **Teorema do Limite Central:**
   - O Teorema do Limite Central afirma que a média de uma amostra suficientemente grande de uma população, independentemente da forma da população original, será aproximadamente distribuída normalmente.

6. **Intervalos de Confiança e Testes de Hipóteses:**
   - A distribuição normal é frequentemente utilizada para construir intervalos de confiança e realizar testes de hipóteses sobre a média de uma população quando o tamanho da amostra é grande.

7. **Variáveis Contínuas:**
   - A distribuição normal é mais apropriada para variáveis contínuas. Para variáveis discretas, uma aproximação normal pode ser válida se o número de categorias for grande.

8. **Simetria e Curtose:**
   - A distribuição normal é simétrica e possui uma curtose (medida da "pesca" das caudas da distribuição) de 0. A curtose maior ou menor que 0 indica caudas mais pesadas ou mais leves do que as da distribuição normal, respectivamente.



### Fórmulas Principais:

1. **Função de Densidade de Probabilidade (PDF):**
 
   $\huge f(x) = \displaystyle\frac{1}{\sqrt{2\pi\sigma^2}} \cdot e^{\displaystyle-\frac{(x - \mu)^2}{2\sigma^2}}$
   
   - **Variáveis:**
     - $x$: Variável aleatória
     - $\mu$: Média da distribuição
     - $\sigma$: Desvio padrão da distribuição
   - **Descrição:**
     - A PDF descreve a densidade de probabilidade em torno de um determinado valor $x$.

4. **Função de Distribuição Cumulativa (CDF):**

   $\huge F(x) = P(X \leq x) = \int_{-\infty}^{x} f(t) \, dt$
   
   - **Variáveis:**
     - $x$: Valor para o qual queremos calcular a probabilidade acumulada
   - **Descrição:**
     - A CDF fornece a probabilidade de que a variável aleatória seja menor ou igual a $x$.

### Testes de Hipótese:

1. **Teste Z para a Média ($\mu$):**

   $\huge Z = \displaystyle\frac{\bar{X} - \mu_0}{\displaystyle\frac{\sigma}{\sqrt{n}}}$
   
   - **Variáveis:**
     - $\bar{X}$: Média da amostra
     - $\mu_0$: Valor sob a hipótese nula
     - $\sigma$: Desvio padrão populacional conhecido
     - $n$: Tamanho da amostra
     - 
   - **Descrição:**
     - Usado quando o desvio padrão populacional é conhecido.

3. **Intervalo de Confiança para a Média ($\mu$):**

   $\huge \bar{X} \pm Z \left(\displaystyle \frac{\sigma}{\sqrt{n}} \right)$
   
   - **Variáveis:**
     - $\bar{X}$: Média da amostra
     - $Z$: Valor crítico da distribuição normal padrão (Z-score)
     - $\sigma$: Desvio padrão populacional conhecido
     - $n$: Tamanho da amostra
     - 
   - **Descrição:**
     - Usado para estimar um intervalo de confiança para a média populacional quando o desvio padrão populacional é conhecido.



&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>
