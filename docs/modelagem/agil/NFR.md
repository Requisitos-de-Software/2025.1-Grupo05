# NFR Framework

## 1. Introdução

<div style="text-align: justify; text-indent: 2cm;">
O NFR Framework (Non-Functional Requirements Framework) é uma abordagem usada para identificar, categorizar e organizar os <a href="https://requisitos-de-software.github.io/2025.1-IBGE/elicitacao/Requisitos/">Requisitos Não-Funcionais</a> (non-functional requirements, NFRs) em sistemas de software.
</div>

## 2. Softgoal Interdependency Graph

<div style="text-align: justify; text-indent: 2cm;">
O Softgoal Interdependency Graph (SIG) é uma representação visual fundamental do funcionamento do NFR Framework. Ele organiza os softgoals (metas não funcionais) e explicita, de forma gráfica e concisa, as decisões da equipe de desenvolvimento em relação a esses objetivos, bem como suas interdependências e possíveis conflitos <a id="anchor_1" href="#REF1">^1^</a>.
</div>

### 2.1 Tipos de Softgoal

Segundo Silva (2019)<a id="anchor_1" href="#REF1">^1^</a>., existem três tipos de Softgoals:
<br><br>
- **NFR:** representa os requisitos não-funcionais e podem estar interrelacionados, organizados em catálogos e apresentados de forma hierárquica no desenvolvimento do projeto.
<br><br>
- **Operacionalização:** representam soluções de implementação para satisfazer softgoals NFR ou outros softgoals de operacionalização. Essas soluções
incluem operações, processos, representações de dados, estruturações e restrições
no sistema alvo para atender às necessidades indicadas pelos softgoals NFR e de
operacionalização.
<br><br>
- **Afirmação:** permitem que as características do domínio (como prio-
ridades e carga de trabalho) sejam consideradas e devidamente refletidas no processo
de tomada de decisão. Eles servem como justificativa para apoiar ou negar a forma
como os softgoals são priorizados, refinados e os componentes são selecionados. Os
softgoals de afirmação fornecem as razões para as decisões de desenvolvimento, facili-
tando a revisão, a justificativa e a mudança do sistema, bem como o aprimoramento
da rastreabilidade.
<br><br>
A representação destes softgoals podem ser observados na Figura 1.


<font size="3"><p style="text-align: center"><b>Figura 1</b> - Tipos de Softgoal</p></font>

<center>
<img src="./../../../assets/images/modelagem/fonte1NFR.png" width= "480">
</center>

<font size="3"><p style="text-align: center"> Fonte: (SILVA, 2019)</p></font>



#### 2.1.1 Interdependências

<div style="text-align: justify; text-indent: 2cm;">
As interdependências representam as relações estabelecidas entre diferentes softgoals no NFR Framework. Essas interdependências são classificadas em dois tipos principais: decomposições e contribuições.
</div>

#### 2.1.2 Decomposições

<div style="text-align: justify; text-indent: 2cm;">
As decomposições no NFR Framework podem ocorrer em diferentes níveis de abstração: softgoals de requisitos não funcionais (NFR), de operacionalização, de afirmação e de priorização (SILVA, 2019)<a id="anchor_1" href="#REF1">^1^</a>. Nas três primeiras categorias, os softgoals são subdivididos em softgoals mais específicos, contribuindo para a redução de ambiguidades e facilitando a análise e o refinamento dos requisitos. Os quatro tipos de decomposição estão representados na Figura 2:
</div>

<div style="text-align: justify; padding-left: 4em; margin-top: 1em;">
<ul>
<li>Decomposição NFR: permite dividir preocupações primordiais em partes menores, promovendo clareza e auxiliando na definição de prioridades.

<li>Decomposição de Operacionalização: visa detalhar uma solução geral, desmembrando-a em soluções específicas e concretas.

<li>Decomposição de Afirmação: utilizada para expressar a aceitação ou negação de justificativas específicas no contexto do projeto.

<li>Decomposição de Priorização: uma decomposição especial em que o softgoal é refinado em outro softgoal de mesmo tipo e tópico, mas com a associação de um nível de prioridade.
</ul>
</div>

<font size="3"><p style="text-align: center"><b>Figura 2</b> - Tipos de Decomposição</p></font>

<center>
<img src="./../../../assets/images/modelagem/fonte2NFR.png" width= "500">
</center>

<font size="3"><p style="text-align: center"> Fonte: (SILVA, 2019)</p></font>

#### 2.1.3 Contribuições


<div style="text-align: justify; text-indent: 2cm;">
No NFR Framework, os softgoals tendem a se especializar progressivamente por meio de refinamentos. Consequentemente, um softgoal derivado pode contribuir para o softgoal do qual se originou de maneira parcial ou integral, e de forma positiva ou negativa. A seguir, apresentam-se os principais tipos de contribuição <a id="anchor_1" href="#REF1">^1^</a>:
</div>

<div style="text-align: justify; padding-left: 4em; margin-top: 1em;">
<ul>

<li>AND: todos os softgoals derivados devem ser satisfeitos para que o softgoal principal também o seja.

