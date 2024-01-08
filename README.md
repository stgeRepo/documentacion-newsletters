# Documentacion Newsletters
## Custom Dark mode
1. Para hablitar el poder controlar el darkmode  añadir en header después de los otros `<metas>`:
```markdown
    <meta name="color-scheme" content="light dark">
    <meta name="supported-color-schemes" content="light dark">
```

2. Añadir estilos css al final de la etiqueta `<style>` del `<head>`
	(Código al final de la nota)

##Logo con dos versiones
1. Creamos la sección/estructura (tabla) con el logo normal con PNG con el fondo blanco (para que los darkmodes que no se pueden editar)
2. Añadimos al `<td>` que envuelve la imagen la clase `light-img`
3. Seleccionamos el `<tr>` que envuelve el <td> del punto anterior y lo duplicamos (esta será la versión darkmode del logo)
4. Añadir a ese `<tr>  class="dark-img" style="display: none;"`
5. Añadir al `<td>` de dentro lo siguiente `class="dark-img" style="display: none;"`
    
Esto lo que hace es lo siguiente:
Al añadir la clase `light-img` al contenedor de la versión light, esta ocutará esta imagnen en la versión dark
Al añadir `<tr>  class="dark-img" style="display: none;"` al conteniedor de la versión dark, esta versión estará oculta por defecto y solo será visible cuando el dispositivo esté en versión dark
