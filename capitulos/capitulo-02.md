---
title: "Capítulo 02 - Herramientas para medir la Web Performance"
description: Describimos las múltiples heramientas que usamos para analizar y monitorizar el rendimiento web de nuestros sitios.
date: 2022-10-02
layout: layouts/post.njk
---

En este capítulo vamos a hablar sobre herramientas para medir la web performance. Cada maestrillo tiene su librillo y hay multitud de opciones a la hora de tomar métricas de performance que cubrimos en este podcast.

<iframe loading="lazy" style="border-radius:12px"
    src="https://open.spotify.com/embed/episode/4yEX0mYbaZuvS1Zk8pu9ZQ" width="100%" height="152"
    frameBorder="0" allowfullscreen=""
    allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"></iframe>

## Temas
- Repaso a herramientas RUM y de Lab test para evaluar el rendimiento de una web. Explicamos:
    - Lighthouse
    - CrUX
    - PageSpeed Insights
    - WebPageTest
    - DebugBear
    - Calibre
    - SpeedCurve
    - New Relic
    - Dynatrace
    - Datadog
    - mPulse de Akamai
    - Vercel Analytics
    - Google Analytics
    - Librería [web-vitals](https://developers.google.com/codelabs/chrome-web-vitals-js)

## Actualidad

- [Google elimina HTTP/2 Server Push a partir de Chrome 106](https://developer.chrome.com/blog/removing-push/)
- [Amazon CloudFront soporta HTTP/3](https://aws.amazon.com/about-aws/whats-new/2022/08/amazon-cloudfront-supports-http-3-quic)
- [Novedades de Performance en Chrome 105](https://developer.chrome.com/blog/new-in-devtools-105/)
- [Curso de web performance gratuito de Scott Jehl (Catchpoint)](https://www.webpagetest.org/learn/lightning-fast-web-performance/)
- [DebugBear introduce in plan de precios más económico](https://twitter.com/DebugBear/status/1572597207463006211)
- [DebugBear añade Request Chain - Flechas en el waterfall de peticiones](https://twitter.com/mattzeunert/status/1571898981772312581) y [tips para añadir fetchpriority="high" para mejorar LCP](https://twitter.com/DebugBear/status/1572616305102180353).

## Eventos y conferencias

- [performance.now()](https://perfnow.nl/): Conferencia sobre web performance en Amsterdam.
- [Next.js Conf](https://nextjs.org/conf): Conferencia sobre Next.js de la gente de Vercel.
- [PWA Summit](https://pwasummit.org/): Charlas y workshops centrados en Progressive Web Apps.
- [Jamstack Conf](https://jamstack.org/conf/): Presentaciones y workshops sobre arquitectura de de desarrollo web moderno.

## Transcripción

**Jose**: Bienvenidas y bienvenidos al capítulo número 2 de WebPerfImpacters. El podcast sobre web performance en el que encontrarás toda la actualidad, recomendaciones y buenas prácticas para conseguir un rendimiento 100. Mi nombre es José Manuel Pérez. Y en el capítulo de hoy me acompaña Estela Franco. Hola, Estela.

**Estela**: Hola, ¿qué tal?

**Jose**: Muy bien, y Joan León. Hola Joan. 

**Joan**: Muy buenas, ¿qué tal?

**Jose**: Perfecto. Vamos a hablar hoy sobre herramientas para medir la web performance. Cada maestrillo tiene su librillo y hay multitud de opciones a la hora de tomar métricas de performance que vamos a cubrir hoy. Pero antes vamos con noticias breves de actualidad.

**Estela**: Estupendo. Pues empiezo yo trayendo una noticia y es que Google eliminará soporte para HTTP/2 Server Push a partir de Chrome 100. Vale, ¿qué es esto del Server Push? Lo que nos permitía es enviar de forma pro activa los recursos que necesita nuestra web para poderse renderizar en vez de esperar a que el navegador los descubra y los solicite. Esto generaba ciertos problemas y luego al final, pues es complicado medir la mejora de rendimiento que esto nos supone, con lo cual, pues no se ha estado utilizando mucho. Y viendo todos los sitios que van con HTTP/2 se estima que sólo el 1,25% estaban utilizando esta feature.

Y al final hay también resultados mixtos. Hay quien dice que funciona mejor, quien dice que funciona peor. Pero bueno que en muchos casos puede incluso ser malo para performance. Si hacemos preload de todo, prefetch de todo, al final si todo es importante, nada es importante, ya lo sabemos. Y bueno, pues ahí hay sentimientos encontrados en como utilizar esto Y luego, en HTTP/2 realmente esto no está implementado, aunque este la especificación. Y al final, pues digamos que está retirado. Entonces, al volver a ejecutar más recientemente un análisis de todo esto, los sitios lo están utilizando todavía menos. Es ya prácticamente la mitad. Estamos hablando de 0,7 % vs 1,25% que se estimaba antes.

¿Qué pasa también con esto? Que hay algunos CDNs que esto te lo implementan y es una funcionalidad que tú tienes de forma practiva por parte del CDN como pasa, por ejemplo, con Akamai, con lo cual tú estás confiando en que Akamai de forma automática puede detectar cuáles son los recursos críticos de tu página web y hacer Server Push de los mismos. 

Vale, pues que sepáis que a partir de Chrome 106 esta funcionalidad no estará disponible para esos usuarios. ¿Qué alternativas nos da Google para todo esto? Pues tenemos principalmente 2. Por un lado, tenemos la opción de responder con 103 Early Hints a los recursos críticos, con lo cual cuando el navegador hace la petición del HTML, además de la respuesta 200 de de lo que es el propio HTML, automáticamente va a venir con los 103 de los archivos que necesita el navegador como pistas.

Aquí no estamos forzando un push, sino que realmente estamos delegando la responsabilidad de decidir al navegador. Esta es la opción que digamos que Google recomienda. Si no podemos hacer esto porque nuestro CDN no permite todavía responder con 103, podemos hacer preload de aquellos archivos que nosotros sabemos que son críticos. Repito, críticos para no volver otra vez a lo que comentábamos antes de precargar todo, y que hagamos preload de esos archivos para que facilite la carga de la página.

Y relacionado con esto, traigo otra noticia y es que hace un par de meses Cloudflare anunció que soportaba los Early Hints 103. Y ahora tenemos la novedad de que Cloudfront soporta HTTP/3 también. Son novedades buenas que nos ayudan a final a que mejore la performance de los diferentes recursos que necesitamos para nuestra página web. ¿Qué más novedades tenemos por aquí? 

**Joan**: Pues tenemos novedades en Chrome 105. Tenemos novedad tanto en la parte del navegador en sí como en la parte de las Developer Tools. Empecemos por las developer tools que son herramientas que tenemos para analizar la performance como "Performance Insights", la nueva pestaña que ya comentamos, que es un híbrido entre la pestaña "Performance", los insights que nos da Lighthouse. Tenemos una pestaña donde están aglutinando toda esa información y la están reordenando.Y se nota muchísimo que están desarrollando sobre esta nueva pestaña continuamente. Tiene de hecho el iconito de la probeta porque está en modo desarrollo, y hay cosas muy buenas, como por ejemplo, que están mejorando la información que nos ofrece para mejorar el Largest Contentful Paint (LCP). 

El Largest Contentful Paint es una de las métricas que tenemos en las Core Web Vitals que detecta el elemento más grande que está afectando a la página. Y luego, por otro lado, también están añadiendo cómo detectar el FOUT, que es la parte de repintado para mejorar el tema de las fuentes que cuando hacemos una carga de cualquier fuente que nos dé el sistema. El navegador previamente tiene las disponibles del sistema y cuando descarga la tipografía que queremos utilizar para ese site, hace un cambio. Pues están mejorando las métricas de esos cambios en la tipografía porque en muchos casos afectan al CLS, que es una de las métricas que últimamente estoy viendo que están dando bastantes problemas.

Y otra de las pestañas que tenemos disponibles es la del Recorder que nos permite grabar un user journey y hacer el flujo de navegación. El ejemplo que se utiliza para mostrar esta herramienta es en una tienda online. Buscar un producto, darle a añadir al carrito, ir al carrito, hacer el pago... ¿Cuál es la performance de todo ese flujo? Pues ahora esta herramienta ha añadido también, por ejemplo, hacer un hover para las interacciones y poder interactuar para desplegar el carrito y cosas así. Y poco a poco van mejorando.

Y por otro lado, en la parte de del navegador, hay un nuevo atributo, el "blocking". Los navegadores de forma automática ya detectan cuales son los recursos que son bloquenates como scripts y CSS que tengamos en el header del documento y ahora nos permite con este atributo blocking="render" establecer explícitamente cualquier recurso que nosotros desde desarrollo queramos que indicar que es render blocking, y lo prioriza.

Sigamos un poco la recomendación que nos decía Estela. Cuidado con ponerlo ahora en todo. Antes estábamos comentando posibles casos de usos de este atributo. Y es cuando estamos utilizando algún componente. Yo desarrollo en React, o incluso Next donde tenemos el componente Header para definir qué código queremos que se añada en el `<head>` entonces pasaría a ser render blocking. Pero en ese punto, podemos explícitamente añadirle el blocking="render" y de esa manera tener un poco más de control. Lo que nos dan de momentos son herramientas para ver cómo funcionan.

Y como dice Estela, si todo todo es importante, de repente todo deja de serlo porque no podemos cargar todo a la vez.

**Jose**: Si to do es urgente, nada es urgente. Como cuando estamos priorizando nuestras tareas de donde el trabajo también.

**Joan**: Exacto. ¿Qué más tenemos José?

**Jose**: Pues hay un curso de web performance que lo acaban de hacer gratuito. Está ahora en WebPageTest. Es un curso que creó Scott Jehl hace un tiempo y antes era de pago. Pero Catchpoint, que es la empresa dueña de WebPageTest lo ha comprado y ahora lo ofrece de forma gratuita en su web.

Es en formato vídeo y está compuesto por varias lecciones y dura unas cuatro horas. Estoy hablando yo sobre él, porque creo que soy el único de los tres que no ha hecho este curso. Así que creo que Joan, Estela, habéis estado echando un vistazo a este curso o lo habéis completado.

**Estela**: Yo lo tengo a medias. Yo, como todo lo empiezo todo, pero luego me faltan horas al día para acabarlo todo. Pero sí que le echado un vistazo. 

**Joan**: Yo soy como Estela que lo empecé. Quizás llevo más de la mitad. Tengo vídeos pendientes de ver, pero además, soy las las personas que pagó por él. Ese ansia, de querer estar siempre a la última, pues me pudo y lo compré.

Pero bueno, realmente no era un coste muy alto. Evidentemente, que sea gratuito es, es muy positivo para la comunidad. Así que os invitamos a que le echéis un rato y lo podíais completar.

**Jose**: Muy bien, está bien dividido en varias secciones. Así que si sólo se interesa una parte de de ellas, podéis ver esos vídeo directamente.

También podéis obtener un certificado al final del curso. Y eso, duran las cuatro horas. Así que si encontráis hueco entre vuestro agenda completa estos días, podéis echar un vistazo.

Y quería hablar también sobre unas novedades de las herramientas que usamos para monitorizar web performance de las que vamos a hablar hoy un poco más. Pero, queríamos destacar que DebugBear ha añadido un plan reducido cuesta $29 al mes, $25 si se hace el pago anual y siguen ofreciendo un período de prueba de 14 días en todos sus planes. Y lo bueno es que este plan se añade a otros que había antes que empezaban en $99. Así que de $99 pasaba $29 y ya no tenemos mucha excusa para intentar probar estas herramientas tanto por el período de prueba como por el coste bastante más bajo.

Y también decir que han añadido un par de features que las encuentro bastante interesantes. Una es poder ver en una cadena de peticiones, tenemos en la vista de waterfall de las peticiones, muchas veces es complicado saber exactamente qué petición está haciendo que el navegador solicite otro recurso. A veces lo sabemos un poquito mirando la vertical, viendo cuándo acaba un recurso cuando empieza el siguiente, pero DebugBear ha añadido flechas para saber exactamente qué recurso está haciendo que se cargue otro recurso. Entonces podemos identificar muy fácilmente cuáles son los paths y cuál es el critical path, e intentar optimizar esos recursos que están dentro del critical path que está determinando cuándo se carga nuestra web.

Y también van a mostrar oportunidades para mejorara el largest Contentful Paint porque en algunas ocasiones hacemos un lazy loading de una imagen grande, por ejemplo, y esa imagen puede acabar siendo el elemento LCP. Al hacer la carga con lazy load la prioridad de carga es baja, pero luego cuando el navegador detecta que esta imagen va a estar en la parte visible lo cambia.

Entonces, gracias a saber cuándo un recurso se está cargando con baja prioridad y el navegador lo cambia a alta, podemos nosotros directamente darle un hint al navegador para que haga la carga ya directamente con alta prioridad.

Y por último, también hablando sobre planes de precios un poco más económicos. Hemos hablado en el pasado sobre SpeedCurve. Es una herramienta que dentro de las herramientas de medición de web performance, era un poco de las más caritas que empezaba sus planes en unos $119. Ahora también tienen un plan básico por $15 al mes, $12 si se contrata un plan anual. De nuevo es de agradecer tener estos planes porque nos da la oportunidad de probar durante un mes estas herramientas, hacer algunas pruebas, algunas evaluaciones en nuestro trabajo y de ahí sacar distintos insights e intentar luego hacer ya la contratación anual o apostar por la herramienta que más nos guste.

**Estela**: Quería añadir que me parece super útil porque muchas veces nos pasa esto, que a lo mejor tenemos claro que necesitamos una herramienta y es mucho más complicado conseguir esa contratación anual sin poder proporcionar esos insights. Con el tier, incluso con la parte de periodo de prueba, podemos monitorizar unas URLs específicas y poder decir ver todo lo que nos está aportando. Incluso si queremos extender ese período de prueba con un mes que estamos viendo que hay precios económicos y poder aportar realmente unos resultados mucho más completos para poder justificar muchas veces esa contratación anual. Porque a veces también nos pasa que la persona responsable de aprobar esa compra no puede verle el jugo y ver con esto qué estamos consiguiendo. Realmente nos facilita muchísimo nuestro trabajo de poder justificar la contratación de una herramienta.
...