# Conectar tu primer repositorio

La primera vez que abres MARC no hay nada conectado — verás el [[02 El Hub|Hub]] vacío con un botón para conectar tu primer repositorio. Este es el único paso manual de toda la herramienta: una vez conectado, todo lo demás es automático.

Hay dos formas de conectar una wiki, según dónde viva tu documentación:

| | Cuándo usarla |
|---|---|
| **GitHub** | Tu documentación ya vive en un repositorio remoto — de tu equipo, o tuyo — y quieres que MARC la traiga y la mantenga sincronizada sola. |
| **Carpeta local** | Tu documentación vive (o va a vivir) directo en tu equipo — con Git propio o sin ningún control de versiones — y no necesitas ni quieres que salga de ahí. |

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
