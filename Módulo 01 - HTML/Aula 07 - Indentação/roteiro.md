# Indentação 
Nesta aula nós iremos ver um dos assuntos mais importantes para um programador, seja ele web ou não. Indentação!

## O que é?
Indentação, ou recuo, é o conceito de programar utilizando recuos/espaços de forma padronizada seu código fonte para que seja ressaltado ou definido sua estrutura. Indentação também é considerada uma das Boas Práticas de Programação.

Não ajudou muito, né? De um modo mais simples, a aplicação de Identação no seu código serve para deixa-lo estruturado, legível e fácil de ler.

Veja abaixo a diferença entre um código não indentado *vs* o mesmo código indentado:

**Código não indentado**
```html
<!DOCTYPE html>
<html>
<head>
<title>Meu primeiro site</title>
</head>
<body>
<h1>Meus parágrafos</h1>
<div>
<h2>Um parágrafo</h2>
<p>
Exemplo de parágrafo <br/>
Esta é uma segunda linha
</p>
<h2>Outro parágrafo</h2>
<p>Este parágrafo possui <i>algumas</i> formatações de <b>texto</b></p>
</div>
</body>
</html>
```
**Código indentado**
```html
<!DOCTYPE html>
<html>
    <head>
        <title>Meu primeiro site</title>
    </head>
    <body>
        <h1>Meus parágrafos</h1>
        <div>
            <h2>Um parágrafo</h2>
            <p>
                Exemplo de parágrafo <br/>
                Esta é uma segunda linha
            </p>
            <h2>Outro parágrafo</h2>
            <p>Este parágrafo possui <i>algumas</i> formatações de <b>texto</b></p>
        </div>
    </body>
</html>
```

Com este exemplo você consegue perceber que quando o código **está** indentado, você consegue entender facilmente que as tags na páginas possuem uma ordem e uma estrutura.

Ou seja, com o código indentado nós vemos claramente que:
- As tags ``<head>`` e ``<body>`` estão dentro de ``<html>``
- As tags ``<h1>`` e ``<div>`` estão dentro de ``body``
- As tags ``<h2>`` e ``<p>`` estão dentro da ``div``

_Note que para as tags ``<i>`` e ``<b>`` nós não aplicamos nenhuma indentação ou formatação diferente do que já vimos nas aulas anteriores, isso é porque essas tags são bem específicas e servem apenas para formatação simples de um texto, diferente das outras tags que formam blocos de conteúdos._


> Lembrete: Para identar este código de exemplos e todos os códigos deste curso nós utilizamos 4 espaços, que é uma das convenções para indentação.

## Por que indentar?
Há inúmeros motivos para você indentar corretamente seu código, veja abaixo os principais deles:

- Legibilidade: Seu código vai ficar mais legível (fácil de ler e entender o que ele faz) para outros programadores que poderão ver seu código no futuro, e podem não conhecer exatamente o que o sistema faz e vão precisar ler e compreender seu código para entender o sistema. Também é muito útil para **você mesmo**, que poderá precisar mexer no código depois de alguns meses e você não vai tudo que aquele código faz.

- Padronização: No mercado de trabalho você com certeza vai precisar alterar ou expandir um código de algum colega seu, e quando você for fazer isso, você irá precisar manter padronizado a indentação utilizada pelo seu colega, assim quando ele for ver o código, ele consiga compreender sem dificuldades o que você programou.

- Debug: Quando acontecer algum erro no seu código, você precisará procurar qual é o erro para poder conserta-lo. Quando seu código está indentado, essa procura (provavelmente) se tornará muito mais fácil, visto que erros nas estruturas do código são um dos erros mais comuns de se cometer.

Entre outros muitos fatores para aprender e utilizar **sempre** a indentação.


## Mas é obrigado a indentar?
Em certos casos, sim.

De maneira simplificada, a grande maioria das linguagens que você vai utilizar não irá obrigar que você indente o código corretamente para ele poder funcionar corretamente, principalmente no desenvolvimento web, mas é importante saber que há linguagens ou até arquivos de configuração que **necessitam** que o seu código esteja indentado perfeitamente.


**O ideal (e o esperado) é sempre indentar seu código!**