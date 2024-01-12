# Documentacion Newsletters
## Check list antes de enviar
1. revisar __Asunto y preheader__
2. `alt` en todas las imágenes
3. Versión __mobile__
4. Versión __dark mode__
5. Revisar en __outlook__
6. Revisar en apple mail
7. Revisar en gmail
8. (esto no estoy seguro) en el html generado, borramos nuestros custom styles y pegamos de nuevo los que tenemos en la hoja de estilos master. Esto lo hago porque creo qeu al compilar el html elimina alguno.
<<<<<<< HEAD
9. Añadir __imagen pixel__ al final, justo antes del cierre de la etiuqeta `</body>`
`<img src="[%url:unique-count; 'https://mediaportal.stage-entertainment.com/m/6d0a01ed0be14042/original/1x1.gif']" alt="pixel" width="1" height="1" style="display:none;" />`
=======
9. Aañador __imagen pixel__ al final, justo antes del cierre de la etiuqeta `</body>`  
` <img src="[%url:unique-count; 'https://mediaportal.stage-entertainment.com/m/6d0a01ed0be14042/original/1x1.gif']" alt="pixel" width="1" height="1" style="display:none;" />`
>>>>>>> 431bf94ec1a7d0d836334a3c2d65d69b055380fe



## Custom Dark mode
1. Para hablitar el poder controlar el darkmode  añadir en header después de los otros `<metas>`:
```markdown
    <meta name="color-scheme" content="light dark">
    <meta name="supported-color-schemes" content="light dark">
```

2. Añadir estilos css al final de la etiqueta `<style>` del `<head>`
	(Código al final de la nota)

## Logo con dos versiones
1. Creamos la sección/estructura (tabla) con el logo normal con PNG con el fondo blanco (para que los darkmodes que no se pueden editar)
2. Añadimos al `<td>` que envuelve la imagen la clase `light-img`
3. Seleccionamos el `<tr>` que envuelve el <td> del punto anterior y lo duplicamos (esta será la versión darkmode del logo)
4. Añadir a ese `<tr>  class="dark-img" style="display: none;"`
5. Añadir al `<td>` de dentro lo siguiente `class="dark-img" style="display: none;"`
    
Esto lo que hace es lo siguiente:
Al añadir la clase `light-img` al contenedor de la versión light, esta ocutará esta imagnen en la versión dark
Al añadir `<tr>  class="dark-img" style="display: none;"` al conteniedor de la versión dark, esta versión estará oculta por defecto y solo será visible cuando el dispositivo esté en versión dark

## Forzar background y color en dark mode

Trabajamos normalente en versión light
Para forzar el background a un color se añade la clase correspondiente:
listado de clases con sus colores.

    .dark-bg-0          #000000
    .dark-bg-0-5        #0a0a0a
    .dark-bg-1          #111111
    .dark-bg-1-5        #1a1a1a
    .dark-bg-2          #222222
    .dark-bg-2-5        #2a2a2a
    .dark-bg-3          #333333
    .dark-bg-3-5        #3a3a3a
    .dark-bg-ald        #191629
    .dark-bg-oscuro-erl #4d2217 
    .dark-bg-ff         #ffffff
    .dark-bg-red-erl    #E74115 (rojo ERL)

Estás clases forzará por defecto el color del texto a un color claro.
Si quiere forzarse a un color concreto usar en el texto la clase de color:

    .dark-color-ff   #ffffff
    .dark-color-ee  #eeeeee !important;
    .dark-color-dd  #dddddd !important;
    }
    .dark-color-cc,
    .dark-color-cc * {
        color: #cccccc !important;
    }

    .dark-color-bb,
    .dark-color-bb * {
        color: #bbbbbb !important;
    }

    .dark-color-aa,
    .dark-color-aa * {
        color: #bbbbbb !important;
    }

    .dark-color-00,
    .dark-color-00 * {
        color: #000000 !important;
    }

    .dark-color-oscuro-erl,
    .dark-color-oscuro-erl * {
        color: #4d2217 !important;
    }

    .dark-color-yellow-ald,
    .dark-color-yellow-ald * {
        color: #ffd200 !important;
    }

    .dark-red-erl,
    .dark-red-erl * {
        color: #E74115 !important;
    }

    .dark-red-stage,
    .dark-red-stage * {
        color: #c9142f !important;
    }
<<<<<<< HEAD


## Botones

Especial atención en la versión outlook
Si en outlook no aparece la última línea revisar el height de esta versión
=======
>>>>>>> 431bf94ec1a7d0d836334a3c2d65d69b055380fe
