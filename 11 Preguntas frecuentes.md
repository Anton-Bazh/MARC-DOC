# Preguntas frecuentes

## "No se pudo sincronizar" al conectar un repositorio privado

Verifica dos cosas: que la URL empiece con `https://github.com/` (no `git@github.com:...`), y que tu Personal Access Token tenga permiso de lectura sobre ese repositorio. Ver [[01 Conectar tu primer repositorio]].

## "Solo se soportan repositorios de GitHub"

En **EN**, entre plataformas remotas, solo se soportan URLs con el formato `https://github.com/usuario/repositorio.git` — otras (GitLab, Bitbucket, SSH) no son compatibles todavía. Si tu documentación vive en alguna de esas, la alternativa es conectarla como **Carpeta local**: clónala tú mismo a tu equipo y apunta MARC directo ahí, sin pasar por GitHub. En **E** y **M** puedes pegar la URL `https://` de cualquier servidor Git. Ver [[01 Conectar tu primer repositorio]].

## "La wiki no está disponible en este momento"

Este mensaje aparece si el motor de renderizado interno no llegó a levantar a tiempo. Espera unos segundos y recarga — si persiste, ve al panel de [[04 Gestionar tus repositorios]] y usa **Resincronizar**.

## ¿Mis archivos se modifican al conectarlos?

No. Conectar, leer, buscar y exportar **solo leen** tus archivos. MARC escribe únicamente cuando tú lo decides: al pulsar **Guardar** en el editor (un `.marc` local en el escritorio; carpetas, `.marc` y documentos sueltos en el móvil) o al **aplicar** un cambio que te propuso el [[09 Asistente IA|asistente]] después de revisarlo. En **E** y **M**, MARC solo hace un commit y lo sube cuando tú pulsas **Publicar** ([[18 Publicar cambios (Git)]]); EN nunca hace commits.

## Guardé un cambio por error, ¿puedo recuperar la versión anterior?

En el móvil, sí: antes de cada guardado, la versión anterior queda en `MARC/Respaldos/<wiki>/<fecha>/`, con la misma ruta del archivo. Ver [[08 MARC en tabletas y teléfonos]].

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

En el escritorio, en el llavero nativo de tu sistema operativo; en el móvil, cifrado en el almacén seguro de Android. Nunca en un archivo de texto plano y nunca dentro de un `.marc`. Lo mismo vale para las claves de los proveedores de IA. Más detalle en [[01 Conectar tu primer repositorio]].

## ¿La IA lee todos mis documentos?

Solo lo que tú eliges en **Ajustes → IA → Qué recibe la IA** (por defecto, solo la página abierta), y solo cuando tú preguntas. Va directo de tu dispositivo a tu proveedor; con **Local (Ollama)** no sale de tu red. Ver [[09 Asistente IA]].

## ¿Necesito internet para exportar a PDF o Word?

No. La exportación se genera completa en tu equipo o tableta. Ver [[06 Exportar PDF, Word y .marc]].

## Mi Word se ve un poco distinto en Google Docs

Google Docs no usa algunas cosas que Word sí (por ejemplo, ecuaciones y gráficas nativas se ven más simples). Si el documento va a abrirse en programas distintos, exporta en el modo **Como imagen**: se ve igual en todos. Ver [[06 Exportar PDF, Word y .marc]].

## ¿Puedo usar un .marc fuera de MARC?

Sí. Es un formato abierto: un ZIP con tus archivos Markdown e imágenes tal cual. Renómbralo a `.zip` para verlo con cualquier programa, o créalo y léelo con tus propias herramientas siguiendo [[13 Especificación del formato .marc]].

## ¿Qué significan EN, E y M?

Son las tres ediciones de MARC: **EN** es el escritorio en navegador (la ligera), **E** el escritorio con ventana propia y **M** el móvil. E y M son las ediciones completas y reciben primero las funciones nuevas; EN las recibe después, si encajan con su idea de ligereza. Todas comparten el primer número de versión (la generación). Ver [[10 Ediciones y versiones]].

## ¿Dónde consigo MARC?

Por ahora los instaladores de escritorio (EN y E) y la app móvil (M) se entregan directamente; para conseguirlos, contacta al autor (ver [[12 Créditos]]). Más adelante se busca publicar M en Google Play y AppGallery. Ver [[10 Ediciones y versiones]].

## ¿Qué hace "Salir" y por qué me pide confirmar?

