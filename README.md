**m-** es una librería CSS/JS creada por [Jnico](https://twitter.com/Jnicocom "Jnico's Twitter") que facilita la maquetación de contenidos para la web de Movistar Colombia.

# ¿Qué necesitas crear?

- [x] [Botón](#botón "Botón")
- [x] [Carrusel](#carrusel "Carrusel")

------------

# Botón

Usa la siguiente estructura para crear un botón:

```html
<div class="m-button" data-href="https://www.movistar.co" data-label="[Texto del botón]">
    Texto del botón
</div>
```

Luego, asigna el atributo `data-category` al padre inmediato `m--buttons` del botón, por ejemplo:

```html
<div class="m-carousel__block m--buttons" data-category="movistarco - home - carrusel">
    //m-button
</div>
```

### Elementos de un botón

| Nombre | Clase |
| :------------ | :------------ |
| [Button](#button "Button") | m-button |

------------

### Button

**&rsaquo; `m-button`** crea un botón.

* <ins>Debe</ins> crearse usando la etiqueta `<div>` como hijo inmediato de un `m--buttons` con el atributo `data-category`.

* <ins>Debe</ins> asignarse el atributo `data-href` que define la ruta a la que dirige el botón.

* <ins>Debe</ins> asignarse el atributo `data-label` que define el label y el action del dataLayer.

* Puede asignarse el atributo `data-target` que define cómo será cargada la página al dar clic. `_self` por defecto.

##### Estilo

**&rsaquo; `m--white`** modifica el fondo del botón a blanco con texto azul oscuro.

**&rsaquo; `m--white-2`** modifica el fondo del botón a blanco con texto y borde azul oscuro.

**&rsaquo; `m--white-3`** modifica el fondo del botón a blanco con texto y borde azul claro.

**&rsaquo; `m--blue-light`** modifica el fondo del botón a azul claro con texto blanco.

**&rsaquo; `m--blue-light-2`** modifica el fondo del botón a azul claro con texto y borde blanco.

------------

# Carrusel

Usa la siguiente estructura para crear un carrusel e incluir un slide:

```html
<div class="m-carousel">
    <div class="m-carousel__slide">
        <div class="m-carousel__block m--hero">
            <div class="m-carousel__text">
                Ingresa el copy secundario del slide
            </div>
            <div class="m-carousel__text">
                Ingresa el copy primario del slide y usa br <br>
                para añadir saltos de línea
            </div>
            <div class="m-carousel__block">
                <img class="m-carousel__bullet" src="" alt="">
            </div>
            <div class="m-carousel__block">
                <div class="m-carousel__block m--buttons" data-category="movistarco - home - carrusel">
                    <div class="m-button" data-href="https://www.movistar.co" data-label="[Texto del botón]">Texto del botón</div>
                    <div class="m-button" data-href="https://www.movistar.co" data-label="[Texto del botón]">Texto del botón</div>
                </div>
                <span class="m-carousel__text m--smaller">
                    Aplican términos y condiciones
                </span>
            </div>
        </div>
    </div>
</div>
```

### Elementos de un carrusel

| Nombre | Clase |
| :------------ | :------------ |
| [Carousel](#carousel "Carousel") | m-carousel |
| [Slide](#slide-carousel "Slide") | m-carousel__slide |
| [Block](#block-carousel "Block") | m-carousel__block |
| [Text](#text-carousel "Text") | m-carousel__text |
| [Bullet](#bullet-carousel "Bullet") | m-carosule__bullet |

------------

### Carousel

**&rsaquo; `m-carousel`** crea un carrusel.

* <ins>Debe</ins> contener exclusivamente `m-carousel__slide`.

##### Tamaño

**&rsaquo; `m--small`** reduce la altura del carrusel y ajusta sus elementos.

##### Utilidad

**&rsaquo; `m--custom-slick`** habilita la creación de un slick personalizado, por ejemplo:

```html
<div class="m-carousel m--custom-slick --mi-carrusel">
    <!-- m-carousel__slider -->
</div>

<script>
    $('.--mi-carrusel').slick({
        //...
    });
</script>
```

**&rsaquo; `m--debug`** habilita el modo debug.

------------

### Slide (carousel)

**`m-carousel__slide`** crea un slide.

* <ins>Debe</ins> crearse como hijo inmediado de un `m-carousel`.

> Cada `m-carousel__slide` y su modificador personalizado posee un wrap de forma automática, por ejemplo:

```html
<div class="m-carousel__slide-wrap --mi-modificador-personalizado-wrap"> <!-- wraps automåticos -->
    <div class="m-carousel__slide --mi-modificador-personalizado">
        //m-carousel__block
    </div>
</div>
```

------------

### Block (carousel)

**&rsaquo; `m-carousel__block`** crea un bloque.

* <ins>Debe</ins> crearse como hijo inmediado de un `m-carousel__slide`.

##### Plantilla

**&rsaquo; `m--hero`** modifica el bloque para la inclusión exclusiva de copys primarios y secundarios.

* <ins>Debe</ins> contener únicamente `m-carousel__text` hasta un máximo de dos.

> Si existe un único `m-carousel__text` este será el copy primario.

```html
<div class="m-carousel__block m--hero">
    <div class="m-carousel__text">
        Copy primario
    </div>
</div>
```

> Si existen dos `m-carousel__text` el primero será el copy secundario y el segundo el primario.

```html
<div class="m-carousel__block m--hero">
    <div class="m-carousel__text">
        Copy secundario
    </div>
    <div class="m-carousel__text">
        Copy primario
    </div>
</div>
```

**&rsaquo; `m--buttons`** modifica el bloque para la inclusión exclusiva de botones.

* **Debe contener únicamente `m-button` hasta un máximo de dos.

------------

### Text (carousel)

**&rsaquo; `m-carousel__text`** crea un texto.

##### Estilo

**&rsaquo; `m--blue-light`** modifica el color del texto a azul claro.

**&rsaquo; `m--blue-dark`** modifica el color del texto a azul oscuro.

**&rsaquo; `m--gray-dark`** modifica el color del texto a gris oscuro.

##### Tamaño

**&rsaquo; `m--smaller`** reduce el tamaño del texto al máximo.

**&rsaquo; `m--small`** reduce el tamaño del texto.

**&rsaquo; `m--medium`** aumenta el tamaño del texto.

**&rsaquo; `m--large`** aumenta el tamaño del texto.

**&rsaquo; `m--larger`** aumenta el tamaño del texto al máximo.

##### Peso (grosor)

**&rsaquo; `m--lighter`** reduce el peso del texto al máximo.

**&rsaquo; `m--normal`** aumenta el peso del texto.

**&rsaquo; `m--bold`** aumenta el peso del texto al máximo.

##### Alineación

**&rsaquo; `m--right`** alinea el texto a la derecha.

**&rsaquo; `m--left`** alinea el texto a la izquierda.

------------

### Bullet (carousel)

**&rsaquo; `m-carousel__bullet`** crea un bullet.

* <ins>Debe</ins> crearse usando la etiqueta `<img>`.

##### Tamaño

**&rsaquo; `m--medium`** aumenta el tamaño de la imagen.

##### Posición

**&rsaquo; `m--end`** desplaza la imagen hacia la derecha.

**&rsaquo; `m--start`** desplaza la imagen hacia la izquierda.
