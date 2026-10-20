---
title: "Lección 12 - Publica el sitio con GitHub Pages"
description: "Usa la aplicación GitHub Copilot para configurar un flujo de trabajo de Pages, revisar su solicitud de incorporación de cambios y comprobar que Space Quiz está disponible."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Publica Space Quiz para que todo el mundo pueda acceder a él mediante GitHub Pages. Copilot puede preparar el flujo de trabajo y guiarte durante el despliegue, pero tú debes revisar los cambios y confirmar que el sitio está disponible.

En esta lección vas a:

- pedir a Copilot que configure un despliegue de GitHub Pages.
- revisar el flujo de trabajo y la solicitud de incorporación de cambios antes de combinarla.
- seguir el despliegue y comprobar el sitio publicado.

## Escenario

Space Quiz ya está en un repositorio de GitHub, pero todavía hace falta una forma sencilla de probarlo. Publicar el sitio de un solo archivo con GitHub Pages lo hace accesible desde una URL pública sin añadir un servidor ni dependencias de ejecución.

## Pide a Copilot que publique el sitio

En la sesión de la aplicación Copilot para `space-quiz`, envía este mensaje:

```plaintext
Habilita GitHub Pages para este repositorio. Crea un flujo de trabajo de GitHub Actions que compile el sitio web si es necesario y lo publique en GitHub Pages. Añade un README que describa la aplicación y cómo ejecutarla localmente si todavía no existe. Crea una solicitud de incorporación de cambios con estos cambios y combínala cuando se superen las comprobaciones obligatorias. Supervisa el despliegue hasta que se complete correctamente y, después, indícame la URL final del sitio web publicado. Si no tienes permiso para habilitar Pages o combinar los cambios, dime exactamente qué debo aprobar o hacer; no informes de que ha terminado hasta que el sitio esté disponible.
```

![Diagrama en tres etapas: una solicitud de incorporación de cambios de space-quiz combinada; una ejecución correcta de GitHub Actions Deploy website con los pasos Build website, Upload artifact y Deploy to Pages; y Space Quiz publicado en yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este mensaje pide al agente que cree y combine una solicitud de incorporación de cambios y cambie la configuración de Pages del repositorio. Revisa el diff, los permisos de despliegue y las solicitudes de aprobación de GitHub antes de continuar.

## Revisa el flujo de trabajo y comprueba el despliegue

1. Confirma que el README solo se añade si el repositorio aún no tiene uno.
2. Revisa los cambios de la solicitud de incorporación de cambios, incluidos los pasos de compilación y despliegue del flujo de trabajo.
3. Combina los cambios solo después de que se superen las comprobaciones obligatorias de la solicitud.
4. Sigue la ejecución del despliegue de GitHub Actions hasta que se complete correctamente.
5. Abre la URL indicada y confirma que Space Quiz se carga.

Si el agente no puede habilitar Pages o combinar la solicitud, sigue las instrucciones concretas que te proporcione. No des la tarea por terminada hasta que el despliegue se complete correctamente y el sitio esté disponible.

## Resumen y siguientes pasos

Space Quiz ya está disponible como sitio publicado y has comprobado el despliegue en lugar de confiar únicamente en el informe del agente. Continúa con la [Lección 13: Repaso y próximos pasos][next-lesson].

[next-lesson]: ../13-review/
