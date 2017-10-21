---
title: Git para iniciantes - Motivação (Parte 1)
date: 2017-10-20 22:12:45
tags: git
---

Joãozinho não sabia usar versionamento. Para ele, era só mais um tópico chato na matéria de engenharia de software.
Joãozinho fazia seus trabalhos e exercícios da faculdade jogando um monte de arquivos fonte em uma pasta no desktop. Joãozinho editava e salvava seus arquivos trocentas vezes, programava por tentativa e erro e nunca lembrava como estava antes de mexer quando estragava uma parte que funcionava.
Pedrinho, seu amiguinho, veio com uma ideia genial:
> Joãozinho, seu energúmeno, faça como eu! Coloque seu código no Dropbox ou no Google Drive por segurança!

Esses caras. Não seja como esses caras

Eu lembro quando ouvi falar sobre sistemas de versionamento pela primeira vez na faculdade. "Mas que diabo é isso?" pensei logo de cara, assim como pensava com qualquer termo novo que aparecia. Devo ter respondido uma ou outra pergunta sobre o assunto em uma prova ou lista de exercícios, o assunto morreu e vida que segue.

Mal eu sabia o quanto eu ia me arrepender de não ter aprendido de verdade.

> Nemly & Nemlerey. Fala logo o que é esse tal de versionamento!

Resumindo: É uma forma de controlar e organizar seu trabalho, ao longo do tempo, através de "checkpoints". INDISPENSÁVEL se você pretende seguir na carreira de desenvolvimento (embora seu uso não seja restrito a desenvolvedores, há muitos designers utilizando, por exemplo). Vai por mim, vale a pena estudar e aprender o quanto antes.

> Não entendir...

Vou dar um exemplo. Imagina que você tem que fazer um trabalho em grupo na faculdade. Seria legal se:
- Todos pudessem saber quem mexeu em qual parte de qual arquivo (seja código, documento do Office ou whatever), por quê e quando;
- Fosse possível reverter aquela caca gigantesca que seu amigo (ou você mesmo, vai saber) fez no texto, salvou e ninguém tem uma cópia da versão anterior;
- Todos pudessem trabalhar no mesmo arquivo, ao mesmo tempo, e não fosse um pesadelo na hora de "juntar as partes".

E se eu te dissesse que uma ferramenta de versionamento como o Git te dá tudo isso? Está convencido? Falo sobre o Git porque é a ferramenta com que tenho mais experiência, mas existem outras semelhantes como SVN e Mercurial, apenas para citar.

Como eu disse antes, ele organiza seu trabalho através de "checkpoints" (oficialmente conhecidos como `commit`s), que são registros de alterações feitas em um conjunto de arquivos (chamado de *repositório* ou *repo* para os chegados). Essas alterações geralmente são arquivos adicionados, removidos, renomeados ou alterados, não necessariamente apenas um arquivo por `commit`. Você pode (e deve) agrupar diversas alterações com uma mesma finalidade em um único `commit`.

Cada `commit` guarda também informações adicionais como o nome do autor da mudança, a data e hora da modificação e "opcionalmente" uma descrição do que foi feito e o motivo. Opcionalmente entre aspas né, porque a ferramenta em si não te obriga a dar uma descrição bem feita. Mas vai por mim, dá uma descrição bem feita. É pro seu próprio bem ;)

Esses commits vão formando uma sequência de alterações, como um "passo a passo" de modificações que levam seu repositório de uma versão inicial até a versão desejada, mantendo um histórico de tudo o que foi feito até o momento e possibilitando voltar a qualquer momento para um determinado `commit` caso tenha feito algo errado.

Mas lembre-se: como diria o tio Ben, com grandes poderes vêm grandes responsabilidades! Você não vai querer acabar como [esse cara](http://archive.is/EZX1O) que apagou TRÊS MESES de trabalho, sem dó, sem backup, usando a função de "descartar alterações" sem saber direito do que se trata. Então vale a pena estudar bem os conceitos de versionamento e as ferramentas que vai usar antes de colocar a mão na massa em um projeto importante.

Isso é o básico do básico que eu queria apresentar sobre a importância de aprender esse bendito Git, seja nos seus estudos ou na sua carreira. Tem muito material bacana nas interwebs sobre o assunto, mas eu também pretendo continuar essa série com alguns tutoriais e dicas para mostrar na prática como o Git vai facilitar sua vida. Até a próxima!
