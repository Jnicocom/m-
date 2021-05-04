**m-** es una librería CSS/JS creada por [Jnico](https://twitter.com/Jnicocom "Jnico's Twitter") que facilita la maquetación de contenidos para la web de Movistar Colombia.

# ¿Qué necesitas crear?

- [x] [Botón](#botón "Botón")
- [x] [Carrusel](#carrusel "Carrusel")
- [x] Tab (próximamente)
- [x] Modal (próximamente)
- [x] Acordión (próximamente)
- [x] Descubre API (próximamente)

------------

# Botón

Usa la siguiente estructura para crear un botón:

```html
<a class="m-button" href="#" data-layer-copy="Texto del botón">
    Texto del botón
</a>
```

###### Elementos de un botón

| Nombre | Clase |
| :------------ | :------------ |
| [Button](#button "Button") | m-button |

###### Modificadores de un botón

| Nombre | Clase |
| :------------ | :------------ |
| [Template](#template "Template") | m--template |
| [Icon](#icon "Icon") | m--icon |

------------

#### Button (elemento)

**&rsaquo; `m-button`** crea un botón.

* <ins>Debe</ins> crearse usando la etiqueta `<a>`.

* <ins>Debe</ins> asignarse el atributo `data-layer-copy` que es igual al texto del botón.

#### Template (modificador)

**&rsaquo; `m--template-white`** modifica el fondo del botón a blanco con texto azul oscuro.

**&rsaquo; `m--template-white-2`** modifica el fondo del botón a blanco con texto y borde azul oscuro.

**&rsaquo; `m--template-white-3`** modifica el fondo del botón a blanco con texto y borde azul claro.

**&rsaquo; `m--template-blue-light`** modifica el fondo del botón a azul claro con texto blanco.

**&rsaquo; `m--template-blue-light-2`** modifica el fondo del botón a azul claro con texto y borde blanco.

**&rsaquo; `m--template-green-light`** modifica el fondo del botón a verde claro con texto blanco.

#### Icon (modificador)

**&rsaquo; `m--icon-call-center`** añade el ícono "call center" al botón.

**&rsaquo; `m--icon-phone`** añade el ícono "phone" al botón.

#### Icon position (modificador)

**&rsaquo; `m--icon-position-end`** desplaza el ícono hacia la derecha del botón.

------------

# Carrusel

Usa la siguiente estructura para crear un carrusel e incluir un slide:

```html
<div class="m-carousel">
    <div class="m-carousel__slide">
        <div class="m-carousel__block m--hero">
            <div class="m-carousel__text">
                Copy secundario del slide
            </div>
            <div class="m-carousel__text">
                Copy primario del slide; usa br <br>
                para añadir saltos de línea
            </div>
        </div>
        <div class="m-carousel__block">
            <img class="m-carousel__bullet" src="" alt="">
        </div>
        <div class="m-carousel__block">
            <div class="m-carousel__block m--buttons" data-category="movistarco - home - carrusel">
                <a class="m-button" href="#" data-layer-copy="Texto del botón">Texto del botón</a>
            </div>
            <span class="m-carousel__text m--smaller">
                Aplican términos y condiciones
            </span>
        </div>
    </div>
</div>
```

###### Elementos de un carrusel

| Elemento | Clase |
| :------------ | :------------ |
| [Carousel](#carousel "Carousel") | m-carousel |
| [Slide](#slide-carousel "Slide") | m-carousel__slide |
| [Block](#block-carousel "Block") | m-carousel__block |
| [Text](#text-carousel "Text") | m-carousel__text |
| [Bullet](#bullet-carousel "Bullet") | m-carousel__bullet |
| [Callback](#callback-carousel "Callback") | m-carousel__callback |

------------

#### Carousel (elemento)

**&rsaquo; `m-carousel`** crea un carrusel.

* <ins>Debe</ins> contener exclusivamente `m-carousel__slide`.

###### Modificadores de m-carrusel

| Modificador | Clase |
| :------------ | :------------ |
| [Template](#template "Template") | m--template |
| [Size](#size "Size") | m--size |
| [Debug](#debug "Debug") | m--debug |

#### Template (modificador)

**&rsaquo; `m--template-custom-slick`** habilita la creación de un slick personalizado, por ejemplo:

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

#### Size (modificador)

**&rsaquo; `m--size-small`** reduce la altura del carrusel y ajusta sus elementos.

#### Debug (modificador)

**&rsaquo; `m--debug`** habilita el modo debug.

------------

### Slide (elemento de mcarousel)

**&rsaquo; `m-carousel__slide`** crea un slide.

* <ins>Debe</ins> crearse como hijo inmediado de un `m-carousel`.

> Cada `m-carousel__slide` y su modificador personalizado posee un wrap de forma automática, por ejemplo:

```html
<div class="m-carousel__slide-wrap --mi-modificador-personalizado-wrap"> <!-- wraps automåticos -->
    <div class="m-carousel__slide --mi-modificador-personalizado">
        <!-- m-carousel__block -->
    </div>
</div>
```

------------

### Block (carousel)

**&rsaquo; `m-carousel__block`** crea un bloque.

* <ins>La primera instancia debe</ins> crearse como hijo inmediado de un `m-carousel__slide`.
* Puede contener otros `m-carousel__block`.

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

* <ins>Debe</ins> contener únicamente `m-button` hasta un máximo de dos.

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

------------

### Callback (carousel)

**&rsaquo; `m-carousel__callback`** crea un callback.

* <ins>Debe</ins> crearse usando la etiqueta `<iframe>`.
