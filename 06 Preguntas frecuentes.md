# Preguntas frecuentes

## "No se pudo sincronizar" al conectar un repositorio privado

Verifica dos cosas: que la URL empiece con `https://github.com/` (no `git@github.com:...`), y que tu Personal Access Token tenga permiso de lectura sobre ese repositorio. Ver [[01 Conectar tu primer repositorio]].

## "Solo se soportan repositorios de GitHub"

Esta versión únicamente soporta URLs con el formato `https://github.com/usuario/repositorio.git`. URLs de otras plataformas (GitLab, Bitbucket, SSH) no son compatibles todavía.

## "La wiki no está disponible en este momento"

Este mensaje aparece si el motor de renderizado interno no llegó a levantar a tiempo. Espera unos segundos y recarga — si persiste, ve al panel de [[04 Gestionar tus repositorios]] y usa **Resincronizar**.

## ¿Mis archivos en el repositorio se modifican al conectarlos?

No, nunca. La app solo **lee** tu repositorio para mostrarlo — jamás escribe, modifica ni hace commits sobre tu contenido fuente. El repositorio de Git es siempre la única fuente de verdad.

## ¿Necesito internet todo el tiempo?

Solo para **sincronizar** (clonar por primera vez, o traer cambios nuevos). Una vez sincronizado, puedes seguir leyendo la wiki sin conexión — se muestra la última copia local que se sincronizó con éxito.

## Quité un repositorio por error, ¿perdí algo?

No. **Quitar** un repositorio solo borra la copia local en tu equipo; el repositorio remoto en GitHub no se toca. Vuelve a conectarlo con la misma URL y se clona de nuevo desde cero.

## No encuentro una página que sé que existe

El buscador del [[02 El Hub|Hub]] y el buscador de la wiki se actualizan cada vez que un repositorio se sincroniza. Si acabas de hacer `push` de una página nueva, resincroniza manualmente desde [[04 Gestionar tus repositorios]] antes de buscarla.

## Cambié un archivo y no veo el cambio reflejado

Asegúrate de que el cambio ya esté en el repositorio remoto (con `push`), no solo en tu copia local del equipo donde editaste. Luego resincroniza desde [[04 Gestionar tus repositorios]].

## ¿Dónde se guarda mi token de acceso?

En el llavero nativo de tu sistema operativo, cifrado — nunca en un archivo de texto plano. Más detalle en [[01 Conectar tu primer repositorio]].

## ¿Por qué esta documentación ya no dice "Wiki Desktop Client"?

Ese fue el nombre de trabajo original del proyecto. El nombre oficial hoy es **MARC** (Markdown Automatizado por Repo y Consulta) — mismo motor, mismo comportamiento, solo un nombre definitivo. Ver [[07 Créditos]].

## ¿Esta documentación siempre está al día con mi versión de la app?

El **contenido** sí: este mismo repositorio (`Wiki-Desktop-Client-doc`) se sincroniza solo cada vez que abres MARC, igual que cualquier otro repositorio conectado — ver [[01 Conectar tu primer repositorio]]. Lo que puede no coincidir es el **número de versión** que ves en la [[00 Portada|portada]] y en [[07 Créditos]]: hoy se actualiza a mano en cada release, así que si tu instalación es más antigua que el número mostrado, la documentación puede describir funciones (como gráficas, fórmulas o iconos) que tu copia instalada todavía no trae empaquetadas. Compara siempre contra el número que ves en **Acerca de** dentro de la propia app.
