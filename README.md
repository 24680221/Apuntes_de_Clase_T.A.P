# Apuntes_de_Clase_T.A.P
# Unidad I. 
# "Interfaz gráfica de usuario"
Introducción
-

El desarrollo de interfaces gráficas y el manejo de eventos constituyen una parte fundamental en la creación de aplicaciones modernas. A través de los componentes gráficos de control (como ventanas, botones, menús y campos de texto) los usuarios pueden interactuar de manera directa con el sistema. Cada acción realizada, ya sea un clic del ratón, la pulsación de una tecla o el cambio de estado de un elemento genera un evento que debe ser gestionado adecuadamente por el programa.

Comprender cómo funcionan los eventos, los modelos de emisor y receptor, y la organización de los componentes dentro de contenedores permite diseñar aplicaciones más dinámicas, organizadas y fáciles de usar. De esta manera, el manejo correcto de componentes gráficos y eventos garantiza una experiencia interactiva eficiente y funcional para el usuario.

1.1 Creación de Interfaz Gráfica para Usuarios
-

La interfaz gráfica de usuario (GUI, por sus siglas en inglés) es un programa informático que permite la interacción entre el usuario y un sistema mediante elementos visuales como íconos, ventanas, botones y menús. A diferencia de las antiguas interfaces de línea de comandos, la GUI ofrece un entorno visual intuitivo que facilita la comunicación con el sistema operativo. Ejemplos claros de entornos con interfaz gráfica son Microsoft Windows, el sistema de ventanas X en GNU/Linux y Aqua en macOS.

En el ámbito de la interacción persona–ordenador, la GUI representa el componente tecnológico que hace posible una experiencia amigable mediante el uso del lenguaje visual. Gracias a la manipulación directa —como hacer clic, arrastrar o seleccionar elementos— el usuario puede ejecutar acciones de manera sencilla y eficiente.

- Computación gráfica

La computación gráfica, también conocida como gráficos por ordenador, es una rama de la informática visual que utiliza computadoras para generar imágenes sintéticas o modificar información visual proveniente del mundo real. Uno de los primeros grandes avances en este campo fue el desarrollo de Sketchpad en 1962 por Ivan Sutherland, considerado un pionero en la gráfica por computadora.

Este campo abarca diversas áreas como el renderizado 3D en tiempo real (común en videojuegos), la animación digital, la edición de imágenes, los efectos especiales y el modelado para aplicaciones de ingeniería y medicina. Durante sus inicios, el desarrollo de la computación gráfica fue impulsado principalmente por el ámbito académico y el patrocinio gubernamental. Con el tiempo, la industria cinematográfica y televisiva comenzó a financiar ampliamente su avance al reconocer su potencial como alternativa a los efectos especiales tradicionales.

Se suele pensar que la primera película en utilizar gráficos por computadora fue 2001: A Space Odyssey. Sin embargo, en esta producción los efectos visuales fueron realizados principalmente mediante animación tradicional y efectos ópticos convencionales, ya que la tecnología digital aún estaba en sus primeras etapas.

- UI vs. UX

En el diseño digital es común encontrar los términos UI (User Interface) y UX (User Experience). Aunque están relacionados, cumplen funciones distintas:

1.-	Diseño UI: Se enfoca en la apariencia visual, los elementos interactivos y la organización estética de una aplicación o sitio web. Busca que la navegación sea atractiva y fácil de usar.
2.- Diseño UX: Se centra en la experiencia global del usuario, asegurando que pueda alcanzar sus objetivos de manera clara, eficiente y satisfactoria.
Mientras que la UI se ocupa de cómo se ve el producto, la UX se enfoca en cómo se siente y funciona durante su uso.

- Tipos de interfaz de usuario

Existen diferentes tipos de interfaces de usuario:

1.	Interfaz Gráfica de Usuario (GUI): Permite interactuar mediante íconos y elementos visuales usando mouse o pantalla táctil.
2.	Interfaz de Usuario de Voz (VUI): Utiliza reconocimiento de voz para ejecutar comandos, como ocurre con asistentes virtuales.
3.	Interfaz basada en menús: Presenta opciones organizadas en listas desplegables, como en cajeros automáticos.
4.	Interfaz táctil: Se basa en el contacto directo con la pantalla.
5.	Interfaz basada en formularios: Emplea campos de texto, casillas de verificación y otros componentes para recopilar información.

- Principios del diseño de interfaz de usuario

