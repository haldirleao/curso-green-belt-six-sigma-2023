## Curso Green Belt Six Sigma - projeto 04/2023
## Aula 18: Controlar do DMAIC.

Conteúdo de 57 a 61 do cronograma.

Data da entrega: 27/04/2023

Autor: [@haldirleao](https://github.com/haldirleao)

## Faça um resumo sobre os vídeos abordados nesta aula

### 57 CEP Controle Estatístico do Processo

Em inglês, _SPC (Statistical Process Control)_.

Nesta aula iniciamos os estudos do grupo de passos Controlar do DMAIC. Ele é composto por:
- Como manter as melhorias obtidas sob controle
- Prevenir ocorrências de falhas
- Alterar documentação de todo o sistema e promover treinamento
- Padronizar e documentar as melhorias

**Antigamente (e ainda hoje!)** para **garantir** os requisitos e necessidades dos clientes as empresas eram dependentes:
- da **Produção** para fazer o produto
- do **Controle de Qualidade** para verificar o produto final e detectar os que estão fora da especificação
  
O CEP:

| **C** | Controle    | Manter algo dentro dos limites                                                                                                       |
|-------|-------------|--------------------------------------------------------------------------------------------------------------------------------------|
| **E** | Estatístico | Ciência que reúne e classifica fatos, baseando-se em seu número e frequência, chegando a conclusões gerais                           |
| **P** | Processo    | Série de atividades sucessivas com nexo de causa e efeito, com um conjunto de variáveis necessárias para obter um produto ou serviço |

O método CEP foi desenvolvido por Walter Andrew Shehart.

Definição de CEP, segundo o instrutor:
> É um método aplicado em tempo real no processo. Visa controlar um processo para minimizar as variações e prevenir defeitos. As ações dos operadores são baseadas em evidências estatísticas relacionadas à estabilidade do processo.

Causas das variações:
- Causas Comuns: representam aproximadamente 85% do total de problemas 
- Causas Especiais: representam aproximadamente 15% do total de problemas

Vantagens do CEP:
- Redução de refugo
- Manter processo centrado
- Não há necessidade de controle peça-a-peça
- Menos retrabalho
- Aumento da produtividade
- Auxilia na tomada de decisões
- Melhoria da qualidade

O **controle de qualidade** atua, basicamente, no **resultado do processo**. O CEP **atua no processo**.

**Ações locais**: Geralmente são necessárias para eliminar **causas especiais** de variação, logo tem potencial para corrigir ~15% dos problemas. As ações podem ser tomadas por pessoas próximas ao processo.

**Ações sobre o sistema**: Geralmente são necessárias para eliminar **causas comuns** de variação. Quase sempre demandam ações gerenciais para a correção. Tem potencial para corrigir ~85% dos problemas.

**Processo sob controle estatístico**: quando as **únicas fontes de variação são as causas comuns**.

**Teorema do Limite Central**
https://pt.wikipedia.org/wiki/Teorema_central_do_limite

Segundo a Wikipedia, esse teorema afirma que quando o tamanho da amostra aumenta, a distribuição amostral da sua média aproxima-se cada vez mais de uma distribuição normal.

Usado para normalizar os dados quando eles não são normais. **Somente pode ser usado no CEP**. Não pode ser usado na fase medir, durante os testes de capacidade do processo (Cp, Cpk)
 
### 58 CARTAS DE CONTROLE

Com as **cartas de controle** acompanhamos os dados do processo. Assim, por meio de **gráficos**, é possível verificar se o **processo está sob controle**, ou seja, **sem causas especiais**.

Tipos de cartas de controle (imagem no slide 845):
- Carta por atributo: passa / não passa, aprovado / reprovado, etc.
  - **Carta NP** (número de itens defeituosos por subgrupo. Cada item deve ser classificado como: Aprovado ou Reprovado)
  - **Carta C** (número de não-conformidades por subgrupo. Note que aqui um mesmo item pode ter n não-conformidades)
  - **Carta U**
  - **Carta P**
- Cartas para variáveis: diâmetro interno da arruela, torque angular, dureza, etc.
  - **Carta x̄-R** (x̄: Média | R: Amplitude)
  - **Carta x̄-S** (x̄: Média | S: Desvio padrão)
  - **Carta I-AM** (média e a variação do processo de observações individuais e não em subgrupos)

**Diário de bordo**: uma planilha que geralmente acompanha a carta de processo, para que o operador anote ocorrências relevantes durante as atividades (hora de mudança de matéria-prima, final de lote, _setup_, mudança inesperada de operador, etc). Os registros podem apoiar na investigação de causas especiais.

### 58.1 Limites de controle

Média das médias dos subgrupos:

$\overline{\overline{X}} = \dfrac{ \overline{X_1} + \overline{X_2} + \overline{X_n}  }{n}$

Média das amplitudes dos subgrupos:

$\overline{R} = \dfrac{ R_1 + R_2 + R_n }{n}$

Para o **gráfico das amplitudes**:

**LICR** e **LSCR** - Limites Inferior e Superior de Controle
 - $LICR = D3 * \overline{R}$
 - $LC = \overline{R}$
 - $LSCR = D4 * \overline{R}$

Sendo D4 e D3 constantes tabeladas conforme o tamanho da amostra.

Para o **gráfico das médias**:

**LICX** e **LSCX** - Limites Inferior e Superior de Controle
 - $LICX = \overline{\overline{X}} - (A2 \times \overline{\overline{R}})$
 - $LC = \overline{\overline{X}}$
 - $LSCX = \overline{\overline{X}} + (A2 \times \overline{\overline{R}})$

Sendo A2 uma constante tabelada conforme o tamanho da amostra.

### 59 ANÁLISE DAS CARTAS DE CONTROLE

Indicativos de problemas devido causas especiais no processo (cartas XbarraR) listados pelo instrutor\*:
- **Pontos fora dos limites de controle**
- **7 pontos ascendentes em sequência**
- **7 pontos abaixo ou acima do LC (Limite Central)**
- **Mais que 2/3 dos pontos dentro do terço médio (LC±1σ)**. Trata-se de possível ocorrência de causa especial. Ou os limites do processo não foram bem coletados e calculados.

\* Outras fontes listam indicativos adicionais. Exemplo aqui: [CEP, prof. Fabrício Gomes, USP](https://edisciplinas.usp.br/pluginfile.php/4145169/mod_resource/content/1/CEP%20-%20cartas%20de%20controle.pdf).

Criação de Cartas de Controle x̄-R com terço médio. Caminho no Minitab: **_Estat >> Cartas de Controle >> Cartas de Variáveis para Subgrupos >> Xbarra-R..._**

**Terço médio**: inclui linhas adicionais de referência nos gráficos, representando além dos LC±3σ, também os LC±1σ. Para saber mais: [Minitab: Modificar os limites de controle para Carta Xbarra-R](https://support.minitab.com/pt-br/minitab/20/help-and-how-to/quality-and-process-improvement/control-charts/how-to/variables-charts-for-subgroups/xbar-r-chart/perform-the-analysis/xbar-r-options/modify-the-control-limits/).

Como não tenho mais acesso ao Minitab, criei a carta de controle Xbarra no Google Sheets. O arquivo está na pasta <u>**projetos-minitab**</u>

 Link para criação de cartas NP online: http://spcchartsonline.com/index.php/online-spc-control-charts/spc-control-charts/background-page-2/the-x-bar-r-chart-2/

### 60 CARTAS POR ATRIBUTO

**Carta NP** (número de itens defeituosos).

Carta NP: Em inglês, _**N**umber **D**efective chart_. 

Exemplos: parafusos com defeitos, televisores com defeitos, pastéis com defeitos, etc. São usadas para determinar se o número de itens com defeito está sob controle estatístico. Caminho no Minitab: **_Stat >> Cartas de Controle >> Cartas de Atributos >> NP..._**

Link para criação de cartas NP online: http://spcchartsonline.com/index.php/online-spc-control-charts/spc-control-charts/attribute-control-charts/np-chart/

**Carta c** (número de não-conformidades por subgrupo).

Carta c: Em inglês, _c-chart Number of Non-**C**onformities Chart_.

Neste caso, o mesmo item pode ter n não-conformidades. Exemplo: para um televisor foram registradas as seguintes não-conformidades: módulo fonte danificado, tomada quebrada, falta de parafuso no suporte-base. Aqui temos 3 não-conformidades a serem consideradas na carta c. 

Caminho no Minitab: **_Stat >> Cartas de Controle >> Cartas de Atributos >> C..._**


Link para criação de cartas C online: http://spcchartsonline.com/index.php/online-spc-control-charts/spc-control-charts/attribute-control-charts/c-chart/

IMPORTANTE: **Os limites de especificação não são usados em cartas de controle**. Os limites são definidos pelos dados do próprio processo.

### 61 CAPACIDADE E ESTABILIDADE

A **capacidade do processo (Cp, Cpk, nível sigma)** é estabelecida pelo cliente.

A **estabilidade do processo** é dado pelo **próprio processo**.

Capacidade vs Estabilidade

| PROCESSO                       |                             |                                                                                                                                                                   |
|--------------------------------|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ESTÁVEL?<br/>(voz do processo) | CAPAZ?<br/>(voz do cliente) | INTERPRETAÇÃO                                                                                                                                                     |
| sim                            | sim                         | Melhor dos mundos. O processo está controlado estatisticamente e atende às especificações do cliente.                                                             |
| não                            | sim                         | Muito provavelmente é possível eliminar causas especiais e melhorar o processo.<br/>O cliente aceita os produtos como estão, já que estão dentro da especificação. |
| sim                            | não                         | O processo está estável, porém não é capaz. Logo não há como "vender" para este cliente.                                                                          |
| não                            | não                         | Pior dos mundos                                                                                                                                                   |


### 61.1 Super controle

**Não use as cartas de controle para fazer supercontrole!**

Exemplo do Lean Six Sigma Brasil:

>Considere um processo de cozimento de pães. **Ligeiras mudanças na temperatura** que são causadas pelo termostato do forno fazem parte da variação de **causa comum natural do processo**.

>Se você **tentar reduzir esta variação natural** do processo alterando manualmente o ajuste da temperatura para cima e para baixo, você irá provavelmente **aumentar a variabilidade em vez de reduzi-la**. Isto é chamado de **supercontrole**.

>Quando **não há sinais fora de controle**, sabe-se que apenas a variabilidade de causa comum está presente e **não deve-se ajustar o processo** porque ele está **sob controle estatístico**.

https://leansixsigmabrasil.com.br/controle-estatistico-de-processo-cep/

## Apresente os pontos mais importantes

- CEP Controle Estatístico do Processo
- O controle de qualidade atua, basicamente, no resultado do processo. O CEP atua no processo.
- Processo sob controle estatístico: quando as únicas fontes de variação são as causas comuns.
- O Teorema do Limite Central afirma que quando o tamanho da amostra aumenta, a distribuição amostral da sua média aproxima-se cada vez mais de uma distribuição normal.
- Carta x̄-R: 2 gráficos: Gráfico das Médias e Gráfico das Amplitudes
- Carta NP: Em inglês, Number Defective chart.
- Carta c: Em inglês, c-chart Number of Non-Conformities Chart.
- IMPORTANTE: Os limites de especificação (do cliente) não são usados em cartas de controle. 
- CEP e criação de cartas de processo. Online e gratuito. Link http://spcchartsonline.com/index.php/online-spc-control-charts/spc-control-charts/
- Não use as cartas de controle para fazer supercontrole!

## Referências
- Videoaulas 57 a 61 https://vimeo.com/showcase/10027791 (Acesso restrito aos alunos)
- CEP http://www.producao.ufrgs.br/arquivos/disciplinas/388_apostilacep_2012.pdf
- [Cartas de controle. Dados contínuos - Ribeiro & Caten - UFRGS](https://edisciplinas.usp.br/pluginfile.php/4145169/mod_resource/content/1/CEP%20-%20cartas%20de%20controle.pdf)
- [Minitab: Modificar os limites de controle para Carta Xbarra-R](https://support.minitab.com/pt-br/minitab/20/help-and-how-to/quality-and-process-improvement/control-charts/how-to/variables-charts-for-subgroups/xbar-r-chart/perform-the-analysis/xbar-r-options/modify-the-control-limits/)
- [Minitab: Interpretar os principais resultados para Carta NP](https://support.minitab.com/pt-br/minitab/20/help-and-how-to/quality-and-process-improvement/control-charts/how-to/attributes-charts/np-chart/interpret-the-results/key-results/#:~:text=A%20carta%20NP%20representa%20graficamente,o%20n%C3%BAmero%20m%C3%A9dio%20de%20defeituosos.)
- [Carta NP (_NP chart_)](http://spcchartsonline.com/index.php/online-spc-control-charts/spc-control-charts/attribute-control-charts/np-chart/)
- [CEP e criação de cartas de processo. Online e gratuito](http://spcchartsonline.com/index.php/online-spc-control-charts/spc-control-charts/)