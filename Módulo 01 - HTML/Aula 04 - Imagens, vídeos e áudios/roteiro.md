# Imagens, vídeos e áudios
Nessa aula veremos como utilizar os principais recursos multimídia no HTML.

## Imagens
Para exibir uma imagem utilizamos a tag ``img``. Seu principal atributo é o ``src``, seu valor deve ser o caminho da imagem(seguindo as regras de caminho de arquivos ensinadas na aula 03).

```html
    <img src="foto.jpg" />
```

_Mostrar no navegador_

 Outro atributo extremamente importante para uma imagem é o ``alt``, seu valor é o texto que será exibido caso ocorra algum problema no carregamento da imagem, ou caso o usuário utilize um leitor de tela.

```html
    <img src="foto.jpg" alt="Margarida" />
```

_Mudar o caminho e mostrar no navegador_

Vale notar que a altura e largura da imagem no site, são exatamente as dimensões da imagem. Caso eu deseje mostrar a imagem maior ou menor do que ela é, podmeos utilizar as propriedades ``width`` (para a largura) e ``height`` para a altura. Caso eu defina apenas uma dessas propriedades, a outra será recalculada para manter a proporção.

## Vídeos
Para exibir um vídeo utilizamos a tag ``video``, esse elemento também possui as propriedades ``width`` e ``height``.
Uma boa prática ao trabalhar com o elemento ``video`` é ao invés de utilizar um atributo ``src`` para declarar o vídeo que será exibido, utilizar a tag ``source`` (que por sua vez possui o atributo ``src``) dentro de ``video``. Isso pois os tipos suportados de vídeo variam de navegador para navegador e a boa prática é oferecer varias versões do mesmo vídeo, em diferentes formatos. A primeira tag ``source`` que indique um vídeo em um formato válido para o navegador, é o vídeo que será renderizado. Também é interessante prover uma mensagem de texto avisando o usuário sobre o suporte de vídeo de seu navegador, que será renderizado caso não haja nenhum formato suportado nas tags ``sources``.
Para indicar ao navegador o formato de cada vídeo nas tags ``sources`` utilizamos o atributo ``type``.

_Mostrar lista completa de types de videos: http://www.iana.org/assignments/media-types/media-types.xhtml#video_

```html
    <video>
        <source src="video.mp4" type="video/mp4">
        Seu navegador não suporta o formato de vídeo oferecido.
    </video>
 ```

 Ao abrir nosso documento HTML podemos ver que nosso vídeo esta na página, mas não há como assistir ele, pois não tem nenhum botão. Para ativar os botões de controle, precisamos colocar o atributo ``controls`` no elemento ``video``.

 ```html
    <video controls>
        <source src="video.mp4" type="video/mp4">
        Seu navegador não suporta o formato de vídeo oferecido.
    </video>
 ```

 Agora sim, nosso vídeo esta funcionando perfeitamente.

 _Créditos vídeo https://www.pexels.com/pt-br/video/857010/_

 ## Áudios
Para exibir um áudio utilizamos a tag ``audio`` de forma similar a tag ``video``. Nesse elemento também utilizaremos a tag ``source`` para possibilitar oferecer diversos formatos.

_Mostrar lista completa de types de videos: http://www.iana.org/assignments/media-types/media-types.xhtml#audio_

```html
    <audio controls>
        <source src="audio.wav" type="audio/wav">
        Seu navegador não suporta o formato de áudio oferecido.
    </audio>
 ```

 _Créditos áudio https://freesound.org/people/Nox_Sound/sounds/522222/_

 ## Resumo
 Nessa aula aprendemos o básico para trabalhar com imagens, videos e áudios em nossos sites.


