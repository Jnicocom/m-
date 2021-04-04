**m-** es una librería CSS/JS creada por [Jnico](https://twitter.com/Jnicocom "Jnico's Twitter") que facilita la maquetación de contenidos para la web de Movistar Colombia.

# ¿Qué necesitas crear?

- [x] [Botón](#botón "Botón")
- [x] [Carrusel](#carrusel "Carrusel")

------------

# Botón

Copia y pega la siguiente estructura para crear un botón:

```html
<div class="m-button" data-url="https://www.movistar.co" data-label="Botón [ingresa el texto del botón]">
    Ingresa el texto del botón
</div>
```

Luego, asigna el atributo `data-category` al padre inmediato `--buttons` del botón, por ejemplo:

```html
<div class="m-carousel__block --buttons" data-category="movistarco - home - carrusel">
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

* <ins>Debe</ins> crearse usando la etiqueta `<div>` como hijo inmediato de un `--buttons` con el atributo `data-category`.

* <ins>Debe</ins> asignarse el atributo `data-url` que define la ruta a la que dirige el botón.

* <ins>Debe</ins> asignarse el atributo `data-label` que define el label y el action del dataLayer.

* Puede asignarse el atributo `data-target` que define cómo será cargada la página al dar clic. `_self` por defecto.

##### Estilo

**&rsaquo; `--white`** modifica el fondo del botón a blanco con letra azul oscuro.

**&rsaquo; `--white-2`** modifica el fondo del botón a blanco con letra y borde azul oscuro.

**&rsaquo; `--white-3`** modifica el fondo del botón a blanco con letra y borde azul claro.

**&rsaquo; `--sky-blue`** modifica el fondo del botón a azul claro con letra blanca.

**&rsaquo; `--sky-blue-2`** modifica el fondo del botón a azul claro con letra y borde blanco.

------------

# Carrusel

Copia y pega la siguiente estructura para crear un carrusel e incluir un banner:

```html
<div class="m-carousel">
    <div class="m-carousel__banner">
        <div class="m-carousel__block --hero">
            <div class="m-carousel__text">
                Ingresa el copy secundario del banner
            </div>
            <div class="m-carousel__text">
                Ingresa el copy primario del banner y usa br <br>
                para añadir saltos de línea
            </div>
            <div class="m-carousel__block">
                <img class="m-carousel__bullet" src="" alt="">
            </div>
            <div class="m-carousel__block">
                <div class="m-carousel__block">
                    <a class="m-carousel__button">Botón 1</a>
                    <a class="m-carousel__button">Botón 2</a>
                </div>
                <span class="m-carousel__text --smaller">
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
| [Banner](#banner-carousel "Banner") | m-carousel__banner |
| [Block](#block-carousel "Block") | m-carousel__block |
| [Text](#text-carousel "Text") | m-carousel__text |
| [Bullet](#bullet-carousel "Bullet") | m-carosule__bullet |

------------

### Carousel

**&rsaquo; `m-carousel`** crea un carrusel.

* <ins>Debe</ins> contener exclusivamente `m-carousel__banner`.

##### Tamaño

**&rsaquo; `--small`** reduce la altura del carrusel y ajusta sus elementos.

##### Desarrollo

**&rsaquo; `--debug`** habilita el modo debug.

------------

### Banner (carousel)

**`m-carousel__banner`** crea un banner.

* <ins>Debe</ins> crearse como hijo inmediado de un `m-carousel`.

------------

### Block (carousel)

**&rsaquo; `m-carousel__block`** crea un bloque.

* <ins>Debe</ins> crearse como hijo inmediado de un `m-carousel__banner`.

##### Plantilla

**&rsaquo; `--hero`** modifica el bloque para la inclusión exclusiva de copys primarios y secundarios.

* <ins>Debe</ins> contener únicamente `m-carousel__text` hasta un máximo de dos.

> Si existe un único `m-carousel__text` este será el copy primario.

```html
<div class="m-carousel__block --hero">
  <div class="m-carousel__text">
      Copy primario
  </div>
</div>
```

> Si existen dos `m-carousel__text` el primero será el copy secundario y el segundo el primario.

```html
<div class="m-carousel__block --hero">
  <div class="m-carousel__text">
      Copy secundario
  </div>
  <div class="m-carousel__text">
      Copy primario
  </div>
</div>
```

**&rsaquo; `--buttons`** modifica el bloque para la inclusión exclusiva de botones.

* **Debe** contener únicamente `m-button` hasta un máximo de dos.

------------

### Text (carousel)

**&rsaquo; `m-carousel__text`** crea un texto.

##### Tamaño

**&rsaquo; `--smaller`** reduce el tamaño de la letra al máximo.

**&rsaquo; `--small`** reduce el tamaño de la letra.

**&rsaquo; `--medium`** aumenta el tamaño de la letra.

**&rsaquo; `--large`** aumenta el tamaño de la letra.

**&rsaquo; `--larger`** aumenta el tamaño de la letra al máximo.

##### Peso (grosor)

**&rsaquo; `--lighter`** reduce el peso de la letra al máximo.

**&rsaquo; `--normal`** aumenta el peso de la letra.

**&rsaquo; `--bold`** aumenta el peso de la letra al máximo.

------------

### Bullet (carousel)

**&rsaquo; `m-carousel__bullet`** crea un bullet.

* <ins>Debe</ins> crearse usando la etiqueta `<img>`.

##### Tamaño

**&rsaquo; `--medium`** aumenta el tamaño de la imagen.

##### Posición

**&rsaquo; `--start`** desplaza la imagen hacia la izquierda.

**&rsaquo; `--end`** desplaza la imagen hacia la derecha.
