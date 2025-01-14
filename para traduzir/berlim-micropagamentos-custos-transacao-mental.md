Micropagamentos e Custos de Transação Mental
============================================

### Nick Szabo

#### szabo@best.com
 http://www.best.com/\~szabo/

Apresentamos argumentos intuitivos sobre o motivo pelo qual os micropagamentos não foram bem-sucedidos na Internet. O "fator de confusão" para os clientes associados a essas transações é caracterizado. Um quadro de custos de transação mental e granularidade de preço é então apresentado, e os argumentos sobre micropagamentos são reformulados à sua luz. Finalmente, fazemos algumas sugestões para reduzir os custos mentais de transação do comércio na Internet.

1 Introdução
------------

Alguns projetos de sistemas de pagamento pela Internet prometem reduzir drasticamente os custos de transação, para que possamos obter micropagamentos (por exemplo, [Be95], [GMAGS95], [RS96]). Outros projetos propõem formas mais sofisticadas de microtransação [MD88]. Até que ponto os custos de transação podem ser reduzidos dessas maneiras? Este artigo argumenta que os custos de transação mentais levantam barreiras fundamentais para a aceitação pelo cliente de pacotes e preços baixos. Exploraremos os problemas tanto informalmente quanto através de um exame mais detalhado de três fontes de gastos cognitivos dos clientes.

Esses custos contábeis mentais, não os custos de pesquisa e desenvolvimento físicos ou computacionais ou amortizados de um método de pagamento ou de faturamento, estabelecem o principal limite inferior da granularidade de preço. A julgar pelas tendências de granularidade de preço, como a tendência de taxas nos serviços online, a granularidade dos preços online está muito acima dos níveis sugeridos de micropagamentos de alguns centavos ou mesmo de frações de um centavo. Os custos de contabilidade mental para um consumidor on-line típico parecem ser um pouco mais altos do que aqueles em áreas de comércio mais familiares.

Os custos de transação mental do cliente vêm de pelo menos três fontes: caixa de itens incertos, observação incompleta e dispendiosa dos atributos do produto e tomada de decisão incompleta e dispendiosa.

### 1.1 Custos Cognitivos versus Custos Tecnológicos de Transação

Para a economia do comércio eletrônico, é importante distinguir entre custos de transação tecnológicos e mentais. Quando os tecnólogos falam sobre custos de transação, eles geralmente falam sobre custos computacionais e de rede. Assim, a alegação de que as tecnologias de micropagamento, que reduzem drasticamente esses custos, reduzirão os "custos de transação". O significado de tais reduções tecnológicas depende dos custos cognitivos associados já estarem muito baixos, uma vez que esses pagamentos não atendem aos custos cognitivos.

Economistas (por exemplo, [B82], [W85], [H89]), por outro lado, geralmente, quando usam o termo "custos de transação", referem-se implicitamente a custos cognitivos. Um dos objetivos deste artigo é tornar essas suposições explícitas. Às vezes, esses custos mentais de transação podem ser reduzidos com o auxílio da tecnologia: daí a afirmação de que ferramentas como os mecanismos de busca da Internet podem reduzir os custos de transação associados à comparação dos atributos de bens e serviços.

Ao examinar os micropagamentos, este artigo assumirá que os custos tecnológicos do próprio sistema de pagamento são zero e examinará quais limites são definidos pelos custos de transação mental associados às transações de varejo visadas pelos micropagamentos. Exploraremos as possibilidades e as barreiras para automatizar e, assim, potencialmente reduzir enormemente, os processos mentais que impõem custos mentais de transação.

Este artigo examina processos de decisão que ocorrem na mente do cliente e não em um computador, bem como os gargalos que são causados pela necessidade de comunicação entre um computador e esse processo mental. Além disso, discutimos algumas barreiras básicas relacionadas às compras automatizadas.

Este artigo argumenta que os custos de transação mental do cliente são significativos e onipresentes, tanto que, em circunstâncias do mundo real, os custos cognitivos geralmente superam os custos tecnológicos e, de fato, os recursos tecnológicos são mais bem aplicados no objetivo de reduzir custos cognitivos. Além disso, os custos tecnológicos continuarão a cair enquanto os custos cognitivos permanecerem constantes e (mais discutivelmente) cairão mais rapidamente do que o custo tecnológico pode substituir os custos mentais descobrindo e automatizando os processos mentais relevantes. Os custos de transação mental do cliente logo irão dominar os custos de transação tecnológica do sistema de pagamento usado na transação (se não o fizerem), e os esforços de tecnologia de micropagamento que enfatizam a economia tecnológica em relação à economia cognitiva se tornarão irrelevantes. Este artigo sugere algumas maneiras de obter economias cognitivas.

### 1.2 Estrutura de Custos do Fornecedor

[BB97] e [FOS97] discutem o agrupamento e, portanto, a granularidade do preço, do ponto de vista dos fornecedores. Quando os custos marginais são pequenos em comparação com a amortização do custo fixo (por exemplo, um trabalho de conteúdo específico, muita infraestrutura de Internet, etc.) não faz sentido, em face da preferência do cliente pelo preço, cobrar os custos unitários para amortizar um investimento em tempo, exceto em alguns casos excepcionais, como nos casos em que o preço de congestionamento fornece maiores melhorias na qualidade do serviço.

