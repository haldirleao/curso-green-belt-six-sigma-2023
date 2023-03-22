## Curso Green Belt Six Sigma - projeto 04/2023
## Aula 08: Medir do DMAIC.

Conteúdo de 3.9.6 a 3.9.9 do cronograma.

Data da entrega: 22/03/2023

Autor: [@haldirleao](https://github.com/haldirleao)

## Faça um resumo sobre os vídeos abordados nesta aula

### 3.9.6 CAUSA COMUM E ESPECIAL

Para exemplificar a variabilidade em amostras o instrutor solicitou que fizéssemos cinco assinaturas em uma folha de papel. E questionou: as assinaturas são idênticas? Obviamente há diferenças entre as assinaturas, que pode ser entendida como variabilidade das cinco amostras.

A **variação** entre as assinaturas tem **causas comuns** ou **especiais**? Segundo o instrutor se trata de **causa comum** neste caso, por que é **natural** que ocorram pequenas diferenças entre as assinaturas.

Então ele solicitou que repetíssemos as cinco assinaturas, **mas agora com a outra mão**. Ao verificar as assinaturas, como é de se esperar, também ocorreram variações, ainda maiores que no exemplo anterior. 

E agora, as **variações entre as cinco assinaturas**, feitas com a "mão ruim", têm **causas comuns** ou **especiais**? O instrutor afirmou que continuam tendo **causas comuns**, já que é natural que a variação aumente quando se usa a nossa "mão ruim".

Finalmente, comparamos as assinaturas feitas com a "mão boa" e com a "mão ruim". Agora sim a variação entre estes dois conjuntos de amostras tem **causa especial**. Neste caso aconteceu uma **causa assinalável**, as assinaturas com a mão trocada.

Exemplos práticos de **potenciais causas especiais**: mudança de fornecedor de matéria-prima, novo contrato de prestação de serviços, o pneu furar durante um trajeto realizado diariamente. 

As causas especiais **alteram a normalidade** do seu processo. Geralmente, os dados que "escapam" da normalidade são causas especiais.

Em um **relatório de capacidade do processo**, tais causas podem levar a uma significativa **diferença** entre a **normal Global** e a **normal Dentro**, indicando instabilidade no processo. Neste caso, a performance Global indica o comportamento real do processo, enquanto a  capacidade (Dentro) indica o comportamento do processo se este for estabilizado.

---
#### Teste de capacidade (Servico de despertador de um hotel, CCR = ± 5 min)
Dado o CCR, os dois limites da especificação são: LIE = -5 min / LSE = +5min.
Ao analisar o **relatório de capacidade** no Minitab, somente pelo gráfico é perceptível deduzir que o nível **sigma é ~3** (já que a variação das **curvas normais Global e Dentro** são da **mesma amplitude e localização** dos limites LIE e LSE). Como as **curvas** são **semelhantes**, pode-se afirmar que o **processo está estabilizado** (sem causas especiais). Neste caso trabalhar na alteração da média não melhorará o processo. **Há que se trabalhar para reduzir a variabilidade do processo!**

### 3.9.7 CAPACIDADE DO PROCESSO (dados por variáveis)

**Cp**: Dispersão dos resultados do processo (**precisão**). **Capacidade potencial**

**CpK**: Localização das médias dos resultados contra os limites da especificação (**exatidão**). **Capacidade real**

Se um processo é:
- Cp = 1 → 3 sigma (potencial)
- Cp = 2 → 6 sigma (potencial) 
- CpK = 1 → 3 sigma (real)
- CpK = 2 → 6 sigma (real) 

Note que **índice_capacidade * 3 = nível_sigma**.  

**Cp Capacidade Potencial** do processo. É uma medida de o quanto o processo é capaz de atender às especificações.

$\text{Cp} = \dfrac{\text{LSE - LIE}}{6 \times \sigma } % Cp = (LSE - LIE) / (6 * σ)$

Onde LSE: Limite Superior de Especificação , LIE: Limite Inferior de Especificação, σ: desvio padrão estimado.

Exemplo. Dado LIE = 2, LSE = 8, σ = 1, logo:

$Cp = \dfrac{8 - 2}{6 \times 1} = 1 % Cp = (LSE - LIE) / (6 * σ)$

Note: **Cp = 1** indica que é um **processo potencial 3 sigma**. Pode-se afirmar que a variação da **distribuição normal** é da **mesma amplitude e localização** dos limites LIE e LSE.

Exemplo. Dado LIE = 2, LSE = 8, σ = 0,5, logo:

$Cp = \dfrac{8 - 2}{6 \times 0,5} = 2 % Cp = (LSE - LIE) / (6 * σ)$

Note: **Cp = 2** indica que é um **processo potencial 6 sigma**. Pode-se afirmar que a variação da **distribuição normal** é a **metade da amplitude** dos limites LIE e LSE, e a média está localizada em $\approx\frac{(LSE - LIE)}{2} % (LSE - LIE)/2$ (centro da especificação).

**CpK** é o índice de **capacidade efetiva**, real do processo.

$$\text{C}_\text{pK}=\frac{{min((\overline{\overline{X}} - LIE),(LSE - \overline{\overline{X}}))}}{3 \times \sigma}% Cpk = min((X - LIE),(LSE - X)) / (3σ)$$

Onde $\overline{\overline{X}} % X$ = média das médias dos subgrupos (média do processo).

Note que na fórmula são calculados os **CpK_inferior** e **CpK_superior**, então se adota para o cálculo o **menor valor**.

Comumente a **indústria automotiva** adota índice de capacidade real **CpK = 1,67**, que corresponde a **nível sigma 5**.

### 3.9.8 EXEMPLO - CÁLCULO DE CAPACIDADE

Foi proposto um exercício para o cálculo do **Cp** e **CpK** de capacidade de atendimento do Hospital 1. Foi dado que LIE = 100 min e LSE = 110 min.
- Passo 1 - Executar o teste de normalidade Anderson-Darling. Caminho no Minitab: _Estat > Estatísticas Básicas > Teste de normalidade..._. O resultado foi **valor-P = 0,277**. Como **valor-P >= 0,05** a distribuição é normal.
- Passo 2 - Cálculo de Cp e CpK com base nos valores da tabela e especificações dadas. Caminho no Minitab: _Estat > Ferramentas da qualidade > Análise de capacidade > Normal..._. Lembre-se que na caixa de diálogo _Opções_ deve ser selecionado "Estatísticas de Capacidade (Cp, Pp)". Os resultados foram **Cp = 4,30** e **CpK = 3,97**. **Os valores são excelentes e dentro do especificado pelo cliente.**. Lembre-se: para obter o resultado em nível sigma, basta calcular: $C_{p} \times 3 % Cp * 3$ e $C_{pK} \times 3 % CpK * 3$. Este processo tem $0,0 \space DPMO % 0,0 DPMO$.

### 3.9.9 CAPACIDADE - DADOS NÃO NORMAIS 

<font color="red">**PENDENTE**</font>


## Apresente os pontos mais importantes

- **Causas Comuns** – aquelas que são **inerentes ao processo** no decorrer do tempo, que afetam a todos que trabalham nele e todos os resultados.
- **Causas Especiais** – aquelas que não são parte do processo o tempo todo ou que não afetam a todos, mas que surgem em função de **circunstâncias específicas**.
- 
- $\text{Cp} = \dfrac{\text{LSE - LIE}}{6σ } % Cp = (LSE - LIE) / (6 * σ)$ → Capacidade **Potencial** do processo.
- 
- $\text{C}_\text{pK}=\frac{{min((\overline{\overline{X}} - LIE),(LSE - \overline{\overline{X}}))}}{3 \times \sigma}% Cpk = min((X - LIE),(LSE - X)) / (3σ)$ → Capacidade **real**, **efetiva**, do processo.
- **índice_capacidade * 3 = nível_sigma**

## Referências
- Videoaulas 3.9.6 a 3.9.9 https://vimeo.com/showcase/9985114 (Acesso restrito aos alunos)
- https://www.nortegubisian.com.br/blog/variacao-de-processos-descubra-como-o-six-sigma-pode-ajudar/
- https://www.harbor.com.br/harbor-blog/2017/07/06/capacidade-performance-significado/
- 