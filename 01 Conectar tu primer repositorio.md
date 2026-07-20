# Conectar tu primer repositorio

La primera vez que abres MARC no hay nada conectado — verás el [[02 El Hub|Hub]] vacío con un botón para conectar tu primer repositorio. Este es el único paso manual de toda la herramienta: una vez conectado, todo lo demás es automático.

## Paso a paso

1. En el Hub, pulsa **Conectar repositorio** (o el ícono de repositorios en la barra superior si ya tienes otros conectados).
2. Pega la **URL del repositorio de GitHub**. Debe tener esta forma exacta:

    ```
    https://github.com/tu-equipo/tu-wiki.git
    ```

3. Si el repositorio es **privado**, pega también un **Personal Access Token** (PAT) de GitHub. Si es público, deja ese campo vacío.
4. Pulsa **Conectar**. La app clona el repositorio, lo analiza y te muestra el resultado.

> [!warning] Solo GitHub, por ahora
> Esta versión solo soporta repositorios alojados en `https://github.com/...`. Otras plataformas (GitLab, Bitbucket, servidores Git propios) todavía no están soportadas.

## ¿Cuándo necesito un token?

Solo si el repositorio es **privado**. Para un repositorio público no hace falta nada más que la URL.

Para generar un token en GitHub:

1. Entra a **Settings → Developer settings → Personal access tokens**.
2. Genera uno nuevo con permiso de **lectura de repositorio** (`repo` o, si usas tokens finos, `Contents: Read-only`) — no necesitas más permisos que ese.
3. Cópialo y pégalo en el campo **Personal Access Token** al conectar.

> [!danger] Dónde se guarda tu token
> Tu token **nunca** se guarda en texto plano ni viaja a ningún servidor externo. Se almacena cifrado en el llavero nativo de tu sistema operativo (Credential Manager en Windows, Llavero en macOS, `gnome-keyring`/`SecretService` en Linux) — el mismo lugar donde tu SO guarda tus contraseñas de Wi-Fi. Ni siquiera queda en el archivo de configuración de la app.

## Qué pasa después de conectar

Si todo salió bien, ese repositorio queda como **activo** y la app te lleva a su wiki. Si algo falla — URL mal escrita, token sin permisos, sin conexión — verás el mensaje de error exacto de Git, para que sepas qué corregir.

A partir de aquí, cada vez que abras la app, el repositorio activo se sincroniza solo (un `git pull` automático) — no tienes que acordarte de nada. Si necesitas forzar una sincronización manual, ve a [[04 Gestionar tus repositorios]].
