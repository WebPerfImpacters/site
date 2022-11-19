---
title: Capítulo 00 - Piloto
description: Os damos la bienvenida al episodio 0. Hablamos sobre WebPageTest, Chrome DevTools y otras novedades.
date: 2022-06-05
layout: layouts/post.njk
---

Os damos la bienvenida al episodio 0 de un podcast con el objetivo de divulgar y dar visibilidad de la importancia de la **Web Performance** ⚡️ para mejorar la experiencia de usuarias y usuarios, y de cómo además puede aumentar la conversión en nuestros productos.

<iframe loading="lazy" style="border-radius:12px" src="https://open.spotify.com/embed/episode/7ImnPje93eZo1yrzaF1eML" width="100%" height="152" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"></iframe>

## Temas
- El auge de WebPageTest como herramienta para auditar web performance.
- Experimentos y oportunidades en WebPageTest y cómo acercar la web performance a otros roles en la empresa.
- Cómo la performance no es sólo cosa del frontend.
- La nueva pestaña Performance Insights en Google Chrome.

## Enlaces

- [WebPageTest](https://www.webpagetest.org/): Sitio web para hacer análisis de rendimiento web.
- [Chrome DevTools](https://developer.chrome.com/docs/devtools/): Herramientas de desarrollo de Chrome integradas en el navegador.
- [Performance Insights](https://developer.chrome.com/docs/devtools/performance-insights/): El nuevo panel para analizar la performance de tu sitio en Chrome.
- [Chrome Canary](https://www.google.com/intl/es/chrome/canary/): La versión experimental de Google con los cambios más recientes.
- [Conferencia Lazy Load](https://webdirections.org/lazyload/): Evento sobre web performance que tiene lugar los días 10 y 17 de junio.
- [No me da la vida](https://anchor.fm/no-me-da-la-vida): El podcast tecnológico de Alba Silvente y Miriam González.

## Transcripción

**Joan**: Muy buenas. Bienvenidas y bienvenidos al capítulo 0 o capítulo piloto de una iniciativa que ha salido a través de un grupo de personas que estamos bastante interesadas e interesados con el tema de la Web Performance, muy relacionado con la User Experience. Vamos a intentar dedicar cada uno de los capítulos a diferentes temas. Habrán secciones comunes como las de recursos o novedades que vayamos encontrando. Si hemos tenido acceso a algún evento que sea público o nosotros hayamos asistido a esos eventos, compartiremos experiencias y también eventos futuros para que podáis estar un poco al día.

Yo soy Joan León. Soy Frontend Engineer. Tengo muchas inquietudes sobre el tema de la web performance. Soy consultor de web performance, haciendo formaciones, y en el equipo hoy no están con nosotros Naiara Abaroa y Carmen Ansio, pero sí forman parte del equipo e irán aportando ideas y contenidos.

Y quienes sí están con nosotros, que ahora les doy paso para que se presenten, son Estela y Jose.

**Estela**: Hola, ¿qué tal? Pues aquí estamos, estrenando este podcast que llevábamos tiempo cocinando, pero todavía no habíamos cuadrado agendas para lanzarnos. Y como dice Joan, pues un poco aquí para poder compartir experiencias, recursos y todo lo que vayamos aprendiendo, ¿no? Yo soy Estela Franco. Soy Web Performance specialist y Technical SEO y con inquietudes con la web Performance desde hace tiempo. Al final también el SEO y la web performance han estado intrínsecamente relacionados desde hace muchísimos años y va evolucionando un montón. Va costando estar al día, con lo cual también es una cosa que vamos a ir aquí comentando. Y aquí estamos, con ganas de compartir. Y comentabas que tenemos por aquí también a José. Hola, José.

**Jose**: Hola, ¿qué tal? Pues nada, yo encantado de estar aquí y creo que es un super buen momento para estar hablando de Web Performance. Hay cantidad de novedades. Parece que se está moviendo mucho el tema y nada vamos a intentar cubrir todo lo que está ocurriendo. Yo trabajo como Business Engineer, que viene a ser un ingeniero que a la vez también está hablando con negocios que están usando las herramientas que desarrollo. Veo qué les preocupa a los negocios, cómo traducir estas métricas de web performance en métricas de negocio en, por ejemplo, conversiones o revenue.

**Joan**: De hecho creo que es una de las partes más complicadas la gente que venimos de Tech, que nos pueda gustar más o menos el tema de la performance y que tengamos esa inquietud, sobre todo mucho foco en la parte de la User Experience. La parte más complicada es venderlo a negocio y mostrarle lo importante que es y hacer ese match del esfuerzo, porque no es poco, que hay que hacer para invertir en web performance y que se vea cuál es el revenue y lo que realmente aporta. Por eso fichamos a Jose. Realmente es porque es el especialista y es el que nos dará un poquito de voz a negocio de que lo que queremos hacer no es porque simplemente nos guste, sino porque realmente es para ayudar a negocio.

**Estela**: En ese sentido la verdad es que Google nos ha ayudado bastante a coordinarnos. Porque desde hace dos años con el anuncio de la Core Web Vitals, la verdad es que el hecho de que te digan "oye que esto te va a impactar a SEO" ya te están diciendo que te va a impactar al negocio. Con lo cual, creo es una cosa que en general a todas y a todos nos ha ayudado bastante a, desde el sector tech, que a lo mejor ya sí que teníamos cierta conciencia de que hay que trabajar en web performance, alinearnos con negocio. Además, si no nos ponemos las pilas y la competencia lo va trabajando mejor que tú, pues te van a pasar por delante por lo menos en tráfico orgánico.

**Jose**: Sí, yo creo que es ahí cuando empezó a dejar de ser un juego para optimizar y hacer las páginas más rápidas, a empezar a ver cuáles eran las consecuencias. También hubo un proyecto de Google, AMP, donde hay muchas opiniones enfrentadas, pero sí que también consiguió que se hablara de tiempo de cargas de páginas en empresas que normalmente no estaban muy interesadas. Pero empezaban a interesarse, aunque fuera sólo por el posicionamiento.

**Estela**: Ahí sí que me tocó de primera mano cuando se lanzó todo el proyecto de AMP. Empecé a trabajar en un medio de comunicación cuando empezó AMP y, claro, fue una jugada de Google en plan de "si quieres salir en la caja de Google News, tienes que tener AMP". Y ya está, no hay más que hablar. Con lo cual era una forma también forzada de hacer que las empresas tuvieran que ponerse las pilas con eso.

**Jose**: Sí, y creo que también fue la principal queja entre muchos desarrolladores que igual tenían una página que iba bastante rápida, pero no había ninguna forma de ocupar ese espacio en el carrusel de arriba del todo.

**Joan**: Muy interesante. Bueno, pues me gustaría explicar las expectativas que tenemos sobre el podcast. Ya hemos comentado que queremos compartir recursos y estar al día. Nos sirve también a nosotros para guionizar todas las novedades que van saliendo, que últimamente no son pocas y compartirlas para que las tengáis. Iremos colgando todos los episodios en diferentes plataformas y [en nuestra propia web](/).

Una de las cosas que queremos comentar porque es muy novedosa, de hecho tiene tres días, el 1 de junio salió como novedad, WebPageTest Pro. Una nueva feature de la herramienta WebPageTest que todas y todos habéis utilizado si estáis relacionados con el tema de web performance. La verdad es que con unas features muy interesantes. Estela, ¿qué nos cuentas de las features?

**Estela**: Pues básicamente lo que nos permiten es hacer modificaciones no code de nuestra página web para poder hacer mejoras. En muchas auditorías de WebPageTest o Lighthouse lo que nos pasa muchas veces es que estimar la mejora esperada de según qué implementaciones es difícil. Y puedes más o menos, en función de la cascada de los diferentes recursos y cómo se cargan, hacer un brindis al sol y estimar ciertas cosas. Pero con esto, lo que nos permite es antes de implementarlo, antes de que el equipo lo implemente, con la propia herramienta en cuatro clicks te lo configuras para hacer las modificaciones en la propia plataforma, y ejecuta un test con esas modificaciones implementadas.

Y te hace una comparativa además. Te ejecuta en paralelo un test sin las modificaciones y otro con las modificaciones y te permite ver tanto video como resultados del test para ver la mejor estimación que puedes tener con esos cambios. Me parece un cambio brutal en lo que se puede hacer a nivel de auditorías y reportes. Cuando estás haciendo una lista de cosas que se pueden implementar, estimar el tiempo de mejora que esperas en según qué métricas es genial. ¿Lo habéis probado vosotros?

**Joan**: Yo no he tenido tiempo de dedicarle un rato porque me gustaría hacerlo con un par de sites que tengo fichados para justamente intentar sacarle un poco de jugo al test. Lo que estás comentando lo estaba haciendo hasta ahora con Google Chrome, con las Overrides. Ir a modificar manualmente, saber que si precargo esto, que si cambio el tamaño de una imagen... hacerlo de una manera muy, muy manual. Pero, evidentemente, requiere muchísimo esfuerzo y conocimiento, saber que estás haciendo. No es algo tan sencillo como lo que nos han ofrecido con la versión Pro, como comentas, a golpe de click, poder añadir precarga para LCP y las típicas recomendaciones que hace Lighthouse. Curiosamente no están utilizando Lighthouse. Esas recomendaciones son desarrollo y cosecha propia del equipo de WebPageTest. Poder implementarlas a golpe de click y volver a lanzar otro test para compararlo... Recordemos que los tests son accesibles, los podemos compartir, si me apuras podemos imprimir un PDF para pasarlo a quien tenga que decidir. Decir "oye, la mejora es muy, muy importante y habría que invertir recursos para mejorar esta parte".

Me parece que ha sido un paso de gigante. Ya tuvimos un pequeño cambio con la UI. Hicieron un rediseño de la web, que tenía muchísimos años. Es mucho más intuitiva. Añadieron toda la parte de las Core Web Vitals y las métricas de campo, todo lo que viene de Crux. Todo eso ya eran añadidos y features que daban un una calidad extra al producto, pero es esta última feature de la versión pro que me parece genial.

**Estela**: Totalmente. Es un salto de calidad. Ahí también quería comentar que no te hace falta la versión pro para poder probar alguna cosa. Con el tier gratuito te permite ver todo lo que podrías llegar a hacer con la pro. Te está detectando todas las oportunidades de mejora. Esas ya las tendrías. La lista de oportunidades a implementar te la da exactamente. En qué recursos podrías hacer preload o que podrías poner en async o defer. Con la versión gratuita, lo que te permite hacer es un primer test en poniendo como defer recursos que son render blocking pero first party. Está bastante limitado, pero con eso ya puedes ejecutar un test y ver la mejora esperada y todo lo otro que entraría con la versión Pro.

Lo que está también chulo es que la versión Pro tiene diferentes niveles en función de los test que vas a ejecutar al mes. No es en plan de "si pagas el primer nivel, tiene sólo cinco features para hacer el test, si pagas el segundo tienes más" No, no, ya con el primer tier ya de pago ya tendrías acceso a todas las mejoras que puedes hacer. Y te puedes hacer custom reports además de las recomendaciones que te da. A lo mejor, tú quieres probar una cosa que no es una recomendación propiamente dicha de la herramienta, pero que tú te quieras customizar. Por ejemplo "es que quiero cargar este otro script para ver qué tal funciona". Pues ahí te lo puedes customizar yañadir un script que ahora mismo no tenías para ver el impacto. Y sólo varía el número de tests que puedes hacer al mes.

Y la verdad que a nivel precio, me parece muy competitivo para las herramientas que hay en el mercado.

**Joan**: Totalmente. De hecho, esta mañana justo leía en el foro que tiene WebPageTest que preguntaban si esta feature la iban a hacer para las instancias privadas. Porque WebPageTest te permite con una API en la versión de pago, tener tu propia instancia privada que puedas desplegar en tus servidores, y le preguntaron sobre eso. Creo que es una buena pregunta, saber si van a tener esa feature en las instancias privadas. Es bastante probable que sí porque si son gente que está pagando una licencia es bastante probable que sí que lo puedan tener. Así que estoy expectante a ver qué responde.

**Estela**: Antes nos decía "behind the scenes" Joan que es "la herramienta". Hay en el mercado bastantes herramientas que utilizan directamente Lighthouse, con lo cual al final las recomendaciones que tienes, pues son las de Lighthouse. Que sí, que te ofrecen otras cosas como poder automatizarlo, poder ejecutar varios tests y que te dé la mediana... O sea, puedes tener diferentes opciones. Pero esto que trabajen en ellos con sus propias metodologías y sus propias recomendaciones y las modificaciones en la propia plataforma, creo que se ha diferenciado. Ya estaban bastante diferenciados en algunos aspectos, pero con esto se acaban de salir del mapa.

**Joan**: De hecho, justo antes de empezar lo comentábamos. La gente que nos dedicamos al tema de la performance, cuando tenemos que dar algún consejo, está la duda de qué podemos aportar más allá de lo que está diciendo Lighthouse. En las recomendaciones de Lighthouse podemos ver el JSON de configuración y, evidentemente, tienen muchísimos datos. Entonces pueden contrastar la consecuencia que tiene implementar esos cambios y Google siempre va a dar buenas recomendaciones. Pero son un número de recomendaciones limitadas y escenarios generalizados y hay veces cosas muy custom.

Ahora Estela comentaba que WebPageTest nos permite añadir nuestras métricas custom, porque realmente los productos no todas las partes son públicas. Tenemos muchos productos que son privados y esas partes son sensibles y no pueden exponerse a que se hagan un test de este tipo. Por eso la opción de utilizar esas instancias. Y con la experiencia que tienen durante años analizando páginas y analizando muchos datos, tienen su propia opinión y pueden aportar.

Lighthouse nos da recomendaciones pero no es "la verdad", simplemente es un punto de vista con unos datos y, en la mayoría de los casos, con el sesgo de que los datos vienen de Chrome. No tenemos las partes que vengan de Safari, no tenemos las partes que vengan de Firefox, todos los dispositivos iOS si no tienen Chrome instalado no están enviando datos. Hemos de ser conscientes de que hay un sesgo. El tener otros puntos de vista que aporten es muy interesante.

**Jose**: Siempre es positivo tener más actores que ofrezcan distintas herramientas para medir la performance. Es bastante interesante el salto cualitativo en WebPageTest, que había estado muchos años sin tocar. Y cómo lo compró Catchpoint y no se sabía muy bien lo que iba a pasar porque tampoco es una empresa que asociemos a web performance. Pero le han dado una vuelta y los están situando como líderes prácticamente. A mí me gusta mucho la funcionalidad que han sacado de experimentos y oportunidades porque la mayoría de estos experimentos son muy fáciles de implementar. Son como "quick wins" de hacer lazy loading o añadir algún atributo a los script... Son cambios bastante sencillos y se puede medir directamente en la herramienta cuál va ser el efecto.

No tienes que complicarte pensando en que para mejorar la performance te toca cambiar todo el stack. Hay una serie de cambios, relativamente sencillos, que pueden tener un impacto grande. Y me gusta que te ofrezcan formas de exponerlo y de que tú, como desarrollador, puedas proponerlo. O incluso cómo alguien que trabaje en equipos de marketing o en cualquier otro equipo que no tenga conocimientos técnicos demasiado avanzados puede usar esta herramienta y puede también sugerir a los equipos técnicos que hagan estos cambios que son bastante sencillos desde mi punto de vista.

**Joan**: Totalmente. Una de las cosas que me gustan y es que el hecho de llamarle "experiments" hace que sea bastante fácil de relacionar con los experimentos A/B tests que se suele hacer en cualquier producto. Sería ideal poder hacerlo justamente por eso, para hacer un test y ver si una feature tiene más conversión, si aporta más... hay un montón de cosas que se pueden analizar. Y creo que ese naming es una buena estrategia porque acerca a departamentos como marketing que tiene en su vocabulario "crear experimentos para hacer un test" más que las Core Web Vitals. LCP, CLS... empezamos con acrónimos y nos venimos arriba. Y a veces es complicado saber qué hay detrás de cada uno de ellos o incluso de cada una de esas métricas. Como dice Jose, hay que acercarlo a otros sectores que no sean tan tech, que les sea mucho más fácil demostrar que dependiendo de qué cambios se hagan se puede mejorar el producto. Evidentemente es un win total.

**Estela**: Yo aquí añadiré algo más. No todo puede ser maravilloso, fantástico y fácil. Y es que hay que recordar también que los experimentos y las cosas que nos recomiendan este tipo de herramientas y el tipo de implementación que podemos hacer está super enfocado en Front. Entonces, genial, vamos a poder mejorar la parte de Front, pero bueno, recordemos que luego también tenemos nuestros queridos amigos de Back y que ahí también se nos puede complicar un poquito la cosa. Y bueno, ahí es un poquito más complicado para rascar. Pero por lo menos, el tener la parte de Front, que ya es una gran parte y que es lo que nos puede estar retrasando el renderizado, etc, etc, es genial poder tener ayuda por lo menos en esta parte.

**Joan**: De hecho ahora en la parte de datos que está exponiendo Crux han añadido el Time to First Byte (TTFB), que de hecho esa es la métrica que afecta a todas. Nuestro TTFB que es la métrica que mide el primer byte de respuesta de servidor. O sea, hacemos una petición al servidor y si tarda 8 segundos en responder, nuestras métricas van todas detrás de esos 8 segundos. Evidentemente es un ejemplo bastante bestia. Pero este TTFB no es sólo en la primera carga. En backend consumimos APIs. Si esa API tarda en responder tarda en renderizar el componente. Incluso podemos tener side effects de que al haber componentes que tarda más en responder, como en local no teníamos ese problema, cuando están en producción podemos tener cambios de la estabilidad visual en la métrica CLS justamente porque de repente tarda en traer los datos. Y la web performance no es solo del frontend. Ahora mismo tenemos mucha carga en el frontend porque estamos creando webapps muy orientadas a cliente y tenemos mucha carga y muchas cosas por mejorar. Pero no es una cosa que venga solo del frontend, también está en backend. Si el backend tarda en responder, evidentemente degrada totalmente la experiencia al final.

**Jose**: Sí, todo suma.

**Estela**: Al final todas las aplicaciones que tengan que hacer el trabajo en cliente, que tengan contenido inyectado e hidratado por JavaScript, van consumiendo APIs y todo lo que te vaya tardando en llegar, por mucho que tú hagas preloads de imágenes y según qué cosas luego, al final, si lo que es la información que te tiene que meter el navegador tarda en llegar es que poco vas a poder hacer por frontend.

**Joan**: Yo he visto casos de hacer preloads de imágenes, pero que el TTFB de esa imagen fuera más de 1 segundo. Por mucho que hagas el preload de esa imagen, evidentemente si el servidor de media tarda en responder, pues allí estamos un poco vendidos desde el punto de vista de frontend. Y ahí es donde trasladamos esa issue. Vamos a backend, vamos a ver qué pasa en infraestructura. En este caso, quizás posiblemente sería el departamento más correcto. Qué pasa en ese TTFB con el que está respondiendo esa imagen. Igual está desarrollado para que devuelva la imagen y está haciendo un crop de la imagen al vuelo. Entonces igual hay que poner una cache entre medio... Se puede trabajar en varias estrategias que se escapan un poco de la parte front. La web performance va relacionada con mejorar la user experience y la user experience lo engloba todo. Es el producto, desde la base datos inicial hasta los pixeles que están pintando en los dispositivos.

**Estela**: Total, que estamos en todos los fregaos, es el resumen. Tocamos todos los palos.

**Joan**: A ver si conseguimos que alguien se una. De hecho, aprovecho para comentar una cosa. Iba a decir que a ver si tenemos un poco de expertise de backend que nos pueda aportar luz o experiencia sobre todo este tema. Pero lo podemos hacer a través de entrevistas. Porque una de las cosas que queremos hacer es hacer entrevistas en los capítulos. Y si por suerte podemos cuadrarlo y en cada episodio tenemos una entrevista pues sería genial. Y justamente la idea es ésa, traer personas que nos hablen de sus experiencias y de diferentes roles tanto en frontend, backend, UX, marketing... ir adquiriendo conocimientos para nosotros conocer sus experiencias y aprender y para compartirlos con la comunidad.

**Estela**: Totalmente, qué bueno. Poder compartir y también hacer un llamamiento que si alguien que nos está escuchando cree que puede aportarnos, que le gustaría compartir su experiencia o incluso un case study, escribidnos, hablamos y lo cuadramos.

**Joan**: Un llamamiento encubierto. Encubierto nada. Estáis invitadísimas e invitadísimos. Ojalá el problema que tengamos sea priorizar entrevistas. Realmente sería todo un lujo que pudierais participar y ayudarnos a crear un poquito de comunidad en todo este tema que nos apasiona y llegar a más gente. Así que me sumo al llamamiento de Estela y si alguien quiere participar con su experiencia, aunque le pueda parecer que puede aportar poco todo aporta.

**Estela**: Sí, porque esto es algo que nos pasa bastante también en el gremio. Muchas veces no compartes o no comentas alguna cosa nos pasa incluso entre nosotros dentro de nuestro grupo porque damos por hecho que la gente ya lo sabe. Y no siempre es así. Por eso este podcast para ayudar. Porque a lo mejor nosotros lo sabemos, damos por hecho que todo el mundo lo sabe y no siempre es así. Con lo cual es genial poder compartir con otras personas que estén interesadas en todo lo que es la web performance. Animar a todo el mundo a que quiera compartir pues que se nos sume y cuadramos agendas.

**Joan**: Dándome un poco por aludido, quien me conozca un poco sabrá que soy muy activo en compartir recursos. Me gusta muchísimo compartir recursos y hay veces que me freno de compartir depende qué cosas pensando, lo primero, en no ser pesado (Joan siempre nos está bombardeando con recursos) y la otra de que igual hay gente que ya lo sabe.

Incluso me he encontrado eso en el día a día en el trabajo y hacer algo en concreto con las developer tools y un compañero preguntarme ¿cómo has hecho eso? Y yo: ah, pues esto se hace así y así. Ah, pues no lo sabía. Y cosas que tenemos tan interiorizadas que es difícil saber si la otra persona lo sabe o no.

La iniciativa de este podcast es justo eso y la apoyaremos también con algunos artículos. Sobre todo la recopilación de enlaces que hagamos en el propio episodio las tendréis disponibles en la web. E intentaremos dar un poquito de visibilidad a algunos temas en concreto con algún artículo para que lo tengáis disponible. Y a través de redes ([@WebPerfImpacter](https://twitter.com/WebPerfImpacter)) podéis lanzarnos las preguntas que queráis y las iremos resolviendo. Así que escuchamos vuestras propuestas.

**Jose**: En web performance el primer paso de reconocer que no puedes saberlo todo y no puedes estar al día. Al final necesitas de gente que te diga que está usando, cuáles son las herramientas que emplean cada día e intentar buscar entre toda la paja la herramienta o la nueva feature que de verdad va a ayudarte a hacer tu trabajo mejor. Yo creo que ahí podemos hacer un gran esfuerzo porque es, de verdad, muy, muy difícil mantenerte al día, leer con todos los cambios que hay en Chrome cada vez que hay una nueva versión o en alguna de estas otras herramientas que estamos empleando. Así que vengo aquí un poco también como terapia para darme cuenta de que no todos estamos a la última. Al final tenemos trabajos que hacer, tenemos vida después del trabajo y queremos ayudarnos a estar un poco todos al tanto. Cada uno aportando lo que ha visto que funciona y compartiendo en comunidad.

**Joan**: Totalmente. Hablando de las developer tools, en la versión 102 de Chrome han añadido una pestaña de Performance Insights. Tiene un icono de una probeta y está en modo experimental. Realmente es una herramienta muy interesante. Es como una mezcla entre las recomendaciones que da Lighthouse y la pestaña de Performance donde tenemos el gráfico de la red y los recursos. En la pestaña de Performance, podemos ver qué cuál es el CLS y qué elemento del DOM es el CLS, qué elemento del DOM es el Last Contentful Paint (LCP) y nos lo selecciona. Pues aquí está haciendo lo mismo y al mismo tiempo en la parte derecha tenemos un sidebar donde no está dando información de ese elemento. Echadle un ojo porque es una herramienta interesante.

**Estela**: Lo que he de decir aquí es que los pantallazos que saca de los cambios en el CLS es mejorable. Me es muy complicado entender el cambio comparándolo, por ejemplo, con lo que hace WebPageTest, que tienes una animación con el hover que ves realmente el cambio que ha habido, el componente que se ha movido, lo que sea. Con las páginas con las que he probado la nueva pestaña de las Chrome DevTools... bueno. Entiendo que esté en experimental porque eso yo creo que le pueden dar una vueltecita.

**Joan**: Yo creo que sí. De hecho, este tipo de funcionalidades lo que hacen es que siempre se están publicando en Chrome Canary, que es la versión de Chrome que se va haciendo en desarrollo. Y cuando hacen una build para probar, está expuesta y la podemos descargar para utilizarla, puede ser que tenga algún bug y pete porque es experimental, no ha pasado por el departamento de QA y no se recomienda como navegador principal. Pero sí es interesante para estar al día y ver este tipo de pruebas.

**Jose**: Yo aún estoy jugando con la herramienta, porque me cuesta ver cómo se diferencia de otras pestañas dentro de las mismas Developer Tools como Performance o incluso Network. Tengo que investigar un poquito. Seguramente hay una razón por la que han creado esta otra visualización y habrá algunas unas cosas que se identifican muy fácilmente ahí.

**Estela**: La han hecho un poquito más user friendly, para un user no técnico, visualmente me parece un poquito más amigable que ponerte a navegar por la pestaña, por ejemplo, de Performance, que es bastante tediosa y bastante densa. Tengo la sensación de que han hecho una cosita intermedia de querer tener más granularidad en el detalle de las cosas sin llegar a ser excesivamente técnica. Es la sensación que me da con lo que la he probado y es opinión completamente personal.

**Joan**: Es justo lo que comentaba, que es una mezcla entre la pestaña de Performance y el report de Lighthouse para poder tenerlo todo en un mismo sitio. Y lo que antes quería comentar era que, cuando abren este tipo de features, en los grupos de Google Developer Experts y Google Developer Groups nos dan acceso para poder probarla, y hay reuniones para pedirnos feedback. Y luego, cuando creen que está lo suficiente madura, a nivel funcional quizás está verde para el objetivo al que quieren llegar, pero cuando está relativamente madura, ya la ofrecen como experimental. Entonces ahí es cuando tienen el feedback del resto de la gente. De hecho, hay una lista de distribución donde ya están hablando de esto (esto me ha dado un fallo, esto no).

Una de las cosas que yo vi es que intentar hacer zoom en el timeline da unos saltos muy bestias, pierde el foco, no se queda donde tienes la línea temporal. Realmente, todavía les queda trabajo para hacer. Pero entiendo que es eso, que es ir a buscar algo más visual, más friendly como comentaba Estela y acercarnos justamente a otro target quizás no tan técnico, pero no dejamos de estar en las developer tools, que por norma general las solemos abrir siempre las personas técnicas.

**Estela**: A lo mejor hay que hacer que la gente de negocio aprenda a abrir las developer tools. Ahí lo dejo.

**Joan**: Sí, sí, sí.

**Estela**: Ya saben utilizar herramientas como Pagespeed Insights. Ya los hemos ido acercando un poquito, así que a lo mejor el siguiente paso es enseñarles el shortcut para que abran las developer tools.

**Joan**: Ya veo cuál es el speach.Les hemos enseñado a utilizar el Pagespeed Insights. Ahora les decimos: ¿sabes que lo tienes en el navegador?

**Estela**: Es el siguiente paso.

**Joan**: Le damos el shortcut. "Ooooh!". Es una manera también de empoderarles y decirles: "mira, si quieres apoyar tu argumento desde el punto de vista de defender algo en lo que quieres que el departamento técnico pueda empezar a trabajar o priorizarlo, tienes herramientas para hacerlo". Y realmente aprender a utilizarlas nunca está de más.

**Estela**: Bueno, como tenemos a Jose aquí como persona que habla con gente de negocio, ya lo tenemos aquí para que haga de betatester con la gente de negocio para que les ofrezca las developers tools.

**Jose**: No sé. Cuando dice Joan que no está de más... Es que también supongo que tienen muchísimas cosas encima de la mesa, igual que nosotros también como desarrolladores, que no sólo jugamos con la developers de Chrome hacemos algunas otras cosas. Pero sí, en general, todo lo que sea exponer datos complejos de una forma fácil, ya sea con un Lighthouse o como decía Estela, por ejemplo, los Insights que hay ahí a la derecha dentro de la pestaña de Performance, están bastante bien. Eso, por ejemplo, no aparecía en otras pestañas y es una forma fácil de capturar los problemas que están pasando.

Por lo menos que tengan acceso a determinada funcionalidad les dé un gráfico, números, iconitos verdes, amarillos, rojos. Algo que sepan ellos que hay un problema sin necesariamente tener que llegar al nivel bajo del todo de saber lo que está ocurriendo, por qué está ocurriendo, protocolos, formatos de imágenes... No deberían tener que preocuparse de eso. Por lo menos saber que está pasando algo para que, si nadie más lo ha visto en la empresa, lo puedan empezar a mover.

**Estela**: Claro, tener las pistas.

**Jose**: Sí. Idealmente todos los equipos de desarrollo deberían tener unas métricas que están evaluando y deberían recibir una notificación cuando hay una regresión. En la práctica sabemos que eso no ocurre muy a menudo. Si hay formas de empoderar a otros departamentos para que encuentren problemas y puedan empezar a mover la conversación, creo que eso es siempre bienvenido.

**Joan**: Porque lo de explicarles que si abren las developer tools las conversiones aumentan, puede estar mal.

**Jose**: Sí, eso está mal. Bueno, si dices "puede", puede que aumenten. Mientras no digas que van a aumentar, puede que aumenten, puede que no.

**Joan**: No, no he leído un estudio donde explicaban que posiblemente, si se abren las developer tools 8 veces al día, las conversiones pueden llegar a crecer.

**Jose**: "Los equipos de desarrollo que abren mucho las developer tools funciona mejor". Este tipo de herramientas están muy bien. Vamos a intentar desgranarlas poco a poco y, si las hemos usado para un problema en concreto y las hemos encontrado muy útiles, vendremos a compartirlo.

**Joan**: Totalmente. Como capítulo piloto y cero está bastante bien. Una de las cosas que haremos es hablar de los eventos pasados y próximos. Vamos a empezar con el próximo que es el Lazy Load que es el día 10 y 17 de junio, son dos sesiones y no perdáis la ocasión porque realmente el lineup que tienen está muy bien y los temas bastante interesantes. Al estar bastante al día con temas de performance y herramientas hay veces que es un poco difícil que en una conferencia de este tipo, hablo al menos por experiencia personal, me sorprendan con algo muy novedoso porque estoy bastante al día siguiendo todo.

Pero sí que me gusta cuando se está hablando de temas de cultura, de cómo implementar la performance de la cultura, cómo utilizar la infraestructura (AWS, Fastly, Google, el Edge Computing de Akamai o los workers de Cloudflare). Esta parte de infraestructura, que está más allá de lo que es el frontend, la verdad es que sí que me llama la atención. Pero también es interesante las las experiencias de cómo implementar la cultura de web performance en la empresa y los performance budgets, que da para un episodio qué son exactamente y cómo podemos trabajarlos, y la respuesta es algo así muy SEO: depende porque evidentemente cada producto tiene sus budgets, cada producto tiene su número de requests, su número de recursos... es complicado. Echad un ojo a Lazy Load está en [webdirections.org/lazyload](https://webdirections.org/lazyload/). No es presencial, sino online, y luego tenéis acceso a las grabaciones. Así que ésa es nuestra recomendación de evento para el episodio de hoy.

**Estela**: Totalmente. Yo tengo ganas de verlas porque a lo mejor hay cosas que ya estás al día y no te sorprenden, pero siempre a lo mejor hay un case study o temas más de acercamiento a business o infraestructura. Son temas que a lo mejor si no estás tan al día siempre sacas chicha interesante para tener ideas o ver de qué manera puedes implementarlo en tu empresa y siempre está bien.

**Joan**: He dedecir que esta edición en concreto es bastante de infraestructura. Es como el next level, salir de justo el server y la web app que se está desarrollando. De hecho, esto acerca muchísimo a reducir ese primer tiempo de respuesta (Time To First Byte).

**Estela**: Es que da para hablar, porque todo lo que se puede hacer con todo el tema de edge es una barbaridad.

**Joan**: Sólo por dejarlo así para no dejarlo en incógnita, es una capa de la infraestructura que está más cercana a los dispositivos.

**Estela**: Y ya no es sólo CDN de que estén ahí cacheadas las cosas. Es que ya hoy en día tienes muchas opciones para hacer ahí en esa capa y se abre un universo increíble que podemos aprovechar. Así que genial, genial.

**Jose**: Ya no tienes que tener un único servidor y que sea el que tenga que hacer todo el trabajo de generar todas las páginas dinámicas y ofrece todos los todas las APIs a todos los usuarios de todo el mundo.

**Joan**: Perfecto. Pues, ¿qué os parece si para ir cerrando hablamos un poco de periodicidad? Intentaremos que sea mensual porque creemos que es un tiempo prudente para primero nosotros tener tiempo para hacerlo o para tener cierta información y recopilar información de las novedades que pueden haber. Estamos grabando esto en junio, lo más seguro es que en pocos días esté publicado. Aún siendo mensual, es bastante probable que el mes de agosto.

**Estela**: Yo creo que una periodicidad mensual es suficiente para poder compartir y, sobre todo, lo que comentábamos de "no me da la vida con todo", con estar al día con todo, la verdad es que poder hacerlo mensual es una cosa más relajada para poder estar al día, incluso siguiendo el podcast.

**Joan**: Totalmente. De hecho, era un nombre bastante, bastante tentador, el de "no me da la vida en web performance" era un buen nombre. Alba y Miriam están haciendo un gran trabajo bajo ese eslogan. Me sorprende la cantidad de contenido que nos están compartiendo, y son dos titanas que son un referente.

Pues muchas gracias. Gracias por escucharnos si habéis escuchado hasta aquí y nos vemos en el próximo episodio.

**Jose**: ¡Hasta luego!

**Estela**: ¡Hasta la próxima!