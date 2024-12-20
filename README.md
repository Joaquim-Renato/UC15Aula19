# WEB Responsividade:

O que são Media Queries?

Pra que serve? 

Media queries são regras no CSS que permitem aplicar estilos diferentes dependendo de características do dispositivo em que o conteúdo está sendo visualizado, como a largura da tela, a resolução, a orientação (retrato ou paisagem), entre outras.

----
Uma boa estratégia/prática é criar um arquivo `media.css` onde devemos centralizar as informações de media queries; 
Só devemos incluir o link href no nosso html;
## Operadores Lógicos:
Em media queries permitem criar condições mais complexas para aplicar estilos

`not`
Inverte uma condição. Os estilos serão aplicados quando a condição não for verdadeira.
Exemplo:
``````CSS
@media not (min-width: 768px) {
    body {
        background-color: lightblue; /* Aplica em telas menores que 768px */
    }
}
``````
`and`
Combina múltiplas condições, todas devem ser verdadeiras para aplicar os estilos.
Exemplo:
``````CSS


@media (min-width: 768px) and (orientation: landscape) {
    body {
        background-color: lightgreen; /* Aplica em telas acima de 768px em modo paisagem */
    }
}
``````
`only`

Restringe a aplicação apenas para dispositivos que suportam as condições especificadas. Útil para evitar que navegadores mais antigos interpretem incorretamente.
Exemplo:
``````CSS
@media only screen and (max-width: 480px) {
    body {
        background-color: pink; /* Aplica apenas em telas menores que 480px */
    }
}
``````
----

## Principais Operadores Relacionais:

`min-width` e `max-width`
Usados para definir um intervalo de larguras da tela em que os estilos devem ser aplicados.

``````CSS
/* Estilos para telas com largura mínima de 768px */
@media (min-width: 768px) {
    body {
        background-color: lightblue;
    }
}

/* Estilos para telas com largura máxima de 480px */
@media (max-width: 480px) {
    body {
        background-color: lightpink;
    }
}

/* Estilos para telas entre 481px e 1024px */
@media (min-width: 481px) and (max-width: 1024px) {
    body {
        background-color: lightgreen;
    }
}
``````
`min-height` e `max-height`
Usados para definir estilos baseados na altura da tela.

``````CSS
/* Estilos para telas com altura mínima de 600px */
@media (min-height: 600px) {
    body {
        font-size: 18px;
    }
}

/* Estilos para telas com altura máxima de 400px */
@media (max-height: 400px) {
    body {
        font-size: 14px;
    }
}

``````
`orientation`
Especifica estilos com base na orientação do dispositivo (paisagem ou retrato).

``````CSS
/* Estilos para orientação paisagem */
@media (orientation: landscape) {
    body {
        background-color: lightcoral;
    }
}

/* Estilos para orientação retrato */
@media (orientation: portrait) {
    body {
        background-color: lightgoldenrodyellow;
    }
}

``````
`aspect-ratio`
Define estilos com base na proporção entre largura e altura.

``````CSS
/* Estilos para telas com proporção maior que 16:9 */
@media (min-aspect-ratio: 16/9) {
    body {
        background-color: lightgray;
    }
}

/* Estilos para telas com proporção menor que 4:3 */
@media (max-aspect-ratio: 4/3) {
    body {
        background-color: lavender;
    }
}

``````

`resolution`
Define estilos com base na densidade de pixels (usado principalmente para dispositivos de alta resolução)

``````````CSS
/* Estilos para dispositivos com resolução mínima de 150dpi */
@media (min-resolution: 150dpi) {
    img {
        border: 2px solid red;
    }
}

/* Estilos para dispositivos com resolução máxima de 1.5dppx */
@media (max-resolution: 1.5dppx) {
    img {
        border: 2px solid blue;
    }
}

``````````

Combinação de Operadores
Você pode combinar vários operadores para criar condições mais específicas.

Exemplo:

``````````CSS
/* Estilos para telas entre 600px e 1200px de largura em modo paisagem */
@media (min-width: 600px) and (max-width: 1200px) and (orientation: landscape) {
    body {
        font-size: 20px;
        background-color: lightsteelblue;
    }
}
``````````
### Boas refs 

https://developer.mozilla.org/pt-BR/docs/Web/CSS/CSS_media_queries/Using_media_queries

https://www.devmedia.com.br/utilizando-css-media-queries/27085