Este artigo fornece explicações para uma forte preferência do cliente pelo preço. Estes são tão significativos que sugerimos que os custos cognitivos do cliente superam os problemas de preço de congestionamento e estrutura de custos do fornecedor nos níveis de micropagamento em quase todos os mercados de varejo. Em contraste com o trabalho anterior, este documento enfoca os custos impostos aos clientes por meio de agrupamento e decisões de granularidade de preço.

2 Argumentos Informais Contra Micropagamentos
---------------------------------------------

Considere uma característica bastante independente do sistema de pagamento específico: a declaração de encargos. Aqui reside uma troca entre completude e complexidade. Por um lado, apenas resumir as acusações cria a oportunidade para as *'salami frauds'* (fraudes de salame), permitindo que micro custos largamente distribuídos, falsos ou exagerados, não sejam detectadas. Além disso, as partes que lêem apenas os resumos não recebem nenhum feedback pelo qual possam ajustar seu comportamento para minimizar os custos. Por outro lado, uma declaração muito complexa para os clientes lerem também permite que fraude, erro e uso ineficiente não sejam detectados, porque uma ou ambas as partes não podem entender a justificativa para as acusações em relação ao acordo presumido sobre termos de serviço e forma de pagamento. O mesmo tipo de raciocínio se aplica a processar essas coisas na cabeça, em vez de no papel, como geralmente é feito em pequenas transações em dinheiro. Um requisito básico para que os preços de mercado funcionem é que ambos os lados de uma transação possam mapear as cobranças ao valor obtido ou processado, para que possam ajustar seu comportamento de compra ou venda de acordo.

Parece haver aqui um gargalo cognitivo fundamental. Uma solução proposta para isso tem sido "agentes inteligentes". Mas como esses agentes são programados remotamente, não pelo consumidor, é difícil para o consumidor determinar se o agente está agindo de acordo com os melhores interesses dos consumidores, ou no melhor interesse da contraparte — talvez, necessariamente, pelo menos tão difícil quanto como ler a correspondente declaração completa de encargos. Além disso, a interface do usuário para permitir que os consumidores simplesmente expressem suas preferências sofisticadas a um agente está faltando e pode representar outro gargalo cognitivo fundamental.

As empresas de comunicação descobriram que o faturamento é um grande gargalo. Segundo algumas estimativas, até 50% dos custos de uma chamada de longa distância são para faturamento, e isso é da ordem de US \$ 100 bilhões por ano no mercado mundial [4]. Os provedores de Internet estão mudando para uma taxa a fim de minimizar esses custos, mesmo que isso crie um incentivo para o excesso de recursos da rede.

Um sistema de micropagamentos pressupõe uma solução para o problema da contabilidade mental. Se alguém pudesse realmente resolver este problema, em vez de simplesmente alegar tê-lo resolvido por meios misteriosos ("agentes inteligentes", etc.), a economia seria enorme mesmo em negócios existentes, como serviços de longa distância e Internet — sem mencionar todos os novos modelos de negócios possibilitados por menores custos de transação (por exemplo, [MD88]).

3 Exemplo - Contas de Eletricidade
----------------------------------

Às vezes, as declarações contabilizam transações em incrementos gratuitos, como a resolução de 100 watts-hora em algumas contas de eletricidade. Há muitas coisas que a maioria das pessoas normalmente não faz em relação às contas de eletricidade, o que poderia melhorar o valor que elas recebem por seus pagamentos de eletricidade :

-   Quais aparelhos estão usando mais eletricidade com menos benefícios pessoais (não disponível na conta de eletricidade — mas é possível conceber um programa de contabilidade pessoal ligado a aparelhos inteligentes que permitem fazer isso).
-   Como equilibrar melhor o calor elétrico com o do gás (você poderia computar isso em detalhes e economizar alguns dólares, mas ganharia dinheiro extra mais rápido ao fazer um trabalho clandestino).
-   Se a empresa de eletricidade fosse uma entidade menos confiável e amplamente conhecida, você também pode não confiar neles com o faturamento e recalculá-los para a resolução com a qual se sentia confortável, além de aceitar fraudes ou truques de letras miúdas abaixo desse nível. (Como a eletricidade é fungível e o conjunto de regras de precificação pequeno, você poderia ter um programa para verificar a conta, o que é eficiente se conseguir informações suficientes para pessoas suficientes recuperarem os custos de desenvolvimento de software e marketing).

A razão pela qual não fazemos essas coisas é que elas não valem os ciclos cerebrais: chegamos a uma barreira contábil mental.

4 Granularidade de Preço
------------------------

Podemos caracterizar quatro maneiras de definir preços:

1.  preço negociado
2.  preços de congestionamento (variável, mas preço postado/pequena unidade de valor)
3.  fungível (uma unidade de preço/valor pequeno)
4.  a taxa (um preço/unidade de grande valor)