Un buen diseño de interfaz debe pasar casi desapercibido, permitiendo que el usuario navegue sin dificultad. Para lograrlo, se aplican principios fundamentales conocidos como las cuatro C:

•	Control: El usuario debe sentirse en dominio de la interfaz.

•	Consistencia: Los elementos deben mantener coherencia visual y funcional.

•	Comodidad: La interacción debe ser sencilla y natural.

•	Carga cognitiva: Se debe evitar saturar al usuario con información excesiva.

Además, es esencial que el diseño sea adaptable a diferentes dispositivos y tamaños de pantalla, que mantenga un buen contraste visual y que utilice imágenes de alta resolución.

- Accesibilidad en la UI

La accesibilidad es un aspecto clave en el diseño de interfaces. Todas las personas, incluyendo aquellas con discapacidades visuales o motoras, deben poder utilizar la interfaz sin obstáculos. Esto implica integrar herramientas de apoyo como lectores de pantalla y ofrecer configuraciones fáciles de encontrar para mejorar la experiencia de todos los usuarios.

- Herramientas de diseño de interfaz

Para crear interfaces efectivas, los diseñadores utilizan herramientas especializadas como:

•	Figma

•	Adobe InDesign

•	Sketch

•	Adobe XD

•	Balsamiq

Estas plataformas permiten crear prototipos interactivos, diseñar elementos visuales y probar la experiencia antes de su implementación final.

- Componentes principales de una GUI

Una GUI integra diseño visual y programación basada en eventos, ya que las acciones del usuario no pueden predecirse de forma lineal. Entre sus componentes más comunes se encuentran:

•	Ventanas

•	Botones

•	Campos de texto

•	Campos de entrada

•	Menús

•	Lienzo (canvas)

•	Marcos

•	Encabezados

Un ejemplo claro es la papelera de reciclaje presente en la mayoría de los sistemas operativos, cuya representación visual permite identificar fácilmente su función.

1.2 Tipos de Eventos
-
En programación orientada a objetos (P.O.O.), los eventos son el mecanismo mediante el cual una clase interactúa con otras clases o con el usuario. Un evento se genera cuando ocurre una acción específica, como presionar una tecla, hacer clic en un botón, mover el ratón o cambiar el tamaño de una ventana. En esencia, los eventos notifican que algo ha sucedido y permiten que el sistema responda de forma adecuada.

Cuando desarrollamos aplicaciones, especialmente aquellas con interfaz gráfica (GUI), es fundamental considerar el manejo de eventos. A medida que las aplicaciones se vuelven más complejas, no solo debemos manejar los eventos que afectan a nuestra clase, sino también crear nuestros propios eventos para que otras partes del programa puedan reaccionar ante determinadas acciones.

- Modelo Emisor/Receptor (Dispatcher/Listener):
El manejo de eventos se basa en el modelo emisor/receptor, también conocido como dispatcher/listener.

•	Emisor (Dispatcher): Es el objeto que genera o lanza el evento cuando ocurre una acción.

•	Receptor (Listener): Es el objeto que recibe el evento y ejecuta el código necesario para gestionarlo.

El programador define cómo se emiten los eventos y cómo se registran los receptores para que reaccionen ante ellos. Cada lenguaje de programación implementa su propio sistema para crear y manejar eventos.

- Eventos de Bajo Nivel y Eventos Semánticos

Los eventos pueden clasificarse en dos grandes grupos:

1. Eventos de Bajo Nivel
Son aquellos que representan interacciones básicas con los elementos de la interfaz gráfica. Se relacionan directamente con acciones físicas del usuario o cambios en los componentes. Algunos

ejemplos son:

•	Cambio de tamaño de una ventana.

•	Cambio de foco entre componentes.

•	Movimiento del ratón.

•	Presión de teclas del teclado.

Estos eventos describen acciones simples y específicas.

2. Eventos Semánticos

Son eventos de más alto nivel que representan acciones significativas dentro del modelo de la interfaz. No están ligados a un componente específico, sino al significado de la acción. Por 
ejemplo:

•	Ejecutar una acción (como enviar un formulario).

•	Cambiar el estado de un botón.

•	Seleccionar una opción de un menú.

Estos eventos encapsulan la intención del usuario, más allá de la acción física que la originó.

3.- Eventos de Foco

El foco indica qué componente está activo y listo para recibir entrada del usuario. Cuando el foco cambia de un componente a otro, se generan dos eventos:

•	focusLost(): Se activa en el componente que pierde el foco.

•	focusGained(): Se activa en el componente que recibe el foco.

