## Curso Green Belt Six Sigma - projeto 04/2023
## Aula 06: Medir do DMAIC.

Conteúdos de 3.5 a 3.9 do cronograma.

Data da entrega: 15/03/2023

Autor: [@haldirleao](https://github.com/haldirleao)

## Faça um resumo sobre os vídeos abordados nesta aula

### 3.5 NÚMERO DE CATEGORIAS DISTINTAS

$$
NDC = \left(\dfrac{\sigma_{\text{peça\_a\_peça}}}{\sigma_{\text{sistema\_medição}}}\right)\times\sqrt{2}
$$

Uma forma simplificada de cálculo é: **NDC = (max_medido - min_medido) / resolução_instrumento**. Ex: Usa-se uma balança com resolução/precisão 0,1kg para medir cachorros que pesam de 29 a 41 kg, logo, NDC = (41 - 29) / 0,1 =  120.

**O NDC deve ser >= 5**. Números muito grandes (Ex.: NDC = 120) indicam que o instrumento tem resolução muito maior do que a necessária. 

O Minitab pode auxiliar na criação de planilhas para estudos de medição R&R. Caminho: menu **_Stat >> Ferramentas da Qualidade >> Estudos de medição >> Criação de uma worksheet…_**

No exercício proposto o **resultado foi ruim**, especialmente na **repe** e **NDC**. As variações foram:
- Total de **R&R da medição = 91,91%** (Variação R&R deve ser menor que 30%, sendo o desejado menor que 10%)
- **Peça a peça = 39,40%** (deveria representar a maior parte da variação, entre 80% e 90%)
- **Repe = 91,91%, repro = 0,00%**. Número de categorias distintas = 1 (deveria ser >=5). 

Deve-se analisar o que ocorre com o instrumento de medição, corrigir, refazer as medições e repetir o estudo R&R da medição.

Nota: A repro, que tem relação com a variação do operador, foi excelente. Logo, sem necessidade de intervenções.

### 3.6 ANÁLISE DE CONCORDÂNCIA

Para a análise proposta (inspeção visual de vidro sem bolha=0 / com bolha=1) foi necessária a criação de um padrão que define “o que é bolha”. Definido o padrão, os operadores devem conhecê-lo e entender perfeitamente “o que é presença de bolha no vidro”.

Nesta análise é possível verificar a **concordância** de:
- cada inspetor vs padrão
- entre os inspetores
- todos os inspetores vs padrão.

Caminho no Minitab: menu **_Stat >> Ferramentas da Qualidade >> Análise de concordância de atributos_**.

**Na análise Avaliador vs Padrão, recomenda-se que o acerto de cada avaliador seja >90\%**. Algumas empresas adotam >95\%.

### 3.7 ÍNDICE KAPP

**Índice Kappa = Índice de concordância** (Pode variar entre **-1 e +1**).

1 = concordância perfeita.

-1 = discordância perfeita.

O índice Kappa mede o grau de concordância entre os avaliadores.
- Intra-avaliador: avaliações feitas com o mesmo inspetor em diferentes períodos de tempo
- Inter-avaliador: avaliações feitas com inspetores diferentes ao mesmo tempo.

O **índice Kappa** é uma **excelente** ferramenta para análise de **ensaios visuais**.

Índice Kappa ou índice de concordância. Interpretação:
- 1: Perfeito
- \>0,8: Excelente
- 0,6 a 0,8: Bom
- 0,4 a 0,6: Regular
- \<0,4: Ruim

Nota: para criar uma planilha com o apoio do Minitab, vá até: **_menu Stat > Ferramentas da Qualidade > Criar worksheet para Análise de concordância por atributos_**.

### 3.8 VARIAÇÃO DO PROCESSO

Revisando os passos realizados até agora no D e M do DMAIC:
- D1: Certificar que o projeto é importante para a empresa. Alinhamento com a estratégia empresarial;
- D2: Definir a equipe, escopo e prazo do projeto;
- D3: Registrar o projeto 
- D4: Mapear o processo. Calcular o _saving_. Buscar por _Quick wins_.
- M1: Desenvolver o plano de coleta de dados;
- M2: Analisar e comprovar que os dados coletados são confiáveis. (MSA, R&R, análise por atributo).
- M3: Esta aula!

Os produtos e serviços que saem dos processos sempre terão variações, mesmo que mínimas. Medir e entender a variação ajuda a identificar:
- o atual nível de desempenho (nível sigma)
- com base nos critérios de aceitação, se é preciso mudar algo para reduzir a variabilidade.

**O tema central do 6 sigma é reduzir a variabilidade**.

Três elementos-chaves para determinar se o requisito do cliente está sendo atendido: 
1. Especificações
2. Média
3. Desvio padrão.

A **média nos mostra a localização do processo** e o **desvio padrão nos mostra a variabilidade**.

Quando processos possuem dados do tipo variável coletado, há se seguintes maneiras de melhorá-lo:
1. Reduzir a variabilidade
2. Deslocando a média
3. Trabalhando para alterar tanto a variabilidade quanto a média

Pode-se citar como formas para apresentação da variação do processo aos interessados:
- desvio padrão
- histograma
- box plot
- gráfico sequencial
- entre outros

### 3.9 DESVIO PADRÃO E HISTOGRAMA

Desvio padrão amostral:

$$
s = \sqrt{\dfrac{\sum_{i=1}^{n}(x_i - \bar{x})^2}{n-1}}
$$

Não se deve analisar unicamente o desvio padrão (que indica a variabilidade do processo). 
Deve-se analisá-lo de forma conjunta com as especificações (critérios de aceitação).

O **histograma** representa graficamente uma **distribuição de frequências**, o que facilita o entendimento dos interessados.

## Apresente os pontos mais importantes
 
- $$NDC = \left(\dfrac{\sigma_{\text{peça\_a\_peça}}}{\sigma_{\text{sistema\_medição}}}\right)\times\sqrt{2}
$$
- A fórmula acima é a utilizada pelo Minitab.
- **NDC = (max_medido - min_medido) / resolução_instrumento**. Esta é a fórmula simplificada apresentada na videoaula.
- **O NDC deve ser >=5**.
-  Análise de concordância de atributos. **Na análise Avaliador vs Padrão, recomenda-se que o acerto de cada avaliador seja >90\%**. Algumas empresas adotam >95\%.
- Índices Kappa ou índice de concordância. Interpretação:
  - 1: Perfeito;
  - \>0,8: Excelente;
  - 0,6 a 0,8: Bom;
  - 0,4 a 0,6: Regular;
  - \<0,4: Ruim.
- O padrão deve ser montado por pessoas experientes, que conheçam o produto e o processo! De preferência por mais de uma pessoa.
- A **variabilidade** é inimiga da **qualidade**.
- O desvio padrão é uma boa forma de expressar a dispersão ou variação média de um conjunto de dados.

## Referências
- Videoaulas 3.5 a 3.9 https://vimeo.com/showcase/9985114 (Acesso restrito aos alunos)