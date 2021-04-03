m- es una librería CSS/JS que facilita la maquetación de contenidos en la web de Movistar Colombia.

# Carrusel

Copia y pega la siguiente estructura para crear un carrusel con un banner:

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
------------
### Elementos de un carrusel

| Nombre | Clase |
| :------------ | :------------ |
| [Carousel](#carousel "Carousel") | m-carousel |
| [Banner](#banner "Banner") | m-carousel__banner |
| [Block](#block "Block") | m-carousel__block |
| [Text](#text "Text") | m-carousel__text |

------------

### Carousel

**`m-carousel` crea un carrusel.**

**&rsaquo; `m-carousel--small` reduce la altura del carrusel y ajusta sus elementos.**

------------

### Banner

**`m-carousel__banner` crea un banner.**

* Debe ser iniciado dentro de un `m-carousel` como hijo inmediato.

------------

### Bloque

**`m-carousel__block` crea un bloque.**

* Debe ser iniciado dentro de un `m-carousel__banner` como hijo inmediato.

**&rsaquo; `m-carousel__block--hero` modifica un bloque para la inclusión exclusiva de *copys* primarios y secundarios.**

* Dentro deben crearse únicamente `m-carousel__text` hasta un máximo de dos.

* Si existe un único `m-carousel__text` este será el copy primario.

```html
<div class="m-carousel__block">
  <div class="m-carousel__text">
      Copy primario
  </div>
</div>
```

* Si existen dos `m-carousel__text` el primero será el copy secundario y el segundo el primario.

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

**&rsaquo; `m-carousel__block--buttons` modifica un bloque para la inclusión exclusiva de botones.**

------------

#### Text

**`m-carousel__text` inicia un texto.**

**&rsaquo; `m-carousel__block--hero` modifica un bloque para la inclusión exclusiva de *copys* primarios y secundarios.**

**&rsaquo; `m-carousel__block--buttons` modifica un bloque para la inclusión exclusiva de botones.**
