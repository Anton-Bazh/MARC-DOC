![MARC](assets/logo.png){ width="120" }

# MARC

### Markdown Automatizado por Repo y Consulta

`v1.2.0`

---

**MARC** es una aplicación de escritorio para leer y navegar la documentación técnica de tu equipo directamente desde su repositorio de Git — sin depender de un servicio en la nube, sin exportar nada a otra plataforma, y sin perder el formato con el que la escribiste.

Si tu equipo ya escribe su documentación en Markdown — por ejemplo con [Obsidian](https://obsidian.md) — MARC la convierte en una wiki navegable, con búsqueda, tema claro/oscuro, gráficas, diagramas, fórmulas matemáticas y una experiencia de lectura cuidada, leyendo el contenido tal como vive en el repositorio.

> [!info] Filosofía
> El repositorio de Git **siempre** es la fuente de verdad. MARC nunca modifica tus archivos fuente — solo los lee, los traduce a HTML y te los muestra. Si algo se ve mal, el arreglo va en tu Markdown, nunca en la app.

## Arquitectura descentralizada

MARC no tiene servidor central ni cuenta de usuario. Cada persona conecta **sus propios** repositorios de Git directamente desde su equipo:

- No hay una nube de MARC donde tu documentación se suba o se indexe.
- No hay dependencia de que un tercer servicio esté disponible para que puedas leer tu wiki.
- Cada repositorio conectado es independiente de los demás — puedes tener varios equipos, varios proyectos, sin que se mezclen entre sí.
- Una vez sincronizado, funciona sin conexión: lees la última copia local que se trajo con éxito.

En otras palabras: MARC es una capa de lectura sobre Git, no una plataforma. El control de la información nunca sale de tu repositorio.

## Empieza aquí

| Página | Qué aprenderás |
|---|---|
| [[01 Conectar tu primer repositorio]] | Cómo conectar un repositorio de GitHub, público o privado |
| [[02 El Hub]] | La pantalla principal: una tarjeta por cada repositorio conectado |
| [[03 Navegar la wiki]] | Buscar, moverte entre páginas y cambiar de tema |
| [[04 Gestionar tus repositorios]] | Conectar más de uno, resincronizar y quitar repositorios |
| [[05 Cómo escribir tu documentación]] | Sintaxis soportada, enlaces a la documentación oficial de cada herramienta y demostraciones en vivo |
| [[06 Preguntas frecuentes]] | Soluciones a los problemas más comunes |
| [[07 Créditos]] | Quién hizo esta herramienta, su visión y con qué está construida |

> [!tip] ¿Tienes prisa?
> Si solo quieres empezar ya, ve directo a [[01 Conectar tu primer repositorio]].