Cada um desses níveis impõe sucessivamente menos custos de transação mental ao cliente do que o nível anterior.

A confusão é um bom exemplo do papel substancial que os custos de transação mental desempenham nas economias. Ocorre historicamente e em todas as sociedades um grande declínio da negociação no varejo, à medida que as sociedades se tornam mais ricas. Os preços de varejo se tornam uma fração total menor da riqueza do cliente. Por razões semelhantes, que são o assunto deste artigo, os próprios preços podem se tornar irrelevantes em frações suficientemente pequenas da riqueza do cliente.

### 4.1 Atributos e Preferências

O que significa quando um economista diz que uma pessoa "prefere" um bom X a um bom Y? Muitas vezes os economistas apenas medem isso em quanto a pessoa está disposta a pagar por X versus quanto por Y. Chamamos isso de "o fornecedor observou uma preferência explícita".

Barzel [B82] dá o exemplo de uma maçã: o cliente prefere uma maçã que tenha um gosto bom. O cliente não pode descrever adequadamente esse gosto para outra pessoa ou para o software [P58]. Além disso, esse atributo não pode ser observado durante as compras. Isso nós chamamos de *preferência tácita*. Em vez disso, o cliente usa um atributo observável, por ex. a cor, como um atributo representante. Chamamos isso de *um cliente que observou uma preferência explícita*. Os fornecedores muitas vezes também podem observar esses atributos mapeados para o comportamento do cliente e, assim, a preferência explícita (revelada) correspondente.

As diferenças entre esses tipos de preferências são geralmente de pouca importância. No entanto, elas se tornam importantes se, por exemplo, desejamos que o usuário escolha entre as mercadorias ou delegue essa tarefa a um agente de software comunicando suas preferências a esse software.

Este modelo de preferências será desenvolvido nas próximas seções.

### 4.2 A Função dos Preços

Nossa conta de granularidade de preço é baseada em uma visão subjetivista [M35], [H45] dos preços. A função dos preços, do ponto de vista de um cliente, é deixar o comprador mapear seus recursos pessoais (orçamento) para suas preferências tácitas (únicas e não observáveis diretamente). Isso requer um esforço cognitivo significativo, que define os limites inferiores mais básicos dos custos de transação. Por exemplo, comparar o valor pessoal de um conjunto grande e diversificado de bens de baixo preço pode exigir um gasto mental maior do que os preços desses bens (onde os gastos mentais podem ser mensuráveis como os custos de oportunidade de não se envolver em trabalho mental por salários, ou de não comprar um número menor de bens comparáveis com menores custos contábeis mentais). Nesse caso, faz sentido juntar as mercadorias em pacotes com um preço mais alto e uma sinergia inicial, até que os custos de contabilidade mental dos compradores sejam suficientemente baixos.

### 4.3 Fungibilidade

Outra correção é possível para mercadorias fungíveis: cobrar um preço fixo por unidade, que o comprador pode avaliar apenas a partir do número acumulado de unidades e informações de preços. Como exemplo concreto, em uma recente campanha publicitária americana, a AT&T está apostando que sua taxa de US \$ 0,15 é mais atraente do que a de US \$ 0,10 — que conhece a taxa variável — que vale a pena o fornecedor renunciar aos preços de congestionamento e que o comprador perde descontos vastos , a fim de ter uma taxa previsível, transformando o tempo do telefone em uma mercadoria fungível e, assim, economizando nos custos contábeis mentais.

Infelizmente, a maior parte do comércio pela Internet não é fungível: conteúdo, serviços, encomenda de produtos por correspondência e assim por diante. Alguns serviços do Provedor de Servidor de Internet (ISP) podem ser vendidos como fungíveis (por exemplo, espaço em disco, tempo de conexão) apenas à custa de preceder o congestionamento e outros métodos de precificação que, se não fossem custos contábeis mentais, poderiam ser bastante eficientes. Além disso, mesmo para mercadorias fungíveis, cada usuário tem uma curva única de retornos decrescentes.

O software teria que deixar o comprador determinar e inserir sua curva de preferência de volume (de alguma maneira intuitivamente familiar, sem pressupor que o comprador está familiarizado com a teoria econômica) antes que ela pudesse agir adequadamente em seus interesses; sem mencionar as complicações das preferências temporais, interações não-lineares entre mercadorias fungíveis quando isoladas e assim por diante.

Essa solução de interface de usuário para o caso de mercadorias fungíveis sugere uma estratégia melhor para lidar com o problema mais geral da contabilidade mental no comércio online: desenvolver melhores maneiras para o comprador comunicar suas preferências pessoais ao software. Os profissionais de marketing há muito criaram esquemas para obter esse tipo de informação: pesquisas detalhadas, rastreamento do comportamento e das respostas do usuário, etc. Provavelmente, os serviços Web, como o www.firefly.com, são os mais utilizados nesse quesito. Firefly cria uma espécie de "espaço subjetivo" de preferências musicais em que o comprador pode navegar e encontrar novas músicas que elas têm maior probabilidade de preferir.

