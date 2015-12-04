:octocat: Git Convention
==============

Todos nós, desenvolvedores, trabalhamos com versionamento. E grande parte de nós optamos por trabalhar com Git, por sua popularidade e facilidade de aprendizagem.

Todo bom programador descobre cedo que é preciso padronizar seu workflow. Seja no modo em que escreve seu código, seja na arquitetura do projeto, seja no método de trabalho. 

E trabalhar com Git muitas vezes significa trabalhar em equipe. E nisso ele é uma mão na roda! Porém também é preciso criar um padrão para que a equipe possa sempre ser performática.

Porém, antes de começar, precisamos analisar o projeto em que estamos trabalhando. 

**As soluções descritas aqui não são balas de prata**!

## :us: Yes, we can! And we must!
Primeiramente é preciso DITAR: todo o trabalho com o Git/GitHub precisa estar escrito em inglês. Sem mais, nem menos. Esse é o primeiro passo. Afinal, você não escreve seu código em português (ao menos não deveria).

## :recycle: Siga padrões já estabelecidos
Não seja rebelde, não reivente a roda. Se o projeto que você começou a trabalhar já tem um **padrão definido** e bem estruturado, não há razão para mudanças drásticas. Se o projeto já tem tempos de vivência, significa que o padrão atual já dá conta do recado.

## :rocket: Commit a cada mudança
O ideal para manter tudo bem versionado é, para cada mudança, um commit. Seja adição de nova funcionalidade, correção de bug ou até remoção de uma funcionalidade antigo.

Isso não só é necessário para o processo de **deploy** da aplicação para mudanças necessárias, mas nos dá a facilidade de usar uma das principais funcionalidades do versionamento: retroceder ao código antes do commit indicado. 

## :anchor: Sitaxe é o segredo para o início triunfal
Ao lidarmos com versionamento, o mais importante não é o software, mas sim a equipe por trás do desenvolvimento dele. E é válido lembrar que esta equipe é composta por humanos. Precisamos não só humanizar nosso software, nosso código mas também nosso processo de trabalho **por inteiro**.

Temos que lidar com **commits** e **merges** descrevendo nossas ações, de forma compreensíva até mesmo para alguém completamente leigo na área de TI.

### Commits
Cada ação significativa realizada no código deve ser tratada como uma ação, um **verbo**. A mensagem dos commits deve ser direta, compreensíva porém breve.

Todo commit deve começar com este verbo, seguido da(s) alteração(ões) feita(s) – apesar do singular, dê prioridade por fazer commit a cada alteração no sistema, seja uma adicão, atualização, remoção.

Alguns dos verbos que costumo usar bastante são: **add, create, update, edit, remove**.

**Exemplo:** Em um projeto onde teremos comentários e trabalharemos com algum framework MVC, ao criarmos uma migration para os comentários, podemos fazer o seguinte commit:

```
git commit -m "Create comments migration"
```

O mais interessante ainda, seria fazer este commit após a criação da migration e do model. Assim, unificamos um commit para criação tanto do database, quanto do model:

```
git commit -m "Create comments migration and Comment model"
```

A ideia não é fazer nem muitos e nem poucos commits. Muitos commits tornam o "changelog" do projeto sujo e grande. Poucos não mantém o projeto devidamente atualizado com atualizações primordiais do projeto e não beneficia no workflow quando se trabalha com **integração contínua**.

### Merges
...