Cualquier componente que pueda recibir entrada (como campos de texto o botones) puede generar este tipo de eventos.

4.- Evento de Teclado

Los eventos de teclado se producen cuando el usuario presiona una tecla. Generalmente, se utiliza un objeto escuchador como KeyListener para detectar estas acciones.

Cuando se presiona una tecla:

•	El componente que tiene el foco genera el evento keyPressed().

•	El objeto receptor identifica qué componente originó el evento.

•	Se ejecuta la acción correspondiente (por ejemplo, mostrar un mensaje en pantalla).

Evento de Ratón (MouseEvent)

Un MouseEvent ocurre cuando el usuario interactúa con el ratón. Esto incluye:

•	Hacer clic.

•	Doble clic.

•	Presionar o soltar un botón.

•	Mover el cursor.

•	Arrastrar un elemento.

Estos eventos son esenciales en interfaces gráficas, ya que gran parte de la interacción del usuario depende del uso del ratón.

1.3 Manejo de Eventos
-

El manejo de eventos es un proceso fundamental en la programación de aplicaciones interactivas, especialmente en aquellas que utilizan interfaces gráficas. Permite que el sistema detecte acciones del usuario —como hacer clic, presionar una tecla o cerrar una ventana— y ejecute una respuesta adecuada mediante controladores de eventos.

- ¿Qué es la gestión de eventos?

La gestión de eventos, en un sentido general, es la actividad profesional encargada de planificar, organizar y dirigir eventos, ya sean presenciales, virtuales o híbridos. Esta actividad es realizada por expertos capacitados y puede influir directamente en la reputación y el éxito de una empresa.

- Importancia de la gestión de eventos
Una correcta gestión de eventos puede:

•	Mejorar la reputación: Una buena organización fortalece la imagen de la empresa y fomenta la fidelidad de los clientes.

•	Propiciar el éxito: Puede generar mayor exposición, nuevas relaciones comerciales y una base de clientes más amplia.

•	Aumentar la satisfacción del cliente: Los asistentes satisfechos y recurrentes reflejan una 
gestión eficiente y bien planificada.

•	Garantizar retorno de inversión: Eventos bien organizados pueden ofrecer beneficios tangibles 
como posicionamiento de marca y nuevas oportunidades de negocio.

- Manejo de eventos en programación

En el ámbito de la programación, cuando un usuario interactúa con un componente (por ejemplo, al hacer clic con el ratón o presionar la tecla Enter), se crea un objeto llamado Event. En el sistema AWT de Java (Abstract Window Toolkit), el manejador de eventos recibe ese objeto y lo envía a través del árbol de componentes para que cada uno tenga la oportunidad de procesarlo antes de que el sistema lo ejecute definitivamente.

Desde la perspectiva de un componente, el sistema funciona como un filtro de eventos: el evento se genera y puede ser modificado, procesado o detenido antes de llegar a su destino final.

- Formas de reaccionar ante un evento

Un componente puede manejar un evento de distintas maneras:
1.	Ignorarlo: Permitir que el evento continúe su recorrido por el árbol de componentes.
2.	Modificarlo: Cambiar la información del evento antes de que siga propagándose (por ejemplo, convertir letras minúsculas en mayúsculas).
3.	Reaccionar ante él: Ejecutar una acción específica, como procesar el contenido de un campo de texto.
4.	Interceptarlo: Detener su propagación si el evento no es válido (por ejemplo, bloquear la entrada de un carácter incorrecto).
Modelo de delegación de eventos

El paquete java.awt.event contiene la mayoría de las clases e interfaces relacionadas con eventos en Java. Este sistema utiliza el modelo de delegación de eventos, que funciona de la siguiente manera:

•	Una fuente genera el evento cuando cambia su estado interno.

•	Uno o varios oyentes (listeners) reciben el evento.

•	Los oyentes procesan el evento mediante métodos específicos llamados controladores de eventos (event handlers).

Componentes y los eventos que generan

Algunos componentes del AWT y los eventos que producen son:

•	Button: Genera ActionEvent cuando se presiona.

•	Checkbox: Genera ItemEvent cuando se selecciona o deselecciona.

•	Choice: Genera ItemEvent al cambiar de opción.

•	List: Genera ActionEvent (doble clic) e ItemEvent (selección).

•	MenuItem: Genera ActionEvent al seleccionarse.

•	Scrollbar: Genera AdjustmentEvent al manipularse.

