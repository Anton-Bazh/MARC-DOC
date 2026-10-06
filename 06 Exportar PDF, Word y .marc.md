# Exportar PDF, Word y .marc

MARC puede entregar cualquier wiki conectada en tres formatos. Todo se genera **en tu equipo o tableta, sin conexión**: tu documentación no se sube a ningún servicio para convertirla.

| Formato | Para qué sirve | Escritorio | Móvil |
|---|---|---|---|
| **PDF** | Leer, imprimir o enviar una versión cerrada, que se ve igual en todas partes | Más opciones → **Descargar PDF** | Descargar → **Esta página** o **Wiki completa** |
| **Word (.docx)** | Entregar un documento que otra persona pueda **editar** en Word, WPS, LibreOffice o Google Docs | Más opciones → **Descargar Word** | Descargar → **Word** |
| **.marc** | Pasar la wiki completa a otra persona o dispositivo en un solo archivo, para abrirla en MARC | Más opciones → **Exportar .marc** | Descargar → **Formato portable** |

## PDF

El PDF incluye una **portada** con el nombre de la wiki y sus cifras (páginas, diagramas, gráficas, fórmulas), un **índice** clicable, cada página de la wiki en hoja nueva con su título en la cabecera, y el número de página al pie.

- Diagramas Mermaid y React Flow, gráficas, fórmulas, iconos e imágenes se dibujan igual que en la wiki.
- Un diagrama muy ancho va en una **hoja apaisada** propia, para que su texto no quede diminuto.
- Los PDF que tu documentación enlaza (adjuntos) se incluyen completos al final, como **Anexos**.
- Si un diagrama o gráfica tiene un error de sintaxis, el PDF muestra un recuadro con el motivo **y su código completo**: nada se pierde.

Al terminar verás un **reporte**: enlaces a notas que no existen, imágenes convertidas, adjuntos incluidos. Es informativo; el PDF siempre se genera.

## Word (.docx)

Al descargar, MARC te pregunta **cómo quieres las gráficas y fórmulas**:

| | Como imagen | Editables |
|---|---|---|
| Gráficas | Imagen, igual que en la wiki | **Gráficas de Word**: barras, columnas, líneas, área, pastel, dona, radar, dispersión, burbujas y combinadas. Sus datos se editan en Excel |
| Fórmulas | Imagen nítida | **Ecuaciones de Word**, editables con su editor de ecuaciones |
| Se ve igual en | Word, WPS, LibreOffice y Google Docs | Word y LibreOffice (Google Docs y WPS también las abren) |

Tablas, listas, texto, bloques de código y avisos son **editables en los dos modos**. MARC recuerda tu elección para la próxima vez.

Lo que Word no admite se **adapta en el documento**, sin quitar nada de tu wiki:

| Elemento | En Word |
|---|---|
| Diagramas Mermaid y React Flow | Imagen nítida, con la misma letra que en MARC |
| Diagrama muy ancho | Hoja apaisada propia, como en el PDF |
| Índice | Índice propio y clicable al inicio |
| PDF adjuntos | Su título y un aviso: Word no puede insertar páginas de un PDF; el contenido completo está en la exportación PDF |
| Gráfica sin equivalente en Word (por ejemplo `polarArea`) | En modo editable queda como imagen y la ventana te lo indica |

> [!tip] ¿Cuál elijo?
> **Como imagen** si vas a enviar el documento y quieres que se vea exactamente igual en cualquier programa. **Editables** si la otra persona va a trabajar sobre las gráficas o las fórmulas.

## .marc

Un `.marc` es la wiki completa en un solo archivo: páginas, imágenes y adjuntos. Quien lo reciba lo abre en MARC (escritorio o móvil) y la lee al instante, sin conexión. Ver [[07 El formato .marc]].

## Dónde se guardan

- **Escritorio:** en tu carpeta de descargas, como cualquier descarga del navegador.
- **Móvil:** en la carpeta `MARC` de tu almacenamiento: `MARC/PDF`, `MARC/Word` y `MARC/Paquetes .marc`. Si vuelves a exportar la misma wiki el mismo día, el archivo se reemplaza. Ver [[08 MARC en tabletas y teléfonos]].