Assumindo que o software possa representar certas preferências, é um problema mais direto para o software mapear essas representações para preços específicos (ou ofertas), participar de compras (ou discussões) e concluir com segurança transações online. Esses problemas mais fáceis têm sido o foco da pesquisa de micropagamentos, mas o problema mais fundamental de obter e representar preferências em grande parte não foi amplamente reconhecido, talvez devido a um viés objetivista que postula as leis matemáticas em vez de preferências subjetivas como a base de uma economia de trabalho, e devido às dificuldades básicas em descobrir e especificar preferências normalmente tácitas.

Dada a solução de outros problemas de custos de transação, os custos da contabilidade mental tornam-se sujeitos ao limite do processo de comunicação de preferências — seja pela escolha mental contábil de um bem sobre outro ou pela criação de um simulacro de software único e suficientemente preciso das preferências do comprador, que completa o processo de orçamento, negociação e compra. Até que ponto e com que eficiência pode (a) um comprador comunicar preferências subjetivas ao software, e (b) o software pode representar e agir no interesse dessas preferências objetivadas? A presença de mecanismos de pesquisa, formulários de pedidos de catálogo, pesquisas de marketing e interações mais sofisticadas como firefly demonstram que tal comunicação e representação são viáveis e importantes, mas parecem ser dispendiosas e talvez fundamentalmente limitados de alguma forma.

5 Fluxo de Caixa Incerto e Seguro
---------------------------------

A primeira fonte de custos de transação mental do cliente que examinaremos é sua incerteza sobre seus futuros fluxos de caixa. Podemos caracterizar dois tipos de incerteza que os clientes têm sobre seus futuros fluxos:

1.  Incerteza de renda
2.  Incerteza das despesas, ou seja, incerteza sobre as preferências futuras e as transações entre preferências em diferentes períodos de tempo. Esse tipo de incerteza também desempenha um papel em uma seção subsequente, "Tomada de decisão Incompleta e Cara".

Uma taxa fixa constitui um contrato de seguro incorporado e implícito. [AL95] discute alguns aspectos das preferências de risco implicitamente incorporadas nas transações econômicas. Esse seguro implícito também é uma hipótese de [CL79] para explicar a preferência do cliente pelas tarifas no setor de telefonia.

Os custos do cliente são especialmente altos quando o cliente tem um rendimento fixo e alto custo de crédito e/ou falta de poupança em relação à variável, demasiado dispendioso para calcular ou prever preferências quanto à quantidade ou mistura de itens comerciais a comprar.

O risco colocado para o cliente não é melhor entendido como ficar sem dinheiro *per si*, mas sim como a inanição de outras preferências devido a incertezas na estimativa de recursos futuros disponíveis para serem gastos em preferências para serem satisfeitas no futuro.

A falta inesperada de dinheiro leva a preferências insatisfeitas. A incerteza sobre a disponibilidade de caixa leva ao custo cognitivo e à incompletude na decisão sobre como normalizar as preferências entre dois períodos de tempo.

Uma abordagem simplificadora para formalizar a incerteza de renda seria assumir que os atributos podem ser observados perfeitamente e sem custos, e todos os atributos são contabilizados de forma perfeita e sem custos, enquanto o cliente retém a incerteza sobre seus rendimentos futuros.

Este risco do cliente deve ser negociado contra o risco para o fornecedor de uso excessivo de recursos (análogo, neste contrato de seguro implícito, ao risco moral, mas não oculto do fornecedor). Na maioria das situações de varejo, a capacidade do fornecedor de controlar esses riscos (cobrindo, distribuindo custos, etc.) é geralmente muito menor do que a do consumidor. A taxa de entrada também pode proteger o cliente contra o comportamento oportunista posterior do fornecedor, onde os custos de troca de clientes são altos.

### 5.1 Delegação

Quando o cliente delega a compra de um produto ou serviço durante um determinado período a um agente, uma taxa fixa limita a exposição do princípio/cliente (mas não o fornecedor) ao abuso do recurso pelo agente. Novamente, isso pode ser desejável quando o fornecedor tem mais capacidade do que o cliente para planejar esses usos e distribuir os custos desse uso de recursos entre muitos clientes.

Uma taxa unitária com um limite superior fixo (por exemplo, cartão de telefone) pode facilitar o uso de sistemas de taxa variável, mantendo o fluxo de caixa. Isso converte o contrato implícito de seguro de propagação de risco com preço médio para apenas um grande "dedutível". Este remédio mantém o risco de preferências famintas por este bem, mas elimina (com algum custo) os riscos de fome de preferência geral devido à falta de dinheiro.

6 Custos de Observação de Atributo
----------------------------------

A segunda fonte de custos de transação mental do cliente que veremos é o custo e o erro envolvidos na observação dos atributos de produtos e serviços. Nós introduzimos este problema acima.

Que a verificação de qualidade do cliente impõe um custo econômico significativo foi discutida desde pelo menos Charles Babbage [B1835]. Tentativas recentes para esclarecer a natureza desses custos incluem ([A70], [B82]).

