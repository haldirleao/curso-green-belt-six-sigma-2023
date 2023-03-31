## Curso Green Belt Six Sigma - projeto 04/2023
## Aula 07: Medir do DMAIC.

Conteúdo de 3.9.1 a 3.9.5 do cronograma.

Data da entrega: 20/03/2023

Autor: [@haldirleao](https://github.com/haldirleao)

## Faça um resumo sobre os vídeos abordados nesta aula

### 3.9.1 BOXPLOT

Representa em um **gráfico de caixa** os seguintes valores de um **conjunto de dados**: 
- Valor mínimo
- Q1 (primeiro quartil ou quartil inferior)
- Q2 (Mediana)
- Q3 (terceiro quartil ou quartil superior)
- Valor máximo

Caminho no Minitab: **_menu Gráfico >> Box plot…_** 

Um **valor atípico (_outlier_)** é aquele muito afastado da grande maioria dos dados. Não significa, necessariamente, que seja um dado errado. **Exemplo**: Em um _dataset_ os dados são <=10, com exceção de um valor 16, logo, 16 é um valor atípico.
Considerar atípicos os valores x tais que:
- $x < Q_1 - (1,5 \times AIQ)$

ou

- $x > Q_3 + (1,5 \times AIQ)$  

Onde $AIQ = Q_3 - Q_1$. (Amplitude interquartil, que é igual ao “tamanho da caixa”).

Se o dado **_outlier_** realmente existir, ok, nada a alterar. Se for algum erro (de coleta, de transcrição, etc), corrigir.

### 3.9.2 GRÁFICO SEQUENCIAL (ou TEMPORAL)

São diagramas simples onde os **dados são ordenados pelo tempo**.

Caminho no Minitab: menu **_Gráfico >> Gráficos de séries temporais…_**

Nos exemplos dados criamos no Minitab:
- Um gráfico temporal (sequencial) simples, com base em uma coluna de dados do Minitab.
- Um gráfico temporal (sequencial) múltiplo, com base em duas colunas de dados.

### 3.9.3 NÍVEL SIGMA

Até aqui já foram realizadas:
- a SMA, R&R ou Análise de Concordância por atributo
- a coleta de dados, que comprovadamente são confiáveis
- a demonstração dos dados (histograma, box plot, gráfico sequencial, entre outros)

**Agora é o momento de incluir na variabilidade os requisitos e especificações do cliente.**

O **nível sigma** faz parte do último passo do M do DMAIC. É usado para determinar o **nível atual do processo**. Os principais objetivos agora são:
- Estou com problema?
- Se sim, como resolver?

Há **dois métodos básicos** para se calcular o **nível sigma** de um processo:
- **Valor Z**:  para tipos de dados variáveis ou contínuos. Nota: A distribuição deve ser aproximadamente Normal;
- **DPMO (Defeitos Por Milhão de Oportunidades)**: para tipos de dados por atributo ou discreto. Nota: é preciso, ao menos, 5 defeitos.

![Fórmula do DPMO, fonte QuickLatex (cor da fonte: #096DFE). DPMO = (D / (n * O)) * 1.000.000](https://quicklatex.com/cache3/14/ql_0c73c06e697631e62bb31acd3318d914_l3.png)

Onde:
- $D$: quantidade de defeitos encontrados na amostra
- $n$: quantidade de amostras
- $O$: número de oportunidades de ocorrer o defeito.

Exemplo de **número de oportunidades de ocorrer o defeito**: Em um copo plástico podem ocorrer defeitos no dimensional do copo (altura, Ø da boca, etc), transparência, rachaduras, cor, textura, entre outros. Logo, em um simples copo existem dezenas de oportunidades de ocorrerem defeitos.

Calculado o **DPMO** de curto ou longo prazo, é possível encontrar o **nível sigma** consultando uma tabela que relaciona **DMPO ⇔ Sigma ⇔ CpK**.

**Lembre-se: dados de curto prazo não conseguem ser representativos da amostra.**

No exercício proposto encontrei 20 oportunidades de defeitos para o produto caneta. Dados: número de amostras = 525 e defeitos = 25.

![Exemplo DPMO, fonte QuickLatex (cor da fonte: #096DFE). DPMO = (25 / (525 * 20)) * 1.000.000 ≈ 2381](https://quicklatex.com/cache3/ac/ql_2716aa492a69c610808b7657bb98c0ac_l3.png)

Consultando a tabela nível sigma de longo prazo este é um processo **2,8 sigma**.

### 3.9.4 TESTE DE NORMALIDADE

**Será que os dados que tenho tendem a uma Distribuição Normal?** Podemos saber aplicando o **teste de normalidade**. Nota: a grande maioria dos processos tendem a ter dados com distribuição normal.

Com o Minitab é possível aplicar o teste _Anderson-Darling_ de normalidade. Caminho: **_Estat >> Estatísticas Básicas >> Teste de Normalidade_**. Na caixa de diálogo, selecionar **_Anderson-Darling_**. 

Interpretação do teste de normalidade _Anderson-Darling_:
  - $P_{value} \geq 0,05$ → Dados normais
  - $P_{value} < 0,05$ → Dados não normais.

### 3.9.5 NÍVEL SIGMA - VALOR Z (Dados por variável)

Caminho no Minitab: **_Stat >> Ferramentas da Qualidade >> Análise de Capacidade >> Normal…_**

No **exercício** proposto são analisados os tempos de espera para atendimento em um banco. Foram coletadas **23 amostras**, em **5 subgrupos**. O tempo especificado é $atendimento \leq 5 \min \space (LIE = 0\space, LSE = 5)$.

Os resultados foram **Z benchmark global = 0,83 sigma**.  **Z benchmark dentro = 0,88 sigma**. O **desempenho global** esperado é que **para cada milhão de atendimentos, 202.659 clientes esperarão mais que 5 minutos**. Há que se trabalhar na melhoria desse processo!

## Apresente os pontos mais importantes

- O **boxplot** representa em um gráfico de caixa os seguintes dados:
  - Valor mínimo
  - Q1 (primeiro quartil ou quartil inferior)
  - Q2 (Mediana)
  - Q3 (terceiro quartil ou quartil superior)
  - Valor máximo
- Os **gráficos sequenciais** (= temporais) são diagramas simples onde os dados são ordenados pelo tempo.
- O **nível sigma** faz parte do último passo do M do DMAIC. É usado para determinar o **nível atual do processo**. Os principais objetivos agora são:
  - Estou com problema?
  - Se sim, como resolver?

- ![Fórmula do DPMO, fonte QuickLatex (cor da fonte: #096DFE). DPMO = (n_defeitos / (n_amostras * n_oportun_defeitos)) * 1.000.000](https://quicklatex.com/cache3/d5/ql_0e20da613b96bc6b20f83d013b6596d5_l3.png)

- **Calculado o DMPO, use a tabela de Níveis Sigma para encontrar o atual nível sigma do processo.**
- Interpretação do teste de normalidade _Anderson-Darling_:
  - P-Value > = 0,05 → Dados normais
  - P-Value < 0,05 → Dados não normais.
- **Quando a amplitude e a localização da curva normal é igual a LIE e LSE, o processo é 3 sigma**.

## Referências
- Videoaulas 3.9.1 a 3.9.5 https://vimeo.com/showcase/9985114 (Acesso restrito aos alunos)
- [Gráfico sequencial](https://docs.google.com/document/d/1EAGl43_Va2GzOj3K1ka_ivEbIIupjMyM)
- https://explorable.com/statistical-data-sets