•	Componentes de texto: Generan TextEvent cuando se introduce un carácter.

•	Window: Genera WindowEvent cuando se abre, cierra, minimiza, maximiza o activa una ventana.

- Controladores de eventos (Event Handlers)

Un controlador de eventos es un método que define qué acciones deben ejecutarse cuando ocurre un evento. Cuando el evento se produce, el sistema invoca automáticamente los métodos asociados.

- Características importantes:

•	Un evento puede estar asociado a múltiples controladores.

•	Los métodos que manejan eventos pueden modificarse dinámicamente.

•	Permiten notificar situaciones especiales a otros objetos del sistema.

1.4 Manejo de Componentes Gráficos de Control
-

El manejo de componentes gráficos de control consiste en administrar los elementos visuales de una interfaz gráfica que permiten la interacción directa del usuario con la aplicación. Estos componentes generan distintos tipos de eventos cuando el usuario realiza acciones como hacer clic, escribir texto o manipular una ventana.

- Eventos generados por componentes gráficos
Algunos componentes generan eventos específicos según la acción realizada:

1.- List:
- Genera eventos de acción cuando se hace doble clic sobre un elemento.
- Genera eventos de elemento (ItemEvent) cuando se selecciona o deselecciona un elemento.

2.- Componentes de texto:
- Generan TextEvent cuando el usuario introduce un carácter.

3.-	Window:
- Genera WindowEvent cuando una ventana se activa, se cierra, se desactiva, se minimiza, se maximiza, se abre o se abandona.

Estos eventos permiten que la aplicación responda dinámicamente ante la interacción del usuario.

- Interfaces EventListener y clases Adapter

Muchas interfaces EventListener están diseñadas para recibir múltiples tipos de eventos. Por ejemplo, MouseListener puede manejar:

•	Pulsación de botón.

•	Liberación del botón.

•	Entrada del cursor.

•	Salida del cursor.

El problema es que, al implementar una interfaz, es obligatorio redefinir todos los métodos que declara, incluso si no se necesitan todos en la aplicación.

Para facilitar esta tarea, AWT proporciona clases adaptadoras (Adapter). Estas clases abstractas:

•	Implementan la interfaz correspondiente.

•	Incluyen todos los métodos con implementaciones vacías.

•	Permiten al programador sobrescribir únicamente los métodos que realmente necesita.

Esto simplifica considerablemente el manejo de eventos en aplicaciones gráficas.

- División de los componentes gráficos

Los elementos de una interfaz gráfica se dividen en dos grandes grupos:

1. Contenedores
Son componentes que pueden alojar otros componentes en su interior.
2. Componentes
Son los elementos individuales con funcionalidad propia.

- Existen distintos tipos de componentes:

•	Componentes atómicos

•	Componentes de texto

•	Componentes de menús

•	Componentes complejos

Elementos principales de una interfaz gráfica en Swing
En Swing, biblioteca gráfica de Java, los principales elementos de una interfaz son:

1.- Ventanas
Son elementos que contienen otros componentes y pueden moverse libremente por la pantalla.
- Tipos de ventanas:

•	Ventanas de aplicación: Contienen todos los elementos principales de la aplicación.

•	Cuadros de diálogo: Se muestran temporalmente para informar al usuario o solicitar datos.

•	Ventanas internas: Se utilizan dentro de la ventana principal para mostrar documentos o herramientas.

2.- Componentes
Son todos los elementos con identidad y funcionalidad propia dentro de la interfaz, por ejemplo:

•	Botones

•	Barras de desplazamiento

•	Etiquetas

•	Listas desplegables

•	Tablas

•	Árboles

No se consideran componentes los colores, líneas, píxeles o letras individuales.

3.- Controles

Son componentes que pueden recibir información del usuario mediante el teclado o el ratón. Los más comunes son:
- Botones
- Cuadros de texto
- Barras de desplazamiento

Estos controles generan eventos que pueden ser capturados y gestionados mediante controladores de eventos.

4.- Contenedores

Un contenedor es un componente capaz de incluir otros componentes en su interior. Los componentes que no pueden contener otros se denominan componentes atómicos.

5.- Menús

Los menús son elementos que contienen opciones organizadas verticalmente. Al seleccionar una opción, se puede:
- Abrir un submenú.
- Ejecutar una acción.

Existen:

•	Menús contextuales: Aparecen al hacer clic derecho sobre un elemento específico.

•	Barras de menú: Se ubican generalmente en la parte superior de la ventana de la aplicación.