### 6.1 Observação de Atributos

Atributos observados raramente são os atributos realmente valorizados. Em uma seção anterior, mencionamos que Barzel [B82], em particular, estudou essa questão. Neste artigo, não presumimos que o observador sumarize as observações como valores numéricos. Então, em contraste com o termo *medição* de Barzel, vamos nos ater à *observação* mais geral. Em uma *observação por representação*, o produto ou serviço X é observado pelos atributos X<sub>o</sub>, enquanto é valorizado pelos atributos X<sub>v</sub>, que são frequentemente tácitos.

### 6.2 Venda às Cegas com uma Marca de Confiança

[B92] e [KK83] desenvolveram o seguinte cenário, o que sugere o cenário abaixo para micropagamentos via Web.

Lembre das maçãs. Suponha que o atributo representativo da cor esteja correlacionado positivamente com o gosto. Em uma lixeira aberta, os clientes usariam esse atributo para selecionar as melhores maçãs coloridas, deixando as mais pálidas e malhadas para a caixa com maior desconto ou para o lixo.

Um comprador que esteja convencido de que recebeu uma seleção aleatória de uma ótima observação de uma mercadoria não usará recursos adicionais para observação. Um exemplo de venda cega é a venda de maçãs em um saco opaco. Enquanto a marca é confiável, os clientes economizam nos custos de competir uns com os outros para escolher as melhores maçãs coloridas.

A venda às cegas exige que os nomes de marca sejam confiáveis com (1) uniformidade do bem ou (2) aleatoriedade representativa, suprimindo informações específicas para forçar a escolha aleatória de todos os compradores.

### 6.3 Um esquema de pagamento por clique

Há algum tempo que se ouve falar da ideia de "pagamento por clique", um pagamento a cada clique na Web para pagar ao proprietário pelo conteúdo. No entanto, como não houve nenhuma chance de navegar pelo conteúdo, não há como determinar diretamente se ele atende às preferências tácitas: não há preferência explícita observável pelo cliente. Navegar em uma visualização ou capa do livro ainda é impreciso e implica em custos mentais cada vez mais precisos.

Uma possível correção é que o software do comprador compare preços de compra com um serviço de "relatórios ao consumidor". Nós aqui examinamos uma ideia similar, a de marcar os links.

Como um exemplo de como alguém pode lidar com os custos de observação de atributos, precisamos desenvolver um atributo representativo de precisão suficientemente alta e baixo custo. Para esse fim, apresentamos um cenário de links de marca para o conteúdo microprecificado. Uma marca famosa abençoa o link com seu logotipo. Podem haver logotipos diferentes para diferentes tipos de conteúdo, conteúdo de especialidade etc. (por exemplo, um periódico acadêmico pode analisar e, em seguida, marcar artigos em sua especialidade). Autores individuais de reputação suficiente podem criar suas próprias marcas. Isso implica um investimento em um único autor por um número significativo (mas proporcionalmente apenas uma participação de mercado muito pequena) de clientes de uma fração substancial de seu "orçamento de rastreamento de marca".

Isso destaca um problema com o conteúdo da marca: as marcas levam em consideração apenas valores amplamente compartilhados, não valores pessoais. Isso não funciona tão bem para conteúdos cujos gostos são idiossincráticos de tal maneira que não podem ser organizados em uma especialidade. Quanto mais especialidades forem marcadas por cliente, maiores serão os custos de manutenção de todas as marcas.

### 6.4 Custos de Mudança

Outro problema dos links de marca é que não eliminamos os custos mentais de transação. Nós apenas mudamos sua natureza, esperançosamente no processo de reduzi-los. A avaliação da marca em si impõe custos cognitivos. Em particular, as marcas exigem que os clientes invistam em observar e relembrar o histórico de qualidade da marca. Este investimento cria "fidelidade à marca" ou custos de troca, estudados por [K95].

Combinado com a incerteza do consumidor sobre o preço futuro, tais investimentos incentivam a criação de contratos de longo prazo em lugar de preços à vista [W85], ou a taxas em vez de micropagamentos.

### 6.5 Atributos Ocultos no Software de Processamento de Transação

Uma tarefa importante das transações comerciais, que tem sido largamente negligenciada pelo comércio eletrônico tradicional, é fundamental para "o encontro das mentes" que está no centro de um contrato: comunicar a semântica dos protocolos às partes envolvidas. Há uma ampla oportunidade no comércio eletrônico para "letras miúdas inteligentes": ações tomadas pelo software escondido de uma parte da transação. Por exemplo, as máquinas POS da mercearia não dizem aos clientes se seus nomes estão ou não sendo vinculados a suas compras em um banco de dados. Os funcionários nem sabem, e eles processaram milhares dessas transações sob o nariz deles. Assim, por meio da ação oculta do software, o cliente está fornecendo informações que podem considerar valiosas ou confidenciais, mas o contrato foi elaborado e a transação foi projetada de modo a ocultar as partes importantes dessa transação do cliente.

