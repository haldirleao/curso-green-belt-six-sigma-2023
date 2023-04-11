## Curso Green Belt Six Sigma - projeto 04/2023
## Aula 13: Analisar do DMAIC.

Conteúdo de 42 a 45 do cronograma.

Data da entrega: 10/04/2023

Autor: [@haldirleao](https://github.com/haldirleao)

## Faça um resumo sobre os vídeos abordados nesta aula

### 42 GRÁFICO DE DISPERSÃO

Os conteúdos desta aula são aplicados para **validar a causa-raiz**, último passo do **Analisar do DMAIC**. A validação é feita com o uso de ferramentas estatísticas, com intervalo de confiança de 95%.

A validação é o estudo do relacionamento entre variáveis:
- $x$ : **Causas**. Entrada, variável independente, controlável
- $y$ : **Efeitos dos defeitos/causas**. Saída, variável dependente.

O que ocorre com a variável y (efeito) quando x (causa)varia?
- pode aumentar
- pode diminuir
- pode não variar
- pode variar aleatoriamente

O primeiro passo para validar uma causa raiz é **verificar a relação entre as variáveis**. Na aula foi apresentado o **Gráfico de Dispersão** para visualização da **relação** entre os **pares de variáveis**.

Para se construir um Diagrama de Dispersão:
- Colete os dados aos pares
  - deve haver, no mínimo, 30 pares de dados
  - as amostras de dados devem ser representativos da população 
- Desenhe o eixo horizontal e o vertical
  - os eixos não necessariamente precisam começar do zero

Caminho no Minitab: **_Gráfico >> Gráfico de dispersão..._** 

Com a **observação visual do Gráfico de Dispersão** é possível afirmar, **qualitativamente, se existe, ou não, relação entre as variáveis**. Já para verificar a **força** desta relação será utilizada a **correlação linear**.

### 43 CORRELAÇÃO LINEAR

A **Correlação Linear**, também conhecida como **Coeficiente de Correlação de Pearson**, é usada para **quantificar a força** de uma relação entre variáveis.

A análise correlacional indica a relação entre 2 variáveis lineares e os **valores** sempre serão entre **-1 e +1**. O sinal indica a direção, se a correlação é positiva ou negativa, e o tamanho da variável indica a força da correlação.

![Fórmula do Coeficiente de Correlação de Pearson, fonte QuickLatex (cor da fonte: #096DFE).](https://quicklatex.com/cache3/c7/ql_616be020b6cfce2d35a746c3a45fdfc7_l3.png)

- **+1** : correlação positiva perfeita
- **-1** : correlação negativa perfeita
- **0**  : sem correlação

Segundo a Wikipedia, a interpretação de r é:
- ± 0.9 a 1.0 indica uma correlação muito forte.
- ± 0.7 a 0.9 indica uma correlação forte.
- ± 0.5 a 0.7 indica uma correlação moderada.
- ± 0.3 a 0.5 indica uma correlação fraca.
- ± 0.0 a 0.3 indica uma correlação desprezível.


### 44 EXEMPLO - CORRELAÇÃO LINEAR

Caminho no Minitab: **_Estat >> Estatísticas básicas >> Correlação..._**.

No exemplo dado é buscada a correlação entre peso (y) e comprimento (x). O resultado foi de **r = 0,883**, que **quantifica uma forte correlação positiva**. 

No Minitab, além do $r_{x,y}$, a interpretação também pode ser feita com base no valor-p. Na aula foi sugerido:
- $p \le 0,05$ : Existe correlação
- $p > 0,05$ : Não existe correlação

O valor-p do exemplo foi de 0,000. Logo, existe correlação.

### 45 REGRESSÃO LINEAR

Com a **regressão linear** é possível definir a **equação matemática** que rege a **relação entre as duas variáveis**. Tal regressão é plausível quando a **correlação** entre as variáveis é **forte**. Cuidado: não aplique para casos com correlação fraca!

A equação da reta de uma regressão linear simples é dada por:

$y = ax + b$

Onde a e b são parâmetros.

Com a regressão, podemos:
- **Prever** o valor de y a partir do valor de x.
- **Estimar** quanto x influencia ou modifica y.

## Apresente os pontos mais importantes

- Com o **gráfico de dispersão** é possível observar se **existe, ou não, relação entre pares de variáveis**. Exemplo: relação entre uma causa (x) e um efeito (y). O resultado é **qualitativo**.
- Com a **Correlação Linear**, também conhecida como Coeficiente de Correlação de Pearson, é possível **quantificar a força de uma relação entre variáveis**.
- O valor da correlação linear sempre será entre **-1 e +1**.
- A regressão linear somente deve ser aplicada com a correlação linear das variáveis é forte (r ≈ ± 0.7 a ± 1.0).

## Referências
- Videoaulas 42 a 45 https://vimeo.com/showcase/9985114 (Acesso restrito aos alunos)
- https://pt.wikipedia.org/wiki/Intervalo_de_confian%C3%A7a
- https://pt.wikipedia.org/wiki/Coeficiente_de_correla%C3%A7%C3%A3o_de_Pearson
- 