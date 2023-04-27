## Curso Green Belt Six Sigma - projeto 04/2023
## Aula 18: Controlar do DMAIC.

Conteúdo de 57 a 61 do cronograma.

Data da entrega: 26/04/2023

Autor: [@haldirleao](https://github.com/haldirleao)

## Faça um resumo sobre os vídeos abordados nesta aula

### 57 CEP Controle Estatístico do Processo

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
| **P** | Processo    | Série de atividades sucessivas com nexo de causa e efeito, ocm um conjunto de variáveis necessárias para obter um produto ou serviço |

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

**Ações locais**: Geralmente são necessidades para eliminar **causas especiais** de variação, logo tem potencial para corrigir ~15% dos problemas. As ações podem ser tomadas por pessoas próximas ao processo.

**Ações sobre o sistema**: Geralmente são necessidades para eliminar **causas comuns** de variação. Quase sempre demandam ações gerenciais para a correção. Tem potencial para corrigir ~85% dos problemas.

**Processo sob controle estatístico**: quando as **únicas fontes de variação são as causas comuns**.

**Teorema do Limite Central**
https://pt.wikipedia.org/wiki/Teorema_central_do_limite

Segundo a Wikipedia, esse teorema afirma que quando o tamanho da amostra aumenta, a distribuição amostral da sua média aproxima-se cada vez mais de uma distribuição normal.

Usado para normalizar os dados quando eles não são normais. **Somente pode ser usado no CEP**. Não pode ser usado na fase medir, durante os testes de capacidade do processo (Cp, Cpk)
 
### 58 CARTAS DE CONTROLE

Com as **cartas de controle** acompanhamos os dados do processo. Assim, por meio de **gráficos**, é possível verificar se o **processo está sob controle**, ou seja, **sem causas especiais**.

Tipos de cartas (imagem no slide 845):
- Carta por atributo: passa / não passa, aprovado / reprovado, etc.
  - Carta P
  - Carta U
- Cartas para variáveis: diâmetro interno da arruela, torque angular, dureza, etc.
  - Carta I-AM
  - Carta x̄-R - Média e Amplitude
  - Carta x̄-S - 

**Diário de bordo**: uma planilha que geralmente acompanha a carta de processo, para que o operador anote ocorrências relevantes durante as atividades (hora de mudança de matéria-prima, final de lote, _setup_, mudança inesperada de operador, etc). Os registros podem apoiar na investigação de causas especiais.

### 58.1 Limites de controle

Média das médias dos subgrupos:

$\overline{\overline{X}} = \dfrac{ \overline{X_1} + \overline{X_2} + \overline{X_n}  }{n}$

Média das amplitudes dos subgrupos:

$\overline{R} = \dfrac{ R_1 + R_2 + R_n }{n}$

Para o **gráfico das amplitudes**:

**LICR** e **LSCR** - Limites Inferior e Superior de Controle
 - $LICR = D3 * \overline{R}$
 - $LSCR = D4 * \overline{R}$

Sendo D4 e D3 constantes tabeladas conforme o tamanho da amostra.

Para o **gráfico das médias**:

**LICX** e **LSCX** - Limites Inferior e Superior de Controle
 - $LICX = \overline{\overline{X}} - (A2 \times \overline{\overline{X}})$
 - $LSCX = \overline{\overline{X}} + (A2 \times \overline{\overline{X}})$

Sendo A2 uma constante tabelada conforme o tamanho da amostra.

### 59 ANÁLISE DAS CARTAS DE CONTROLE

🚧 <font color='red'>**Parei aqui em 26/04/2023**</font> 🚧

### 60 CARTAS POR ATRIBUTO



### 61 CAPACIDADE E ESTABILIDADE

## Apresente os pontos mais importantes

- CEP Controle Estatístico do Processo
- O controle de qualidade atua, basicamente, no resultado do processo. O CEP atua no processo.
- Processo sob controle estatístico: quando as únicas fontes de variação são as causas comuns.
- O Teorema do Limite Central afirma que quando o tamanho da amostra aumenta, a distribuição amostral da sua média aproxima-se cada vez mais de uma distribuição normal.
- Carta x̄-R: 2 gráficos: Gráfico das Médias e Gráfico das Amplitudes

## Referências
- Videoaulas 57 a 61 https://vimeo.com/showcase/10027791 (Acesso restrito aos alunos) 