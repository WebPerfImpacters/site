---
title: "Capítulo 01 - Experimental Metrics: Interaction to Next Paint - Entrevista a Núria Soriano de Codely TV"
description: Hablamos a fondo sobre la Core Web Vital Interaction to Next Paint (INP) y entrevistamos a Núria Soriano de CodelyTV.
date: 2022-08-15
layout: layouts/post.njk
---

Exploramos la nueva Core Web Vital, Interaction to Next Paint (INP) y entrevistamos a [Núria Soriano](https://twitter.com/nuria_codes), frontend en [CodelyTV](https://codely.com/).

<iframe loading="lazy" style="border-radius:12px"
    src="https://open.spotify.com/embed/episode/76a0CN1gijPRwWOGZ9jrI3" width="100%" height="152"
    frameBorder="0" allowfullscreen=""
    allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"></iframe>

## Actualidad

- [SpeedCurve - novedades de junio 2022](https://www.speedcurve.com/blog/product-update-june-2022/)
- [Soporte de AVIF en macOS Ventura y iOS16](https://twitter.com/jensimmons/status/1547693585922789381)
- [Release de Next.js 12.2](https://nextjs.org/blog/next-12-2)

## Eventos y conferencias

- [performance.now()](https://perfnow.nl/): Conferencia sobre web performance en Amsterdam.

## Transcripción

**Estela**: Bienvenidas y bienvenidos al capítulo número de WebPerf Impacters, el podcast sobre Web performance en el que encontrarás toda la actualidad, recomendaciones y buenas prácticas para conseguir un rendimiento 100. Mi nombre es Estela Franco y en el capítulo de hoy, como en el anterior, me acompañan al mando del podcast Joan León.

**Joan**: Muy buenas, qué tal? Muy bien, por aquí muy bien.

**Estela**: Y por aquí también estamos con José Manuel Pérez. ¿Qué tal, José?

**Jose**: Muy bien, encantado de estar aquí.

**Estela**: Pues un capítulo más. Ha pasado un poquito más de un mes desde nuestro capítulo 0, porque todo el mundo sabe que empezamos a contar en 0. Estamos a las puertas del verano para contar la actualidad que hemos tenido en este último mes y pico.

**Jose**: Pues podemos hablar de SpeedCurve, que es una herramienta para hacer monitorización de métricas de rendimiento. Hace poco anunciaron algunas novedades para interpretar los resultados más fácilmente y también, sobre todo, para actuar en ellos y conseguir mejoras. Hace aproximadamente un año crearon un dashboard específico para hacer el seguimiento de las Core Web Vitals y ahora, para cada una de ellas, proporcionan una lista de recomendaciones y potenciales mejoras. Por ejemplo, si el LCP (Largest Contentful Paint) es alto y tienes un CSS con mucho contenido que no utilizas,  pues te va a ofrecer reducir el CSS que no estés usando porque así se supone que puede mejorar el LCP porque el CSS es un elemento crítico. De la misma forma en el dasboard Improve, que muestra también potenciales mejoras, puedes ver a qué Web Core Vital afecta cada mejora. Intentando un poquito, no sólo explicar las métricas, sino cómo poder actuar sobre ellas.

**Estela**: ¡Qué bueno! Está genial entonces que no es como otras herramientas que únicamente muestra qué mejoras tienes con la información que te viene directamente de Lighthouse, sino que realmente aplican su capa de recomendaciones específicas. Yo es que la verdad, _shame on me_, es que no he utilizado todavía SpeedCurve. Joan, me parece que tú sí que lo has estado toqueteando, ¿verdad?
...