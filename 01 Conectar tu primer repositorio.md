# Conectar tu primer repositorio

La primera vez que abres MARC no hay nada conectado — verás el [[02 El Hub|Hub]] vacío con un botón para conectar tu primer repositorio. Este es el único paso manual de toda la herramienta: una vez conectado, todo lo demás es automático.

Hay tres formas de conectar una wiki en el escritorio (EN), según dónde viva tu documentación (en tabletas y teléfonos, ver [[08 MARC en tabletas y teléfonos]]):

> [!info] ¿Usas E o M?
> Las ediciones completas conectan con el botón **+ Conectar** y traen más opciones: tu cuenta de GitHub, elegir dónde clonar, usar un repositorio que ya tenías clonado y crear wikis nuevas. Ve a [[#En E y M]].

| | Cuándo usarla |
|---|---|
| **GitHub** | Tu documentación ya vive en un repositorio remoto — de tu equipo, o tuyo — y quieres que MARC la traiga y la mantenga sincronizada sola. |
| **Carpeta local** | Tu documentación vive (o va a vivir) directo en tu equipo — con Git propio o sin ningún control de versiones — y no necesitas ni quieres que salga de ahí. |
| **Archivo .marc** | Alguien te pasó una wiki empaquetada en un solo archivo, o quieres abrir una que exportaste. Se lee al instante y sin conexión. |

## GitHub

1. En el Hub, pulsa **Conectar repositorio** (o el selector de repositorio en la barra superior si ya tienes otros conectados) y elige la pestaña **GitHub**.
2. Pega la **URL del repositorio**. Debe tener esta forma exacta:

    ```
    https://github.com/tu-equipo/tu-wiki.git
    ```

3. Si el repositorio es **privado**, pega también un **Personal Access Token** (PAT) de GitHub. Si es público, deja ese campo vacío.
4. Pulsa **Conectar**. La app clona el repositorio, lo analiza y te muestra el resultado.

> [!warning] Solo GitHub, por ahora
> Entre plataformas remotas, esta versión solo soporta `https://github.com/...`. Otras (GitLab, Bitbucket, servidores Git propios) todavía no están soportadas — si tu documentación vive ahí, la alternativa mientras tanto es clonarla tú mismo a una carpeta y conectar esa carpeta como **Carpeta local**.

### Opciones avanzadas: carpeta de destino

Por defecto MARC clona el repositorio en su propia carpeta interna, que no necesitas tocar nunca. Si prefieres elegir tú dónde vive el clon — por ejemplo para apuntar ahí otra herramienta, o tu propio agente de código — despliega **Opciones avanzadas** y elige una carpeta con el explorador integrado. MARC sigue sincronizando esa carpeta igual que la interna; lo único que cambia es dónde vive en tu disco.

## Carpeta local

1. En el mismo formulario, elige la pestaña **Carpeta local**.
2. Elige una carpeta de tu equipo con el explorador integrado (o escribe la ruta completa a mano).
3. Pulsa **Conectar carpeta**.

MARC lee esa carpeta tal cual, en el momento en que la abres — no la copia ni la clona a ningún otro lado. Si la carpeta tiene su propio `.git` (porque tú la versionas con Git por tu cuenta), MARC aprovecha eso solo para mostrarte la fecha del último commit en el [[02 El Hub|Hub]]; nunca hace `push`, `pull` ni `fetch` sobre ese repositorio — es 100% tuyo, MARC solo mira.

> [!tip] Se actualiza sola, sin repositorio remoto
> No hace falta ningún botón para ver tus cambios: si editas un archivo dentro de la carpeta conectada — con tu editor, con Obsidian, con un agente de código — MARC lo nota solo en cuanto vuelves a mirar la wiki. Ver [[04 Gestionar tus repositorios]].

> [!warning] Esa carpeta nunca se toca al desconectar
> Igual que con la carpeta de destino avanzada de GitHub: si quitas un repositorio conectado como carpeta local, MARC olvida la conexión pero **jamás borra la carpeta** — es tuya, tú decides qué hacer con ella.

## Archivo .marc

En el Hub, **Abrir archivo .marc** (o la pestaña **Archivo .marc** del panel de conexión) te deja elegir el archivo. MARC lo valida y lo abre como una wiki más:

- Si el `.marc` salió de un **repositorio de Git**, queda en **solo lectura**: la fuente de verdad sigue siendo el repositorio. MARC te avisa si el repositorio tiene una versión más nueva (para un repositorio privado te pedirá el token, que se guarda aparte, nunca en el archivo).
- Si salió de una **carpeta local**, es **editable**: el botón **Editar** de cada página guarda el cambio de vuelta en el `.marc`.

Más detalle en [[07 El formato .marc]].

## ¿Cuándo necesito un token?

Solo si el repositorio es **privado**. Para un repositorio público no hace falta nada más que la URL.

Para generar un token en GitHub:

1. Entra a **Settings → Developer settings → Personal access tokens**.
2. Genera uno nuevo con permiso de **lectura de repositorio** (`repo` o, si usas tokens finos, `Contents: Read-only`) — no necesitas más permisos que ese.
3. Cópialo y pégalo en el campo **Personal Access Token** al conectar.

> [!danger] Dónde se guarda tu token
> Tu token **nunca** se guarda en texto plano ni viaja a ningún servidor externo. Se almacena cifrado en el llavero nativo de tu sistema operativo (Credential Manager en Windows, Llavero en macOS, `gnome-keyring`/`SecretService` en Linux) — el mismo lugar donde tu SO guarda tus contraseñas de Wi-Fi. Ni siquiera queda en el archivo de configuración de la app.

## Qué pasa después de conectar

Si todo salió bien, ese repositorio queda como **activo** y la app te lleva a su wiki. Si algo falla al conectar por GitHub — URL mal escrita, token sin permisos, sin conexión — verás el mensaje de error exacto de Git, para que sepas qué corregir.

Para un repositorio de **GitHub**: a partir de aquí, la app lo mantiene sincronizado sola (al abrir MARC, y en segundo plano mientras navegas la wiki activa) — no tienes que acordarte de nada. Si necesitas forzarlo ya, ve a [[04 Gestionar tus repositorios]].

Para una **carpeta local**: no hay nada que sincronizar — ya estás viendo el contenido real de tu disco, siempre. Ver [[04 Gestionar tus repositorios]] para el detalle de cómo MARC detecta tus cambios.

## En E y M

En **E** (escritorio con ventana propia) y **M** (tableta y teléfono), el botón **+ Conectar** de la barra lateral o del inicio abre una hoja con tres pestañas:

| Pestaña | Para qué |
|---|---|
| **Git** | Conectar un repositorio: de tu lista de GitHub (con tu cuenta) o pegando su URL |
| **Carpeta local** | Abrir una carpeta con archivos Markdown tal como está (en M, dentro de la carpeta MARC o la que elijas) |
| **Crear** | Crear una wiki nueva: **en GitHub** (pública o privada) o **local** |

Los archivos `.marc` se abren con **doble clic** (E) o **Abrir con MARC** desde el gestor de archivos (M). Ver [[07 El formato .marc]].

### Git con tu cuenta (recomendado)

En la pestaña **Git**, pulsa *«¿Usas GitHub? Conecta tu cuenta y elige tus repositorios, sin pegar URL ni token»*. Tras iniciar sesión ([[15 Tu cuenta de GitHub]]) verás tu lista de repositorios, públicos y privados, con buscador: elige uno y listo. Se clona con **todo su historial**, listo para [[16 Historial y trabajo en equipo|Historial]] y [[18 Publicar cambios (Git)|Publicar]].

> [!tip] Repositorios de tu organización
> Si faltan los de tu escuela o empresa, usa el enlace del final de la lista: *«¿Faltan repositorios de tu organización? Su administrador debe aprobar la app MARC: pide acceso aquí»*.

### Git con URL

También puedes pegar la URL (`https://…`) de cualquier servidor Git (GitHub, GitLab, un servidor propio), elegir la **Rama (opcional · main)** y, si es privado y no usas tu cuenta, un **Token (opcional · repos privados)**. El token se guarda cifrado en el llavero del sistema.

### Dónde guardarlo (E)

En el escritorio, **Dónde guardarlo** muestra la carpeta donde se clonará (por defecto una carpeta de MARC). Pulsa **Cambiar…** para elegir otra, por ejemplo tu carpeta de proyectos. Al quitar la wiki, una carpeta elegida por ti **nunca se borra**.

### ¿Ya lo tienes clonado? (E)

Si ya tienes el repositorio en tu equipo (clonado con Git, VS Code u otra herramienta), pulsa **¿Ya lo tienes clonado? Elegir su carpeta…**. MARC lo usa **en su sitio**, sin copiarlo: verás su historial, podrás publicar y actualizar, y tus otras herramientas siguen usando la misma carpeta.

### Crear una wiki

En **Crear**, escribe el nombre y elige:

- **GitHub**: MARC crea el repositorio en tu cuenta (marca si es **privado**), con una primera página, y lo conecta.
- **Local**: una carpeta nueva en tu equipo (en M, dentro de la carpeta MARC).

Después, añade páginas con **Nueva página** en la barra lateral y escribe con el [[17 Editar sobre la página|editor visual]].

> [!note] Para probarlo
> El paso 5 de [[22 Practica las funciones]] crea una wiki de práctica en GitHub.
