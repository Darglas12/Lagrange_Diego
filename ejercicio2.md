#  Ejercicio 2 — Crear un sitio Jekyll con el tema *Lagrange* y desplegarlo en GitHub Pages

El objetivo de este ejercicio es crear un segundo sitio Jekyll usando un **tema externo**, en este caso **Lagrange**, configurarlo correctamente, personalizarlo y publicarlo en GitHub Pages en la URL:


##  1. Descarga o clonado del tema *Lagrange*

Tienes tres opciones permitidas en el ejercicio:

### Opción A (La que yo he escogido) — Fork del repositorio oficial
1. Ve al repositorio del tema (ejemplo: *jekyll-lagrange*).
2. Haz clic en **Fork** → se copiará a tu cuenta de GitHub.
3. En tu PC ejecuta:

```bash
git clone https://github.com/tu_usuario/lagrange.git
cd lagrange

```

![foto](/assets/img/Captura%20de%20pantalla%202025-12-04%20120042.png)

![foto](/assets/img/Captura%20de%20pantalla%202025-12-04%20120112.png)

##  2. Instalación de dependencias

Antes de usar Jekyll asegúrate de tener instalado:

```bash
sudo apt install ruby-full build-essential zlib1g-dev
gem install bundler jekyll

```
Dentro del proyecto:

```bash
bundle install

```
##  3. Estructura del proyecto

El tema Lagrange incluye normalmente:

_includes/
_layouts/
_sass/
_posts/
assets/
index.html
_config.yml
Gemfile

##  4. Configurar _config.yml

Modifica los datos mínimos:

```bash
title: "Gym en casa – Lagrange"
description: "Sitio Jekyll usando el tema Lagrange"
author: "Tu nombre"
url: "https://tu_usuario.github.io"
baseurl: "/lagrange"
theme: null         # obligatorio para usar temas externos

```
![foto](/assets/img/Captura%20de%20pantalla%202025-12-04%20124909.png)

##  5. Crear tus propios posts

En la carpeta _posts/, crea archivos con el formato correcto:

```bash
YYYY-MM-DD-nombre-del-post.md

```
Ejemplo:

```bash
---
layout: post
title: "Cómo crear un espacio de entrenamiento en casa"
date: 2025-12-04
categories: ejercicios
---

Contenido del post...

```
![foto](/assets/img/Captura%20de%20pantalla%202025-12-09%20104749.png)

![foto](/assets/img/Captura%20de%20pantalla%202025-12-09%20104907.png)

##  6. Probar el sitio localmente

Ejecuta:

```bash
bundle exec jekyll serve

```
Abre en tu navegador:

```bash
http://localhost:4000/lagrange/

```
Comprueba:

1. Páginas funcionando

2. Posts visibles

3. Rutas de imágenes correctas

##  7. Subir el sitio a GitHub

Por ultimo mediante los comandos:

```bash
git add .
git commit -m "Sitio Lagrange listo"
git push 

```

Subimos los cambios a github y automaticamente se crea la páguina en github pages