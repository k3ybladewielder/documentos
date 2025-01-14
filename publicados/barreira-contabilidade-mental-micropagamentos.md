---
title:  "A barreira da contabilidade mental aos micropagamentos"
date:   1996-01-01
categories:
   -  Artigo
tags:
  - Economia
  - Micropagamentos
author:
  - Nick Szabo
---

```
Traduzido por: jeffeson
Revisado por: Cypherpunks Brasil
```

## Nick Szabo  

###### Copyright (c) 1996 por Nick Szabo - permissão para redistribuir sem alteração ora concedida

---

===exibe no card daqui pra baixo===

Alguns projetos de comércio eletrônico prometem custos de transação dramaticamente menores, para que possamos obter "micropagamentos", "microintermediação" e assim por diante. Uma ideia ainda mais avançada é a utilização de mercados de granularidade muito pequenos para a alocação de recursos de computadores e de rede <sup>[1]</sup>. Até que ponto essas coisas são realizáveis? Considere uma característica bastante independente do sistema de pagamento específico: a declaração de encargos. Aqui reside uma troca aqui entre completude e complexidade. Por um lado, apenas resumir as acusações cria a oportunidade para as _'salami fraud'_ (fraudes de salame), permitindo que micro custos largamente distribuídos, falsos ou exagerados, não sejam detectados. Além disso, as partes que lêem apenas os resumos não recebem nenhum feedback pelo qual possam ajustar seu comportamento para minimizar os custos. Por outro lado, uma declaração muito complexa para os clientes lerem também permite que fraude, erro e uso ineficiente não sejam detectados, porque uma ou ambas as partes não podem entender a justificativa para as cobranças em relação ao acordo presumido em termos de serviço e pagamento. O mesmo tipo de raciocínio se aplica a processar essas coisas na cabeça, em vez de no papel, como geralmente é feito em pequenas transações em dinheiro. Um requisito básico para que os preços de mercado funcionem é que ambos os lados de uma transação possam mapear as cobranças ao valor obtido ou processado, para que possam ajustar seu comportamento de compra ou venda de acordo.

Parece haver aqui um gargalo cognitivo fundamental. Uma solução proposta para isso tem sido "agentes inteligentes". Mas como esses agentes são programados remotamente, não pelo consumidor, é difícil para o consumidor determinar se o agente está agindo de acordo com os melhores interesses do consumidor, ou no melhor interesse da contraparte — talvez, necessariamente, pelo menos tão difícil quanto ler a correspondente declaração completa de responsabilidades. Além disso, a interface do usuário para permitir que os consumidores simplesmente expressem suas preferências sofisticadas a um agente está faltando e pode representar outro gargalo cognitivo fundamental.

As empresas de comunicação descobriram que o faturamento é um grande gargalo. Segundo algumas estimativas, até 50% dos custos de uma chamada de longa distância são para faturamento, e isso é da ordem de US $ 100 bilhões por ano no mercado mundial. Os provedores de Internet estão migrando para uma taxa fixa a fim de minimizar esses custos, embora isso crie um incentivo para o uso excessivo de recursos na rede.

Um sistema de micropagamentos pressupõe uma solução para o problema da contabilidade mental. Se alguém pudesse realmente resolver o problema, em vez de simplesmente alegar tê-lo resolvido por meios misteriosos ("agentes inteligentes", etc.), a economia seria enorme mesmo em negócios já existentes, como longa distância e serviço de Internet — para não mencionar todas as novas possibilidades possíveis por menores custos de transação.

### Exemplo - Contas de eletricidade

Às vezes, as declarações contabilizam transações em incrementos gratuitos, como a resolução de 100 watts-hora em algumas contas de eletricidade. Há muitas coisas que a maioria das pessoas normalmente não planeja com relação às contas de eletricidade, o que pode melhorar o valor que elas recebem pelos pagamentos de eletricidade:

*   Quais aparelhos estão usando mais eletricidade com menos benefício pessoal (não disponível na conta de energia elétrica — mas pode-se conceber um programa de contabilidade pessoal ligado a aparelhos inteligentes que permitem que você faça isso).
*   Como equilibrar melhor o calor elétrico com o do gás (você poderia computar isso em detalhes e economizar alguns dólares, mas ganharia dinheiro extra mais rápido ao fazer um trabalho clandestino).
*   Se a empresa de eletricidade fosse uma entidade menos confiável e amplamente conhecida, você também pode não confiar neles com o faturamento e recalculá-los para a resolução com a qual se sentia confortável, além de aceitar fraudes ou truques de letras miúdas abaixo desse nível. (Como a eletricidade é fungível e o sistema de preços é pequeno, você pode ter um programa para verificar a conta, o que é eficiente se conseguir informações suficientes para que um número suficiente de pessoas recupere os custos de desenvolvimento e marketing de software).

A razão pela qual não fazemos as coisas é que elas não valem os ciclos cerebrais: chegamos à barreira da contabilidade mental.

### Uma teoria da granularidade de preços

