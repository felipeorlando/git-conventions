<p align="center">
	<img src="https://raw.githubusercontent.com/felinalabs/git-conventions/master/cover.png" alt="Git Conventions Cover" style="max-width:100%;">
</p>

<h1 align="center">
	<a id="user-content-octocat-git-conventions" class="anchor" href="#octocat-git-conventions" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" role="img" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a>
	Git Conventions
</h1>

<p align="center">
	:warning:<br><strong>ATENÇÃO</strong>
</p>
<p align="center">
	Esse repositório foi feito há anos atrás, agora está descontinuado. Recomendo seguirem o <a href="https://www.conventionalcommits.org/en/v1.0.0/" target="_blank">Conventional Commits</a>.
</p>

---

Todos nós, desenvolvedores, trabalhamos com versionamento. E grande parte de nós optamos por trabalhar com Git, por sua popularidade e facilidade de aprendizagem.

Todo bom programador descobre cedo que é preciso padronizar seu workflow. Seja no modo em que escreve seu código, seja na arquitetura do projeto, seja no método de trabalho. 

E trabalhar com Git muitas vezes significa trabalhar em equipe. E nisso ele é uma mão na roda! Porém também é preciso criar um padrão para que a equipe possa sempre ser performática.

Porém, antes de começar, precisamos analisar o projeto em que estamos trabalhando. 

**As soluções descritas aqui não são balas de prata**!

## :us: Yes, we can! And we must!
Primeiramente é preciso DITAR: todo o trabalho com o Git/GitHub precisa estar escrito em inglês. Sem mais, nem menos. Esse é o primeiro passo. Afinal, você não escreve seu código em português (ao menos não deveria).

## :recycle: Siga padrões já estabelecidos
Não seja rebelde, não reinvente a roda. Se o projeto que você começou a trabalhar já tem um **padrão definido** e bem estruturado, não há razão para mudanças drásticas. Se o projeto já tem tempos de vivência, significa que o padrão atual já dá conta do recado.

## :rocket: Commit a cada mudança
O ideal para manter tudo bem versionado é, para cada mudança, um commit. Seja adição de nova funcionalidade, correção de bug ou até remoção de uma funcionalidade antiga.

Isso não só é necessário para o processo de **deploy** da aplicação para mudanças necessárias, mas nos dá a facilidade de usar uma das principais funcionalidades do versionamento: retroceder ao código antes do commit indicado. 

## :anchor: Sintaxe é o segredo para o início triunfal
Ao lidarmos com versionamento, o mais importante não é o software, mas sim a equipe por trás do desenvolvimento dele. E é válido lembrar que esta equipe é composta por humanos. Precisamos não só humanizar nosso software, nosso código mas também nosso processo de trabalho **por inteiro**.

Temos que lidar com **commits** e **merges** descrevendo nossas ações, de forma compreensíva até mesmo para alguém completamente leigo na área de TI.

### Commits
Cada ação significativa realizada no código deve ser tratada como uma ação, um **verbo**. A mensagem dos commits deve ser direta, compreensíva porém breve.

Todo commit deve começar com um verbo, seguido da(s) alteração(ões) feita(s) – apesar do singular, dê prioridade por fazer commit a cada alteração no sistema, seja uma adicão, atualização, remoção.

Alguns dos verbos que costumo usar bastante são: **add, create, update, edit, remove**.

**Exemplo:** Em um projeto onde teremos comentários e trabalharemos com algum framework MVC, ao criarmos uma migration para os comentários, podemos fazer o seguinte commit:

```
git commit -m "Create comments migration"
```

O mais interessante ainda, seria fazer este commit após a criação da migration e do model. Assim, unificamos um commit para criação tanto do database, quanto do model:

```
git commit -m "Create comments migration and Comment model"
```

Obs: É bom notar nos dois exemplos o início da mensagem com letra maiúscula. Como eu disse: padrões são necessários... inclusive os pequenos detalhes.

A ideia não é fazer nem muitos e nem poucos commits. Muitos commits tornam o "changelog" do projeto sujo e grande. Poucos não mantém o projeto devidamente atualizado com atualizações primordiais do projeto e não beneficia no workflow quando se trabalha com **integração contínua**.

Outro ponto que podemos atingir é a necessidadede de uma PAUSA, o momento em que nosso trabalho precisa de um hiato para dormirmos, comermos, sairmos ou **tomar um café** :coffee:. Nessas horas, podemos estabelecer nosso trabalho em partes, usando os números que a matemática neandertal nos provém: 1, 2, 3, 4...

**Exemplo:** Estou lá eu, resolvendo uma awesome feature quando o meu ~~combustível~~ café e percebo que preciso ir comprar mais, do outro lado da cidade... Lá vou eu, mas antes vou commitar para não perder nada! Então, como sei que parei na metade do caminho, vou dar um commit enumerado:

```
git commit -m "Add awesome feature #1"
```

Assim que eu tiver café o suficiente e codando novamente, posso terminar meu trabalho e commitar quando tudo estiver pronto:

```
git commit -m "Add awesome feature #2"
```

### Merges
O conceito de merge é extremamente simples. Simples assim! Não há o porquê complicar, pois não é uma cilada, Bino. :laughing:

A nomeclatura de um merge deve ser simples e coesa, condizendo com o motivo daquele merge. Mais específicamente, indicar a ação realizada naquele merge logo no início.

É comum usar **fix**, **add**, **remove**, **refactoring**.

