**m-** es una librería CSS/JS que facilita la maquetación de contenidos para la web de Movistar Colombia.

# Carrusel

Copia y pega la siguiente estructura para crear un carrusel e incluir un banner:

```html
<div class="m-carousel">
    <div class="m-carousel__banner">
        <div class="m-carousel__block m-carousel__block--hero">
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
                <span class="m-carousel__text m-carousel__text--extra-small">
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
| [Button](#button-carousel "Button") | m-carousel__button |

------------

### Carousel

**&rsaquo; `m-carousel`** crea un carrusel.

* Debe contener exclusivamente `m-carousel__banner`.

##### Tamaño

**&rsaquo; `--small`** reduce la altura del carrusel y ajusta sus elementos.

##### Desarrollo

**&rsaquo; `--debug`** habilita el modo debug.

------------

### Banner (carousel)

**`m-carousel__banner`** crea un banner.

* Debe crearse como hijo inmediado de un `m-carousel`.

------------

### Block (carousel)

**&rsaquo; `m-carousel__block`** crea un bloque.

* Debe crearse como hijo inmediado de un `m-carousel__banner`.

##### Plantilla

**&rsaquo; `--hero`** modifica el bloque para la inclusión exclusiva de copys primarios y secundarios.

* Debe contener únicamente `m-carousel__text` hasta un máximo de dos.

> Si existe un único `m-carousel__text` este será el copy primario.

```html
<div class="m-carousel__block">
  <div class="m-carousel__text">
      Copy primario
  </div>
</div>
```

> Si existen dos `m-carousel__text` el primero será el copy secundario y el segundo el primario.

```html
<div class="m-carousel__block">
  <div class="m-carousel__text">
      Copy secundario
  </div>
  <div class="m-carousel__text">
      Copy primario
  </div>
</div>
```

**&rsaquo; `--buttons`** modifica el bloque para la inclusión exclusiva de botones.

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

* Debe crearse usando la etiqueta `<img>`.

##### Tamaño

**&rsaquo; `--medium`** aumenta el tamaño de la imagen.

##### Posición

**&rsaquo; `--right`** desplaza la imagen hacia la derecha.

**&rsaquo; `--left`** desplaza la imagen hacia la izquierda.

------------

### Button (carousel)

**&rsaquo; `m-carousel__button`** crea un botón.

* Debe crearse usando la etiqueta `<a>`.

##### Color

**&rsaquo; `--white`** modifica el color del botón a blanco con letra azul oscuro.