Sem interfaces de usuário, o comércio eletrônico é praticamente invisível, como a eletrônica nos motores de carros mais novos. Isso é uma bênção — as contrapartes não precisam se sentir como se estivessem lidando com computadores hostis ao usuário — e uma maldição — com o problema de "letras miúdas inteligentes" de ações ocultas.

Aqui está um pequeno exemplo de letras miúdas inteligentes:

        
            if(x == true){
                display("x is false");
            }
        

Para comunicar a semântica de transação adequadamente, precisamos de boas metáforas visuais para os elementos do contrato. Estes ocultariam os detalhes do protocolo sem renunciar ao controle sobre o conhecimento e a execução dos termos do contrato. Isso é discutido mais adiante em uma seção subsequente.

Uma maneira de proteger-se contra ações ocultas é especificar mais detalhes contratuais para cobrir situações mais excepcionais e evitar mais oportunidades estratégicas. Contudo, isso também é incompleto e caro [W85].

7 Tomada de Decisão Incompleta e Caro
-------------------------------------

Assumindo, no momento, informações perfeitas sobre o produto em questão e nenhuma incerteza quanto aos futuros fluxos, uma terceira e mais básica fonte de custo cognitivo do cliente permanece, ou seja, o custo de tomar decisões com um grande, mas muito incompleto, conjunto de alternativas.

### 7.1 Tomada de Decisão

A incompletude da tomada de decisões decorre da incompletude da observação de todos os atributos do mundo que podem ser preferidos. Foi também argumentado, por outros motivos, que a teoria da decisão, a base para a maioria das teorias econômicas de preferências, é incompleta, por exemplo Pettit [P91].

Ao equilibrar um portfólio de preferências, o número de alternativas que podem ser consideradas, embora minúsculas em comparação ao número de alternativas realmente no mundo, é tão vasto a ponto de ser computacionalmente inviável de pesquisar quando se toma uma decisão sobre um determinado item comercial . A completitude com que as preferências comerciais podem ser feitas localmente e eficientemente não é clara [K88].

### 7.2 Preferências Tácitas

Um modelo de tomada de decisões, que engloba tudo, desde uma computação altamente heurística a uma tabela completa de alternativas, pode ser fornecido postulando uma função de atributos e preferências para decisões:

T<sub>c</sub> : customer tacit preference rule
 a<sub>c,s</sub>: atributo observado pelo cliente e fornecedor
 p<sub>c,s</sub>: cliente e fornecedor observaram preferência por atributo
 função de formação de preferências (regra de preferência tácita): T<sub>c</sub> : a<sub>c</sub> → p<sub>c,s</sub>

Uma regra tácita semelhante pode ser especificada para atributos, conforme observado apenas pelo cliente.

Chamamos isso de "tácito", porque essas regras não precisam ser articuladas para funcionar adequadamente e, provavelmente, não estão na prática. Em particular, "elicitação de preferência" na literatura econômica provoca apenas a saída, o fornecedor observou preferências explícitas, não a regra em si, nem as preferências alternativas deixadas de lado na decisão observada. Polanyi [P58], entre outros, argumentou que a maioria das decisões humanas é tácita.

Na prática, haverá outra função para pré-calcular as informações para alimentar a regra de preferência tácita, para conservar os custos cognitivos em tempo real que são mais caros do que os custos cognitivos no lazer.

Outra fonte de incompletude é a incapacidade de predizer preferências antes de serem mostrados atributos que podem ser preferidos — porque o processo de tomada de decisão é baseado em uma regra tácita abstrata ao invés de conhecimento de todos os atributos particulares que podem ser encontrados. Devido à indução incompleta das preferências por atributos específicos às regras gerais, o cliente muitas vezes não pode expressar preferências sem o estímulo de observar os atributos, mesmo nos casos em que o atributo foi observado antes em outros contextos.

### 7.3 Preferências Tácitas Intertemporais

A formação de preferências, nesta teoria, ocorre pelo menos parcialmente quando novos atributos são observados. Esses atributos são inseridos na regra de preferência tácita, resultando em decisões ou preferências explícitas. Como, então, as compensações podem ser feitas contra preferências futuras quando a natureza dessas preferências ainda não é bem conhecida? A regra tácita é acionada no instante t1, depois novamente em t2: como essas duas avaliações da regra podem ser comensuráveis?

As preferências tácitas são uma área rica para trabalhos futuros na caracterização de custos de transação mental.

8 Preferências e Metáforas Visuais
----------------------------------

Para avaliar a conveniência de uma transação, e para evitar ser cobrado incorretamente, as partes de uma transação têm que contabilizar, ou seja, contabilizar o dinheiro pago por produtos e serviços específicos — garantindo que os pagamentos em dinheiro sejam feitos como prometido (por exemplo, no visor, à medida que os produtos são digitalizados na loja ou após o recebimento), ou garantindo que a conta telefônica seja adequada. Nesta seção, "contabilidade" é usada nesse sentido amplo.

