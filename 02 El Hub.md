# El Hub

El Hub es la pantalla principal de la app — lo primero que ves siempre al abrirla. Muestra **una tarjeta por cada repositorio conectado**, no una tarjeta por página: la idea es que elijas primero *qué wiki* quieres leer, y luego navegues dentro de ella.

## Qué trae cada tarjeta

- **Nombre y dueño** del repositorio (ej. `tu-equipo / wiki-interna`).
- **Cantidad de páginas** que tiene esa wiki.
- **Última actualización**, en fecha relativa ("hoy", "hace 3 días", "hace 2 meses") — la fecha del último commit real en el repositorio.
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
