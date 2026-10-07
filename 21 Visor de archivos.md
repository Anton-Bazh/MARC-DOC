# Visor de archivos

Los enlaces de una página a **PDF, textos y otros archivos de la wiki** se abren **aparte**, sin dejar la página: puedes leer el manual mientras sigues en la wiki. Está en **E** y en **M**.

## Pruébalo aquí

Estos enlaces abren un PDF de 8 páginas donde cada página dice en grande **"Página N"**:

- [Manual de prueba completo](assets/pruebas/manual-de-prueba.pdf)
- [Manual de prueba en la página 3](assets/pruebas/manual-de-prueba.pdf#page=3)
- [Manual de prueba en la página 6](assets/pruebas/manual-de-prueba.pdf#page=6)
- [Notas de prueba en texto](assets/pruebas/notas-de-prueba.txt)

Si el enlace "página 3" muestra **Página 3**, el visor llegó al lugar exacto.

## Cómo se abre en cada edición

| Edición | Ventana | Formatos |
|---|---|---|
| **E** | Una ventana aparte que mueves y cambias de tamaño junto a MARC. Se **reutiliza**: el siguiente enlace se abre en la misma | PDF (con su índice, búsqueda y zoom), texto, imágenes y lo que el navegador integrado sabe mostrar |
| **M** | **Ventana flotante** (como un teléfono encima de MARC) o **pantalla dividida** (MARC a un lado, el visor al otro) | PDF (desplazamiento continuo, zoom con dos dedos, contador `3 / 8`) y textos (`.txt`, `.md`, `.csv`, `.json`, `.yaml`, `.log`) |

Ambas son de **solo lectura**: el visor nunca modifica el archivo. Si el tipo aún no se puede mostrar, M lo dice: *"Este tipo de archivo llegará al visor más adelante."*

## Flotante o pantalla dividida (M)

MARC funciona desde **Android 8**. La pantalla dividida existe en todas las tabletas; la ventana flotante, solo en algunas (por ejemplo Huawei, Samsung y Android recientes). En **Ajustes → Apariencia → Visor de archivos**:

| Opción | Qué hace |
|---|---|
| **Automático** | Flotante si la tableta lo permite; si no, pantalla dividida |
| **Ventana flotante** | Siempre flotante |
| **Pantalla dividida** | Siempre al lado de MARC |

Si tu tableta no tiene ventanas flotantes, el ajuste solo dice *"Este dispositivo no tiene ventanas flotantes: el visor se abre en pantalla dividida."* La ventana del visor se mueve, se agranda y se cierra con los controles del propio sistema.

## Escribir enlaces a archivos

```markdown
[Manual](anexos/manual.pdf)            abre el PDF desde el principio
[Manual, pág. 3](anexos/manual.pdf#page=3)   abre en la página 3
[Datos](anexos/datos.csv)              abre el texto
```

- La ruta es **relativa a la página** (como en [[05 Cómo escribir tu documentación]]). Si el nombre tiene espacios, escríbelos como `%20`.
- `#page=N` elige la página del PDF.
- El archivo tiene que estar **dentro de la wiki** (y, en una wiki con Git, publicado).

## Enlaces a un `.marc`

Un enlace a un archivo `.marc` no abre el visor: abre ese `.marc` **como wiki**, desde una **copia**. Así puedes editarlo y guardar sin tocar la wiki de donde salió. Así funciona la [[22 Practica las funciones|wiki de práctica]] de esta documentación.

> [!note] Lo que viene
> Ver las páginas `.md` con formato y documentos de Word en el visor llegará en próximas versiones.