Um cliente pode estar pagando em dinheiro, mas muitas vezes ele ainda gostaria de saber como e por que seu dinheiro entra e sai. Um log de transações é a ferramenta mais usada para auxiliar nessa tarefa. Podem haver outras metáforas mais apropriadas para algumas circunstâncias (por exemplo, medidores de nível absolutos, medidores de vazão com marcas de água altas e baixas, etc.); Este é um novo campo potencialmente fértil para explorar. Podem haver agentes que possam fazer parte da contabilidade (por exemplo, comparando pagamentos feitos com termos prometidos, limites de pagamento, etc.), mas para a grande maioria dos produtos e serviços, o software não pode julgar a qualidade ou o desejo pessoal do produto ou serviço. e, portanto, a desejabilidade líquida da transação. O usuário deve realizar essa comparação com qualquer informação que o computador possa fornecer através do display. A interface do usuário e a cognição do usuário, portanto, permanecem o gargalo para a granularidade da transação.

Uma grande tarefa é usar o poder da interface gráfica do usuário para criar novas metáforas para tornar isso mais fácil. É a metáfora intuitiva, porém precisa, que reduzirá os custos contábeis. Protocolos criptográficos reduzem potencialmente apenas os custos de transação relacionados à segurança, como falsificação e extorsão. Para os custos normais de transação contábil, que atualmente são muito altos para micropagamentos, precisamos de melhores metáforas visuais interativas.

Para transações livres de registros, precisamos de transações que possam ser transacionadas de maneira justa uma vez, imediatamente explicadas pelas partes por meio de uma metáfora visual agradável e depois esquecidas. O potencial para disputas não resolvidas em sistemas sem registros é vasto para transações onde isso não é possível (provavelmente a maior parte do comércio desejado: onde a qualidade de um produto ou serviço não pode ser bem determinada até que a transação de compra seja concluída ou onde o crédito esteja envolvido).

O preço é um tipo de termo contratual; também precisamos de boas metáforas para rastrear outros tipos de termos contratuais. A falta de observabilidade do protocolo por parte do usuário leva à capacidade da contraparte de se envolver em ações ocultas. Veja [S97] para uma discussão mais aprofundada deste e de outros problemas de contratação informatizados.

Uma das barreiras para criar bons contratos é determinar o que as partes querem em primeiro lugar. As pessoas tendem a pensar em termos de condições padrão ou estereotipadas: pagamento em dólares, investimento em ações, etc., quando existe uma variedade muito maior de estruturas contratuais alternativas que, combinadas adequadamente, poderiam atender melhor às necessidades das partes. Seria útil ter ferramentas que permitissem às partes explorar seus desejos de forma interativa com o computador. Em finanças, isso pode incluir curvas de juros pessoais interativas, determinando a ordem parcial dos desejos (como na teoria da decisão) para títulos, derivativos e produtos sintéticos alternativos específicos; e assim por diante. O software então analisaria essa entrada, faria recomendações e até mesmo realizaria contratações automatizadas. As metáforas devem ser desenvolvidas de modo que seja fácil para os usuários leigos expressar tais desejos sem amplo conhecimento de finanças ou teoria da decisão. Tais metáforas forneceriam um front-end amigável para trocas automatizadas, leilões e outros mecanismos de contratação online.

Uma metáfora específica é o orçamento pessoal, como o tipo que pode ser mantido no software Quicken(tm). Ao escrever um orçamento, o cliente cria um simulacro crasso de suas preferências tácitas esperadas, expressas de uma forma muito abstrata.

9 Conclusão
-----------

Algum trabalho foi feito para determinar as preferências do cliente para uso versus taxas. Uma tentativa recente de comércio na Internet é o INDEX (the INternet Demand Experiment ou Experimento de Demanda Interna) [I99]. A Internet em geral (e a AOL, em particular, é um bom exemplo) viu o movimento se afastar das taxas horárias ou de uso para as taxas.

Também houve trabalho em estudos de empresas de telefonia durante a desregulamentação dos EUA. [FOS97] faz referência e discute algumas das evidências empíricas, originalmente apresentadas em [CL79] e trabalhos relacionados, mostrando a preferência do cliente por taxas no setor de telefonia.

Uma lição para os esforços de micropagamento é que os custos mentais geralmente excedem, e frequentemente diminuem, os custos computacionais. As reduções nos custos computacionais por transação das transações podem muitas vezes ser economicamente insignificantes. Outros custos de transação endereçáveis por hardware ou software, como preocupações com segurança, bem como custos de melhor comunicação da qualidade do produto versus compensações de preço na interface do usuário, são geralmente objetivos mais importantes para redução de custo tecnológico do que conservação em recursos computacionais ou de rede.

Vimos como os custos mentais de transação do cliente podem derivar de pelo menos três fontes: caixa de itens incertos, observação incompleta e dispendiosa dos atributos do produto e tomada de decisão incompleta e dispendiosa. Esses custos irão dominar cada vez mais os custos tecnológicos dos sistemas de pagamento, estabelecendo um limite para a granularidade do agrupamento e dos preços. Os preços não vêm de graça.