Aqui apresento brevemente uma teoria da granularidade de preços baseada em uma visão subjetivista dos preços. A função dos preços, do ponto de vista de um comprador, é deixar o comprador mapear seus recursos pessoais (orçamento) para seus valores pessoais (únicos e não observáveis diretamente). Esse processo mental exige a comparação do preço de compra de um bem com seu valor pessoal. Isso implica um custo mental significativo, que define os limites inferiores mais básicos dos custos de transação. Por exemplo, comparar o valor pessoal de um conjunto grande e diversificado de bens de baixo preço pode exigir um gasto mental maior do que os preços desses bens (onde os gastos mentais podem ser mensuráveis ​​como os custos de oportunidade de não se envolver em trabalho mental por salários, ou de não comprar um número menor de bens comparáveis ​​com menores custos contábeis mentais). Neste caso, faz sentido juntar as mercadorias em pacotes com um preço mais alto e uma sinergia inicial, até que os custos de contabilidade mental dos compradores sejam suficientemente baixos.

Esses custos contábeis mentais, não os custos físicos ou computacionais ou custos de P&D amortizados de pagamento ou de faturamento, estabelecem o principal limite inferior da granularidade de preço. A julgar pelas tendências de granularidade de precificação, como a tendência para taxas fixas em serviços online, a granularidade de precificação online está muito acima dos níveis sugeridos de micropagamento de alguns centavos ou mesmo de frações de um centavo. Os custos de contabilidade mental para um consumidor online típico parecem ser um pouco mais altos do que aqueles em áreas de comércio mais familiares.

Uma possível correção é que o software do comprador compare preços de compra com um serviço de "relatórios ao consumidor". Mas essa informação imparcial é rara e, em qualquer caso, leva em conta apenas valores amplamente compartilhados, não valores pessoais.

