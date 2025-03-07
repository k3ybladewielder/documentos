---
title:  "Remailers pagos"
date:   1994-10-28
categories:
   -  Artigo
tags:
  -
author:
  - Hal Finney
---
```
Traduzido por: Steffan Diorgy 
Revisado por: Cypherpunks Brasil
```


# Remailers pagos  
<small>Hal Finney</small>  

#### 28 de Outubro de 1994

===exibe no card daqui pra baixo===

E se você pudesse ganhar dinheiro executando um remailer?  
Neste momento, a maioria dos operadores de remailer está operando por altruísmo. Isso é bom em muitos aspectos, mas tem seus problemas, como os eventos recentes mostraram:  
* falta de motivação para manter os remailers operando diante de dificuldades e possíveis riscos legais  
* facilidade de ataques de spam de usuários mal-intencionados  
* falta de incentivo para um serviço de remailer de qualidade comercial  
Tenho certeza de que todos podemos pensar em mais. Eu sei que seria muito mais fácil justificar continuar a administrar o repostador a mim mesmo se ele trouxesse alguns dólares por mês.  
Eu acho que existem alguns experimentos em remailers pagos que foram tentados. Penso que Sameer está cobrando por alguns serviços, embora talvez fosse apenas para endereços de retorno anônimos. Há muito tempo atrás, Karl Barrus tinha um serviço que exigia "selos digitais" pré-emitidos, mas não creio que muitas pessoas o usassem.  
O tempo pode estar maduro para encarar isso com mais seriedade. Vários fatores estão se unindo:  
* alguns esforços na padronização de comandos de remailer e cooperação de operadores (por exemplo, esta lista)  
* uso mais amplo de scripts e programas utilitários para ajudar as pessoas a usarem os remailers em  
vários sistemas de dinheiro real que estão on-line último mês ou assim que * permitem que você seja pago por coisas na net  
Para ser mais específico:  
É obviamente difícil operar um serviço de reencaminhamento que cobra se outras pessoas oferecerem o serviço equivalente gratuitamente. Como é muito fácil iniciar um remailer, o custo marginal para fazer isso é baixo, por isso os lucros também são baixos. No entanto, embora seja fácil iniciar um repostador, não é tão fácil manter uma execução em face de reclamações de destinatários de mensagens abusivas ou postagens inadequadas; dificuldades de sysops, proprietários, feeds de rede, ou outros para cima nessa grande cadeia de comando; possíveis problemas de aplicação da lei quando ocorrem comunicações ilegais; possíveis ameaças de ações judiciais (tais como dos cientologistas quando seus documentos sagrados são postados), etc. Portanto, não devemos ser enganados em pensar que a execução de um repostador é gratuita.  
Por outro lado, devo deixar claro que não esperaria uma morte neste serviço. Algo na ordem de um centavo uma mensagem parece razoável apenas em um palpite. Talvez devesse ser um fator de 10 maior ou menor.  
Uma questão é, evidentemente, a dificuldade adicional que isso causará no uso do repostador. Há várias coisas a considerar aqui. Por um lado, você poderia argumentar que já é muito difícil usar os remailers, e qualquer complicação adicional envolvida em incluir algum tipo de tokens de pagamento acabaria com o mercado. OTOH Eu posso concordar em espírito com os sentimentos expressos aqui recentemente sobre a baixa qualidade que parece caracterizar muito do uso dos remailers.  
Não olho para mensagens, mas de vez em quando vejo saltos, e com muita frequência são pequenas chamas feias ou material sem valor semelhante. Agora, espero ver os resíduos, que os tipos de pessoas sem noção que cometem os erros que me levam a ver as mensagens são os menos propensos a usar o serviço de uma maneira que vale a pena. Mas ainda assim, é desanimador. Nesse contexto, talvez tornar o sistema um pouco mais difícil de usar valeria a pena, na medida em que filtraria o harrasser casual. (Ou, mais realisticamente, isso pode manter apenas os harrassers excepcionalmente motivados.)  
De qualquer forma, acho que a presença dos scripts de remailer pode fazer com que usar um remailer para pagamento não seja muito mais difícil do que usar um programa gratuito. Se o custo for tão baixo quanto sugeri e a inclusão de tokens de pagamento for quase automática, a adição de custos não deverá ter um impacto muito negativo sobre o uso, certamente não em uso significativo e válido.  
E mesmo um custo modesto pode deter o spam que Detweiler e / ou a recente "Scythe" parecem amar. Pelo menos seríamos pagos por suportar o incômodo das reclamações.  
Agora, a próxima pergunta é os detalhes do pagamento. Francamente, não creio que nenhum dos sistemas atuais seja adequado para nós devido a nossas necessidades especiais, mas as coisas estão mudando rapidamente. Deixe-me descrever algo sobre como eles funcionam.  
Eu sei de dois sistemas que são baseados em VISA / Mastercard. Um é chamado First Virtual ([http://www.fv.com] (http://www.fv.com)). Eles são orientados para a venda de informações e dizem que não são para prestadores de serviços, mas, na prática, pareciam-me que poderiam ser usados ​​para serviços. Quando um cliente quer pagar, ele lhe envia seu ID de FV. Você envia isso para o FV e eles enviam uma mensagem de e-mail para o cliente perguntando se ele autoriza o pagamento. Se ele disser "sim", o FV creditará sua conta. Você recebe um cheque todo mês. Os clientes que sempre dizem "não" saem do sistema (assim como os comerciantes que enviam notas falsas). Eles cobram 29 centavos mais 2% por transação, mas os comerciantes podem agrupar vários pedidos de um único cliente antes de enviá-lo.  
Existem alguns problemas com um sistema como este, muitos dos quais são um pouco genéricos para a nossa situação. O mais fundamental é que não sabemos quem são nossos clientes na maior parte do tempo. De fato, o ponto principal da rede de remailers é que não conhecemos esse fato em nenhum caso, exceto o primeiro salto na cadeia. Se exigíssemos que os clientes expusessem sua ID de conta FV em cada salto, seria muito mais fácil rastrear mensagens através da rede (mesmo que as identificações estivessem escondidas no envelope de criptografia, parece arriscado). Se, em seguida, enviarmos uma mensagem ao FV dizendo que precisamos cobrar o ID XXX e o FV responder com um e-mail ao endereço residencial da pessoa, isso oferece mais possibilidades de rastreamento.  
Uma solução seria apenas cobrar ao entrar na rede de repotenciação. Talvez os operadores de reencaminhamento cobrassem um ao outro, e o primeiro remailer cobraria uma quantia maior para lidar com um comprimento "típico" da cadeia? Muitas possibilidades interessantes aqui.  
Outra questão é que as despesas indiretas por FV exigiriam mensagens em lote antes de enviá-las. Deixe-me esclarecer que o lote deve consistir em todos os encargos para um único usuário. Não adianta enviar uma mensagem para o FV, pedindo-lhe para, por favor, cobrar um centavo para cada uma das 100 contas do VISA. Não, você teria que contar as mensagens de cada usuário, separadamente, e quando o usuário XXX tivesse enviado, digamos, US $ 1 em mensagens, você poderia enviar a solicitação para o FV e receber 70 centavos de dólar.  
Então isso adiciona um pouco de overhead e manutenção de registros que atualmente não temos que fazer, embora talvez não seja tão difícil. Mas isso levantaria novas questões sobre a autenticação de IDs de FV e compartilha alguns dos impactos negativos de privacidade e problemas de links de mensagens mencionados acima.  
O outro sistema baseado em VISA é chamado OpenMarket. Acabei de ler sobre isso hoje à noite, então eu não sei também (http://www.openmarket.com) (http://www.openmarket.com)). É muito ligado à WWW, então não parece funcionar para nós. Os clientes se conectam a um determinado servidor WWW que os autentica e cobra seu cartão VISA adequadamente, então eles são redirecionados para o comerciante com algum tipo de token que diz que eles pagaram.  
O NetBank (e-mail para netbank-intro@agents.com) é um sistema similar a dinheiro digital. Os clientes obtêm tokens que são basicamente grandes números secretos que possuem um valor em dinheiro. Eles os enviam para os comerciantes, e os comerciantes os enviam para o banco que credita a conta. O NetBank envia um cheque todo mês.  
O interessante é como os clientes compram os tokens em dinheiro. Uma maneira é se conectar a um número 900 com o seu modem. Eles cobram do cliente US $ 10,00 e dão a ele um valor em dinheiro digital que vale muito. Outra maneira é enviando um cheque por fax para eles. Eu não estava claro sobre como você recebe a ficha em dinheiro nesse caso; Eu acho que eles enviam para você em um endereço que você especificar. Do ponto de vista da privacidade, eles não são tão bons assim; Os números 900 têm Identificação Automática de Número, a menos que você esteja disposto a sair para um telefone público para receber seu dinheiro, então ele pode estar ligado ao seu número de telefone. E o sistema de fax deve ter algum tipo de endereço de retorno que seja vinculado a você.  
O outro problema com o NetBank é que a menor denominação que pode ser gasta é de 25 centavos. Devido à natureza de caixa dos tokens, não vejo uma maneira natural de acumular várias mensagens em um único pagamento. Talvez pudéssemos colocar nosso próprio sistema de dinheiro digital de baixo valor em cima do NetBank, onde os usuários poderiam comprar nosso dinheiro anônimo por 25 centavos e receber fichas suficientes para 25 mensagens, então nós resolveríamos entre nós (ou na verdade com o anon-mail- token bank). Na verdade, isso pode ajudar com os problemas de privacidade também. O dinheiro digital anônimo é altamente patenteado, no entanto.  
Com um sistema similar a dinheiro, cada mensagem incluiria um token numérico no cabeçalho, que é o dinheiro digital. O remailer iria retirar isso e enviá-lo para o crédito. Este é um sistema simples e pode ser amplamente automático. No entanto, existem algumas questões complicadas sobre os trapaceiros reutilizarem dinheiro.  
O NetBank cobra US $ 4 por mês, mais, para o caixa baseado em 900, 20% de desconto no valor de face.  
O último sistema que descreverei é o DigiCash de David Chaum (http://www.digicash.com) (http://www.digicash.com). Chaum é o inventor do dinheiro digital e ele certamente conhece suas coisas, além disso, como eu disse, ele tem a propriedade intelectual muito bem costurada em termos de patentes. O sistema de pagamento da DC também é baseado na WWW atualmente. O cliente tem que estar executando um programa especial em seu computador, separado de seu navegador. Este programa mantém seu dinheiro digital, que é similar conceitualmente ao caixa do NetBank, porém mais sofisticado criptograficamente. Quando ele quer comprar algo, o servidor da Web do comerciante faz uma conexão com o programa de DC do cliente e transfere o dinheiro para o comerciante.  
DigiCash disse que eles estão planejando um sistema baseado em e-mail, mas por enquanto sua ênfase é na WWW. No momento, eles estão apenas em beta e não usam dinheiro real. Eu não sei quando eles serão reais e baseados em e-mail, e não sei se eles disseram qual será a comissão deles. Mas quando isso acontece, pode ser a melhor abordagem se transações de valor pequeno puderem ser suportadas. O DigiCash é totalmente anônimo no sentido de que, uma vez que um cliente recebe o dinheiro, ele fica "cego" de uma maneira criptográfica especial, de modo que o banco não possa associá-lo a esse cliente (e ninguém mais pode, também). Esse tipo de anonimato se encaixa muito bem com nossos requisitos de remailer.  
Bem, eu sei que isso é muita informação para trabalhar, mas principalmente eu quero que as pessoas estejam cientes das possibilidades. A maioria dessas coisas é muito, muito nova, com apenas algumas semanas de idade, geralmente. Provavelmente nos próximos meses veremos muito mais opções. Estou confiante de que em breve haverá sistemas de pagamento que fornecerão a base técnica para o reencaminhamento baseado em taxas. Eu não espero que ninguém fique rico com isso, mas isso pode ajudar a compensar os riscos que todos enfrentamos, e pode servir para melhorar a qualidade da rede de remailers.  
{% endfilter %}

Hal Finney  
_hal@rain.org_

[Página de Hal Finney](http://web.archive.org/web/20130624115154/http://finney.org/~hal/home.html)