10 referências
--------------

[A70] Akerlof, G.A., "The Market for 'Lemons': Quality Uncertainty and the Market Mechanism," Quarterly Journal of Economics, 84(3), 488-500.

[AL95] Allen, D.W. and Lueck, D. (1995), 'Risk Preferences and the Economics of Contracts', 5 American Economic Review, Papers and Proceedings, 447-451.

[B1835] Babbage, C. *On the economy of machinery and manufactures*, 4th ed. New York: Kelley, 1963. (Facsimile reprint of the edition published in London by Knight, 1835).

[Be95] Bellare, M. et. al., "A Family of Secure Electronic Payment Protocols", *Proceedings of the Usenix Electronic Commerce Workshop*, 1995

[Bz82] Barzel, Y., "Measurement Costs and the Organization of Markets," *Journal of Law and Economics*, 25, 27-48.

[BB97] Bakos, Y., and Brynjolfsson, E. "Aggregation and disaggregation of information goods: Implications for bundling, site licensing and micropayment systems." In *Internet Publishing and Beyond: The Economics of Digital Information and Intel lectual Property*. D. Hurley, B. Kahin, and H. Varian, eds., MIT Press. Also at [http://www.gsm.uci.edu/bakos/aig/aig.html](http://www.gsm.uci.edu/bakos/aig/aig.html)

[CL79] Cosgrove, J. G., and Linhart, P. B., "Customer choices under local measured telephone service.", *Public Utilities Fortnightly*, Aug. 30, 27-31.

[FOS97] Fishburn, P, Odlyzko, A.M., and Siders, R.C., "Fixed fee versus unit pricing for information goods: competition, equilibria, and price wars", *First Monday*, Vol.2 No.7 - July 7th. 1997, [http://www.firstmonday.dk/issues/issue27/odlyzko/index.html](http://www.firstmonday.dk/issues/issue27/odlyzko/index.html)

[GMAGS95] Glassman, S., Manasse, M. Abadi, M., Gauthier, P.S., "The MilliCent Protocol for Inexpensive Electronic Commerce", Proceedings of the 4th International World Wide Web Conference — December, 1995. For proposed uses, see [http://www.millicent.digital.com/works/white\_papers/index.html](http://www.millicent.digital.com/works/white_papers/index.html)

[H45] Hayek, F. "The Use of Knowledge in Society", *American Economic Review*, 35 (September 1945): 519-530

[H89] Hart, O., "Incomplete Contracts," In: John Eatwell, Murray Milgate, and Peter Newman (eds.), *The New Palgrave: Al location, Information, and Markets*. New York: Norton.

[I99] [http://www.index.berkeley.edu](http://www.index.berkeley.edu)

[K88] Kreps, D. M., *Notes on the Theory of Choice*, Westview, 1988

[K95] Klemperer, P., "Competition When Consumers Have Switching Costs: An Overview with Applications to Industrial Organization, Macroeconomics, and International Trade", *Review of Economic Studies* 62(4) pages 515-39.

[KK83] Kenney, R. W. and Klein, B., "The Economics of Block Booking", *Journal of Law and Economics*, 26, 497-541.

[M35] Mises, L. v. *Human Action*, 3d edition (Regnergy, 1996)

[MD88] Miller, M. and Drexler., K.E., "Markets and Computation: Agorics Open Systems", in *The Ecology of Computation*, Bernardo Huberman (ed.) Elsevier Science Publishers/North-Holland, 1988.

[N98] Nielsen, J., "The Case for Micropayments", Jakob Nielsen's Alertbox for January 25, 1998, [http://www.useit.com/alertbox/980125.html](http://www.useit.com/alertbox/980125.html). See also sidebar "User Interfaces for Internet Payments" and reader comments.

[P58] Polanyi, M. *Personal Knowledge*, University of Chicago Press, 1958

[P91] Pettit, P., "Decision Theory and Folk Psychology", in Bacharach, Michael and Hurley, Susan ed., *Foundations of Decision Theory*, Blackwell, 1991

[RS96] Rivest, R.L. and Shamir, A. "PayWord and MicroMint—Two Simple Micropayment Schemes", *CryptoBytes*, volume 2, number 1 (RSA Laboratories, Spring 1996), 7—11

[S97] Szabo, N. (1997) "Formalizing and Securing Relationships on Public Networks", First Monday, Vol.2 No.9 - September 1st. 1997, [http://www.firstmonday.dk/issues/issue29/szabo/index.html](http://www.firstmonday.dk/issues/issue29/szabo/index.html)

[W85] Williamson, O. E. *The Economic Institutions of Capitalism*, Free Press/McMillan, 1985

11 Agradecimentos
-----------------

Meus agradecimentos a Robert Horn, Hal Varian, Doug Barnes, Ian Grigg e outros por seus comentários úteis.

        Fonte: http://www.fon.hum.uva.nl/rob/Courses/InformationInSpeech/CDROM/Literature/LOTwinterschool2006/szabo.best.vwh.net/berlinmentalmicro.pdf