Cierra MARC de verdad: apaga el servidor local que corre en tu equipo, no solo la ventana que tenías abierta. Te lo pide confirmar porque, a diferencia de cerrar la ventana con la X, no hay forma de deshacerlo sin volver a abrir la app — útil saberlo antes de que se cierre de golpe a medio leer algo. Volver a abrir MARC lo arranca de nuevo sin ningún problema; no se pierde nada de tus repositorios conectados. Ver [[03 Navegar la wiki]].

## ¿Por qué esta documentación ya no dice "Wiki Desktop Client"?

Ese fue el nombre de trabajo original del proyecto. El nombre oficial hoy es **MARC** (Markdown Automatizado por Repo y Consulta) — mismo motor, mismo comportamiento, solo un nombre definitivo. Ver [[12 Créditos]].

## ¿Esta documentación siempre está al día con mi versión de la app?

El **contenido** sí, en todas las ediciones: esta documentación vive en un repositorio de Git y MARC la actualiza sola. En el escritorio en navegador (EN) se sincroniza cada vez que abres MARC, igual que cualquier otro repositorio conectado — ver [[01 Conectar tu primer repositorio]]. En el móvil (M) se actualiza desde el mismo repositorio cuando hay conexión; sin conexión, ves la última copia que se trajo (o la que viene dentro de la app). Lo que puede no coincidir es el **instalador**: cada nueva función se documenta aquí en cuanto queda lista en el código, pero el `.exe`/`.deb` que tienes instalado solo se actualiza cuando lo reinstalas con una versión nueva. Si tu instalación es más antigua que el número que ves aquí o en [[00 Portada|portada]]/[[12 Créditos]], esta documentación puede describir funciones que tu copia instalada todavía no trae empaquetadas. Compara siempre contra el número que ves en **Acerca de** dentro de la propia app (`EN…` en el escritorio en navegador, `E…` en el escritorio con ventana propia, `M…` en móvil, ver [[10 Ediciones y versiones]]).

## Publiqué y dice que "tocan lo mismo"

Otra persona publicó un cambio en **las mismas líneas** que tú. MARC no elige qué texto queda: tu commit quedó guardado en tu equipo y el de la otra persona en el servidor; **no se perdió nada**. Pónganse de acuerdo y únanlo desde un equipo de escritorio con una herramienta de Git; luego pulsa **↻ actualizar**. Si los cambios son en partes distintas, MARC los une solo. Ver [[18 Publicar cambios (Git)#Cuando dos personas cambian a la vez]].

## No aparece el botón Publicar

Aparece solo cuando hay algo que publicar, en una wiki con **Git**: guarda primero un cambio o deja una nota. Una carpeta sin Git o un `.marc` no tienen Publicar (en E, una carpeta te ofrece **Publicar esta carpeta en GitHub**). En la tableta, una wiki conectada antes de M2.2.0 necesita **Traer historial completo**. Ver [[18 Publicar cambios (Git)]].

## "El servidor pidió permiso" al publicar

Tu cuenta no tiene permiso de escritura en ese repositorio, o no has iniciado sesión. Conecta tu [[15 Tu cuenta de GitHub|cuenta de GitHub]] (o revisa el token de esa wiki) y pide al dueño del repositorio que te agregue como colaborador.

## No veo los repositorios de mi escuela o empresa

Su organización de GitHub debe aprobar la app MARC. Al final de tu lista de repositorios pulsa **pide acceso aquí** y espera a que un administrador la apruebe. Ver [[15 Tu cuenta de GitHub#Repositorios de una organización]].

## La voz no suena en mi tableta

Abre **Ajustes → Accesibilidad → Lector de voz → Probar voz** y lee el aviso. Casi siempre falta la voz de tu idioma: en Android con Google instala **Servicios de voz de Google**; en **Huawei** instala **SherpaTTS** y descarga tu idioma. Revisa también el **volumen multimedia**. Ver [[20 Lectura cómoda y accesibilidad#Si no se oye]].

## ¿E tiene lector de voz?

Todavía no: E tiene toda la lectura cómoda (dislexia, luz de noche, énfasis, regla) y la voz llegará en una próxima versión. Ver [[14 Novedades]].

## Abrí un .marc y no hay historial ni Publicar

Es normal: un `.marc` lleva el **contenido** de la wiki, no su historia de Git. Para el historial, conecta el repositorio original con **+ Conectar → Git**. Ver [[16 Historial y trabajo en equipo]].

## El enlace a un PDF no abre en la página correcta

Revisa que el enlace termine en `#page=N` (por ejemplo `manual.pdf#page=3`) y que el archivo esté dentro de la wiki, con la ruta relativa a la página. Ver [[21 Visor de archivos]].

## Quiero practicar sin tocar mis wikis

Usa la wiki de práctica: [[22 Practica las funciones]].
