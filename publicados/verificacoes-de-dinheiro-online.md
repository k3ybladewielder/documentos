---
title:  "Verificações de dinheiro online"
date:   1989-01-01
categories:
   -  Artigo
tags:
  -
author:
  - David Chaum
---
```
Traduzido por: Steffan Diorgy 
Revisado por: Cypherpunks Brasil
```

<style>.references{ list-style:none; text-indent: none; padding:0; margin:0; }</style>


# Verificações de dinheiro online  
<small>David Chaum</small>  

#### 1989  


### Introdução
===exibe no card daqui pra baixo===

Economias de aproximadamente uma ordem de grandeza em espaço, armazenamento e largura de banda sobre protocolos de dinheiro eletrônico on-line publicados anteriormente são alcançadas pelas técnicas aqui apresentadas. Além disso, essas técnicas podem aumentar a conveniência, fazer uso mais eficiente dos recursos e melhorar a privacidade.

O dinheiro eletrônico "off-line"<sup>[[CFN88]](#fnCFN88)</sup> é adequado para transações de baixo valor, em que a "prestação de contas após o fato" é suficiente para impedir o abuso; o pagamento on-line<sup>[[C89]](#fnC89)</sup>, no entanto, continua sendo necessário para transações que exigem "restrição prévia" contra pessoas que gastam além de seus fundos disponíveis.

Três esquemas online são apresentados aqui. Cada um depende das mesmas técnicas para codificar as denominações em assinaturas e para "desvalorizar" as assinaturas para o valor exato escolhido no momento do pagamento. Eles diferem em como o valor não gasto é devolvido ao pagador. No primeiro, todas as alterações são acumuladas pelo pagador em um único "pote de biscoitos", que pode ser depositado no banco durante a próxima transação de retirada. Os segundo e terceiro esquemas permitem que a mudança seja distribuída entre as notas não gastas, que podem depois ser gastas. O segundo esquema revela à loja e ao banco o montante máximo pelo qual uma nota pode ser gasta; o terceiro não divulga essa informação.

### Denominações e desvalorização

Por simplicidade e concretude, mas sem perda de generalidade, um esquema de denominação particular será usado aqui. Atribui o valor de 1 centavo ao expoente público 3 em um sistema RSA, o valor de 2 centavos ao expoente 5, 4 centavos ao expoente 7 e assim por diante; cada valor sucessivo de potência-de-dois é representado pelo correspondente expoente público ímpar correspondente, todos com o mesmo módulo. Assim como em [C89], uma terceira raiz de uma imagem sob a função unidirecional f (juntamente com o módulo de pré-imagem do composto RSA do banco) vale 1 centavo, uma raiz 7 vale 4 centavos e uma raiz 21 5 centavos. Em outras palavras, um expoente primário público distinto é associado a cada dígito da representação inteira binária de uma quantia de pagamento; para uma determinada quantia de pagamento, o produto de todos aqueles expoentes principais correspondentes a 1 '

Uma assinatura em uma imagem sob f é "desvalorizada", elevando-a aos poderes públicos correspondentes aos valores de moeda que devem ser removidos. Por exemplo, uma nota com uma raiz de 21 pode ser desvalorizada do seu valor de 5 cêntimos para 1 cêntimo, simplesmente aumentando-a para a 7ª potência.

Nos sistemas de pagamento on-line anteriores<sup>[[C89]](#fnC89)</sup>, o número de assinaturas separadas necessárias para um pagamento era, em geral, o peso de Hamming da representação binária do valor. Como os sistemas on-line seriam usados ​​para pagamentos de valor mais alto (como mencionado acima), e uma resolução extra pode ser desejada para fornecer juros para fundos não gastos<sup>[[C89]](#fnC89)</sup>, uma média de aproximadamente uma ordem de magnitude é salva aqui.

### Pote de biscoitos

Neste primeiro esquema, o pagador retira periodicamente uma oferta de notas do banco, cada uma com o valor máximo para todo o sistema. Considere um exemplo, mostrado na Figura 1.1, no qual duas notas são retiradas. N e ri são aleatórios. O ri "cego" (do banco) as imagens sob a função pública, unidirecional f. A assinatura do banco corresponde à raiz h-ésima, onde h = 3 * 5 * 7 * 11\. Como em todos os números, o pagador envia mensagens da esquerda e o banco envia da direita.

<pre>                    h             h
          f(n1) * r1 ,  f(n2) * r2
     ----------------------------------------->
PAGADOR                                        BANCO
     <------------------------------------------
               1/h            1/h
          f(n1)    * r1, f(n2)    * r2

           Fig. 1.1\. Retirada do pote de biscoitos
</pre>

Na preparação do primeiro pagamento, o pagador divide r1 out. A assinatura é então aumentada para a 55ª potência para desvalorizá-la de 15 centavos a 5 centavos. A figura 1.2 mostra esse primeiro pagamento. É claro que a loja é um intermediário entre o pagador (à esquerda) e o banco (à direita) em cada pagamento on-line, mas isso não é indicado explicitamente. Também não são mostrados nos números as mensagens usadas para concordar com os valores de pagamento.

<pre>                   1/(3*7)           5*11
          n1, f(n1)       , f(j) * s1
     ----------------------------------------->
PAGADOR                                        BANCO
     <------------------------------------------
              1/(5*11)
          f(j)         * s1

           Fig. 1.2\. Primeiro pagamento pelo pote de biscoitos
</pre>

Os dois primeiros resíduos enviados pagando, n1 e sua imagem assinada sob f, são facilmente verificados pelo banco valendo 5 centavos. O terceiro resíduo é um "cookie jar" cego, uma imagem cega sob f de um valor escolhido aleatoriamente j. Este cookie jar é modulo um segundo composto RSA que é usado apenas para jars de cookie. Uma vez que o banco verifique os fundos recebidos e que n1 não tenha sido gasto anteriormente, ele assina e retorna o frasco de cookie cegado (sob o módulo jar do cookie) com expoentes públicos correspondentes à alteração devida.

O segundo pagamento, mostrado na figura 1.3, é essencialmente o mesmo que o primeiro, exceto que a quantia é de 3 centavos e o cookie jar agora tem algumas raízes. Se mais pagamentos fossem feitos usando o mesmo pote de biscoitos, todas as assinaturas resultantes para mudança se acumulariam.

<pre>                   1/(3*5)      1/(5*11)    7*11
          n2, f(n2)       , f(j)        * s2
     ----------------------------------------->
PAGADOR                                        BANCO
     <------------------------------------------
              1/(5*11*7*11)
          f(j)              * s2

           Fig. 1.3\. Segundo pagamento pelo pote de biscoitos
</pre>

O pode de biscoitos pode ser convenientemente depositado, como mostrado na figura 1.4, durante a retirada do próximo lote de notas. É verificado pelo banco como uma nota de pagamento seria: as raízes devem estar presentes na multiplicidade reivindicada e a pré-imagem em f não deve ter sido depositada antes.

<pre>                 1/(5*7*11*11)
          j, f(j)
     ----------------------------------------->
PAGADOR                                        BANCO

           Fig. 1.4\. Depósito no pote de biscoitos
</pre>

A abordagem do pode de biscoitos o efeito de um formulário on-line de "cheques off-line"<sup>[[C89]](#fnC89)</sup>, em que as notas de um valor fixo são retiradas e as partes não gastas posteriormente creditadas ao pagador durante uma transação de reembolso.

### Valor da nota declarada

A Figura 2 descreve um esquema um pouco diferente, que permite que a mudança seja gasta sem uma transação de retirada intermediária. As retiradas podem ser exatamente como no esquema cookie-jar, mas aqui um único módulo é usado para tudo no sistema. Os produtos de exponentes públicos que representam os vários valores são os seguintes: d é o valor pago, g é o valor da nota, a "mudança" c é g / d e h é novamente a quantia máxima, onde d | g | h. Um pagamento (ainda para o banco através de uma loja) inclui primeiro e segundo componentes que são os mesmos que no esquema cookie-jar. O terceiro componente é a quantidade de mudança que o solicitante deve devolver. O quarto é um número (cego) m, que poderia ser uma imagem sob f usada em um pagamento posterior, assim como n é usado neste.

<pre>                 1/d        c
          n, f(n)   , c, m*s
     ----------------------------------------->
PAGADOR                                        BANCO
     <------------------------------------------
                     +------------+
           1/c       |       1/c  | (Cadeado gráfico)
          m    * s * | f(f(n)   ) |
                     +------------+

           Fig. 2\. Pagamento do valor da nota declarada
</pre>

A assinatura retornada contém um fator de "proteção" (mostrado dentro do cadeado). Esse fator garante que o pagador realmente tenha a c-ésima raiz de f (n), exigindo que o pagador lhe aplique f antes de dividir o resultado da assinatura. Sem essa proteção, um pagador pode obter a mudança máxima em todo o sistema, independentemente da quantidade de mudança realmente devida; com isso, a mudança reivindicada só pode ser recuperada se as raízes correspondentes em n forem de fato conhecidas do pagador.

### Distribuição de mudança

A alteração retornada em um pagamento pode ser dividida em partes que preenchem as denominações ausentes nas notas ainda não gastas. Suponha, por exemplo, que o último pagamento seja gasto com d = 5 * 11, c = 3 * 7 e que m seja formado pelo pagador conforme mostrado na primeira linha da Figura 3.1\. Em seguida, desbloquear após o pagamento produz o a mostrado na segunda linha.

(Use === for "é equivalente a")

<pre>                         3        7
              m === f(n1)  * f(n2)

                     1/21
              a === m

           Fig. 3.1\. Forma de mudança retornada
</pre>

De a, as duas raízes mostradas nas duas últimas linhas da Figura 3.2 são prontamente calculadas. (Essa técnica é facilmente estendida para incluir qualquer número de raízes separadas.) Assim, os valores não utilizados no último pagamento preenchem as raízes ausentes nas notas n1 e n2.

<pre>                   -1
              u = 3   mod 7

              v = 3u div 7

          1/7       3        -1  u        -v
     f(n1)    === (a  * f(n2)   )  * f(n1)

          1/3              -1/7
     f(n2)    === a * f(n1)

           Fig. 3.2\. Distribuindo a mudança
</pre>

Como o pagamento a maior permite que a mudança seja devolvida em quaisquer denominações escolhidas (não mostradas), o pagador tem flexibilidade extra e é capaz de usar todos os fundos retidos. Isso também aumenta a conveniência, reduzindo a necessidade de retiradas.

### Valor da nota oculta

Embora a combinação das duas subseções anteriores seja bastante viável, pode ser desejável que o pagador não tenha que revelar c à loja ou ao banco. A figura 4 mostra um sistema permitindo isso. A mensagem de pagamento é exatamente como no protocolo de valor de nota declarado acima, exceto que c não é enviado. O fator de proteção (mostrado novamente em uma trava) também é colocado sob a assinatura, mas falta o f extra e é elevado para uma potência aleatória z escolhida pelo banco

<pre>                 1/d     c
          n, f(n)   , m*s
     ----------------------------------------->
PAGADOR                                        BANCO
     <------------------------------------------
                        +----------+
           d/h    g/h   |     zd/h |
          m    * s    * | f(n)     |, z
                        +----------+

           Fig. 4\. Pagamento com valor de nota oculto
</pre>

Se z fosse conhecido do pagador antes do pagamento, então o pagador poderia trapacear incluindo f (n) no terceiro componente; isso daria ao pagador a mudança máxima em todo o sistema, mesmo que nenhuma fosse devida. Considere um único expoente de mudança q. Se z mod q é adivinhado corretamente por um pagador de trapaça, então o pagador recebe indevidamente o valor da moeda correspondente. Assim, a chance de fazer batota bem sucedida é 1 / q. Se, no entanto, os divisores de h forem escolhidos suficientemente grandes, a segurança bastante prática pode ser alcançada. Quando as possibilidades de distribuição de troca e reembolso são incluídas, a privacidade desse esquema supera a de um sistema de moedas.

### Conclusão

A combinação de moedas on-line melhora a eficiência, o uso de fundos, a conveniência e a privacidade.

### Referências

1.  Chaum, D., "Privacy Protected Payments: Unconditional Payer and/or Payee Anonymity," in Smart Card 2000, North-Holland, 1989, páginas 69-92. [↩](#refC89-1) [↩](#refC89-2) [↩](#refC89-3) [↩](#refC89-4)

2.  Chaum, D., A. Fiat, & M. Naor, "Offline Electronic Cash," Proceedings of Crypto '88. [↩](#refCFN88)

