# El Hub

El Hub es la pantalla principal de la app — lo primero que ves siempre al abrirla. Muestra **una tarjeta por cada repositorio conectado**, no una tarjeta por página: la idea es que elijas primero *qué wiki* quieres leer, y luego navegues dentro de ella.

## Qué trae cada tarjeta

- **Nombre** del repositorio o carpeta, y su **dueño** de GitHub si viene de ahí (ej. `tu-equipo / wiki-interna`) — las carpetas locales (ver [[01 Conectar tu primer repositorio]]) muestran un ícono de carpeta en vez del de GitHub, y no tienen dueño.
- **Cantidad de páginas** que tiene esa wiki.
- **Última actualización**, en fecha relativa ("hoy", "hace 3 días", "hace 2 meses") — la fecha del último commit real, si el repositorio (o la carpeta local con su propio Git) la tiene.
- Un indicador **activo** (punto verde) si esa es la wiki que se está sirviendo en este momento.

Pulsa cualquier tarjeta para abrir esa wiki. Si no era la activa, la app la sincroniza y la vuelve la activa automáticamente.

## Buscador del Hub

La caja de búsqueda del Hub no solo filtra por el nombre del repositorio — también busca dentro de los **títulos de todas sus páginas**. Así, si escribes "arquitectura" y ningún repositorio se llama así, pero uno de ellos tiene una página titulada "Arquitectura del sistema", esa tarjeta va a aparecer igual.

> [!tip]
> Esto es útil cuando tienes varios repositorios conectados y no recuerdas en cuál vive cierto tema.

## Si todavía no conectaste nada

El Hub te lo dice claramente y te ofrece el botón para conectar tu primer repositorio — ver [[01 Conectar tu primer repositorio]].

## Siguiente paso

Una vez dentro de una wiki, [[03 Navegar la wiki]] explica cómo moverte, buscar y cambiar de tema.