<li>OR: a satisfação de qualquer um dos softgoals derivados é suficiente para satisfazer o softgoal principal.

<li>MAKE (++): o softgoal derivado contribui de forma totalmente positiva para o softgoal principal, garantindo sua satisfação.

<li>BREAK (--): o softgoal derivado contribui de forma totalmente negativa, comprometendo a satisfação do softgoal principal.

<li>HELP (+): há uma contribuição positiva parcial, que favorece o softgoal principal, mas sem garanti-lo plenamente.

<li>HURT (-): contribuição negativa parcial, que dificulta a satisfação do softgoal principal, porém sem invalidá-lo completamente.

<li>UNKNOWN (?): o tipo e intensidade da contribuição são indeterminados.

<li>EQUALS: indica uma relação direta de equivalência entre o softgoal derivado e o softgoal principal — satisfazer um implica satisfazer o outro.

<li>SOME: a forma da contribuição (positiva ou negativa) é conhecida, mas sua intensidade permanece indefinida.
</ul>
</div>

#### 2.1.4 Procedimentos de Avaliação

<div style="text-align: justify; text-indent: 2cm;">
Segundo Silva (2019), o procedimento de avaliação determina o grau que os requisitos não funcionais são satisfeitos por um conjunto de decisões. Dessa forma, o procedimento de avaliação determina
se cada softgoal ou interdependência do SIG foi suficientemente satisfeito. Para isso, são
atribuídos rótulos para os softgoals <a id="anchor_1" href="#REF1">^1^</a>:
</div>

**✓ (Satisfeito):** Indica que um requisito contribui positivamente para a satisfação de outro.


**𝒲⁺ (Fracamente satisfeito):** Representa uma contribuição positiva, porém com intensidade reduzida.


**✗ (Negado):** O requisito impacta negativamente outro, negando ou contradizendo sua realização.


**𝒲⁻ (Fracamente negado):** Sinaliza um impacto negativo menos intenso que o anterior.

**⚡(Conflitante):** Indica a existência de um conflito entre requisitos, com características tanto positivas quanto negativas.

**u (Indeterminado):** Representa uma relação cujo impacto é desconhecido ou não pode ser determinado com as informações disponíveis.


## 3. Metodologia
<div style="text-align: justify; text-indent: 2cm;">
Os frameworks foram agrupados por temas, que por sua vez foram divididos em três categorias para limitar o escopo da análise. A partir desses temas, foi realizada uma introspecção para a construção do Softgoal Interdependency Graph (SIG), tomando como base os tópicos gerais definidos. O objetivo foi estabelecer relações com os requisitos não funcionais da Tabela 12.
</div>
<div style="text-align: justify; text-indent: 2cm;">
Em seguida, realizou-se uma revisão da literatura para embasar teoricamente o modelo, seguida pela validação do SIG construído. A ferramenta utilizada para a elaboração do gráfico foi o <a href="https://app.diagrams.net/">Draw.io</a>.
</div>

## 4. Cartões de Especificação
<div style="text-align: justify; text-indent: 2cm;">
 O cartão de especificação é um documento utilizado na engenharia de requisitos para registrar, de forma clara e padronizada, os Requisitos Não Funcionais (RNFs) de um sistema. Ele serve como um guia para garantir que todos os envolvidos no projeto compreendam o propósito, a origem, a prioridade e os critérios de aceitação de cada requisito. O cartaão de especificação do presente projeto segue o seguinte formato:
</div>

<font size="3"><p style="text-align: center">Tabela 1: Template de cartão de especificação </p></font>

| Campo              | Descrição |
|--------------------|-----------|
| **Nr Requisito:**  | RNFXX |
| **Classificação:** | Classificação do RNF conforme a hierarquia do catálogo. |
| **Descrição:**     | Declaração única do significado do requisito |
| **Justificativa:** | Justificativa sobre a criação do requisito |
| **Origem:**        | Origem do requisito (*stakeholder*, norma técnica e etc...) |
| **Critério de Ajuste:** | Métrica do requisito que possa ser testada e que deve ser satisfeita. |
| **Dependências:**  | Requisitos relacionados a este. |
| **Prioridade:**    | Um número usado para decidir a importância relativa deste requisito entre os outros RNFs (varia de 1 a 10). A prioridade mínima é 1 e a máxima é 10. |
| **Conflitos:**     | Requisitos conflitantes com este. |
| **História:**      | Data de criação e de modificações. |

