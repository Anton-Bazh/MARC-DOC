---
title: Portada
---

![MARC — Margaret, la abeja de MARC](assets/logo.png){ width="140" }

# MARC

### Markdown Automatizado por Repo y Consulta

`EN2.0.1` · `E2.2.3` · `M2.7.3`

---

**MARC** es una herramienta para leer, consultar y compartir la documentación técnica de tu equipo **tal como vive en sus archivos Markdown** — en un repositorio de Git, en una carpeta de tu equipo o en un paquete `.marc` — sin depender de un servicio en la nube y sin perder el formato con el que la escribiste.

Empezó como una aplicación de escritorio ligera. Desde la versión 2 es una **familia de ediciones** que comparten motor y formato:

| | **EN** · escritorio en navegador | **E** · escritorio con ventana propia | **M** · móvil |
|---|---|---|---|
| Dónde corre | Windows y Linux, en tu navegador | Windows y Linux, en su propia ventana | Tabletas y teléfonos Android (8 o superior) |
| Idea | **Ligera**: consultar sin tener una aplicación pesada abierta | **Completa**: todas las funciones de MARC en el escritorio | **Completa**: tus wikis en el bolsillo, sin conexión, con edición y asistente de IA |
| Conectar | GitHub, carpeta local, archivo `.marc` | GitHub (con tu cuenta), carpeta local, archivo `.marc` y doble clic en un `.marc` o `.md` | GitHub, carpeta local, archivo `.marc` y "Abrir con" desde cualquier gestor de archivos |
| Exportar | PDF, Word y `.marc` | PDF, Word y `.marc` | PDF, Word y `.marc` |
| Funciones nuevas | Se mantiene como está | Sí | Sí |
| Estado | Disponible | Disponible (`E2.2.3`) | Disponible (`M2.7.3`) |
| Guía | Páginas [[01 Conectar tu primer repositorio\|01]] a [[05 Cómo escribir tu documentación\|05]] | Páginas 01 a 06 y [[14 Novedades\|14]] a [[22 Practica las funciones\|22]] | [[08 MARC en tabletas y teléfonos]], [[09 Asistente IA]] y [[14 Novedades\|14]] a [[22 Practica las funciones\|22]] |

La diferencia entre las tres, por qué existe cada una y cómo conseguirlas está en [[10 Ediciones y versiones]].

```mermaid
flowchart LR
    subgraph Fuentes["Tu documentación (siempre tuya)"]
        G["Repositorio de GitHub"]
        C["Carpeta local"]
        P["Paquete .marc"]
    end
    subgraph Apps["MARC"]
        EN["Escritorio en navegador · EN"]
        M["Móvil · M"]
        E["Escritorio con ventana · E"]
    end
    subgraph Salidas["Lo que puedes entregar"]
        PDF["PDF"]
        W["Word (.docx)"]
        MK[".marc portable"]
    end
    G --> EN & M & E
    C --> EN & M & E
    P --> EN & M & E
    EN --> PDF & W & MK
    M --> PDF & W & MK
    E --> PDF & W & MK
```

> [!info] Filosofía
> Tus archivos son **siempre** la fuente de verdad. MARC los **lee** para mostrarlos y solo **escribe** cuando tú lo decides: al pulsar **Guardar** en el editor, o al **aceptar** un cambio que te propuso el asistente después de revisarlo. Antes de cada guardado, la versión anterior queda respaldada. Lo que se ve distinto en un formato (PDF, Word, la tableta) lo resuelve el motor, nunca tocando tu Markdown.

## Arquitectura descentralizada

MARC no tiene servidor central ni cuenta propia (si quieres, te conectas con **tu** cuenta de GitHub, que vive solo en tu equipo: [[15 Tu cuenta de GitHub]]):

- No hay una nube de MARC donde tu documentación se suba o se indexe.
- Cada persona conecta **sus propias** fuentes, en su propio equipo o tableta.
- Una vez sincronizada, cada wiki funciona **sin conexión**: también la exportación a PDF y Word, que se genera en tu dispositivo.
- Lo único que puede salir a internet es lo que tú pides: sincronizar o publicar en GitHub, una nota de equipo que decides publicar como *issue*, o una pregunta al [[09 Asistente IA|asistente]] con el proveedor de IA que tú configures.

En otras palabras: MARC es una capa de lectura y consulta sobre tus archivos, no una plataforma. El control de la información nunca sale de tus manos.

## Empieza aquí

| Página | Qué aprenderás |
|---|---|
| [[01 Conectar tu primer repositorio]] | Conectar GitHub, una carpeta local o un archivo `.marc` en el escritorio |
| [[02 El Hub]] | La pantalla principal: una tarjeta por cada wiki conectada |
| [[03 Navegar la wiki]] | Buscar, moverte entre páginas, cambiar de tema y el menú de opciones |
| [[04 Gestionar tus repositorios]] | Conectar más de una, resincronizar y quitar |
| [[05 Cómo escribir tu documentación]] | Sintaxis soportada y demostraciones en vivo |
| [[06 Exportar PDF, Word y .marc]] | Entregar tu wiki como PDF, documento de Word o paquete portable |
| [[07 El formato .marc]] | Qué es un `.marc` y por qué conviene para compartir |
| [[08 MARC en tabletas y teléfonos]] | La aplicación móvil: carpeta MARC, conectar, leer, editar |
| [[09 Asistente IA]] | Preguntar sobre tus documentos con tu propio proveedor de IA |
| [[10 Ediciones y versiones]] | Las ediciones EN, E y M: diferencias, razón de cada una, cómo conseguirlas y cómo se numeran sus versiones |
| [[11 Preguntas frecuentes]] | Soluciones a los problemas más comunes |
| [[12 Créditos]] | Quién hizo esta herramienta y con qué está construida |
| [[13 Especificación del formato .marc]] | La especificación oficial y abierta del `.marc`: para crear o leer paquetes con tus propias herramientas |
| [[14 Novedades]] | Qué trae cada versión y qué edición tiene qué |
| [[15 Tu cuenta de GitHub]] | Iniciar sesión con un código, sin tokens |
| [[16 Historial y trabajo en equipo]] | Quién escribió qué, qué cambió y a quién preguntar |
| [[17 Editar sobre la página]] | Escribir sobre la página (Visual) sin tocar el resto del Markdown |
| [[18 Publicar cambios (Git)]] | Guardar, Publicar, unir cambios, actualizar y resolver choques |
| [[19 Notas de equipo]] | Comentarios por párrafo, con respuestas y en GitHub |
| [[20 Lectura cómoda y accesibilidad]] | «Aa», modo dislexia, luz de noche, regla, énfasis y lector de voz |
| [[21 Visor de archivos]] | Abrir PDF y textos aparte, en la página exacta |
| [[22 Practica las funciones]] | Wiki de práctica editable, PDF de prueba y la documentación en PDF |

> [!tip] ¿Tienes prisa?
> En el escritorio (EN o E), ve directo a [[01 Conectar tu primer repositorio]]. En una tableta o teléfono (M), a [[08 MARC en tabletas y teléfonos]]. ¿Ya usas MARC? Mira [[14 Novedades]] y prueba todo en la [[22 Practica las funciones|wiki de práctica]]. ¿No sabes cuál edición es la tuya? Ver [[10 Ediciones y versiones]].

> [!note] Esta documentación en PDF
> Toda la documentación, con índice, en un solo archivo: [MARC — Documentación de uso.pdf](assets/MARC%20—%20Documentación%20de%20uso.pdf).
