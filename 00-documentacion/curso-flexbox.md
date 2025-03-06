# Curso CSS Flexbox

1. [Introduccion](#1-introducción)

2. [¿Qué es Flexbox?](#qué-es-flexbox)

3. [¿Por qué Flexbox?](#por-qué-flexbox)

4. [¿Qué debo conocer?](#qué-debo-conocer)

5. [¿Qué herramientas usaremos?](#qué-herramientas-usaremos)

6. [Preparando el entorno antes de comenzar](#preparando-el-entorno-antes-de-comenzar)

7. [Propiedades relacionadas al contenedor](#propiedades-relacionadas-al-contenedor)

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

## Propiedades relacionadas al contenedor

- [display flex](#display-flex)
- [flex-direction](#flex-direction)
- [justify-content](#justify-content)
- [flex-wrap](#flex-wrap)
- [flex-flow](#flex-flow)
- [align-items](#align-items)
- [Cómo centrar un div](#cómo-centrar-un-div)
- [align-content](#align-content)

Para continuar nos vamos a nuestro css y voy a estar poniendo otra vez la etiqueta de (`<ul>`) porque no quiero mezclarla con los colores los espacios en este ul y los Li que vamos a ver a continuación vamos a estar hablando puramente de flexbox vamos a comenzar con todas las propiedades que le podemos asignar al padre y que hacen estas y luego vamos a pasar a los hijos.

### display flex

Lo primero que debemos saber para que un contenedor se comporte de manera flexible es su propiedad display. En este caso, estamos hablando de `display: flex;`. Simplemente con aplicar esto, ya verás que todos los elementos li se colocan uno al lado del otro, y nos queda un **espacio disponible al final**.

Este espacio disponible se debe a que el ul (la lista no ordenada) es un elemento que, por defecto, se comporta como un elemento de bloque. La mayoría de las veces, querremos que siga comportándose como un elemento de bloque. Sin embargo, si en algún momento no queremos que tenga ese espacio extra y deseamos que ocupe solo el espacio de sus elementos hijos, en lugar de usar flex, utilizaremos inline-flex (`display: inline-flex;`).

Al hacer esto, le estamos diciendo al contenedor: "Ya no te comportarás como un bloque, sino que tendrás un comportamiento similar a inline-block, pero además serás un **contenedor flexible**". Aunque, como te decía, la mayoría de las veces simplemente usarás flex.

### flex-direction

Ahora, ¿por qué todos los elementos del menú se colocaron uno al lado del otro? Esto sucede porque se van a regir por el **eje principal** de nuestro contenedor flexible. Seguramente te estarás preguntando: ¿tenemos alguna forma de manipular estos ejes? ¡Por supuesto que sí! Y aquí es donde entra en juego la propiedad `flex-direction`, o **dirección del contenedor flexible**.
En este caso, el valor por defecto de flex-direction es row, que significa fila (`flex-direction: row;`). Por eso, nuestro eje principal estará, por defecto, en posición horizontal.

Si quisiéramos mantener la disposición horizontal pero cambiar la dirección (es decir, que en lugar de ir de izquierda a derecha, fuese de derecha a izquierda), podemos usar el valor row-reverse (`flex-direction: row-reverse;`). Si te fijas, no es que los elementos se hayan movido hacia la derecha, sino que **cambió el orden de los elementos**. Recuerda que antes teníamos "menú 1", "menú 2" y "menú 3", y ahora empieza desde la derecha: "menú 3", "menú 2" y "menú 1".

Si quisiéramos que este eje principal no fuera horizontal, sino vertical, podemos usar el valor column (`flex-direction: column;`). En este caso, la dirección por defecto sería de **arriba hacia abajo**. Pero si quisiéramos cambiar la dirección, es decir, que fuese de **abajo hacia arriba**, podemos utilizar la misma técnica aplicando reverse (flex-direction: column-reverse;).

Ahora, a simple vista parece que no cambió nada, pero si te fijas bien, "menú 1" empieza desde abajo, seguido de "menú 2" y "menú 3".

Algo muy importante a tener en cuenta con los ejes es que el **eje cruzado** siempre va a ser **perpendicular al eje principal**. Es decir, si con flex-direction rotamos el eje principal, el eje cruzado también se va a rotar. Voy a borrar esta línea porque quiero que se mantenga en forma de row, es decir, horizontalmente y en forma de fila.

### **justify-content**

Quiero comenzar a hablar un poco sobre el **espacio disponible**. La propiedad que vamos a utilizar para distribuir este espacio es `justify-content`. Esta propiedad se rige por el **eje principal**, sin importar si está en posición horizontal o vertical, y su función es distribuir el espacio disponible, siempre guiándose por ese eje principal.
El valor por defecto de `justify-content` es flex-start (`justify-content: flex-start;`). Como puedes ver, no ocurre ningún cambio notable. Sin embargo, si quisiéramos mover ese espacio disponible al inicio y los elementos al final, usamos flex-end (`justify-content: flex-end;`).
Es importante destacar que esto no es lo mismo que lo que ocurría con row-reverse. En este caso, el orden de los elementos no cambia: "menú 1" sigue siendo el primero, luego "menú 2" y finalmente "menú 3".
Además, existen dos propiedades que, a simple vista, parecen similares: start (`justify-content: start;`) y end (`justify-content: end;`). La diferencia es que estas **no tienen en cuenta la flexibilidad de los elementos**, a diferencia de flex-start y flex-end.

```css
/* Flexbox */
ul {
  display: flex;
  /* display: inline-flex; */
  /* flex-direction: row; */
  /* flex-direction: row-reverse; */
  /* flex-direction: column; */
  /* flex-direction: column-reverse; */
  /* justify-content: flex-start; */
  /* justify-content: flex-end; */
  /* justify-content: start; */
  /* justify-content: end; */
}
```

Vamos a demostrarlo para que se visualice mejor. Si tuviésemos `flex-direction: row;` (es decir, la configuración actual), no se nota una diferencia significativa. Sin embargo, la diferencia se hace evidente cuando aplicamos reverse (`flex-direction: row-reverse;`) y, en lugar de usar end, usamos start (`justify-content: start;`).

En este caso, los elementos, que estaban corridos hacia la derecha, se mueven hacia el inicio. Es decir, el orden sería: "menú 3", "menú 2" y "menú 1". Sin embargo, si usamos flex-start (`justify-content: flex-start;`), los elementos no se mueven hacia la izquierda como lo hacen con start. En su lugar, flex-start coloca los elementos donde comienza realmente el eje principal, según su dirección. En cambio, start siempre los alinea a la izquierda del navegador, independientemente de la dirección del eje.

Vamos a quitar el reverse y volver a row (`flex-direction: row;`). Otra forma de distribuir el espacio residual entre los elementos es usando center (justify-content: center;). Lo que hace center es tomar ese espacio residual y distribuirlo equitativamente al inicio y al final, colocando los elementos justo en el centro.

Además, tenemos otras tres formas de distribuir el espacio residual entre los elementos:

1. space-between (`justify-content: space-between;`): En este caso, el espacio residual se distribuye equitativamente entre los elementos, pero no hay espacio al inicio del primer elemento ni al final del último.

2. space-around (`justify-content: space-around;`): Aquí, el espacio residual se distribuye alrededor de los elementos. Esto significa que hay un espacio al inicio del primer elemento y al final del último, pero este espacio es la mitad del espacio que hay entre los elementos.

3. space-evenly (`justify-content: space-evenly;`): Este valor distribuye el espacio de manera uniforme. El espacio que hay antes del primer elemento y después del último es exactamente igual al espacio entre los elementos.

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

ul {
  display: flex;
  flex-direction: row;
  /* justify-content: space-between; */
  /* justify-content: space-around; */
  justify-content: space-evenly;
}
```

### **flex-wrap**

Seguramente te estarás preguntando: **¿Qué pasa cuando tengo demasiados elementos en la misma línea?** Para demostrarlo, vamos a duplicar en nuestro HTML varias veces el "menú 2", porque fue el elegido.

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
        <li><a href="#">Menú 2</a></li>
        <li><a href="#">Menú 2</a></li>
        <li><a href="#">Menú 2</a></li>
        <li><a href="#">Menú 2</a></li>
        <li><a href="#">Menú 2</a></li>
        <li><a href="#">Menú 2</a></li>
        <li><a href="#">Menú 2</a></li>
        <li><a href="#">Menú 2</a></li>
        <li><a href="#">Menú 2</a></li>
        <li><a href="#">Menú 3</a></li>
      </ul>
    </nav>
  </body>
</html>
```

Si observamos nuestra página, veremos que los elementos no caben todos en el 100% del espacio disponible. Lo que ocurre es que, primero, el navegador intenta comprimir los espacios en blanco al máximo, es decir, trata de apretar lo más posible a todos los elementos hijos. Sin embargo, una vez que alcanzan el 100% del espacio, no pueden seguir expandiéndose más allá de ese límite. Entonces, el navegador nos muestra una **barra de scroll** para permitirnos desplazarnos y ver el contenido restante.

Si quisiéramos evitar esto y hacer que, al llegar al 100% del espacio, los elementos no desborden sino que simplemente bajen (es decir, se coloquen uno debajo del otro), podemos utilizar la propiedad flex-wrap. El valor por defecto de esta propiedad es nowrap (` flex-wrap: nowrap;` ), que es el comportamiento que estamos viendo actualmente. Sin embargo, podemos cambiarlo a wrap (` flex-wrap: wrap;` ).

Al hacer esto, notarás que, cuando un elemento (como este "menú 2" que tenemos aquí) ya no cabe en la línea, simplemente se mueve hacia abajo, y así sucesivamente con los demás elementos.

Además, flex-wrap tiene un valor especial llamado wrap-reverse (` flex-wrap: wrap-reverse;` ). Si lo aplicamos, veremos que el "menú 1" ahora está abajo a la izquierda, y los elementos se ordenan en dirección contraria, terminando con el "menú 3" arriba a la derecha.

```css
ul {
  display: flex;
  /*  flex-wrap: nowrap; */
  /* flex-wrap: wrap; */
  /*  flex-wrap: wrap-reverse; */
}
```

### flex-flow

Si quisiéramos combinar las propiedades `flex-direction` y `flex-wrap`, existe una propiedad llamada `flex-flow`. A esta propiedad le podemos asignar dos valores: el primero corresponde a la dirección (flex-direction) y el segundo al ajuste de línea (flex-wrap). Por ejemplo, podríamos usar column para la dirección y wrap para el ajuste de línea: `flex-flow: column wrap;`.

Si observamos, al cambiar el valor de column a row (como teníamos hace un momento), obtenemos el mismo resultado que antes. Vamos a borrar esta propiedad por un segundo y también eliminaremos todos los elementos adicionales de "menú 2", dejando solo los tres elementos originales que teníamos al inicio.

```css
ul {
  display: flex;
  /*  flex-flow: column wrap; */
  /* flex-flow: row wrap; */
}
```

### **align-items**

¿Si tenemos una propiedad para mover los elementos en el eje principal, tendremos otra para moverlos en el eje cruzado? ¡Pues sí! Estamos hablando de `align-items`, o "alinear elementos". Por defecto, el valor de esta propiedad es stretch (`align-items: stretch;`), lo que hace que los elementos se estiren para ocupar todo el espacio disponible en el eje cruzado.

Sin embargo, si cambiamos este valor por otros que ya hemos visto en propiedades anteriores, como flex-start (`align-items: flex-start;`) o flex-end (`align-items: flex-end;`), parece que no ocurre nada. Esto se debe a que el padre de estos elementos (en este caso, el ul) tiene un alto por defecto que es exactamente igual al alto de sus hijos.

Para tener una mejor visualización, vamos a modificar el `ul`. Vamos a darle un alto específico, por ejemplo, de 10 rem (`height: 10rem;`). Esto nos permitirá observar cómo los elementos se alinean en el eje cruzado según el valor que le demos a align-items.

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
  height: 10rem;
}

li {
  background-color: chocolate;
  color: white;
  border: dashed black;
  padding: 0.3rem 0.7rem;
}

ul {
  display: flex;
  /* align-items: stretch; */
  /* align-items: flex-start; */
  align-items: flex-end;
}
```

¿Ven? Simplemente al darle un alto al contenedor, ahora sí se nota que algo pasó. Aunque todavía no sabemos exactamente qué ocurrió, algo cambió. Vamos a revisar nuestras propiedades de Flexbox. Como les decía, el valor por defecto de align-items es stretch (`align-items: stretch;`). Lo que hace este valor es que los elementos hijos ocupan todo el espacio disponible en el eje cruzado.

Pero si quisiéramos que los hijos solo tomaran el espacio que les corresponde según su contenido y, al mismo tiempo, se alinearan al inicio del contenedor, podemos usar el valor flex-start (`align-items: flex-start;`). Como pueden ver, los elementos ahora se alinean al inicio del contenedor flexible y solo ocupan el espacio necesario según su contenido.

Si, por el contrario, quisiéramos que los elementos se alinearan al final del contenedor, usaríamos flex-end (`align-items: flex-end;`). Como se puede observar, los elementos ahora se colocan al final del contenedor, pero siguen ocupando solo el espacio que necesitan.

Hasta ahora, hemos visto dos propiedades clave:

1. `justify-content`: Maneja la distribución de los elementos en el eje principal.
2. `align-items`: Maneja la alineación de los elementos en el eje cruzado.

Con la combinación de estas dos propiedades, podemos resolver uno de los grandes problemas de la humanidad... (bueno, al menos en el mundo del diseño web 😄).

### Cómo centrar un div

Antes de Flexbox, lograr esto era casi imposible. Pero ahora, simplemente le decimos al contenedor:
`align-items`: center; para centrar los elementos en el eje cruzado, y `justify-content`: center; para centrarlos en el eje principal.

¡Y así, nuestros elementos quedan perfectamente centrados de manera fácil y rápida!

```css
ul {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

Vamos a borrar un segundito `justify-content` y vamos a ver el último de los valores, que sería `align-items: baseline`. Tal parece que no hizo nada, pero esta propiedad a lo que se está refiriendo es que la línea de la fuente, es decir, la línea base de la fuente, esté alineada. Para visualizarlo mejor, vamos a decirle al segundo `<li>` con `nth-child`, le decimos el número dos, `li:nth-child(2)`, vamos a decirle que el `font-size` va a ser aproximadamente dos rem, `font-size: 2rem;`. Como notan, los elementos se acomodan para que la fuente, es decir, la base de la fuente, esté alineada.

```css
li:nth-child(2) {
  font-size: 2 rem;
}

ul {
  display: flex;
  align-items: baseline;
}
```

Lo otro es que, si tuviésemos más texto en uno de los elementos, por ejemplo, vamos a ir al mismo 'menú dos' y vamos a decirle que va a tener un Loren de 10 para agregar 10 palabras medio random.

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
        <li>
          <a href="#"
            >Menú 2Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed
            do eiusmod.</a
          >
        </li>
        <li><a href="#">Menú 3</a></li>
      </ul>
    </nav>
  </body>
</html>
```

Ahora, en el CSS, vamos a decirle que en vez de `baseline` va a ser `last baseline`. `align-items: last baseline`. Esto se está refiriendo a la misma línea de la fuente, pero en este caso dice: "alinea las últimas líneas de los elementos". Y como rompimos toda nuestra interfaz, vamos a borrar por ahora esto de la demostración. Y también vamos a echar para atrás el texto del menú 2.

```css
li:nth-child(2) {
  font-size: 2 rem;
}

ul {
  display: flex;
  align-items: last baseline;
}
```

### **align-content**

La próxima propiedad que vamos a ver va a ser muy parecida a `justify-content`, incluso va a tener prácticamente los mismos valores que `justify-content`. Simplemente que esta la vamos a aplicar una vez que nuestros elementos no entren en el 100% de la pantalla y le digamos de alguna manera `flex-wrap: wrap;` o `wrap-reverse`, para que acomode todos estos elementos en el 100% de su padre. Vamos a utilizar `align-content` para distribuir el espacio residual entre los elementos. Vamos a ver un ejemplo: si agregamos, como hace un momento, varios elementos de 'menú 2', como ven, lo que pasaba ahorita, no entran todos en el 100%.

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
        <li><a href="#">Menú 2</a></li>
        <li><a href="#">Menú 2</a></li>
        <li><a href="#">Menú 2</a></li>
        <li><a href="#">Menú 2</a></li>
        <li><a href="#">Menú 2</a></li>
        <li><a href="#">Menú 2</a></li>
        <li><a href="#">Menú 2</a></li>
        <li><a href="#">Menú 2</a></li>
        <li><a href="#">Menú 2</a></li>
        <li><a href="#">Menú 2</a></li>
        <li><a href="#">Menú 3</a></li>
      </ul>
    </nav>
  </body>
</html>
```

Acá vamos a decirle `flex-wrap: wrap;` y, como el padre tiene el alto justo para contener a todos los elementos, vamos a darle un poquitico más de alto para que se note bien esto. Vamos a decirle a la `ul`, por ejemplo, `15rem`. Venimos al final para seguir trabajando con nuestras propiedades de flexbox y le decimos `align-content`. Podemos comenzar con `flex-start`: `align-content: flex-start;`. Se fijan, todos los elementos se van al inicio. Luego podemos ver `flex-end`: `align-content: flex-end;`. Todos los elementos se van al final. Luego tenemos `center`: `align-content: center;`. Todos los elementos se centran y seguro estarán pensando: "eso es lo que acabamos de ver con `align-items`", es decir, cómo alinear elementos en el eje cruzado. Pero no, existe una pequeña diferencia de cómo distribuimos el espacio residual entre esas filas de elementos que hemos puesto uno debajo del otro. Y lo vamos a notar con los valores de `space-between`: `align-content: space-between;`. Como vimos con `justify-content`, es decir, ahora el espacio residual se pone entre las filas de elementos. Luego tenemos, de igual manera, `space-around`: `align-content: space-around;`. Se ponen espacios iguales, pero delante y detrás de cada elemento, por eso el primero y el último va a tener menos espacio que entre los elementos. Y de igual manera, vamos a tener `space-evenly`: `align-content: space-evenly;`, donde el espacio residual va a estar repartido igualmente entre todas las filas de elementos. Y el valor por defecto de este sería `stretch`: `align-content: stretch;`, donde todos los elementos van a tener un alto acorde para no tener un espacio residual en el padre.

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
  height: 15rem;
}

li {
  background-color: chocolate;
  color: white;
  border: dashed black;
  padding: 0.3rem 0.7rem;
}
ul {
  display: flex;
  flex-wrap: wrap;
  align-content: stretch; /* dafault */
  /* align-items: last baseline; */
  /* align-content: flex-start; */
  /* align-content: flex-end; */
  /* align-content: center; */
  /* align-content: space-between; */
  /* align-content: space-around; */
  /* align-content: space-evenly; */
}
```


[Indice](#curso-css-flexbox)
