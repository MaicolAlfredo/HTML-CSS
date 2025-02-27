# Curso CSS Flexbox

1. [Introduccion](#1-introducción)

2. [¿Qué es Flexbox?](#qué-es-flexbox)

3. [¿Por qué Flexbox?](#por-qué-flexbox)

4. [¿Qué debo conocer?](#qué-debo-conocer)

5. [¿Qué herramientas usaremos?](#qué-herramientas-usaremos)

6. [Preparando el entorno antes de comenzar](#preparando-el-entorno-antes-de-comenzar)


## 1. Introducción

Hola a todos. En este curso aprenderán CSS Flexbox para crear diseños web responsivos que se adapten a distintos tamaños de pantallas y dispositivos. Flexbox es un modelo de diseño que te permite reorganizar elementos dentro de un contenedor en base a propiedades CSS que definen cómo los descendientes de un contenedor deben moverse para ajustarse a su tamaño.

Durante el curso, aprenderás a trabajar con propiedades CSS que son esenciales para Flexbox, como `flex-direction`, `justify-content`, `flex-wrap`, `align-items`, `align-content`, `flex-grow`, `flex-basis` y `flex-shrink`. Practicarás tu conocimiento creando proyectos prácticos, como una barra de navegación y un diseño clásico.

El curso fue creado por Leosbel Poll Sotomayor (Leo), ingeniero de software con más de 10 años de experiencia, quien comenzó a programar hace más de 20 años en Cuba. Ahora vive en Canadá, gracias a sus habilidades de programación, y creó este curso especialmente para la comunidad de FreeCodeCamp. Así que, si están listos, ¡comencemos!

Hola, soy Leo, y te prometo que hoy vas a entender de una vez por todas Flexbox. Vamos a hablar de tres conceptos fundamentales que siempre tengo en mente cuando pienso en Flexbox. Luego, hablaremos de algo que casi nadie menciona en CSS: **la pérdida de datos**. Después, iremos en detalle por cada una de las propiedades y sus valores. Por último, analizaremos dos casos de uso donde el 90% de las veces resolverás los problemas con Flexbox.

## Qué es Flexbox

Antes de irnos al código, me gustaría aclarar algunas preguntas. Lo primero sería: ¿Qué es Flexbox? Este no es más que un modelo de diseño unidimensional que se utiliza en CSS para organizar y distribuir elementos en una dirección. Quédense con esa palabra: **unidimensional**, porque la vamos a usar más adelante. Como es una definición un poco compleja, me gustaría simplificarla: imagina que estás jugando con bloques de construcción y te gustaría ponerlos uno al lado del otro o apilarlos uno encima del otro. Flexbox es el conjunto de reglas especiales que nos ayudará a organizar y distribuir esos bloques de manera fácil y flexible en una página web.

## Por qué Flexbox

Otra pregunta importante es: **¿Por qué fue creado Flexbox?** Antes de Flexbox, se usaban los modelos de diseño de línea o de bloque, y con estos era bastante difícil lograr un diseño a medida y flexible. Teníamos que flotar los elementos, jugar con las posiciones y asignar tamaños fijos. Esto funcionaba cuando hacíamos diseños para un solo tamaño de pantalla, pero, como saben, ya no es así. Existen muchísimos tamaños de pantallas, y es casi obligatorio hacer diseños para dispositivos móviles. Flexbox llegó para suplir todas estas necesidades. Lo más importante es que ahora podemos hacer diseños flexibles y responsivos de manera fácil e intuitiva. Además, nos permite manejar la alineación y el espaciado de forma sencilla. También nos permite reorganizar nuestros elementos de manera extremadamente fácil. Antes de Flexbox, teníamos que usar JavaScript para manipular el DOM o duplicar elementos y mostrarlos en algunas configuraciones mientras los ocultábamos en otras. Básicamente, Flexbox surgió para resolver uno de los grandes problemas de la humanidad. Más adelante te muestro cómo.

## Qué debo conocer

**¿Qué deberías saber con antelación para tomar este curso?** Si tienes los conceptos básicos de HTML y CSS, con eso bastaría. En la parte de HTML, vamos a usar algunos elementos de HTML5 para jugar con la semántica, pero mayormente trabajaremos con listas y sus elementos. En la parte de CSS, utilizaremos algunos selectores básicos, así como propiedades básicas para espaciado o colores, simplemente para visualizar mejor lo que vamos a hacer.

## Qué herramientas usaremos

Sobre las herramientas que vamos a utilizar en este curso, no necesitamos más que un editor de texto y un navegador. En mi caso, voy a utilizar **Visual Studio** Code como editor de texto, pero tú puedes usar el que prefieras. Como navegador, voy a usar Brave, pero tú puedes usar Chrome, Safari, Firefox o cualquiera de estos. Aquí podemos ver en la página de Can I Use que la propiedad de Flexbox está soportada en la mayoría de los navegadores modernos. En mi caso, voy a utilizar una extensión para evitar tener que ir al navegador y actualizarlo en cada cambio. Realmente, esta no es necesaria para lo que vamos a hacer, pero si te gustaría usarla para evitar tener que actualizar constantemente, te muestro cómo utilizarla. En Visual Studio Code, podemos ir al icono de las extensiones, y esta nos desplegará una lista de extensiones. Buscamos Live Server, y verás que tiene muchas descargas. En mi caso, ya la tengo instalada, pero a ti te saldrá un botón para instalarla. Luego de que esté instalada, puedes pararte en tu archivo de HTML y hacer clic en el botón Go Live. Se abrirá una pestaña en el navegador que estés usando con tu página web. Para usar Flexbox, no necesitamos nada más que nuestro CSS. Esto no es una librería, ni un framework, ni una extensión. Es puro CSS. Sin más preámbulos, ¡vamos al código!

## Preparando el entorno antes de comenzar

Preparando el entorno antes de comenzar
Lo primero que voy a hacer es crear una nueva carpeta llamada `flexbox-curso`. Dentro de esta carpeta, voy a crear dos archivos: un fichero HTML llamado `index.html` y un fichero CSS llamado `index.css`.

En el archivo HTML, vamos a crear una estructura básica utilizando el atajo de Emmet. Para ello, escribimos el signo de admiración (!) y presionamos la tecla Tab. Esto generará la estructura básica de un documento HTML. Luego, vamos a cambiar el título del documento a "Curso de Flexbox".

Dentro del cuerpo de la página (`<body>`), utilizaremos la técnica de Emmet para crear una estructura básica. En este caso, vamos a crear una barra de navegación (`<nav>`), que contendrá una lista no ordenada (`<ul>`). Esta lista, a su vez, contendrá tres elementos de lista (`<li>`), y cada uno de estos elementos contendrá una etiqueta de anclaje (`<a>`) con el texto "Menú" seguido de su indice (1, 2, 3). El código de Emmet que utilizaremos es el siguiente: `nav>ul>li*3>a{Menú $}`.
Con esto, ya tenemos la estructura básica con la que vamos a trabajar para demostrar los conceptos de Flexbox en este curso.

`index.html`

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Curso de Flexbox</title>
  </head>
  <body>
    <nav>
      <ul>
        <li><a href="#">Menú 1</a></li>
        <li><a href="#">Menú 2</a></li>
        <li><a href="#">Menú 3</a></li>
      </ul>
    </nav>
  </body>
</html>
```

Como una ayuda a previsualizar mejor lo que está pasando voy a crear unos estilos base sin hablar todavía de flexbox y para eso voy a estar linkando nuestro fichero de ccs acá en el html la etiqueta link y en el hrf decimos 'index.css'
`<link rel="stylesheet" href="index.css">` no vemos ningún cambio aún porque no hemos hecho nada en nuestro ccs pero vamos a empezar con el `body` primero le vamos a decir que queremos un background negro `background-color: black;` y la letra Me gustaría que fuese sans serif `font-family: sans-serif;` luego los vínculos que serían la etiqueta (`<a>`) vamos a decirle que no queremos que tenga ese esa línea que tiene por debajo y se la vamos a quitar con `text-decoration: none;` y luego vamos a quitarle ese azul que viene por defecto de los vínculos diciéndole que en el color queremos inherit que significa que herede de su padre `color: inherit;`, luego vamos a continuar con nuestra lista no ordenada (`<ul>`) vamos a decirle que el color de fondo va a ser blanco `background-color: white;` no queremos esos puntitos tampoco en las listas vamos a decirle `list-style: none;` y por defecto ven que tiene una separación con respecto a los bordes y también a la izquierda eso sería el margin vamos a quitárselo `margin: 0;` y también el padding `padding: 0;` ahora ese espacio que seguimos viendo sería en el body vamos a ir a este y vamos a decirle que el margin sea cero `margin: 0;`. Ya casi estamos listos Pero como me interesa que vean los espaciados y los delimitadores entre un elemento y los otros vamos a agregar algunos estilos en nuestros elementos de la lista sería al final vamos a decirle la etiqueta el Vamos a darle un color de fondo chocolate `background-color: chocolate;` el color de letra queremos que sea blanco `color: white;` vamos a agregarle también un poquito de Border en este caso vamos a decirle dashed para que sea con puntitos y el color va a ser negro `border: dashed black;` y por último como somos un poquito tikis micki como la letra está super pegada a la caja Vamos a darle un poquitito de padding también vamos a decirle padding .3rem arriba y abajo y .7rem a los costados `padding: 0.3rem 0.7rem;` ahora ya estamos más que listos para comenzar a hablar de flexbox.

Un concepto que te mencionaba al principio, y que siempre tengo en mente, es el primero: Los ejes. Siempre vamos a tener en cuenta un eje principal, que también tendrá una dirección, y perpendicular a este, vamos a tener un eje cruzado. Durante las demostraciones, voy a ir jugando visualmente con estos ejes para ayudarte a visualizar mejor lo que está pasando.

El segundo concepto, super importante, es el espacio disponible. Una vez que Flexbox acomode los elementos, verás que queda un espacio disponible. Vamos a ver cómo distribuimos ese espacio entre los elementos.

Y, por último, algo que siempre voy a tener en mente es: ¿Quién es el padre y cuáles son los hijos? Ya que las propiedades que se pueden usar con Flexbox se dividen en algunas para los padres y otras para los hijos. Muchas de estas propiedades dependen unas de otras.

```css
body {
  background-color: black;
  font-family: sans-serif;
  margin: 0;
}

a {
  text-decoration: none;
  color: inherit;
}

ul {
  background-color: white;
  list-style: none;
  margin: 0;
  padding: 0;
}

li {
  background-color: chocolate;
  color: white;
  border: dashed black;
  padding: 0.3rem 0.7rem;
}
```