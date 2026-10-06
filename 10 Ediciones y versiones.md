# Ediciones y versiones

MARC tiene **tres ediciones**. Todas leen las mismas wikis, comparten el formato `.marc` y exportan a PDF y Word; cambian en **dónde corren** y en **para qué están pensadas**.

| | **EN** · escritorio en navegador | **E** · escritorio con ventana propia | **M** · móvil |
|---|---|---|---|
| Qué es | Un servicio pequeño en tu equipo; la wiki se ve en tu navegador | Una aplicación de escritorio completa, con la interfaz de MARC en su propia ventana | La aplicación para tabletas y teléfonos |
| Dónde corre | Windows y Linux | Windows y Linux | Android 8 o superior |
| Pensada para | Leer y consultar **ligero**, sin tener una aplicación pesada abierta | Trabajar a fondo con tus wikis en el escritorio | Llevarte tus wikis, leerlas sin conexión, editarlas y consultarlas con IA |
| Funciones nuevas | Las recibe **después**, y solo las que encajan con su idea de ligereza | **Primero** | **Primero** |
| Estado | Disponible: `EN2.0.0` | **En desarrollo** | Disponible: `M2.0.0` |

```mermaid
flowchart TB
    subgraph Potentes["Ediciones completas: reciben primero funciones y actualizaciones"]
        E["E · escritorio con ventana propia<br/>(en desarrollo)"]
        M["M · tabletas y teléfonos"]
    end
    subgraph Ligera["Edición ligera"]
        EN["EN · escritorio en navegador"]
    end
    F["Funciones nuevas"] --> E & M
    F -. "después, si encajan<br/>con su idea de ligereza" .-> EN
```

## Por qué existe cada una

### EN — la ligera

MARC nació como **EN**, con una idea: que fuera **ligero** y que no tuvieras que tener todo abierto. EN corre como un servicio pequeño en tu equipo y la wiki se ve en el navegador que ya usas, en una pestaña más. Así seguirá: EN es la opción para consultar tus wikis sin cargar una aplicación completa.

Por esa misma idea, EN recibe las funciones nuevas **después** que E y M, y solo las que no la hacen pesada.

### E — el escritorio completo

**E** lleva al escritorio la misma interfaz de MARC móvil, en su propia ventana: barra lateral, lector, búsqueda, edición, asistente de IA y exportación. Junto con M es una edición **completa**: las funciones y actualizaciones llegan **primero** a ellas.

E está **en desarrollo**. Cuando esté lista, está previsto que en Windows puedas elegir al instalar qué interfaz quieres: **E** (ventana propia) o **EN** (en el navegador).

### M — el móvil

**M** es MARC para tabletas y teléfonos Android: tus wikis sin conexión, edición con respaldos, el asistente de IA y la carpeta MARC en tu almacenamiento. Igual que E, recibe **primero** las funciones nuevas. Ver [[08 MARC en tabletas y teléfonos]].

## Cómo conseguir cada una

| Edición | Hoy | Más adelante |
|---|---|---|
| **EN** | Instalador para Windows (`.exe`) y Linux (`.deb`), entregado directamente por el autor (ver [[12 Créditos]]) | — |
| **M** | Archivo de instalación de Android (`.apk`), entregado directamente por el autor | Se busca publicarla en **Google Play** y **AppGallery** |
| **E** | Todavía no disponible (en desarrollo) | Canal de distribución por definir |

> [!info] Una sola documentación para las tres
> Esta documentación es la misma para todas las ediciones y se actualiza sola en cada una desde su repositorio. Cuando una página habla de una edición en particular, lo indica.

## Versiones

Cada versión lleva la **letra de su edición** seguida de su número:

| Edición | Ejemplo |
|---|---|
| EN | `EN2.0.0` |
| E | `E2.0.0` (cuando salga) |
| M | `M2.0.0` |

El número tiene tres partes: **mayor . menor . parche**.

- **Mayor:** es **el mismo en todas las ediciones**: marca la generación de MARC y cambia en todas a la vez.
- **Menor y parche:** son propios de cada edición, porque cada una recibe sus propias mejoras y correcciones.

Por ejemplo, `M2.3.1` y `EN2.0.7` son de la misma generación (la 2): M ya recibió más funciones, como corresponde a una edición completa.

```mermaid
flowchart LR
    G1["Generación 1<br/>v1.x · solo escritorio en navegador"] --> G2["Generación 2"]
    G2 --> EN2["EN2.0.0 → EN2.0.1 → …"]
    G2 --> M2["M2.0.0 → M2.0.1 → …"]
    G2 -.-> E2["E2.0.0 (en desarrollo)"]
```

### Por qué estamos en la 2

La generación 1 (`v1.x`) era solo el escritorio en navegador. La **generación 2** llegó con MARC móvil, el formato `.marc`, la exportación a PDF y Word y el asistente de IA: MARC dejó de ser solo un lector de escritorio y se convirtió en una familia de ediciones.

### Dónde ver tu versión

- **EN:** Más opciones → **Acerca de MARC**.
- **M:** **Ajustes → Acerca de**.

> [!info] El formato .marc tiene su propia versión
> Los archivos `.marc` llevan dentro la versión de su **formato** (hoy `1.0.0`), independiente de la edición. Un `.marc` creado en cualquier edición se abre en las demás, mientras compartan la versión mayor del formato.