Outra correção é possível para mercadorias fungíveis: cobrar um preço fixo por unidade, que o comprador pode avaliar apenas a partir do número acumulado de unidades e informações de preços. (Como exemplo concreto, em uma campanha publicitária atual nos EUA, a AT&T está apostando que sua taxa fixa de US $ 0,15 é mais atraente do que a US $ 0,10 da Sprint — que conhece taxa variável — que vale a pena o fornecedor renunciar ao preço de congestionamento e o comprador perder descontos vastos, a fim de ter uma taxa previsível, transformando o tempo do telefone em uma mercadoria fungível e, assim, economizando em custos contábeis mentais.

Infelizmente, a maior parte do comércio pela Internet não é fungível: conteúdo, serviços, encomenda de produtos por correspondência e assim por diante. Alguns serviços do Provedor de Servidor de Internet (ISP) podem ser vendidos como fungíveis (por exemplo, espaço em disco, tempo de conexão) apenas à custa de preceder o congestionamento e outros métodos de precificação que, se não fossem custos contábeis mentais, poderiam ser bastante eficientes. Além disso, mesmo para mercadorias fungíveis, cada usuário tem uma curva única de retornos decrescentes. O software teria que deixar o comprador determinar e inserir sua curva de preferência de volume (de alguma maneira intuitivamente familiar, sem pressupor que o comprador está familiarizado com a teoria econômica) antes que ela pudesse agir adequadamente em seus interesses; sem mencionar as complicações das preferências temporais, interações não-lineares entre mercadorias fungíveis quando isoladas e assim por diante.

Essa solução de interface de usuário para o caso de mercadorias fungíveis sugere uma estratégia melhor para lidar com o problema mais geral da contabilidade mental no comércio online: desenvolver melhores maneiras para o comprador comunicar suas preferências pessoais ao software. Os profissionais de marketing há muito criaram esquemas para obter esse tipo de informação: pesquisas detalhadas, rastreamento do comportamento e das respostas do usuário, etc. Provavelmente, os serviços Web, como o www.firefly.com, são os mais utilizados nesse quesito. Firefly cria uma espécie de "espaço subjetivo" de preferências musicais em que o comprador pode navegar e encontrar novas músicas que elas têm maior probabilidade de preferir.

Dado que o software pode representar certas preferências, é um problema mais direto para o software mapear essas representações para preços específicos (ou ofertas), participar de compras (ou pechinchar) e concluir transações online com segurança. Esses problemas mais fáceis têm sido o foco da pesquisa de micropagamentos, mas o problema mais fundamental de obter e representar preferências em grande parte não foi reconhecido, talvez devido a um viés objetivista que postula leis matemáticas em vez de preferências subjetivas como a base de uma economia de trabalho.

Dada a solução de outros problemas de custos de transação, os custos da contabilidade mental ficam sujeitos ao limite do processo de comunicação de preferências — seja pela escolha de contabilidade mental de um bem em detrimento de outro, seja pela criação de um simulacro de software único e suficientemente preciso das preferências do comprador, que completa o processo de orçamento, negociação e compra. Até que ponto e com que eficiência pode (a) um comprador comunicar preferências subjetivas ao software, e (b) o software pode representar e agir no interesse dessas preferências objetivadas? A presença de mecanismos de pesquisa, formulários de pedidos de catálogo, pesquisas de marketing e interações mais sofisticadas como firefly demonstra que tal comunicação e representação são viáveis e importantes, mas parecem ser dispendiosas e talvez fundamentalmente limitadas de alguma forma.

### Preferências e metáforas visuais

Para avaliar a conveniência de uma transação, e para evitar ser cobrado incorretamente, as partes de uma transação têm que contabilizar, ou seja, contabilizar o dinheiro pago por determinados produtos e serviços — certificando-se de que os pagamentos em dinheiro são feitos como prometido (por exemplo olhando para a tela como os produtos são digitalizados na loja, ou o recibo depois), ou certificando-se de que a conta de telefone é adequada. Aqui eu uso "contabilidade" nesse sentido amplo.

Eu posso estar pagando em dinheiro, mas eu ainda gostaria de acompanhar como e por que meu dinheiro está entrando e saindo, por muitas das mesmas razões que os contadores reconciliam e analisam entradas nos livros. Neste momento, um log de transações (seja o dinheiro digital ou um cartão de crédito) é a maneira mais útil de fazer isso. Pode haver outras metáforas mais apropriadas para algumas circunstâncias (por exemplo, medidores de nível absolutos, medidores de vazão com marcas de água altas e baixas, etc.); Este é um novo campo potencialmente fértil para explorar. Pode haver agentes que possam fazer parte da contabilidade (por exemplo, comparando pagamentos feitos a termos prometidos, limites de pagamento, etc.), mas para a grande maioria dos produtos e serviços o software não pode julgar a qualidade ou desejo pessoal do produto ou serviço, e, portanto, a conveniência líquida da transação. O usuário deve realizar essa comparação com qualquer informação que o computador possa fornecer através do display. A interface do usuário e a cognição do usuário, portanto, permanecem o gargalo para a granularidade da transação.

Uma grande tarefa é usar o poder da GUI para criar novas metáforas para tornar isso mais fácil. É a metáfora intuitiva, porém precisa, que reduzirá os custos contábeis. Protocolos criptográficos reduzem potencialmente apenas os custos de transação relacionados à segurança, como falsificação e extorsão. Para os custos normais de transação contábil, que atualmente são muito altos para micropagamentos, precisamos de melhores metáforas visuais interativas.

Para transações livres de registros, precisamos de transações que possam ser transacionadas de maneira justa uma vez, imediatamente explicadas pelas partes por meio de uma metáfora visual agradável e depois esquecidas. O potencial para disputas não resolvidas em sistemas sem registro é vasto para transações onde isso não é possível (provavelmente a maior parte do comércio desejado: onde a qualidade de um produto ou serviço não pode ser bem determinada até que a transação seja concluída ou onde o crédito esteja envolvido).

O preço é um tipo de termo contratual; Também precisamos de boas metáforas para rastrear outros tipos de termos contratuais. A falta de observabilidade do protocolo por parte do usuário leva à capacidade da contraparte de se envolver em ações ocultas. Consulte "http://www.fon.hum.uva.nl/rob/Courses/InformationInSpeech/CDROM/Literature/LOTwinterschool2006/szabo.best.vwh.net/smart.contracts.2.html" para uma discussão mais detalhada sobre este e outros problemas de contratação informatizados.

Uma das barreiras para criar bons contratos é determinar o que as partes querem em primeiro lugar. As pessoas tendem a pensar em termos de condições padrão ou estereotipadas: pagamento em dólares, investimento em ações, etc., quando existe uma variedade muito maior de estruturas contratuais alternativas que, combinadas adequadamente, poderiam atender melhor às necessidades das partes. Eu gostaria de ver ferramentas que permitem que as partes explorem seus desejos de forma interativa com o computador. Em finanças, isso pode incluir curvas de juros pessoais interativas, determinando a ordem parcial dos desejos (como na teoria da decisão) para títulos, derivativos e produtos sintéticos alternativos específicos; e assim por diante. O software, então, analisaria essa entrada, faria recomendações e até mesmo realizaria contratações automatizadas (*). As metáforas devem ser desenvolvidas de modo que seja fácil para os usuários leigos expressar tais desejos sem amplo conhecimento de finanças ou teoria da decisão. Tais metáforas forneceriam um front-end amigável para trocas automatizadas, leilões e outros mecanismos de contratação online.

Atualmente, os programas de orçamento (como o Quicken) fornecem algumas das metáforas e os programas de análise financeira fornecem um amplo feedback sobre as propriedades de fluxo de caixa de determinados contratos, mas um mercado potencialmente inexplorado está entre uma combinação dessas duas tecnologias.

(*) transações semelhantes a contratos feitas por agentes automatizados levantam questões interessantes sobre o que constitui uma "reunião das mentes".

## Referências

[1] A proposta mais avançada ainda se encontra no [Agorics Papers](http://www.agorics.com/agorpapers.html).

Por favor, envie seus comentários para nszabo (at) law (dot) gwu (dot) edu

---
Fonte: http://www.fon.hum.uva.nl/rob/Courses/InformationInSpeech/CDROM/Literature/LOTwinterschool2006/szabo.best.vwh.net/micropayments.html
