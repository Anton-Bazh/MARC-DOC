# Gestionar tus repositorios

El panel de **Repositorios** (accesible desde el ícono correspondiente en cualquier pantalla) es donde administras todo lo relacionado con tus repositorios conectados: cuáles tienes, cuál está activo, y cómo mantenerlos al día.

## Conectar otro repositorio

El mismo formulario que usaste la primera vez — ver [[01 Conectar tu primer repositorio]] — está siempre disponible aquí, debajo de tu lista de repositorios. Puedes tener **varios repositorios conectados** al mismo tiempo; solo uno está activo (siendo servido) en un momento dado.

## Cambiar el repositorio activo

Pulsa cualquier repositorio de tu lista que no esté marcado como **activo**. La app lo vuelve el activo, lo sincroniza si hace falta, y te lleva directo a su wiki.

## Resincronizar

Junto al repositorio activo verás un botón **Resincronizar**. Úsalo cuando sepas que hubo cambios nuevos en el repositorio (un `push` reciente de tu equipo) y no quieras esperar al próximo arranque de la app — la sincronización automática al abrir la app ya cubre la mayoría de los casos, este botón es para el "quiero verlo ya".

> [!tip]
> No hace falta resincronizar manualmente en el uso normal: cada vez que abres la app, el repositorio activo se sincroniza solo.

## Quitar un repositorio

El botón **Quitar** desconecta el repositorio: borra su copia local y su token guardado (si tenía uno). El repositorio remoto en GitHub **no se toca** — nada se borra ahí. Si vuelves a conectarlo después, la app simplemente lo clona de nuevo desde cero.

> [!warning]
> Quitar el repositorio activo te deja sin wiki activa hasta que conectes o selecciones otro.

## Estado de cada repositorio

Cada fila muestra una píldora de estado:

- **✓ activo** — es el que se está sirviendo ahora mismo.
- **desactivado** — está conectado y disponible, pero no es el que ves en este momento.
