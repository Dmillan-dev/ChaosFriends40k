# ChaosFriends40k

Proyecto académico de una web sencilla para una tienda y hermandad ficticia de
Warhammer 40.000. Sirve como tablón de anuncios de partidas, torneos y eventos.
Está realizado **solo con HTML**, sin CSS, JavaScript ni dependencias.

La tienda, su dirección, los eventos y las redes sociales son inventados.
El formulario es una muestra sin envío de mensajes ni reservas. La web no
permite publicar mensajes y no tiene vinculación oficial con Games Workshop.

## Tabla de contenido

- [Instalación](#instalación)
- [Estructura](#estructura)
- [Mejoras implementadas](#mejoras-implementadas)
- [Proceso paso a paso](#proceso-paso-a-paso)
- [Pull Requests de las mejoras](#pull-requests-de-las-mejoras)
- [Historial y comprobación](#historial-y-comprobación)
- [Entrega](#entrega)

## Instalación

```bash
git clone https://github.com/Dmillan-dev/ChaosFriends40k.git
cd ChaosFriends40k
```

Abre `index.html` en el navegador. También puedes descargar el ZIP desde GitHub,
extraerlo y abrir el mismo archivo. No hace falta instalar nada más.

## Estructura

```text
ChaosFriends40k/
├── .gitignore
├── index.html
└── README.md
```

Estos son los únicos archivos subidos a GitHub. La carpeta `.vscode/` existe
en local y está excluida. El `.gitignore` contiene únicamente:

```gitignore
.vscode/
.idea/
Thumbs.db
```

El enunciado, las copias de seguridad, las herramientas de trabajo y los
documentos de entrega se conservan en `.vscode/` y no se publican.

## Mejoras implementadas

- Menú de navegación con enlaces internos e información de la hermandad.
- Tabla semanal de horarios y tablón de torneos y eventos.
- Formulario de contacto con campos etiquetados y botón de envío desactivado.
- Pie de página con redes sociales ficticias y enlace para volver al inicio.

## Proceso paso a paso

El siguiente registro muestra el orden de creación del proyecto. Las mejoras
tienen su propia rama y su propio PR. La documentación se añade al final
directamente en `main`, sin crear un PR adicional.

### 1. Estructura básica y primer commit

Se parte del `index.html` básico del enunciado, con el título "Mi Proyecto Web",
el encabezado "Bienvenido/a a mi sitio web" y el párrafo de presentación.
Se crea la carpeta `.vscode/` y el archivo `.gitignore`.

Comandos para iniciar y conectar un repositorio desde cero:

```bash
git init -b main
git remote add origin https://github.com/Dmillan-dev/ChaosFriends40k.git
git add index.html .gitignore
git commit -m "Inicio del proyecto: estructura básica"
git push -u origin main
```

### 2. Menú de navegación

```bash
git checkout -b feature/menu
# Editar index.html para añadir el menú y la presentación.
git add index.html
git commit -m "Añadir menú de navegación y presentación de la hermandad"
git push -u origin feature/menu
```

Se crea el [PR #1](https://github.com/Dmillan-dev/ChaosFriends40k/pull/1)
desde `feature/menu` hacia `main` y se fusiona con un commit de merge.
Después se actualiza la rama principal local:

```bash
git checkout main
git pull --ff-only origin main
```

### 3. Tabla de horarios y eventos

```bash
git checkout -b feature/horarios-eventos
# Editar index.html para añadir la tabla y los anuncios.
git add index.html
git commit -m "Añadir tabla de horarios y tablón de torneos y eventos"
git push -u origin feature/horarios-eventos
```

Se crea y fusiona el [PR #2](https://github.com/Dmillan-dev/ChaosFriends40k/pull/2)
desde `feature/horarios-eventos` hacia `main`. Después:

```bash
git checkout main
git pull --ff-only origin main
```

### 4. Formulario de contacto

```bash
git checkout -b feature/contacto
# Editar index.html para añadir el formulario de muestra.
git add index.html
git commit -m "Añadir formulario de contacto de demostración"
git push -u origin feature/contacto
```

Se crea y fusiona el [PR #3](https://github.com/Dmillan-dev/ChaosFriends40k/pull/3)
desde `feature/contacto` hacia `main`. Después:

```bash
git checkout main
git pull --ff-only origin main
```

### 5. Pie de página

```bash
git checkout -b feature/footer
# Editar index.html para añadir el footer y las redes ficticias.
git add index.html
git commit -m "Añadir pie de página y redes sociales ficticias"
git push -u origin feature/footer
```

Se crea y fusiona el [PR #4](https://github.com/Dmillan-dev/ChaosFriends40k/pull/4)
desde `feature/footer` hacia `main`. Después:

```bash
git checkout main
git pull --ff-only origin main
```

### 6. Documentación directamente en main

Se crea en local este `README.md`, con la descripción, el índice, la estructura,
las mejoras y los pasos del proyecto. Se sube sin rama ni PR de documentación:

```bash
git checkout main
git add README.md
git commit -m "Añadir README con documentación y pasos del proyecto"
git push origin main
```

## Pull Requests de las mejoras

| PR | Rama | Mejora | Estado |
| --- | --- | --- | --- |
| [#1](https://github.com/Dmillan-dev/ChaosFriends40k/pull/1) | `feature/menu` | Navegación y presentación | Fusionado en `main` |
| [#2](https://github.com/Dmillan-dev/ChaosFriends40k/pull/2) | `feature/horarios-eventos` | Horarios y eventos | Fusionado en `main` |
| [#3](https://github.com/Dmillan-dev/ChaosFriends40k/pull/3) | `feature/contacto` | Formulario de contacto | Fusionado en `main` |
| [#4](https://github.com/Dmillan-dev/ChaosFriends40k/pull/4) | `feature/footer` | Pie de página | Fusionado en `main` |

Cada PR se fusiona conservando el commit de la mejora y creando un commit de
merge. Así se distinguen las ramas en el gráfico de Git.

## Historial y comprobación

Desde la carpeta del proyecto:

```bash
git status
git ls-files
git branch --merged main
git log --oneline --graph
```

El historial contiene **10 commits**: uno inicial, cuatro de mejoras, cuatro de
merge y uno final de documentación. Git muestra primero los más recientes.

`git status` debe mostrar `main` sincronizada y sin cambios pendientes.
`git ls-files` debe listar solo `.gitignore`, `README.md` e `index.html`.
Las cuatro ramas de mejoras deben aparecer como fusionadas en `main`.

Abriendo `index.html` puedes comprobar los enlaces del menú, la tabla de
horarios, los eventos, el formulario de muestra y el pie de página.

## Entrega

Repositorio: [Dmillan-dev/ChaosFriends40k](https://github.com/Dmillan-dev/ChaosFriends40k).

El PDF para el profesor se guarda solo en local en
`.vscode/entrega/entrega-chaosfriends40k.pdf`. Incluye el enlace al repositorio
y una captura de la salida de `git log --oneline --graph` con el historial final.
La imagen se conserva en `.vscode/entrega/historial-commits.png`.

Los archivos de entrega están excluidos y no se descargan al clonar el proyecto.
