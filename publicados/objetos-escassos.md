---
title:  "Objetos Escassos"
date:   2004-01-01
categories:
   -  Artigo
tags:
  -
author:
  - Nick Szabo
---
```
Traduzido por: Steffan Diorgy 
Revisado por: Cypherpunks Brasil
```


Objetos Escassos 
Nick Szabo
================

#### Originalmente publicado em 2004

### Abstrato
===exibe no card daqui pra baixo===

*Uma abordagem mais intuitiva e segura para programação com objetos distribuídos através de limites de confiança é apresentada. A abordagem envolve objetos escassos e software para apoiar os mercados na negociação de "direitos" de objetos escassos.*

### Introdução

Objetos escassos são objetos computacionais que, como objetos físicos, são finitos e excludentes, e forçam o cliente a conservar ou consumir (usar) seus próprios direitos para usar o objeto. Referências a objetos escassos são [certificados de portador](http://nakamotoinstitute.org/contracts-with-bearer/) com duas propriedades principais: (1) são tokens use uma vez ou usados N vezes e (2) como dinheiro digital são transferidos usando compensação on-line usando "listas gastas" para conservar o número dessas referências de objetos escassos.

Objetos escassos, também conhecidos como objetos conservados, fornecem uma metáfora amigável ao usuário e ao programador para objetos distribuídos que interagem entre limites de confiança. (Para simplificar o idioma, usarei o tempo presente para descrever arquiteturas e software hipotético). Objetos escassos também nos dão a capacidade de traduzir as preferências do usuário em contratos sofisticados, através do tradutor de mercado descrito abaixo. Essas inovações nos permitirá, pela primeira vez para romper a [barreira mental do custo de transação](http://szabo.best.vwh.net/micropayments.html) para micropagamentos e uma [economia de micromercados](https://web.archive.org/web/20000229091752/http://www.agorics.com/agorpapers.html).

Um objeto escasso é um objeto de software (ou um de seus métodos) que usa um recurso finito e excludente - seja espaço em disco, largura de banda de rede, uma fonte de informações cara como um segredo comercial ou uma cotação de ações minimamente atrasada ou uma ampla variedade de outros recursos escassos usados ​​por aplicativos on-line. Objetos escassos restringem os chamadores remotos a invocar métodos de maneiras que usam apenas determinados recursos e não divulgam os segredos comerciais. Além disso, os invólucros de objetos escassos formam a base para uma economia on-line de objetos escassos que faz uso eficiente dos recursos escassos subjacentes.

Objetos escassos também são um novo modelo de segurança. Nenhum modelo de segurança até o momento foi amplamente usado para distribuir objetos entre limites de confiança. Isto é devido a suas conseqüências obscuras, suas origens na computação TCB-unica, ou ambos. A segurança de objetos escassos é muito mais facilmente compreendida, uma vez que se baseia na duplicação em objetos computacionais das características intuitivas essenciais das posses físicas. Nossos cérebros raciocinam de maneiras muito mais sofisticadas sobre objetos físicos do que sobre objetos computacionais. Objetos escassos são assim facilmente compreendidos por programadores e usuários finais. Objetos escassos reduzem os custos de transação mental, que são a principal barreira para o comércio sofisticado de pequena escala na Internet. Finalmente, objetos escassos resolverão pela primeira vez ataques de negação de serviço,

A metáfora física intuitiva de objetos escassos dá aos objetos escassos as seguintes propriedades básicas:

1.  Conservação de objetos atômicos
2.  Composição hierárquica de objetos (análoga à composição espacial)

Intimamente relacionado a estes é uma propriedade social de objetos críticos para o sucesso das economias:

1.  Um delineamento claro de direitos e responsabilidades de propriedade. Em outras palavras, externalidades mínimas. Os direitos de propriedade especificam controle residual e responsabilidade sobre estados do mundo para os quais obrigações ou direitos específicos não são completamente especificados em contratos.

Direitos de propriedade e contratos são metodologias altamente evoluídas para lidar com objetos econômicos e entre si através de limites de confiança. A escassa arquitetura de objetos pode reutilizar esse paradigma de trabalho, porque reutiliza o modelo mental do mundo físico no qual esse paradigma de segurança foi inventado.

Com objetos escassos, qualquer cálculo entre os limites de confiança terá essas propriedades de atomicidade, conservação, composição e a clara delimitação de direitos e responsabilidades. Esse modelo é bastante restritivo em comparação com o que estamos acostumados dentro dos limites de confiança. No entanto, será muito mais fácil impedir que os programadores escrevam código obscuramente inseguro, o que é fácil de fazer com ACLs, recursos ou criptografia. Além disso, a conservação (escassez) e a falta de externalidades são os dois principais pressupostos da microeconomia, o estudo das transações comerciais através dos limites da confiança. Assim, o escasso modelo de segurança de objetos nos permite herdar uma rica literatura de raciocínio formal sobre esses sistemas.

Objetos escassos são, em outras palavras, commodities online. Essas mercadorias podem representar, normalmente, direitos (ou expectativas) aos serviços - o direito de usar um serviço de notícias ou e-mail (ou um componente desse pacote de direitos, por exemplo, o direito de usar o servidor de e-mail desse serviço), direito de fazer o upload ou cache de conteúdo, o "direito" (aqui mais como uma expectativa) de ter e-mail lido (postagem digital para evitar spam), etc. Tais direitos de serviço geralmente serão limitados ao cliente pelo tempo ou uso de recursos ou número de invocações. Quando representados adequadamente, por objetos escassos, esses serviços são conservados. Tais "direitos" ou expectativas codificadas são aplicadas contra o servidor pela reputação, pela "física" de objetos escassos, ou ambos, em substituição ou em adição aos caros meios legais tradicionais.

Objetos escassos também podem representar relacionamentos únicos ou finitos entre pessoas e bits - nomes que correspondem a endereços, propriedade de marcas registradas, autoria de conteúdo, propriedade de certos direitos ao conteúdo (o que provavelmente não inclui, por razões de segurança, o direito de excluir outros de copiar os bits), etc.

Objetos escassos não são um modelo completo de computação entre limites de confiança. Na verdade, existem muitos [contratos inteligentes](http://szabo.best.vwh.net/idea.html) que podem ser implementados com protocolos criptográficos e / ou hardware seguro, mas não com objetos escassos. O que os objetos escassos oferecem é uma base direta para a implementação, de forma intuitivamente segura, das economias de troca de mercadorias anônimas formalizadas na microeconomia de maneira P2P na Internet.

Outra área importante para objetos escassos é o raciocínio sobre as cadeias de suprimentos. Em objetos distribuídos, o gráfico de chamadas é a cadeia de suprimentos. Para estender os gráficos de chamadas através dos limites de confiança, devemos substituir os relacionamentos rígidos cliente-servidor com relacionamentos de cliente-fornecedor dinamicamente adaptáveis. O ideal aqui é criar um rico conjunto de ferramentas de manipulação de exceções entre limites de confiança. Observe que os riscos de crédito são um subconjunto adequado dos riscos da cadeia de suprimentos. Recentemente, Ka-Ping Yee colocou o problema da cadeia de suprimentos de maneira sucinta: "Desconfie de valores de retorno de objetos nos quais você não confia".

### Controle de Uso vs. Controle de Acesso

A escassa arquitetura de objetos sugerida aqui compartilha algumas coisas em comum com os recursos, mas protege mais tipos de recursos e é muito mais acessível para usuários e programadores. Capacidades (juntamente com ACLs) são um meio de implementar o [controle de acesso](http://srl.cs.jhu.edu/pubs/SRL2003-03.pdf). O controle de acesso simplesmente lida com o primeiro nível de questão sobre se uma entidade tem acesso ou não a um determinado recurso. Se uma entidade tiver esse acesso, esse acesso será, conforme modelado ou implementado por recursos básicos ou ACLs, efetivamente ilimitado em escopo. Objetos escassos, por outro lado, limitam o uso de recursos de três maneiras - primeiro, limitando a quantidade de recursos usados ​​por invocação, segundo, limitando o número de recursos usados ​​por direito (por ticket) e terceiro, limitando o número de bilhetes emitidos.

### Objetos escassos e POLA

Um sistema de capacidade bruta distribuída (ou seja, o que Mark Miller chama de ["caps-as-data"](http://www.eros-os.org/pipermail/cap-talk/2004-November/002337.html), para distinguir de capacidades locais para o TCB ("objeto caps"), que têm propriedades de segurança estritamente mais fortes) dar capacidades de duração infinita e invocações ilimitadas, não pode ser considerado como um verdadeiro princípio do sistema de menor autoridade (POLA). Para uma referência de objeto para implementar o POLA, ele deve ser finito em todas as dimensões. Um verdadeiro sistema POLA nunca dá mais autoridade do que é necessário e apropriado para calcular a função necessária. Nunca é necessário ou apropriado alocar recursos infinitos e, geralmente, não é necessário alocar recursos grandes. A escassa arquitetura de objetos é o primeiro design para sistemas de objetos a atingir autoridade finita e permitir pequenas alocações para objetos que precisam apenas de pequenas quantidades de recursos. Objetos escassos são, portanto, a primeira arquitetura a tornar possível o verdadeiro POLA.

### Arquitetura de objetos escassos

A arquitetura de objetos escassos epende de uma arquitetura de objetos distribuídos que faz suposições mínimas de segurança. Uma boa estratégia de implementação pode ser, portanto, para implementar este modelo em cima de [E](http://www.erights.org/). Nenhum uso sofisticado de sua arquitetura de capacidade distributecd precisa ser feito para distribuir com segurança objetos escassos; em vez disso, os recursos de conservação de recursos de objetos escassos podem ser confiáveis ​​para proteger recursos.

Um direito de portador de invocar um método de objeto escasso assume a forma de um certificado de portador ou *ticket*. Ele pode ser *genérico*, significando um direito a uma invocação N de um conjunto de objetos semelhantes ou idênticos, ou *específico*, significando um direito de invocar um método de objeto específico de uma maneira única. Os direitos genéricos são fungíveis e podem ser transferidos sem relação, usando a cegueira de Chaumian.

As etapas gerais para criar um objeto escasso são (1) definir um objeto normal e, em seguida, (2) envolvê-lo em uma camada que proteja seus métodos públicos usando tickets. Nosso esboço da arquitetura aqui descreve como essa camada de embalagem pode funcionar.

A camada em questão envolve três servidores diferentes: um agente de transferência (TA), um Provedor e um Emissor. O Emitente e o TA funcionam como uma moeda digital sem dinheiro. O Emitente assina bilhetes. O TA elimina a transferência de bilhetes para direitos genéricos. Tanto a Emissora quanto a TA possuem cópias das chaves privadas ("chapas") correspondentes a cada emissão de direito genérico. Um tipo específico de direito genérico (por exemplo, uma denominação específica de moeda digital) pode ter vários problemas, geralmente ordenados sequencialmente. O dinheiro digital é um caso especial: o dinheiro é o mais genérico dos direitos. Aqui está outro exemplo de um direito genérico, ou classe de objetos fungíveis: "Um banco de dados SQL queriable com até 10 MB de armazenamento, e certas garantias de tempo de resposta padrão".

É uma opção de design combinar ou não o Emissor e o TA em um único servidor (portanto, reduzir a exposição da chave privada) ou mantê-los separados (permitindo assim determinados controles pessoais baseados na [separação de tarefas](http://szabo.best.vwh.net/groupcontrols.html)). Servidores distribuídos, descritos abaixo, são uma maneira ainda melhor de aumentar a confiabilidade dos Emissores e TAs.

O Provedor é responsável por realmente manter o objeto, que pode conter um estado exclusivo. Publica uma descrição assinada de seu método de objeto escasso, descrevendo um tipo particular de direito genérico (por exemplo, na forma de pré e pós-condições de projeto por contrato). O emissor e o agente de transferência criam as placas e preparam-se para emitir tickets para o método.

Qualquer um ou todos esses servidores de componentes podem ser distribuídos, usando os métodos descritos [aqui](http://szabo.best.vwh.net/coalition.html) e [aqui](http://nakamotoinstitute.org/secure-property-titles/). Uma assinatura distribuída é usada para emitir tickets (M de N deve assinar usando uma chave privada distribuída para que uma assinatura verificável seja produzida). Essa distribuição reduz muito a exposição à quebra de confiança e, portanto, reduz os custos de transação mental do rastreamento de reputação.

Para implementar transferências exclusivas, o TA mantém uma lista de números de tickets cancelados. Um bilhete é cancelado sempre que é transferido ou usado. O Provedor instrui o TA quando um ticket foi usado ou, alternativamente, ambos gravam em uma lista compartilhada de tickets limpos.

O TA e o Emissor veem apenas classes de objetos fungíveis. O Provedor e os usuários vêem instâncias particulares com um estado exclusivo. No exemplo acima de um direito genérico do banco de dados, o Provedor vê um banco de dados preenchido com informações exclusivas, enquanto o TA e o Emissor veem apenas a descrição genérica dos métodos de invocação do objeto de banco de dados.

Em contraste com os servidores, o usuário remoto de um objeto escasso encapsula seu stub de invocação de objeto com chamadas que trocam por tickets necessários (novamente usando um tradutor do mercado), envia os tickets conforme necessário com invocações de método para os métodos 'Provider (s). Em alguns casos (esperamos que muitos), serviços genéricos suficientemente idênticos serão fornecidos pelos concorrentes. Quando isso ocorre, um "cliente de ticket" também pode "pesquisar", no sentido de que, se as condições pré ou pós-falha falharem, ou se a chamada for detectada como defeituosa, o cliente do ticket tentará novamente invocando a solicitação. método do concorrente.

O servidor Provider é quase apenas mais um cliente de ticket para o TA, o qual, como outros clientes, pode transferir ou receber tickets. Seu papel especial é informar ao TA quando os tickets foram usados, portanto, deve ser cancelado (ou, ainda, escrever o número do ticket cancelado diretamente para uma lista de números de tickets cancelados que ele compartilha com o TA). Somente o Emissor pode criar tickets e somente o Provedor pode consumi-los.

No núcleo do Provedor está o próprio objeto bruto, o conjunto de métodos que fornece os serviços definidos para clientes de objetos escassos. O provedor é o wrapper em torno desse objeto. Além de suas funções de gatekeeping, verificação de ticket e consumo de tickets, o Provedor pode acompanhar e informar o Emitente sobre o uso de recursos.

A Emissora, por sua vez, é a interface para as funções do micromercado, especialmente o tradutor do mercado descrito abaixo. O Emissor pode, por exemplo, por meio de um tradutor do mercado, que incorpora as preferências da pessoa que opera o Provedor, negociar acordos de permuta nos quais determinados tíquetes são emitidos e trocados por determinados outros tíquetes dando direito de invocar a contraparte ou um escasso métodos de objeto. As negociações também podem ser multipartidárias, ou seja [leilões e trocas secundárias](https://web.archive.org/web/20000229091752/http://www.agorics.com/agorpapers.html) para direitos genéricos também podem ser desenvolvidas para bilhetes de objetos escassos. Por sua vez, o tradutor do mercado, para permitir operações de barganha automatizadas (baixo custo de transação mental), depende da existência de trocas on-line razoavelmente líquidas de direitos genéricos de objetos escassos.

O TA gera a oferta de ingresso somente a pedido do Emissor, e o destrói apenas a pedido do Provedor. Todas as suas próprias transferências conservam o fornecimento de um determinado direito genérico. O Provedor também é responsável pela entrega do serviço ao cliente que satisfaz a descrição do serviço (contrato, por exemplo, condições pré e pós), quando o Provedor "deposita" o (s) bilhete (s) genérico (s), ou seja, adiciona-os à lista cancelada.

O Provedor emite junto com o ticket inicial de direitos genéricos um affadavit assinado, máquina ou legível, descrevendo aspectos do objeto que podem ser não exclusivos e exclusivos, juntamente com o número do ticket da instância e as chaves públicas do direito genérico (s) para os quais é válido. Por exemplo, pode-se dizer "um banco de dados contendo cotações dessas duas dúzias de ações listadas às 12:22 de segunda-feira", sem conter as cotações. Muitas vezes, essa descrição vale mais quando agrupada com direitos exclusivos genéricos, como o direito a um tempo de resposta rápido. Os direitos específicos podem elaborar de maneira única os direitos genéricos, desde que essas elaborações não sejam tomadas para definir direitos exclusivos. Os direitos genéricos permitem que os TAs garretam exclusividade aos usuários e conservação de recursos aos Provedores, enquanto os direitos específicos descrevem o estado único para qualquer grau desejado de elaboração. O Provedor deve estar preparado para atender a qualquer promessa específica que tenha emitido, contanto que seja acompanhado pelos tickets genéricos conservados adequados.

Esse método de composição de direitos específicos e genéricos, transferidos como um pacote, mas com átomos genéricos exclusivos liberados por diferentes TAs, permite que pacotes de direitos arbitrariamente sofisticados, referindo-se a objetos com estado arbitrariamente exclusivo, sejam transferidos sem vinculação. Uma grande variedade de derivados e combinações são possíveis. A única restrição é que a obtenção de direitos a recursos exclusivos específicos deve ser adiada para a fase de consumo ou transferida com compensação on-line por meio de mix de comunicações caras.

Se o Provedor desejasse garetar a exclusividade a um direito específico, a transferência parece exigir um mix de comunicações dispendiosas entre Provedor e cessionário, em vez de um bilhete cego barato. Por exemplo, "Deep Space Station 60 de 0500-0900 de domingo" ou "um bloqueio de autoexec.bat agora" exige exclusividade para um direito específico e, portanto, parece exigir um mix de comunicações para transferir de forma não vinculativa. Por outro lado, "Um bloco de uma hora no DSS-60 em maio" e "o direito de travar o autoexec.bat em algum momento" são genéricos e podem ser transferidos de forma privada com o cegamento muito mais barato, dada uma população suficiente de outros bilhete para esta classe de direito genérico transferido entre a emissão e o consumo de um determinado bilhete.

Os clientes podem lidar com o TA sem um mix de comunicação. Eles lidam com o provedor por meio de um mix de comunicação. Se os titulares inicial e final não conseguissem fazer isso, o Provedor poderia vinculá-los. Se apenas o detentor final não o fizesse, o Provedor poderia identificá-lo como o usuário real do recurso. Assim, para a privacidade total, as transferências genéricas são baratas, e as transferências não exclusivas são baratas, enquanto transferências exsclusivas específicas e, na verdade, o uso do objeto parecem exigir o dispendioso mix de comunicações.

Aqui está uma revisão da nossa arquitetura:

Objetos atômicos conserváveis ​​compositáveis ​​(objetos escassos propriamente ditos):

-   [Tickets (contratos de portador)](http://nakamotoinstitute.org/contracts-with-bearer/) são certificados digitais emitidos por emissores confiáveis ​​ou distribuídos. Cada tipo de ticket representa um direito específico e limitado a um objeto escasso - por exemplo, o direito de invocar um método nesse objeto (ou seja, usar um serviço fornecido por esse objeto) até N vezes ou até um certo limite de uso de recursos . Os ingressos são uma parte essencial do "invólucro de objetos" que faz com que um objeto escasso pareça e aja de maneira rara.
-   Emissores distribuídos, que mantêm [títulos de propriedade](http://nakamotoinstitute.org/secure-property-titles/) para certos contratos ao portador, namespaces e outras entidades publicamente identificáveis ​​de outra forma inseguramente conservadas.
-   Projeto por contrato (por exemplo, especificação detalhada e teste de pré e pós-condições) como uma parte central e não opcional da programação de objetos.

Uma infra-estrutura avançada de objetos escassos também pode incluir:

-   Manipulação de exceções como procedimento de quebra ou quebra de contrato, para converter relacionamentos rígidos cliente-servidor em relacionamentos mutuamente benéficos e dinamicamente reconfiguráveis ​​(competitivos) cliente-fornecedor, adequados para invocação de objetos através de limites de confiança.
-   Rastreamento de reputação do comportamento das cadeias de suprimentos. Protocolos criptográficos, como aqueles usados ​​para criar logs de transações não comprovados e confidencialmente auditáveis, podem ser usados ​​para melhorar a troca de privacidade versus informações de reputação, contanto que estejam ocultos sob uma metáfora intuitivamente clara da reputação do comportamento da cadeia de suprimentos.

Objetos escassos, criando um modelo de computação mais simples e intuitivo através de fronteiras de confiança, podem tornar realidade a distribuição de objetos na Internet global, assim como a simplificação do hipertexto em HTML tornou a Web uma realidade.

### Diagrama da arquitetura proposta de objetos escassos

[![](/static/img/docs/scarce-objects/ScarceObjects.jpg)](/static/img/docs/scarce-objects/ScarceObjects.jpg)

Clique para uma versão maior

### Compras de objetos escassos - O tradutor do mercado

O problema dos [custos mentais de transação](http://szabo.best.vwh.net/micropayments.html) é aquele que sustenta todos os mercados - o esforço mental necessário para fazer compras - para mapear as preferências privadas em relação aos preços, a fim de decidir se um conjunto de direitos vale o custo. Em particular, este problema apresenta uma barreira severa para micropagamentos e alocação de recursos baseada em mercado para redes e computadores.

O tradutor do mercado tem como objetivo resolver, pela primeira vez, esse problema para o comércio na Internet. Um tradutor de mercado permite e depende de micro-mercados on-line para automatizar a alocação de recursos entre objetos escassos. Isso será feito permitindo o seguinte:

-   Expressão de preferências - e sua tradução em expectativas codificadas, ou direitos e deveres - com GUIs de fácil utilização ("idioma de origem") e uma [linguagem de contrato formal](http://nakamotoinstitute.org/contract-language/) ("idioma de destino") e tradução entre eles.
-   Agrupamento e recombinação de estruturas sofisticadas de direitos.
-   A entrada de preferências do usuário e sua tradução de humano expressável para forma legível por computador.

#### O Problema

O problema de "traduzir" entre contratos ao portador (que representam e garantem direitos a objetos escassos) pode ser lançado como um problema de tradução entre [moedas](http://nakamotoinstitute.org/shelling-out/). Para nossos propósitos, uma "moeda" em uma economia de objeto escassa é simplesmente qualquer tipo de [contrato de portador](http://nakamotoinstitute.org/contracts-with-bearer) utilizado para a detenção e transferência de riqueza, e não para consumo pelo detentor. É assim um ["colecionável"](http://nakamotoinstitute.org/shelling-out/#attributes-of-collectibles) (ou "mercadoria intermediária", para usar o termo de Carl Menger). O tradutor do mercado, aliás, faz os preços O (n \^ 2) em uma economia de escambo, contra O (n) em uma economia monetária, uma distinção muito menos importante.

Então, vamos olhar para as moedas. Vamos dizer que o pequeno empresário Alice está negociando contratos ciberespaciais com Bob, Charlie, etc. Típicos dos contratos internacionais, os termos podem ser denominados de várias maneiras. Estes são potencialmente não confiáveis: postagem de repostagem de Joe-Bob, Notas da Reserva Federal dos EUA em sua modalidade de 1970 (ou em 2003), recibos de depósito de ouro em Seychelles, moedas "Tigre Asiático" em 1997 e assim por diante.

Moedas não confiáveis ​​podem causar estragos:

1.  termos contratuais de longa duração
2.  contabilidade a longo prazo do próprio orçamento de uma maneira consistente.

Cada problema interfere nas possíveis soluções para o outro. Por um lado, escolher uma única moeda melhor para todos os contratos concentra o risco. Em alguns casos, não há nada próximo a uma moeda confiável e, de qualquer forma, a diversificação é preferível. Sem cobertura, Alice permanece exposta a riscos que os traders mais sofisticados podem facilmente proteger.

Outra maneira de olhar para ele: não há emissores no mundo que sejam 100% confiáveis ​​e 100% seguros. Na falta de um protocolo de segurança para garantir que uma moeda retenha seu valor, Alice precisa de gerenciamento de risco.

Por outro lado, Alice, para planejar seu orçamento (pessoal e / ou de pequena empresa) e expressar adequadamente suas preferências, precisa de uma unidade de conta de longo prazo simples e consistente. Orçamento com uma única moeda flutuante já é ruim o suficiente, mas se Alice denomina gastos e receitas diferentes em moedas diferentes, seu orçamento se torna uma bagunça inconsistente. Também não é razoável pedir a um profissional não financeiro que se preocupe com os pontos mais sutis das taxas de câmbio, cobertura, etc.

O que Alice faz? Resposta antiga: Alice contrata, a um custo de dinheiro e privacidade, um contador ou planejador financeiro, e pode ganhar algumas melhorias brutas. Principalmente, ela está sem sorte: pequenos empresários deixaram a maior parte do comércio internacional para grandes corporações, cujos executivos financeiros participam de sofisticadas estratégias de hedge.

Proposta de nova resposta: use um tradutor do mercado para ajudar Alice a redigir seus contratos. Este tradutor de mercado deve ser útil tanto para contratos normais executados por lei quanto para contratos auto-obrigatórios não rastreáveis, onde estes são viáveis. No post seguinte vou esboçar como um tradutor de mercado pode funcionar.

#### Uma solução

A conversão automática de moeda, como feito hoje por alguns cartões de crédito e máquinas ATM, é um tipo primitivo útil de tradução de mercado. O leitor casual (e usuário) pode pensar no tradutor de mercado (MT) como um tipo sofisticado de conversor de moeda automatizado e obter a essência básica dele. O MT serve para converter, fazer hedge e, em geral, reestruturar os contratos de condições de pagamento negociados de qualquer maneira.

Nossa principal novidade é dar conta dos orçamentos pessoais, não em termos de qualquer padrão externo de valor, mas sim em termos de unidades contábeis pessoais (PAUs). PAUs correspondem ao que Alice pode expressar de sua utilidade pessoal. O MT determina as preferências estáticas e temporais de Alice a partir do orçamento que Alice já mantém (por exemplo, seu orçamento para pequenas empresas em Quicken). Formulários de especificação de preferência adicionais podem ser fornecidos além daqueles de um programa de orçamento normal. Por exemplo, as configurações de preferência de software de Alice, seu comportamento com teclado e mouse e dicas semelhantes podem ser interpretadas como preferências econômicas, por exemplo, com relação a onde alocar o escasso espaço na tela e a largura de banda da rede.

Por conveniência, o PAU de Alice pode corresponder à moeda local mais usada por Alice. Se a maioria dos itens orçamentários de Alice lidam com contratos on-line negociados via MT, o uso da moeda local não é necessário, e é indesejável se essa moeda for instável.

Aqui está um diagrama mostrando Alice e Bob negociando um contrato usando seus tradutores de mercado:

    Alice                            Bob

    Esboço de contrato, "fonte"         Esboço de contrato,  "fonte"
      (Alice PAUs)                       (Bob PAUs)
             ^                               ^
             |                               |
             MT                              MT
             |                               |
             v                               v
    Esboço de contrato, "alvo" <-----> Esboço de contrato, "alvo"

Um modo em que o MT pode ser usado é fazer com que Bob ofereça um contrato binário take-it-leave-it, correspondendo à prática atual de varejo de preços take-it-or-it-it. No modo mostrado acima, Alice e Bob negociam para frente e para trás. A negociação dos termos do contrato de origem geralmente será manual. O "idioma de origem" normalmente será uma GUI legível, enquanto o "alvo" será uma [linguagem de contrato formal](http://nakamotoinstitute.org/contract-language/). Se Alice e Bob puderem inserir preferências que levem a negociações automáticas, um "bot de compras" e um "bot de catálogo", respectivamente, poderão ser usados. Esta é uma camada acima e além do escopo do MT. O MT é apenas um "bot de compras" na área restrita mas importante de contratos compostos de contratos de suporte atômico - direitos a objetos escassos - na medida em que as relações de preço entre esses contratos ao portador estão disponíveis em mercados cotados.

O MT funciona como um compilador de linguagem de computador. Mas isso se traduz nos dois sentidos e, em tempo real, Alice e Bob negociam as condições de pagamento. Assim, por exemplo, Alice muda um termo em seu contrato, propondo pagar menos Alice-PAUs pelos serviços de Bob. Seu MT traduz isso em uma série de pagamentos e hedges: um sofisticado contrato sintético tão obscuro para Alice e Bob quanto o código binário é para muitos programadores atualmente. Este sintético é construído a partir de títulos do mercado líquido (contratos ao portador) e derivados de baixo custo de transação. Um contrato sintético é naturalmente representado como um objeto composto, uma hierarquia de partes inteiras que compõe "átomos" contratualizados primitivos, como títulos e derivativos.

O MT de Bob inverte os termos reais de mercado em Bob-PAUs. Apesar de cada um concordar com diferentes quantias de pagamento, a estrutura visível além dos valores e o contrato subjacente completo é o mesmo. Eles podem estar confiantes de que, quando suas preferências tiverem sido satisfeitas, suas mentes se encontraram e podem se comprometer com o contrato.

Como resultado, Alice e Bob vêem o contrato em termos de suas próprias unidades de utilidade pessoal consistentes. Todas as considerações sobre taxas de câmbio, riscos de inflação e assim por diante são tratadas pelo MT.

Os MTs de Alice e Bob podem fazer conversões paralelas, coberturas e reestruturações para equilibrar seus portfólios. Essas sebes laterais não são reveladas umas às outras. Quaisquer termos binários que possam ser protegidos de uma só vez podem ser feitos quase arbitrariamente distantes do que Alice e Bob preferem financeiramente. Assim, Alice e Bob não precisam revelar suas preferências financeiras uns aos outros.

(Nota: Para contratos com prazos de pagamento atrasados, Alice e Bob determinando o risco de crédito causado pelas exposições de crédito de cada um é um problema importante, mas além do escopo do MT como descrevi).

Todo o conjunto de contratos de Alice com todas as suas contrapartes constitui seu portfólio completo - não apenas uma carteira de investimento segregada, mas uma carteira completa abrangendo todas as suas finanças. Este portfólio é representado como um composto de contratos compostos e forma a base para todo o planejamento financeiro de Alice e para a atividade de reequilíbrio de portfólios automatizados do MT.

A principal estrutura de dados que representa os contratos para fins analíticos é a árvore de decisão de chance / escolha. Esta árvore tem dois tipos de nós, nós "casuais", que percorrem todas as possibilidades materiais, e nós de "escolha", onde a escolha ótima é feita. O resultado é o valor esperado de um conjunto de termos contratuais. As árvores podem representar um grande número de contratos com baixa resolução (lotes de poda e heurística), ou um contrato simples com alta resolução (todas as possibilidades consideradas). Os computadores desktop são ou serão em breve suficientemente rápidos para pesquisar milhares de contingências e contratos sintéticos compostos por centenas de contratos atômicos, com atrasos menores que as latências da Internet. Então o contrato binário pode ser um sintético muito sofisticado, desde que sua análise seja totalmente automatizada,

### Conclusão

O MT baseia-se em trocas automáticas on-line que hospedam mercados líquidos para títulos de renda fixa e derivativos. Esses mercados revelam as informações que o MT precisa para proteger adequadamente as moedas. Os criadores de mercado e os arbitradores mantêm esses mercados, garantindo que as informações mais precisas sobre prêmios de risco, curvas de juros e assim por diante estejam disponíveis para os MTs. Algumas informações não deriváveis ​​automaticamente dos preços de mercado podem ser disponibilizadas on-line por consultores financeiros, em formato padrão, para download por MTs por uma taxa.

O contrato de origem é normalmente negociado e fechado manualmente, conforme compras normais. O MT é um "bot de compras", mas apenas no domínio muito restrito, mas importante, das finanças relacionadas a condições de pagamento. Desde a

1.  Alice tem informações suficientes sobre suas preferências financeiras para o risco e o valor do tempo, através de seu programa de orçamento e / ou formulários especializados, e essas preferências se aplicam a todos os termos de pagamento usados ​​pelo MT,
2.  Todas as informações necessárias para determinar o risco apresentado por um termo de pagamento estão disponíveis on-line (geralmente na forma de preços de mercado para securitários e derivativos, mas também de consultores financeiros on-line que publicam notícias financeiras em formato legível por MT), e
3.  Assumindo que todos os valores mobiliários de cobertura e derivados podem ser automaticamente comprados ou vendidos pelo MT,

não deve haver necessidade de intervenção manual no processo de tradução de cobertura. Se tal intervenção manual for necessária, o sistema perderá rapidamente seu apelo para a maioria dos usuários.

Se a informação de preferência ou de mercado não estiver disponível, ou as trocas de títulos e derivativos não estiverem disponíveis, o tradutor do mercado pode reverter para a conversão de moeda automatizada simples.

O tradutor do mercado resolve assim um problema inquietante enfrentado pelas pequenas empresas multinacionais, a cobertura de termos de pagamento usando moedas potencialmente não confiáveis. Em termos mais gerais, o tradutor de mercado construído sobre uma arquitetura de objetos escassa reduzirá a barreira do custo de transação mental para micropagamentos e micro-mercados. Ele converterá habilidades e preferências em microlights e microduties para uso na alocação de recursos e serviços - seja contas de e-mail on-line, colecionáveis ​​de jogos on-line, imóveis na tela, largura de banda de rede e armazenamento em cache ou uma variedade de outros objetos de rede que , graças à escassa arquitetura de objetos, tornam-se objetos econômicos.
