# Créditos

## Acerca de MARC

**MARC** — *Markdown Automatizado por Repo y Consulta* — nació con otro nombre de trabajo, **Wiki Desktop Client**, mientras la idea todavía se estaba probando: leer la documentación técnica de un equipo directo desde su repositorio de Git, sin nube, sin plataforma, sin fricción. El nombre cambió; la idea y la arquitectura descentralizada detrás — ver [[00 Portada|Portada]] — se mantienen igual desde el primer commit.

`v1.2.0`

## Stack técnico

| Capa | Herramienta |
|---|---|
| Traducción de Markdown → HTML | [MkDocs](https://www.mkdocs.org/) + [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) |
| Servidor local | [FastAPI](https://fastapi.tiangolo.com/) |
| Clonado y sincronización de repos | [pygit2](https://www.pygit2.org/) (libgit2), sin depender de `git` instalado en el sistema |
| Almacenamiento seguro de tokens | [`keyring`](https://pypi.org/project/keyring/), sobre el llavero nativo del sistema operativo |
| Diagramas | [Mermaid](https://mermaid.js.org/) |
| Gráficas | [Chart.js](https://www.chartjs.org/) |
| Fórmulas matemáticas | [KaTeX](https://katex.org/) |
| Wikilinks, transclusión y callouts estilo Obsidian | [mkdocs-obsidian-links](https://pypi.org/project/mkdocs-obsidian-links/), [mkdocs-embed-file-plugins](https://pypi.org/project/mkdocs-embed-file-plugins/), [mkdocs-callouts](https://pypi.org/project/mkdocs-callouts/) |

Todas las librerías de terceros están vendorizadas — nada se carga desde un CDN — para que la wiki funcione completamente sin conexión una vez sincronizada.

## Creado por Antonio Baeza

- GitHub: [github.com/Anton-Bazh](https://github.com/Anton-Bazh)
- Correo: [baezaantoniocontacto@gmail.com](mailto:baezaantoniocontacto@gmail.com)

```
          .                                                      .
        .n                   .                 .                  n.
  .   .dP                  dP                   9b                 9b.    .
 4    qXb         .       dX                     Xb       .        dXp     t
dX.    9Xb      .dXb    __                         __    dXb.     dXP     .Xb
9XXb._       _.dXXXXb dXXXXbo.                 .odXXXXb dXXXXb._       _.dXXP
 9XXXXXXXXXXXXXXXXXXXVXXXXXXXXOo.           .oOXXXXXXXXVXXXXXXXXXXXXXXXXXXXP
  `9XXXXXXXXXXXXXXXXXXXXX'~   ~`OOO8b   d8OOO'~   ~`XXXXXXXXXXXXXXXXXXXXXP'
    `9XXXXXXXXXXXP' `9XX'   DIE    `98v8P'  HUMAN   `XXP' `9XXXXXXXXXXXP'
        ~~~~~~~       9X.          .db|db.          .XP       ~~~~~~~
                        )b.  .dbo.dP'`v'`9b.odb.  .dX(
                      ,dXXXXXXXXXXXb     dXXXXXXXXXXXb.
                     dXXXXXXXXXXXP'   .   `9XXXXXXXXXXXb
                    dXXXXXXXXXXXXb   d|b   dXXXXXXXXXXXXb
                    9XXb'   `XXXXXb.dX|Xb.dXXXXX'   `dXXP
                     `'      9XXXXXX(   )XXXXXXP      `'
                              XXXX X.`v'.X XXXX
                              XP^X'`b   d'`X^XX
                              X. 9  `   '  P )X
                              `b  `       '  d'
                               `             '

           mmmmmm        mmm    mmmmm    mmmmmmmm      mmm
           ##""""##     m###   #""""##m  """""###     m###
     mmm#  ##    ##    #" ##        m##      ##"     #" ##   #mmm
 mm#"""    #######   m#"  ##     #####     m##"    m#"  ##     """#mm
 ""#mmm    ##    ##  ########       "##   m##      ########    mmm#""
     """#  ##mmmm##       ##   #mmmm##"  ###mmmmm       ##   #"""
           """""""        ""    """""    """"""""       ""
```
