# Divisórias e estruturação de um site
Nesta aula você irá aprender sobre as tags que utilizamos para dividir e separar os conteúdos (ou blocos) de um site, além de aprender as principais estruturas uma página web.

## Divisórias
Toda página web é composta por várias divisórias que separam os conteúdos e demarcam áreas no seu site. Para você criar uma divisória, você pode utilizar ``div``, que criará uma divisória em forma de bloco, ou ``span``, que criará uma divisória em forma de texto.

```html
<!DOCTYPE html>
<html>
    <body>
        <div>Este é meu primeiro bloco</div>
        <div>
            Este é meu segundo bloco e dentro dele eu <span>possuo uma divisória</span> de <span>texto</span>.
        </div>
    </body>
</html>
```

_Mostrar no navegador_.

Aqui nós podemos observar duas coisas principais:  
1 - Quando separamos o conteúdo com ``div`` ele irá "pular a linha". Isso acontece porque um bloco ``div`` ocupa todo o espaço horizontal, fazendo com que o segundo bloco ``div`` fique abaixo do primeiro bloco, diferente do ``span``, que é interpretado pelo navegador como uma divisória de texto e não como um bloco.

2 - Você reparou que, diferente da maioria das tags que aprendemos, nós não utilizamos nenhum atributo? Isso é porque a principal função da ``div`` e do ``span`` é apenas separar conteúdos, então eles não possuem atributos especiais como a tag ``a`` e a tag ``img``.

## Estruturas de um site
Agora que já sabemos dividir nosso conteúdo HTML em blocos, vamos aprender os principais blocos (ou estruturas) de uma página web.

É esperado (mas não obrigatório) que toda página web tenha entre três e cinco áreas principais, sendo estas:

#### Header (ou topo) - Obrigatório
São os conteúdos que ficam no topo do site, geralmente com informações como login, barra de pesquisa, menu configurações, identificação do seu site entre outros conteúdos importantes para seu site.
No Youtube, o Header possui o logotipo à esquerda, a barra de pesquisa centralizada e os botões de configurações à direita - Todos no topo do site.

#### Nav / Menu (ou menu)
É geralmente o seu menu principal, que contém os links principais para a navegação do seu site. Geralmente ele se encontra entre o Header e o Content.
No Youtube, o Menu é uma barra lateral, que contém os principais links para você navegar dentro do site.

#### Content (ou conteúdo) - Obrigatório
É onde fica todo o conteúdo do seu site, ou seja, se o seu site é um blog, todas as suas postagens estarão dentro do Content.
No Youtube, o Content possui a listagem dos vídeos na página principal, e quando estamos assistindo um vídeo, o Content possui o player do vídeo e comentários.

#### Aside (ou conteúdo extra)
É onde você pode incluir todo conteúdo que não necessariamente é parte principal da sua página, mas que está relacionado ao conteúdo dentro do Content e geralmente serve como uma extensão ou complementação do mesmo.
No Youtube, quando você está assistindo um vídeo, a lista de vídeos relacionados da lateral direita do site pode ser considerada como uma área Aside.

#### Footer (ou rodapé) - Obrigatório
Aqui você irá colocar todo conteúdo (principalmente links) que irá complementar o seu Header, oferecer ações únicas de ajuda ou configurações e outros elementos que geralmente só encontramos no Footer.
No Youtube, o Footer dele fica na barra lateral (mas separado da Nav/Menu), contento vários links únicos de Direitos autorais, Sobre a empresa, Termos de privacidade e a exibição do copyright.

_Exibir imagens identificando cada área nas páginas do Youtube, conforme fala de cada área._

## Imaginando os blocos
Pronto, agora que você sabe como dividir um site usando ``div`` e você sabe quais são as principais áreas de um site, vamos fazer um exercício simples?

O exercício é muito fácil de se fazer, e serve apenas para entender as divisórias é brincar de adivinhar as divisões de um site. Isso você pode fazer, no começo, usando o _Paint_ mesmo, mas depois você vai perceber que naturalmente você vai reconhecer as divisões de um site apenas de olhar para ele, e é aí que queremos chegar!

> **Única regra para este exercício é:** Para aplicar as divisões em um site, basta você começar sempre da maior área, até a menor, tentando respeitar as áreas principais de um site.

Vamos pegar o Google como exemplo:

_Mostrar o exemplo do google._

Verde: ``<html>``  
Vermelho: Header  
Azul: Content  
Rosa: ``<div>``  
Laranja: ``<div>``

**Este tipo de exercício, seja no Paint ou apenas na sua cabeça, irá de facilitar a compreensão dos elementos (blocos) tanto no início dos seus estudos quanto quando você já for um programador experiênte.**
