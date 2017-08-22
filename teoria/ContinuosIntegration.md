## Reaching true agility with continuous integration

Porque solo avanzas tan rápido como tus pruebas.

No hay nada que construya (o destruya) la agilidad como el compromiso del equipo con la integración continua (IC). Puede sonar inquietante (sobre todo si tu equipo aún está por acoger la IC), pero tenemos buenas noticias. Independientemente de las tecnologías que utilice el equipo, es probable que haya un marco de integración continua y pruebas automatizadas compatible con su base de código.

Invertir en IC se traduce en disponer rápidamente de feedback sobre los cambios del código. Tan rápido como "en unos minutos". Los equipos que se basan principalmente en pruebas manuales pueden recibir feedback en un par de horas, pero, en realidad, todo el feedback de las pruebas llegará un día, o varios días, después de cambiar el código. Para entonces, habrán tenido lugar más cambios, lo que convierte la resolución de errores en una expedición arqueológica en la que los desarrolladores tienen que excavar varios estratos de código hasta llegar a la raíz del problema.

    Definitivamente, eso no es rápido.
    
    Los equipos ágiles entregan software de calidad con rapidez, sin heroicidades ni marchas forzadas. Todo gracias a la IC

#### Proteger la calidad de la base de código

¿Quién no se ha descargado el último código fuente y resulta que no se compilaba o que tenía un error importante? 

¡Adiós a la productividad!

Hay dos formas de evitar esta situación:

* Compilaciones continuas: Compilar el proyecto en cuanto se realice un cambio. Lo ideal sería que la diferencia entre compilaciones fuera de una sola modificación.

* Automatización de pruebas: Validación programática del software para garantizar la calidad. En las pruebas se pueden iniciar acciones en el software desde la interfaz de usuario (ahora hablaremos más de este tema), o desde el servidor.

Piensa que estas dos prácticas son como la mantequilla y la mermelada: por separado, saben bien, ¡pero juntas mucho mejor! La integración continua aúna las compilaciones continuas con la automatización de pruebas. Así se garantiza que en las compilaciones se evalúe también la calidad del código.

Y no olvides que, para disfrutar plenamente de sus ventajas, el equipo también tiene que tener la disciplina de interrumpir el desarrollo y tratar las averías al instante. La energía que invierte un equipo (no nos engañemos: se trata de una inversión) en escribir pruebas y configurar la automatización será en balde si se deja que las compilaciones con errores caigan en el olvido. Proteger la inversión en IC y proteger la calidad de la base de código son sinónimos.

#### Flexibiliza las pruebas automatizadas

Las ejecuciones de IC constan de dos fases principales. El primer paso garantiza que el código se compile (o, dicho en lenguaje llano, encajen todas las piezas). El segundo paso asegura que el código funciona según lo previsto. La forma más segura de hacerlo es con una serie de pruebas automatizadas que validen el producto en todos los niveles. 

##### Pruebas unitarias

Las pruebas unitarias se ejecutan en un nivel muy bajo. Son la primera línea de defensa para garantizar la calidad.
* Ventajas: son fáciles de escribir, se ejecutan con rapidez y se asemejan enormemente a la arquitectura del proyecto.

* Inconvenientes: las pruebas unitarias solo sirven para validar los componentes principales del software; no reflejan el workflow del usuario, que normalmente entraña el funcionamiento conjunto de varios componentes.

Puesto que las pruebas unitarias indican cómo debería funcionar el código, los desarrolladores pueden revisarlas para ponerse al corriente sobre esa área del código concreta. 

##### Pruebas de API

El buen software es modular, cosa que permite separar mejor el trabajo entre distintas aplicaciones. Las API son el punto final en el que se comunican módulos diferentes entre sí, y las pruebas de API los validan realizando llamadas de uno a otro.

* Ventajas: normalmente son fáciles de escribir, se ejecutan con rapidez y modelan fielmente las interaciones entre las aplicaciones.

* Inconvenientes: en casos sencillos, las pruebas de API pueden ser exactamente igual que algunas pruebas unitarias.
Puesto que las API actúan como nexo entre los componentes de la aplicación, son de especial utilidad a la hora de preparar de una publicación. Cuando una compilación que aspire a publicarse haya pasado todas las pruebas de API, el equipo puede sentirse mucho más seguro al proporcionársela a los clientes. 

##### Pruebas funcionales

Las pruebas funcionales trabajan con áreas más amplias de código y muestran el workflow del usuario. En aplicaciones web, por ejemplo, HTTPUnit y Selenium interactúan directamente con la interfaz de usuario para probar el producto.

* Ventajas: hacen más probable encontrar errores, ya que imitan las acciones del usuario y prueban la interoperabilidad de múltiples componentes.

* Inconvenientes: son más lentas que las pruebas unitarias y, en ocasiones, arrojan falsos negativos, debido a la latencia de la red o a una interrupción momentánea de alguno de los servicios de los que depende.

Con frecuencia los equipos observan que, a medida que se acercan al workflow real del usuario, disminuye la velocidad de ejecución de las pruebas automatizadas. HTTPUnit es más rápido, ya que no es un navegador web en toda regla. Selenium solo funciona a la velocidad del navegador web, pero tiene la ventaja de ejecutarse en varios de ellos de forma simultánea. 

A pesar de estas desventajas, las pruebas funcionales tienen un gran valor y dan feedback mucho más rápido de lo que jamás podrían los evaluadores humanos.

Y hablando del rey de Roma...

Algunos evaluadores consideran las pruebas automatizadas una amenaza existencial. Este pensamiento es de poca visión de futuro, y no podría estar más lejos de la realidad. Al no tener que repetir soporíferas tareas de prueba, los evaluadores pueden dedicarse al análisis de riesgos, la planificación de pruebas y adquirir otras habilidades... ¡como aprender a programar! 

