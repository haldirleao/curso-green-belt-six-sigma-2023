## Curso Green Belt Six Sigma - projeto 04/2023
## Aula 14: Analisar do DMAIC.

Conteúdo de 46 a 48 do cronograma.

Data da entrega: 12/04/2023

Autor: [@haldirleao](https://github.com/haldirleao)

## Faça um resumo sobre os vídeos abordados nesta aula

### 46 EXEMPLO - REGRESSÃO LINEAR

Nesta aula é proposto o uso do Minitab para determinar a **equação da reta**, dados os pares de dados de **comprimento (x) e peso (y)** de um tubo.

Caminho no Minitab: **_Stat >> Regressão >> Regressão >> Ajustar modelo de regressão_**

No Minitab, variáveis de interesse em um experimento (aquelas que são medidas ou observadas) são chamadas de **variáveis de resposta ou dependentes**. Outras variáveis, no experimento que afetam a resposta e podem ser definidas ou medidas pelo experimentador, são chamadas **preditoras, explicativas ou independentes**. No nosso caso:
- Comprimento: variável preditora
- Peso: variável de resposta

Resultados da 1a Análise de Regressão - Comprimento (x) vs Peso (y):
- Equação: $y = -9,28 + 28,15 x$
- R²(aj) = 66,94%: indica que 66,9%  da variável Peso é explicada pela variável Comprimento
- Também foi apresentado um **resíduo** no resultado, indicada pela letra R em uma das observações.

Segundo o instrutor, **os dados indicados como resíduos devem ser analisados e revisados. E, talvez, excluídos da amostra**.

Resultados da 2a Análise de Regressão - após excluir o resíduo:
- Equação: $y = -18,70 + 37,48 x$
- R²(aj) = 84,11%: indica que 84,1% da variável Peso é explicada pela variável Comprimento

A tabela (dados de entrada) **sem ocorrência de resíduos** é a evidência de qua a Regressão Linear **é confiável**.

### 47 TESTE DE HIPÓTESES

>_"O teste de hipóteses fornecem ferramentas que nos permitem rejeitar ou não rejeitar uma hipótese estatística através da evidencia fornecida pela amostra."_

Os tipos de testes de hipótese mais usados, e disponíveis no Minitab, são:
- Teste Z para uma amostra
- Teste t para uma amostra
- Teste t para duas amostras
- Teste t paresdo

Caminho no Minitab: **_Stat >> Estatísticas básicas >>_ Teste...**

Um teste de hipótese examina duas hipóteses opostas sobre uma população: a hipótese nula ($H_{0}$) e a hipótese alternativa ($H_{1}$). A hipótese nula é a declaração que está sendo testada. Normalmente, a hipótese nula é uma declaração de "nenhum efeito" ou "nenhuma diferença". A hipótese alternativa é a declaração que você quer ser capaz de concluir que é verdadeira com base em evidências fornecidas pelos dados da amostra.

Exemplos de perguntas que podem ser respondidas com um teste de hipótese:
- A altura média de mulheres universitárias difere de 1,55 m?
- O desvio padrão dessa altura é igual ou menor do que 12,5 cm?- 
- Os estudantes do sexo masculino e feminino diferem na altura, em média?
- Os estudantes de graduação do sexo masculino apresentam proporção significativamente maior do que a proporção de estudantes do sexo feminino de graduação?

### 48 TESTES Z 1 AMOSTRA

Este teste faz a **comparação** estatística **entre uma média** e **um valor pré-determinado**. O **desvio padrão** deve ser **conhecido** e o tamanho da amostra deve ser **_n ≥ 30_**.

Nessa aula foi proposto o seguinte exercício:

Uma empresa compra tubos com  Ø11,16 cm de um fornecedor. Suspeita-se que o fornecedor não está entregando os tubos com tal dimensão.

Na inspeção de recebimento foram coletadas 30 amostras. O desvio padrão calculado destes dados foi $s = 1,198$.

Hipóteses:
- $H_{0}: \mu = 11,16 \space cm$ : O fornecedor entrega os tubos no diâmetro correto
- $H_{1}: \mu \neq 11,16 \space cm$ : O fornecedor entrega os tubos com diâmetros errados

Interpretação do valor-p:
- $p < 0,05$ : rejeitar a hipótese nula ($H_{0}$)
- $p \ge 0,05$ : aceitar a hipótese nula ($H_{0}$)

O valor-p calculado foi $p = 0,000$. Logo se deve rejeitar a hipótese nula $H_{0}: \mu = 11,16 \space cm$. Conclusão: **o fornecedor entrega os tubos com diâmetros errados**.   

## Apresente os pontos mais importantes

- A **regressão linear** somente é **aplicável** para dados com **forte correlação linear**;
- Cuidados com o **resíduos** dos dados de entrada. Eles devem ser analisados, revisados e/ou excluídos para que a **equação da reta** seja **confiável**.
- _"Um teste de hipótese é regra que especifica se deve aceitar ou rejeitar uma alegação sobre uma população de acordo com as provas fornecidas por uma amostra de dados."_
- Teste Z 1 amostra. Interpretação do valor-p:
  - $p < 0,05$ : rejeitar a hipótese nula ($H_{0}$)
  - $p \ge 0,05$ : aceitar a hipótese nula ($H_{0}$)

## Referências
- Videoaulas 46 a 48 https://vimeo.com/showcase/10009507 (Acesso restrito aos alunos)
- [Minitab: O que são variáveis de resposta e variáveis preditoras](https://support.minitab.com/pt-br/minitab/21/help-and-how-to/statistical-modeling/regression/supporting-topics/basics/what-are-response-and-predictor-variables/)
- Calculadora de regressão linear Online https://www.graphpad.com/quickcalcs/linear1/
- https://www.inf.ufsc.br/~andre.zibetti/probabilidade/teste-de-hipoteses.html
- [Minitab: O que é teste de hipótese](https://support.minitab.com/pt-br/minitab/20/help-and-how-to/statistics/basic-statistics/supporting-topics/basics/what-is-a-hypothesis-test/)