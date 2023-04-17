## Curso Green Belt Six Sigma - projeto 04/2023
## Aula 15: Analisar do DMAIC.

Conteúdo de 49 a 51 do cronograma.

Data da entrega: 17/04/2023

Autor: [@haldirleao](https://github.com/haldirleao)

## Faça um resumo sobre os vídeos abordados nesta aula

### 49 TESTE T. 1 AMOSTRA

Teste de hipótese t para 1 amostra:
- Faz a comparação estatística entre **uma média** e **um valor pré-determinado**.
- O **desvio padrão** é **desconhecido** e o tamanho da amostra é **n < 30**.

Nessa aula foi proposto o seguinte exercício:

A resistência à tração do aço inoxidável produzido numa usina permanecia estável, com uma **resistência média de 72 kg/mm²**. Recentemente a máquina sofreu manutenção preventiva e foi ajustada.

A fim de determinar o efeito do ajuste, 10 amostras foram medidas.

Hipóteses:
- $H_{0}: \mu = 72 \space kg/mm²$ : A máquina continua com resultado igual a antes do ajuste. 
- $H_{1}: \mu \neq 72 \space kg/mm²$ : A máquina está com resultado diferente do antes do ajuste.

Caminho no Minitab: **_Stat >> Estatísticas básicas >> Teste t para 1 amostra..._** Nas opções configurar o **nível de confiança = 95%** e a hipótese alernativa para **média ≠ média_hipotética**.

Interpretação do valor-p:
- $p < 0,05$ : rejeitar a hipótese nula ($H_{0}$)
- $p \ge 0,05$ : aceitar a hipótese nula ($H_{0}$)

O valor-p calculado foi $p = 0,205$. Logo se deve aceitar a hipótese nula $H_{0}: \mu = 72 \space kg/mm²$. Conclusão: **a máquina continua com resultado igual a antes do ajuste**.   

### 50 TESTE T. 2 AMOSTRAS

Teste de hipótese t para 2 amostras:
- Faz a comparação estatística **entre duas médias independentes**.

Nessa aula foi proposto o seguinte exercício:

Um empresário gostaria de saber se há mudança média na produção **após ter adquirido uma máquina nova**. De posse dos dados históricos, ele comparou com os dados coletados recentemente. Verifique se a produção atual é superior.

Hipóteses:
- $H_{0}: nova = antiga$ : A produção é igual. 
- $H_{1}: nova > antiga$ : A produção da máquina nova é maior que da antiga.

Caminho no Minitab: **_Stat >> Estatísticas básicas >> Teste t para 2 amostras..._** Nas opções configurar:
- Amostra 1: Antiga
- Amostra 2: Nova
- Nível de confiança = 95%
- Hipótese alernativa para **diferença < diferença_hipotética**

Interpretação do valor-p:
- $p < 0,05$ : rejeitar a hipótese nula ($H_{0}$)
- $p \ge 0,05$ : aceitar a hipótese nula ($H_{0}$)

O valor-p calculado foi $p = 0,011$. Logo se deve rejeitar a hipótese nula $H_{0}: antiga = nova$. Conclusão: **a produção da máquina nova é maior que da antiga**.   

### 51 TESTE T. PAREADO

Teste de hipótese t pareado:
- Faz a comparação estatística **entre duas médias de amostras dependentes**.

Nessa aula foi proposto o seguinte exercício:

Noves pessoas participaram de um **novo programa de emagrecimento**. Verifique se a nova dieta é eficiente, ou seja, diminuindo o peso dos participantes.

Hipóteses:
- $H_{0}: peso\_antes = peso\_depois$
- $H_{1}: peso\_antes > peso\_depois$

Caminho no Minitab: **_Stat >> Estatísticas básicas >> Teste t pareado..._** Nas opções configurar:
- Amostra 1: Antes
- Amostra 2: Depois
- Nível de confiança = 95%
- Hipótese alernativa para **diferença > diferença_hipotética**

Interpretação do valor-p:
- $p < 0,05$ : rejeitar a hipótese nula ($H_{0}$)
- $p \ge 0,05$ : aceitar a hipótese nula ($H_{0}$)

O valor-p calculado foi $p = 0,04$. Logo se deve rejeitar a hipótese nula $H_{0}: peso\_antes = peso\_depois$. Conclusão: **a dieta funcionou, já que o peso antes era maior que o peso depois**.

## Apresente os pontos mais importantes

- Teste de hipótese **t para 1 amostra**:
  - Faz a comparação estatística entre **uma média** e **um valor pré-determinado**.
  - O **desvio padrão** é **desconhecido** e o tamanho da amostra é **n < 30**.

- Teste de hipótese **t para 2 amostras**:
  - Faz a comparação estatística **entre duas médias independentes**.

- Teste de hipótese **t pareado**:
  - Faz a comparação estatística **entre duas médias de amostras dependentes**.

## Referências
- Videoaulas 49 a 51 https://vimeo.com/showcase/10009507 (Acesso restrito aos alunos)
- https://blog.minitab.com/pt/nocoes-basicas-sobre-testes-t-para-uma-amostra-para-duas-amostras-e-pareados
- 