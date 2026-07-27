# Preguntas frecuentes

## "No se pudo sincronizar" al conectar un repositorio privado

Verifica dos cosas: que la URL empiece con `https://github.com/` (no `git@github.com:...`), y que tu Personal Access Token tenga permiso de lectura sobre ese repositorio. Ver [[01 Conectar tu primer repositorio]].

## "Solo se soportan repositorios de GitHub"

Entre plataformas remotas, esta versión únicamente soporta URLs con el formato `https://github.com/usuario/repositorio.git` — otras (GitLab, Bitbucket, SSH) no son compatibles todavía. Si tu documentación vive en alguna de esas, la alternativa es conectarla como **Carpeta local**: clónala tú mismo a tu equipo y apunta MARC directo ahí, sin pasar por GitHub. Ver [[01 Conectar tu primer repositorio]].

## "La wiki no está disponible en este momento"

Este mensaje aparece si el motor de renderizado interno no llegó a levantar a tiempo. Espera unos segundos y recarga — si persiste, ve al panel de [[04 Gestionar tus repositorios]] y usa **Resincronizar**.

## ¿Mis archivos en el repositorio se modifican al conectarlos?

No, nunca. La app solo **lee** tu repositorio para mostrarlo — jamás escribe, modifica ni hace commits sobre tu contenido fuente. El repositorio de Git es siempre la única fuente de verdad.

## ¿Necesito internet todo el tiempo?

Para un repositorio de **GitHub**, solo para **sincronizar** (clonar por primera vez, o traer cambios nuevos) — una vez sincronizado, puedes seguir leyendo la wiki sin conexión, se muestra la última copia local que se trajo con éxito. Una **carpeta local** no necesita internet en ningún momento, ni siquiera la primera vez.

## Quité un repositorio por error, ¿perdí algo?

No, en ningún caso. Si era un repositorio de GitHub clonado en la carpeta interna de MARC, solo se borra esa copia local — el remoto en GitHub no se toca, vuelve a conectarlo con la misma URL y se clona de nuevo. Si era una carpeta local (o una carpeta de destino que tú elegiste para un repositorio de GitHub), MARC nunca la borra: sigue intacta en tu disco, solo vuelve a conectarla. Ver [[04 Gestionar tus repositorios]].

## No encuentro una página que sé que existe

El buscador del [[02 El Hub|Hub]] y el buscador de la wiki se actualizan cada vez que un repositorio se sincroniza. Para GitHub esto ya pasa solo, cada pocos segundos mientras navegas — si acabas de hacer `push` y quieres verlo ya sin esperar, resincroniza manualmente desde [[04 Gestionar tus repositorios]]. Para una carpeta local no hay que esperar nada: se detecta el cambio en cuanto ocurre.

## Cambié un archivo y no veo el cambio reflejado

Depende de cómo conectaste esa wiki (ver [[01 Conectar tu primer repositorio]]):

- **GitHub**: asegúrate de que el cambio ya esté en el repositorio remoto (con `push`), no solo en tu copia local del equipo donde editaste. MARC lo detecta solo en unos segundos; si no quieres esperar, resincroniza desde [[04 Gestionar tus repositorios]].
- **Carpeta local**: no hace falta ningún `push` — basta con guardar el archivo. Si aun así no se ve, confirma que guardaste en la carpeta correcta (la que aparece en el panel de Repositorios) y no en una copia.

## ¿Dónde se guarda mi token de acceso?

En el llavero nativo de tu sistema operativo, cifrado — nunca en un archivo de texto plano. Más detalle en [[01 Conectar tu primer repositorio]].

## ¿Qué hace "Salir" y por qué me pide confirmar?

Cierra MARC de verdad: apaga el servidor local que corre en tu equipo, no solo la ventana que tenías abierta. Te lo pide confirmar porque, a diferencia de cerrar la ventana con la X, no hay forma de deshacerlo sin volver a abrir la app — útil saberlo antes de que se cierre de golpe a medio leer algo. Volver a abrir MARC lo arranca de nuevo sin ningún problema; no se pierde nada de tus repositorios conectados. Ver [[03 Navegar la wiki]].

## ¿Por qué esta documentación ya no dice "Wiki Desktop Client"?

Ese fue el nombre de trabajo original del proyecto. El nombre oficial hoy es **MARC** (Markdown Automatizado por Repo y Consulta) — mismo motor, mismo comportamiento, solo un nombre definitivo. Ver [[07 Créditos]].

## ¿Esta documentación siempre está al día con mi versión de la app?

El **contenido** sí: este mismo repositorio se sincroniza solo cada vez que abres MARC, igual que cualquier otro repositorio conectado — ver [[01 Conectar tu primer repositorio]]. Lo que puede no coincidir es el **instalador**: cada nueva función se documenta aquí en cuanto queda lista en el código, pero el `.exe`/`.deb` que tienes instalado solo se actualiza cuando lo reinstalas con una versión nueva. Si tu instalación es más antigua que el número que ves aquí o en [[00 Portada|portada]]/[[07 Créditos]], esta documentación puede describir funciones que tu copia instalada todavía no trae empaquetadas. Compara siempre contra el número que ves en **Acerca de** dentro de la propia app.
