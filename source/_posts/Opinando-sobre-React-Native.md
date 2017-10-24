---
title: Opinando sobre React Native
date: 2017-10-24 20:13:07
tags: react-native
---

Em um emprego anterior, tive a chance de trabalhar com o desenvolvimento de um app multiplataforma, com a vantagem de poder utilizar uma linguagem com a qual eu já tinha familiaridade (JS :D), sem me enroscar na curva de aprendizado de duas ou mais linguagens novas. Nesse artigo, quero comentar um pouco sobre a experiência de trabalhar com React Native, ressaltando algumas vantagens e desvantagens da plataforma!

## Começando pelo começo: o que é React Native?

É um framework de desenvolvimento de aplicativos móveis que de fato usa componentes nativos de Android, iOS e Windows (sim, estão empurrando isso) por baixo dos panos, diferente de outros como Ionic e Phonegap que são (falando de maneira bem superficial) webviews, como se fosse uma página web em um navegador capaz de interagir com os recursos do seu aparelho.

Sabemos que o Facebook anda investindo bastante em tecnologias Open Source, como é o caso do React, um dos frameworks web mais populares atualmente. Como um dos principais produtos, digamos assim, do FB para seus usuários é o aplicativo móvel, é claro que eles não ficariam de fora da oportunidade de ter em mãos uma ferramenta que agiliza bastante o desenvolvimento de apps e ainda tem apoio da comunidade.

## Características, vantagens e desvantagens

### Linguagem: Javascript
A ideia de usar uma linguagem popular em aplicações web no desenvolvimento de apps móveis não é grande novidade, como nos exemplos que citei (Ionic e Phonegap). É um grande atrativo para startups pelo fato de acelerar a chegada de um app às lojas, tanto do Android quando do iOS (vou deixar o Windows de fora dos exemplos, apenas saibam que ele existe :sweat_smile:).

Além disso, é bem menos custoso, tanto em tempo quanto em dinheiro, manter um desenvolvedor que sabe JS para cuidar de um único projeto do que manter um dev para cada plataforma, em projetos separados. Claro que vão haver diferenças nos aplicativos, mas é possível ter no código estruturas como:

```
if (Platform.OS === 'android') {
  console.warn('Tô no Android!');
} else {
  console.warn('Tô no iOS!');
}

console.warn('Tanto faz /shrug');
```

Mesmo assim, é possível ter algo em volta de 90% de código em comum para os dois sistemas.

Sem falar na estrutura de componentes que é quase idêntica à do React, com JSX e tudo mais, e os mesmos conceitos de `state` e `props` se aplicam. Para quem já manja React, o -Native é um degrauzinho a mais. Para quem não manja, também não tem muito segredo.

### Linguagens nativas

Projetos de React Native são compostos basicamente de 3 partes:
- o Javascript que comentei acima;
- um projeto Android, com direto a `gradle` e tudo mais (sim, você provavelmente vai precisar do Android Studio);
- um projeto iOS (do XCode).

Para acessar algumas features do sistema operacional que não vêm por default no React Native, no entanto, vai ser necessário usar código nativo, mas não é complicado. Muitas bibliotecas da comunidade já cuidam de tudo pra você, desde notificações Push até leitura de SMS, automatizando até a importação do código nativo nos respectivos projetos (olá `react-native link`).


Se você entende de desenvolvimento em linguagens nativas, também pode escrever suas bibliotecas, fazendo a comunicação com o thread do Javascript através de uma "bridge". Só tenha em mente que essa bridge é um dos maiores gargalos de performance, então tente minimizar a troca de dados entre código nativo e JS.

### CodePush

A Microsoft resolveu entrar na brincadeira e também vem contribuindo bastante com o Open Source, trazendo um presentão pra comunidade do React Native: o CodePush, uma ferramenta que permite o envio de atualizações pro seu aplicativo sem ter de passar pelo processo cansativo de "deploy" nas lojas (especialmente da App Store, que é bem burocrático).
Funciona mais ou menos assim: se a sua atualização tem apenas modificações no código JS, o CodePush vai gerar um "bundle", um pacotão com seu código, mandar pra nuvem (Azure, suponho) e seus usuários vão baixar este novo bundle em segundo plano, substituindo o bundle da versão anterior a partir da próxima vez que o app for aberto (o evento que provoca a atualização pode ser configurado).

Por outro lado, caso você tenha modificado código nativo vai ter que fazer o processo padrão que é compilar novamente e enviar os binários para as respectivas lojas (relaxa, só leva uns 15 dias pra ser publicado na App Store).

Uma desvantagem do CodePush, que eu não pesquisei a fundo para saber se tem solução, é que caso esse bundle falhe ao instalar não será feita outra tentativa de instalar a mesma atualização. Isso é pra prevenir que o aplicativo fique num loop de crash, caso seu JS jogue um erro logo de cara. Mas também faz com que seus usuários fiquem com uma versão atrasada até a próxima atualização.

----

Vou fechar esse artigo por aqui pra não ficar muito extenso, mas pretendo continuar com algumas considerações sobre performance, a participação da comunidade e o que mais vier à mente. Espero que esse pedaço já seja suficiente para ter uma noção do que esperar caso resolva começar um projeto em React Native!
