## Curso Green Belt Six Sigma - projeto 04/2023
## Aula 05: Medir do DMAIC.

Conteúdos de 3.0 a 3.4 do cronograma.

Data da entrega: 13/03/2023

Autor: [@haldirleao](https://github.com/haldirleao)

## Faça um resumo sobre os vídeos abordados nesta aula

### 3.0 COLETA DE DADOS

A primeira atividade do M do DMAIC é desenvolver o plano de coleta de dados. 
A coleta de dados é o equilíbrio entre tempo, dinheiro, exatidão e precisão!

A etapa **medir** pode ser **uma das mais demoradas de projetos 6 sigma**, por motivos como:
- as medições somente têm valor se o sistema de medição for confiável. Enquanto não for, há que melhorá-lo antes das medições
- a execução da medição pode depender de fatores como: processo em andamento, disponibilidade da peça, disponibilidade de recursos (pessoas, instrumentos)

O **MSA (_Measurement System Analysis_)** é um método para medição, validação dos instrumentos, treinamento e testes dos operadores (com base em procedimentos), teste das interações, cálculos da incerteza, repetibilidade, reprodutibilidade, etc.

Passo-a-passo para a coleta de dados:
- Definições operacionais (“o que” e “como” medir). As definições operacionais uniformizam as informações. O objetivo final é “acertar de primeira”
- Elaborar plano de medição
- Coletar dados
- Exibir os dados

### 3.1 AMOSTRAGEM

Amostragem é uma **inferência estatística**. Segundo a Wikipedia, a inferência estatística é um ramo da Estatística cujo objetivo é fazer afirmações a partir de um conjunto de valores representativo (amostra) sobre um universo (população).

A amostragem:
- poupa tempo e dinheiro
- é uma boa alternativa em razão das limitações e/ou dificuldades de se coletar os dados da população
- com o nível de confiança adequado, pode-se tomar decisões razoáveis

Amostragens podem ser sistemáticas (baseada num conjunto de regras) ou aleatórias.

As amostras devem representar o todo (a população). Se isso não ocorrer, as análises e tomadas de decisão não serão minimamente confiáveis. **Exemplo ruim**: peças fabricadas de segunda a sexta-feira, em dois turnos. As amostras retiradas somente na segunda e terça-feira. **Exemplo bom**: as amostras são retiradas todos os dias e turnos.

Entre os diversos métodos/formulários para registrar a coleta de dados, pode-se citar: - diagrama de concentração; - folhas de verificação; - distribuição do processo.

Resultados esperados na coleta de dados:
- desempenho do processo ao longo do tempo
- determinar a relação entre duas ou mais variáveis (Ex.: tempo de fritura x pastéis queimados)
- base confiável para a tomada de decisão

### 3.2 DADOS CONFIÁVEIS

Feita a coleta de dados, a próxima atividade do M do DMAIC é **comprovar** que tais **dados** são **confiáveis**.

**É importante notar que a variabilidade está sempre presente, mesmo num bom sistema de medição!**

O **Sistema de Medição (SM)** é a combinação de:
- instrumentos de medição
- pessoas que estão medindo
- condições em que os dados foram coletados (temperatura, luminosidade, umidade, etc)

Um SM pode não funcionar bem devido:
- à alta variação
- à medição incorreta (descalibrado - mede um valor diferente do real)
- ao uso de instrumento inadequado

Para sabermos realmente qual é a variação atual de um processo, é necessário:
- conhecer quanto da variação tem origem no SM
- que o SM tenha variação bem menor que a variação do processo

**Resolução ou discriminação**: É a menor fração medida pelo equipamento de medição (Ex.: a **resolução** de uma régua escolar comum é de **1 mm**). Recomendação da ISO / TS: usar **instrumentos com resolução de 1/10 da tolerância** especificada para a medição (Ex.: se a tolerância é de 1cm, usar instrumento com resolução de **1/10 cm = 1 mm**).

O que deve ser avaliado em um SM? A repetitividade e a reprodutibilidade (repe-repro ou R&R). 

**Repetitividade tem relação com o instrumento**. 

**Reprodutibilidade tem relação com o operador**.

A repe avalia a precisão do instrumento (ou variação do equipamento). É conseguida pela variação nas medidas obtidas com um instrumento de medição quando usado várias vezes por um mesmo operador medindo a mesma peça. 

A repro avalia a precisão dos operadores (ou variação do operador). É conseguida pela variação nas  medidas realizadas por diferentes operadores, utilizando o mesmo instrumento e medindo a mesma característica na mesma peça.

**Variabilidade_total_do_processo = Variabilidade_do_produto + Variabilidade_do_SM**

**Variabilidade_do_SM = variabilidade_repe + variabilidade_repro**

**ANOVA GR&R (_Analysis of variance Gauge Repe & Repro_)**, técnica que usa um modelo de efeitos aleatórios de análise de variância (ANOVA) para avaliar um sistema de medição. A avaliação de um sistema de medição não se limita ao instrumento de medição, mas a todos os tipos de métodos de teste e outros sistemas de medição.

Critérios de aceitação - Estudo do SM. GR&R: 
- 0% a 10%:  Aceitável;
- 10% a 30%: Aceitável dependendo da importância, custo-benefício de reparo ou retrabalho, etc. Comum acordo entre fornecedor e cliente;
- \>30%: Inaceitável. Corrigir SM e repetir R&R.

### 3.3 PRECISÃO E EXATIDÃO

Ao se analisar um processo se deve levar em consideração a sua **precisão e exatidão**. O objetivo é sempre chegar a processos precisos e exatos. 

A **precisão** tem relação com a dispersão dos dados. Quanto **menor a dispersão, maior a precisão**. 

A **exatidão** tem relação com a **localização da média dos dados**, ou seja,  é o grau de concordância entre um valor medido e um valor verdadeiro de um mensurando. Exemplos:
1. Os tiros atingirem o centro do alvo, ou bem próximo dele.
2. você coloca sobre a plataforma da balança um peso-padrão de 20kg que está certiﬁcado pelo Inmetro ou Ipem. Se a balança indicar os mesmos 20 kg, ela possui exatidão.

A **análise do SM** pode ser realizada por **dados variáveis** ou de **atributos**.

Valor por atributo = qualitativo (Ex.: sim / não, passa / não passa, satisfeito / insatisfeito, sexo) 

Valor por variável = dado medido = quantitativo (Ex.: comprimento, diâmetro, massa, volume, coluna d’água).

As variáveis se medem com instrumentos que possuem escala de medição: micrômetro, régua, torquímetro, balança, etc.

Os atributos se verificam com instrumentos de resultado discreto: calibrador passa/não-passa, bom ou ruim, aceita-rejeita, etc.

A partir deste vídeo será usado o **Minitab _Statistical Software_**. Slogan do fabricante:

_“Visualize, analise e aproveite o poder dos dados para resolver seus maiores desafios comerciais em qualquer lugar que esteja, na nuvem”_.

Optei por usar a versão Web, ao menos por enquanto. Atenção com a qualidade da fonte de dados: “sujeiras” nos dados leva a erros 

### 3.4 EXEMPLO: DADOS CONFIÁVEIS

Neste vídeo é dado um exemplo de como usar o Minitab para fazer a análise do SM via R&R, sendo que os dados são do tipo variável (diâmetro).

No primeiro Estudo de R&R ANOVA os resultados foram ruins, logo o SM não está confiável. As variações foram:
- Total de R&R da medição = 80,24% (Variação R&R deve ser menor que 30%, sendo o desejado menor que 10%);
- Peça a peça = 59,68% (deveria representar a maior parte da variação, entre 80% e 90%).

Existem tanto variações na repe = 68,11% quanto na repro = 42,41%. Número de categorias distintas = 1 (deveria ser >=5).

O **número de categorias distintas** é uma métrica utilizada nos estudos de medição R&R para identificar a capacidade de um sistema de medição para detectar uma diferença na característica medida. O número de categorias distintas representa o número de intervalos de confiança não sobrepostos que abrangem a gama de variação do produto. O número de categorias distintas também representa o número de grupos dentro de seus dados do processo que o seu sistema de medição é capaz de discernir. O Manual de MSA publicado pelo Automotive Industry Action Group (AIAG) recomenda que 5 ou mais categorias indiquem um sistema de medição aceitável. 

**O estudo acima indica que se deve treinar os operadores, bem como trocar o instrumento ou calibrá-lo.**

## Apresente os pontos mais importantes

- As medições somente têm valor se o **Sistema de Medição** for **confiável**. Não acredite nas medidas, simplesmente porque recebeu a informação. **Teste e valide o MSA!**
- A **coleta de dados** é um **equilíbrio entre tempo, dinheiro, exatidão e precisão**! Estes são os principais motivos para a escolha da **amostragem**.
- As amostras devem ser representativas do todo (da população). Se isso não ocorrer, as análises e tomadas de decisão não serão minimamente confiáveis.
- Lembre-se: **O principal objetivo da coleta de dados é termos uma base confiável para a análise e tomada de decisão**.
- Para sabermos realmente qual é a variação atual de um processo, é necessário: 
   - conhecer quanto da variação tem origem no SM; 
   - que o SM tenha variação bem menor que a variação do processo.
- Se a **repe** e **repro (R&R)** não estiverem satisfatórias, não inicie a coleta de dados até resolver o problema no SM!
- **Variabilidade_total_do_processo = Variabilidade_do_produto + Variabilidade_do_SM**
- **Variabilidade_do_SM = variabilidade_repe + variabilidade_repro**
- Critérios de aceitação - Estudo do SM. GR&R: 
  - 0% a 10%:  Aceitável;
  - 10% a 30%: Aceitável dependendo da importância, custo-benefício de reparo ou retrabalho, etc. Comum acordo entre fornecedor e cliente;
  - \>30%: Inaceitável. Corrigir SM e repetir R&R.

## Referências
- Videoaulas 3.0 a 3.4 https://vimeo.com/showcase/9985114 (Acesso restrito aos alunos)
- https://pt.wikipedia.org/wiki/Infer%C3%AAncia_estat%C3%ADstica
- https://en.wikipedia.org/wiki/ANOVA_gauge_R&
- [Minitab: Uso do número de categorias distintas](https://support.minitab.com/pt-br/minitab/20/help-and-how-to/quality-and-process-improvement/measurement-system-analysis/supporting-topics/gage-r-r-analyses/using-the-number-of-distinct-categories)