<font size="2"><p style="text-align: center">Fonte:[Caio Duarte](https://github.com/caioduart3), 2025.</p></font>

<font size="3"><p style="text-align: center">Tabela 2: Cartão de especificação - RNF80 </p></font>

| Campo              | Descrição |
|--------------------|-----------|
| **Nr Requisito:**  | RNF80 |
| **Classificação:** | Usabilidade  |
| **Descrição:**     | O sistema deve apresentar feedback visual e/ou sonoro para todas as ações do usuário, como cliques, carregamentos e envios de formulários. |
| **Justificativa:** | O feedback imediato melhora a experiência do usuário, reduz a incerteza sobre o funcionamento do sistema e aumenta a confiança nas interações. |
| **Origem:**        | Stakeholder (usuários), diretrizes de UX (User Experience). |
| **Critério de Ajuste:** | Para 100% das interações de entrada do usuário, deve haver resposta visual (como mudança de cor, loading spinner ou mensagem de sucesso/erro). Testes devem confirmar que usuários percebem o feedback em até 1 segundo após a ação. |
| **Dependências:**  | Nenhuma |
| **Prioridade:**    | 8 |
| **Conflitos:**     | Pode conflitar com configurações de acessibilidade ou desempenho em dispositivos com recursos limitados. |
| **História:**      | Criado em 31/05/2025. Sem modificações até o momento. |



<font size="2"><p style="text-align: center">Fonte:[Mayara Marques](https://github.com/maymarquee), 2025.</p></font>


<font size="3"><p style="text-align: center">Tabela 3: Cartão de especificação - RNF77 </p></font>

| Campo              | Descrição |
|--------------------|-----------|
| **Nr Requisito:**  | RNF77 |
| **Classificação:** | Usabilidade |
| **Descrição:**     | A interface do aplicativo deve seguir as diretrizes de design responsivo, garantindo usabilidade adequada em dispositivos móveis e tablets. |
| **Justificativa:** | Com o crescente uso de dispositivos móveis, é essencial que o aplicativo ofereça uma boa experiência de uso em diferentes tamanhos de tela. |
| **Origem:**        | Stakeholder (usuários finais) e boas práticas de design (Material Design, Human Interface Guidelines). |
| **Critério de Ajuste:** | O sistema deve se adaptar corretamente a resoluções de tela entre 320px e 1280px, sem perda de funcionalidade ou legibilidade. Testes de usabilidade devem confirmar uma taxa de sucesso mínima de 90% em tarefas básicas. |
| **Dependências:**  | Nenhuma |
| **Prioridade:**    | 9 |
| **Conflitos:**     | Pode conflitar com requisitos que definem layouts fixos ou específicos para desktop. |
| **História:**      | Criado em 31/05/2025. |

<font size="2"><p style="text-align: center">Fonte:[Caio Duarte](https://github.com/caioduart3), 2025.</p></font>

## 5. NFR

Analisados os requistos, conclui-se que, no geral, os requisitos do projeto buscam englobar as seguintes softgoals de **Usabilidade** e **Portabilidade**.

O NFR do projeto pode ser visualizado ao clicar aqui: [ABRIR IMAGEM](./../../assets/images/modelagem/NFR-IBGE.drawio.svg) ou visualizado na Figura 3: 

<font size="3"><p style="text-align: center">Figura 3: NFR framework - IBGE </p></font>

![NFR](./../../assets/images/modelagem/NFR-IBGE.drawio.svg)

<font size="2"><p style="text-align: center">Fonte: [Caio Duarte](https://github.com/caioduart3), [Gabriel Pinto](https://github.com/GabrielSPinto), [João Félix](https://github.com/joaofmoreiraa), [Laryssa Felix](https://github.com/felixlaryssa), [Letícia Monteiro](https://github.com/LeticiaMonteiroo), [Ludmila Nunes](https://github.com/ludmilaaysha) e [Mayara Marques](https://github.com/maymarquee), 2025.</p></font> 

## 4. Bibliografia

> <a id="REF1" href="#anchor_1">1.</a> SILVA, Reinaldo Antônio. NFR4ES: Um Catálogo de Requisitos Não-Funcionais para Sistemas Embarcados. Centro de Informática UFPE, Recife, 2019. Disponível em: <https://repositorio.ufpe.br/handle/123456789/34150>. Acesso em: 22/05/2023.

> <a id="REF2" href="#anchor_2">2.</a>CHUNG, L., NIXON, B. A., YU, E., MYLOPOULOS, J. Non-functional requirementsin software engineering. Springer Science & Business Media: [S.l.], 2000. v. 5.

## 5. Histórico de Versões 

<font size="3"><p style="text-align: center">Tabela X: Histórico de versões</p></font>

| Versão |Descrição     |Autor                                       |Data    |Revisor|
|:-:     | :-:          | :-:                                        | :-:        |:-:|
|1.0     |Criação do documento com introdução e bibliografia| [Caio Duarte](https://github.com/caioduart3)| 28/05/2025 | [Mayara Marques](https://github.com/maymarquee) |
|1.1     |Adiciona tabela 2| [Mayara Marques](https://github.com/maymarquee)  | 31/05/2025 | [Caio Duarte](https://github.com/caioduart3) |
|1.2     |Adiciona tabela 3| [Caio Duarte](https://github.com/caioduart3)| 31/05/2025 | [Mayara Marques](https://github.com/maymarquee) |

<font size="2"><p style="text-align: center">Fonte: [Caio Duarte](https://github.com/caioduart3), [Gabriel Pinto](https://github.com/GabrielSPinto), [João Félix](https://github.com/joaofmoreiraa), [Laryssa Felix](https://github.com/felixlaryssa), [Letícia Monteiro](https://github.com/LeticiaMonteiroo), [Ludmila Nunes](https://github.com/ludmilaaysha) e [Mayara Marques](https://github.com/maymarquee), 2025.</p></font> 