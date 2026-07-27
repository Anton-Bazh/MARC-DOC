# Gestionar tus repositorios

El panel de **Repositorios** (accesible desde el selector de repositorio en la barra superior de cualquier wiki, o desde el Hub) es donde administras todo lo relacionado con tus repositorios conectados: cuáles tienes, cuál está activo, y cómo mantenerlos al día.

## Conectar otro repositorio

El mismo formulario que usaste la primera vez — con sus dos pestañas, **GitHub** y **Carpeta local**, ver [[01 Conectar tu primer repositorio]] — está siempre disponible aquí, debajo de tu lista de repositorios. Puedes tener **varios repositorios conectados** al mismo tiempo, mezclando ambos tipos libremente; solo uno está activo (siendo servido) en un momento dado.

## Editar un repositorio de GitHub

Cada repositorio de GitHub tiene un botón **Editar** para cambiar su token de acceso o su carpeta de destino sin tener que desconectarlo y volver a conectarlo desde cero. Las carpetas locales no tienen "editar": si quieres apuntar a otra carpeta, conecta esa carpeta nueva y, si ya no quieres la anterior, quítala aparte.

## Cambiar el repositorio activo

Pulsa cualquier repositorio de tu lista que no esté marcado como **activo**. La app lo vuelve el activo y te lleva directo a su wiki — si es de GitHub, lo sincroniza primero si hace falta; si es una carpeta local, no hay nada que sincronizar, ya estás viendo su contenido real.

## Cómo se mantiene al día cada tipo de repositorio

| | Cómo se actualiza | Botón manual |
|---|---|---|
| **GitHub** | Al abrir MARC, y automáticamente cada pocos segundos mientras navegas la wiki activa (solo reconstruye si de verdad hubo un `push` nuevo) | **Resincronizar**, junto al repositorio activo — para el "quiero verlo ya" sin esperar el próximo chequeo |
| **Carpeta local** | En cuanto MARC nota que algo cambió en el disco — edites con lo que edites, incluso sin Git de por medio | El mismo botón dice **Actualizar desde la carpeta**: relee el contenido al instante |

> [!tip]
> En el uso normal no hace falta tocar ningún botón: los dos tipos de repositorio se mantienen al día solos. Los botones existen para el momento puntual en que no quieres esperar ni un segundo.

## Quitar un repositorio

El botón **Quitar** desconecta el repositorio de MARC. Qué tan a fondo depende de dónde vivía:

- **Clon interno de MARC** (GitHub, sin carpeta de destino elegida a mano): se borra la copia local y el token guardado, si tenía uno. El repositorio remoto en GitHub **no se toca**.
- **Carpeta elegida por ti** (destino avanzado de GitHub, o cualquier carpeta local): MARC **nunca borra esa carpeta**. Es tuya — olvida la conexión y ya, tú decides qué hacer con el contenido.

Si vuelves a conectar la misma fuente después, la app la reconoce: un repositorio de GitHub se clona de nuevo desde cero (o retoma la carpeta, si sigue ahí); una carpeta local simplemente se vuelve a activar tal como está.

> [!warning]
> Quitar el repositorio activo te deja sin wiki activa hasta que conectes o selecciones otro.

## Estado de cada repositorio

Cada fila muestra una píldora de estado:

- **✓ activo** — es el que se está sirviendo ahora mismo.
- **desactivado** — está conectado y disponible, pero no es el que ves en este momento.
