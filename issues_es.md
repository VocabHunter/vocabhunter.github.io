---
title: Cómo informar sobre un error
layout: page
permalink: /es/issues/
description: Cómo informar sobre un error o problema
image: /assets/VocabHunter-Issue.png
ref: issues
lang: es
---

Puedes ayudar informando sobre el mismo o incluso solucionando el problema que encuentres.

# Utiliza el "GitHub Issue Tracker"

El proyecto de VocabHunter usa el "GitHub Issue Tracker". En primer lugar, necesitas tener una cuenta en GitHub. Si no la tienes, puedes crearla [aquí](https://github.com/join).

Conéctate a tu cuenta de GitHub y ve a [VocabHunter Issues Page](https://github.com/VocabHunter/VocabHunter/issues). Allí podrás ver todos los comentarios que se reciben al respecto. Verifica en primer lugar si el problema que has detectado ha sido ya identificado previamente. Si no lo encuentras, puedes clickar en "New Issue" para informar sobre el error.

# Qué debes incluir en el informe del error

Por favor incluye toda la información relevante sobre el problema que puedas. La siguiente lista te dará una idea del tipo de información a incluir:

* Lista de pasos para reproducir el problema.
* Pantallazo para ilustrar el problema de manera visual.
* ¿Utilizas VocabHunter en Windows, Mac o Linux?
* Detalles sobre el texto que estas analizando si crees que es un dato relevante.
* El fichero `system.log`. Mira en la sección de abajo para detalles sobre cómo obtenerlo.

Por favor, no subas ningún material sujeto a copyright.

# Dónde encontrar el fichero "system.log"

El fichero `system.log` contiene información que puede ayudar a saber qué estaba haciendo VocabHunter cuando sucedió el problema. La localización de este fichero depende del sistema operativo que estés usando:

| Sistema Operativo  | Directorio                              |
|--------------------|-----------------------------------------|
| Apple OSX:         | `~/Library/VocabHunter/logs/system.log` |
| Microsoft Windows: | `%APPDATA%\VocabHunter\logs\system.log` |
| Linux:             | `~/.VocabHunter/logs/system.log`        |

# Solucionar problemas

VocabHunter es un software de Open Source y por ello recibe gratamente cualquier contribución a nivel de código. Si puedes arreglar un problema, por favor, envía tu solución a través de un [GitHub Pull Request](https://help.github.com/es/github/collaborating-with-issues-and-pull-requests/about-pull-requests).

{% include language.html %}
