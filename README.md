# Responsividade:

O que são Media Queries?

Pra que serve? 

Media queries são regras no CSS que permitem aplicar estilos diferentes dependendo de características do dispositivo em que o conteúdo está sendo visualizado, como a largura da tela, a resolução, a orientação (retrato ou paisagem), entre outras.

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