Ya con toda la teoría entendida lo aplicaremos en un código  en el siguiente link esta completo el código y explicado, pero aquí brevemente daremos explicación del código de la calculadora realizada con la librería de flet:

1.- interfaz grafica
-
Primero se importó la librería de flet 
```Import flet as ft ```que es una herramienta que nos permitirá crear la interfaz grafica de usuario es decir una aplicación visual con ventanas, botones, textos.La función ```def main(page: ft.page):``` esta función creara la ventana principal que en teoría corresponde a un componente tipo window en el cual se define:

```Page.title``` es el titulo de la ventana

```Window_width y window_height``` es el tamaño de la ventana

Y esto corresponde a los elementos principales de una interfaz grafica que vimos anteriormente: ventanas y contenedores.

2.- componentes gráficos de control
-

En la calculadora aparecen estos tipos de componentes:
•	Text (display_text) → Componente de texto.

•	Container (display) → Contenedor que organiza y da estilo.

•	Button → Componente de control.

•	GridView → Contenedor que organiza botones en cuadrícula.

•	Column → Contenedor que organiza elementos verticalmente.

Lo cual  se relaciona con la clasificación teórica:

•	Contenedores: Column, GridView, Container.

•	Componentes atómicos: Button, Text.

•	Controles: Los botones, porque reciben interacción del usuario.

3.- manejo de eventos:
-
Aquí lo conectamos con la teoría de eventos y eventlistener 
En la función : ```def botón_click(e):```

Donde e es nuestro objeto evento y cuando el usuario presiona un botón ocurre lo siguiente:

-	El botón actúa como fuente del evento (emisor).
-	 Se genera un evento ```on_click.```
-	 La función ```botton_click``` actúa como listener o manejador del evento.
-	 Se ejecuta la lógica dependiendo del botón presionado.

En esta línea ```on_click=botón_click ``` este es nuestro modelo emisor es decir el receptor explicado anteriormente.

El botón genera el evento, la función lo recibe y este lo procesa.

4.- eventos de acción:
-

Cuando se presiona un botón:
- Se genera un evento de acción.
- El sistema ejecuta el controlador.
- Se actualiza el texto.
- Se refresca la interfaz con: ```page.update()```

Lo cual corresponde a la teoría donde el controlador puede:
- Reaccionar ante el evento.
- Modificar datos.
- Actualizar la interfaz.

5.- organización en contenedores:
-
La layout principal ```layout_principal = ft.Column(...) ``` Este se encarga de organizar los componentes dentro de un contenedor:
- Los contenedores alojan componentes.
- Permiten organizar visualmente la interfaz.
- Mantienen estructura y orden.

Link de calculadoratap: https://github.com/24680221/calculadoratap 

Otro ejemplo donde aplicamos estos temas es el código de formulario.

En el siguiente link esta explicado el código: https://github.com/24680221/Proyecto_Integrador_U1_T.A.P

Bibliografías
-
Unknown. (s. f.). 1.4 Manejo de componentes gráficos de control. https://topicosavanzadosdprogramacion.blogspot.com/p/14-manejo-de-componentes-graficos-de.html

Staff, C. (2023, 29 noviembre). ¿Qué es el diseño de interfaz de usuario? Definición, consejos, mejores prácticas. Coursera. https://www.coursera.org/mx/articles/ui-design

GUI: qué es una interfaz gráfica de usuario. (2021, 28 enero). IONOS Digital Guide. https://www.ionos.mx/digitalguide/paginas-web/desarrollo-web/que-es-una-gui/

Tipos de eventos. (s. f.). Studocu. https://www.studocu.com/es-mx/document/instituto-tecnologico-de-cerro-azul/ingenieria-en-sistemas-computacionales/tipos-de-eventos/37649445

Manejo de eventos. (s. f.). Studocu. https://www.studocu.com/es-mx/document/instituto-tecnologico-de-saltillo/topicos-avanzados-de-programacion/13-manejo-de-eventos-actividad-completada-unix-programacion-avanzada/46939963

Esdai. (s. f.). ¿Qué es la gestión de eventos y cuál es su importancia? https://blog.up.edu.mx/gdl/posgrados-esdai/que-es-la-gestion-de-eventos-y-cual-es-su-importancia

Manejo de componentes graficos de control. (s. f.). Studocu. https://www.studocu.com/es-mx/document/instituto-tecnologico-de-cerro-azul/ingenieria-en-sistemas-computacionales/manejo-de-componentes-graficos-de-control/37649441
