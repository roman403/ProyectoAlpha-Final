---
date : 2025-02-09T12:19:03+01:00
draft : false
title : "HUGO"
---

# Documentación con Hugo y GitHub Pages

## 1. Instalar Hugo

En Debian:

```bash
sudo apt update
sudo apt install hugo -y
```

Verifica la instalación:

```bash
hugo version
```

## 2. Crear un nuevo sitio con Hugo

```bash
hugo new site mi-documentacion
cd mi-documentacion
```

![](https://roman403.github.io/ProyectoAlpha-Final/temahugo.png)

## 3. Agregar el tema `hugo-tale`

El tema `tale` es una excelente opción para documentación porque ofrece una navegación clara y estructurada.

```bash
git init
git submodule add https://github.com/alex-shpak/hugo-tale.git themes/hugo-tale
```

Configura el tema en `hugo.toml`:

![](https://roman403.github.io/ProyectoAlpha-Final/temahugo2.png)


## 4. Estructurar la documentación en `.md`

Crea el directorio `content/docs` y agrega un archivo Markdown:

```bash
hugo new docs/introduccion.md
```

Edita `content/docs/introduccion.md` y agrega contenido:

![](https://roman403.github.io/ProyectoAlpha-Final/contenidohugo.png)


# Bienvenido a la Documentación

Este es un ejemplo de documentación con Hugo.


## 5. Configurar hugo.toml para documentación

Edita el archivo `hugo.toml` y agrega:

```toml
baseURL = 'https://roman403.github.io/ProyectoAlpha-Final/'
languageCode = 'es'
title = 'Mi Documentación'
theme = 'hugo-tale'

[params]
  BookTheme = 'light'
  BookSection = 'docs'
```

## 6. Compilar el sitio y probar localmente

```bash
hugo server -d
```

Visítalo en `http://localhost:1313/`.

## 7. Subir a GitHub

1. **Crea un repositorio en GitHub** (ej. `mi-documentacion`).
2. **Sube los archivos:**

```bash
git remote add origin https://github.com/tuusuario/mi-documentacion.git
git branch -M main
git add .
git commit -m "Inicialización del sitio Hugo"
git push -u origin main
```

## 8. Publicar la documentación en GitHub Pages

GitHub Pages requiere que los archivos generados estén en la rama `gh-pages`. Para hacerlo:

```bash
hugo -d docs
```

Agrega `docs` como directorio de publicación en `hugo.toml`:

```toml
publishDir = "docs"
```

Sube los archivos generados:

```bash
git add .
git commit -m "Publicación en GitHub Pages"
git push
```

En GitHub, activa GitHub Pages en la configuración del repositorio, seleccionando la rama `main` y la carpeta `/docs`.

### Enlace de la documentación

En github el repositorio creado, vemos el contenido subido de nuestra pagina en Hugo

![](https://roman403.github.io/ProyectoAlpha-Final/gihub.png)

Si vamos a ajustes -> páginas podemos ver la url de nuestra paginaweb para poder acceder 

![](https://roman403.github.io/ProyectoAlpha-Final/gihub2.png)

La url sería está:

![](https://roman403.github.io/ProyectoAlpha-Final/urlgihub.png)


### Enlace de la documentación

Para sincronizar los cambios que vayamos haciendo el local tendremos que hacer un commit y sincronizarlo con github para que se actualice nuestra página


![](https://roman403.github.io/ProyectoAlpha-Final/commit.png)

![](https://roman403.github.io/ProyectoAlpha-Final/sincronizar.png)