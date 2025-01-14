---
title:  "RPOW – Provas de Trabalho Reutilizáveis"
date:   2004-08-15
categories:
   -  Artigo
tags:
  -
author:
  - Hal Finney
---
```
Traduzido por: Marcos Monteiro
Revisado por: Cypherpunks Brasil
```

### Hal Finney

##### [Website arquivado GitHub]
---
Para: [cypherpunks@al-qaeda.net]
Assunto: RPOW - Provas de Trabalho Reutilizáveis
Data: domingo, 15 de agosto de 2004 às 10:43:09 -07:00 (PDT)
De: hal arroba finney ponto org ("Hal Finney")

---
===exibe no card daqui pra baixo===

Eu gostaria de convidar os membros dessa lista para testar meu novo servidor baseado em hashcash, [rpow.net].

Esse sistema recebe hashcash como um token de Prova de Trabalho (POW), e, em troca, cria tokens assinados por RSA que eu chamo de tokens de Prova de Trabalho Reutilizável (RPOW). RPOWs podem ser transferidos de pessoa para pessoa e trocados por novos RPOWs a cada passo. Cada RPOW ou token POW só pode ser usado uma vez já que dá vida a um novo, é como se o mesmo token pudesse ser entregue de pessoa a pessoa.

Porque RPOWs são criados apenas a partir de POWs ou RPOWs de igual valor, eles são tão raros e "valiosos" quanto o hashcash que foi usado para criá-los. Mas eles são reutilizáveis, diferentemente do hashcash.

O novo conceito no servidor é o modelo de segurança. O servidor RPOW está rodando em um cartão de processamento de alta segurança, o IBM 4758 SCC, validado para FIPS-140 nível 4. Esse cartão tem a capacidade de entregar um atestado assinado do software de configuração na placa, que qualquer usuário (suficientemente motivado) pode verificar o código fonte publicado do sistema. Isso permite a todos verem que o sistema não tem back doors e criará apenas tokens RPOW quando fornecidos com token POW/RPOW de igual valor.

Isso é o que cria confiança em RPOWs, de fato incorporando seus valores, o conhecimento que eles foram, na verdade, criados baseado em um token POW (hashcash) de igual valor.

Eu tenho muito mais informações sobre o sistema em [rpow.net], juntamente ao código fonte baixável. Há também uma interface web crua que te deixa trocar POWs por RPOWs sem precisar baixar o cliente.

Esse sistema está em fase beta inicial no momento, então eu gostaria de ler comentários se alguém tiver a chance de testá-lo. Por favor, tenha em mente que se houver problemas eu posso ter que recarregar o código do servidor, o que invalidará os tokens RPOW que as pessoas criaram previamente. Então não enlouqueça acumulando muitos RPOWs ainda.

Muito obrigado -

Hal Finney Fonte: https://nakamotoinstitute.org/rpow/

[Website arquivado GitHub](https://nakamotoinstitute.org/finney/rpow/index.html)
[cypherpunks@al-qaeda.net](cypherpunks@al-qaeda.net)
[rpow.net](https://nakamotoinstitute.org/finney/rpow/index.html)
