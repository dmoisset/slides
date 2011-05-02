Introducción a Python
=====================

## PyDay Cordoba 2011
## Daniel F. Moisset

dmoisset@machinalis.com
@dmoisset

## Machinalis - http://www.machinalis.com/
## Python Argentina - http://python.org.ar/

.notes: Hola. Me llamo Daniel, y lamento tanto como ustedes que me hayan hecho levantar temprano. Pero por otro lado, me han dado un poco el honor de arrancar este evento, al cual le han puesto mucho laburo; estos eventos son una de las cosas que hace que la comunidad de Python Argentina, de la cual soy orgullosos miembro, sea tan grosa


----

(o así me dijeron que se titulaba la charla)

## Solía dar otra charla titulada «De 0 a Python en 45'»

.notes: A los organizadores los estoy estafando un poco. Me invitaron para que de una charla que solía dar antes. Esta charla tenía un estilo más de tutorial y entraba más en detalle fino sobre sintaxis de Python. La charla es *buenísima*, tanto que la he visto robada en internet con otra gente como autores, y también me han copiado el título para otras charlas de este evento. En realidad es una charla que vengo dando hace cerca de 5 años, y si bien el público se renueva, como dice Mirta, yo no

----

.fx: foo

## Pero después me aburrí de darla tantas veces

## y además va quedando cada vez más desactualizada

<http://github.com/dmoisset/slides/>

Aunque si se van y lo que quieren es parender el lenguaje, mejor lean [el tutorial](http://tutorial.python.org.ar/)

.notes: Así que esta es una versión un poco distinta, y un poco más dinámica. Para que sepan lo que se están perdiendo, les dejo un link a la otra charla. Tenían más chances de salir directamente programando, pero había algo importante que creo que tiene que tener esta charla, que es mostrar las cosas más picantes. O sea, convencerlos de que Python es la posta. En realidad les acabo de quemar la charla, porque es todo lo que tengo para decir. que

----

#Python

----

#es

----

#la

----
#posta!

----

#Preguntas?

.notes: Preguntas? (pausa) OK, supongo que no alcanza con que les diga que Python es la posta, sino que los tengo que convencer un poco. En realidad, este slide dice "Preguntas"" como para que yo me acuerde que les tengo que hacer unas preguntas a ustedes para conocer a mi audiencia. La charla va a ser la misma pero me gusta enterarme de a quienes estoy aburriendo. Quienes de acá escucharon hablar de Python por primera vez cuando les anunciaron el evento? (pausa) Y quienes nunca han hecho nada en Python? (pausa) Y quienes han ecrito un "hola mundo"? y quienes se consideran "programadores en Python" (aunque sean newbies)? (pausa) OK. gracias, vamos a los bifes

----

# Python es portable

 * 32 y 64 bits
 * **Windows**, **Linux**, **OS X**(Mac)
 * Solaris, 
 * MS-DOS
 * AIX, AROS, AS/400, BeOS, MorphOS, OS/2, OS/390, QNX, VMS...
 * iPod, Playstation, Palm, Nokia S60, Android, Windows CE....

.notes: No voy a perder mucho tiempo hablando de features y listas que pueden encontrar en la web, asi que muy a la pasada les voy a contar que pueden correr Python en cualquier lado, 

----

# Python es software libre

* © Python Software Foundation
* Bajo una licencia libre
* La licencia no restringe uso para software cerrado

.notes: Y que es libre, con todo lo que eso implica,

----

# Python es orientado a objetos

## de verdad!

 * Los `int`s son objetos
 * Los arreglos son objetos
 * Los módulos son objetos
 * Las funciones y métodos son objetos
 * Las clases son objetos

.notes: y que es orientado a objetos, puro. 

----

# Python es de propósito general

 * Sistemas basados en BBDDs
 * Sistemas con GUI
 * Webservices
 * Webapps 
 * Scripts cortos
 * Servicios en red
 * Extensiones scripteables para otros sistemas
 
.notes: También les puedo decir que sirve para hacer realmente de todo.

----
# Y se usa para proyectos de verdad

* Youtube
* BitTorrent
* Bazaar
* Civilization 4
* EVE Online
* Reddit

.notes: Y cuando digo de todo digo *de todo*.

----

# El desarrollo está muy activo

* La línea 2.x es la más usada
    * Actualmente por 2.7
    * Último release: Noviembre de 2010
* La gente de a poco se pasa a 3.x
    * No es 100% compatible para atrás
    * Pero han mejorado/simplificado varias cosas
    * 3.2 salió el Febrero de 2011

.notes: También podría dedicarle minutos a decirles que tiene un desarrollo muy activo y se mantiene al día de forma permanente

----
# Y hay varias implementaciones

* CPython
    * La original, implementada en C
    * La "oficial", con los cambios más nuevos
* Jython
    * Corre sobre la JVM
    * Se integra bien con código Java
* IronPython
    * Corre sobre la CLR de .NET
    * Se integra bien con código .NET
* PyPy
    * Compilador JIT. ¡Más rápido!
* Stackless
    * Features interesantes para concurrencia liviana

.notes: no sólo la versión oficial, sino las diversas implementaciones.

----
# Mas features

* Puede interfacear con cosas en otros lenguajes
* Tipado dinámico, flexible
* Embebible en otros sistemas
* ...

.notes: Podrías listarles infinitos features

----

# Todo eso en 

# <http://python.org/>

.notes: No pierdo tiempo en decirles toda esa info porque esta en la web. Y si bien son todas cosas buenas, y lindas, no terminan de ser el motivo por el cual Python es la posta, que es de lo que vine a convencerlos.

----

# Mito 1

## ¡Es algo nuevo, poco probado!

.notes: Y lo primero que tengo que hacer para convencerlos, es sacar de sus cabezas los rumores que la gente hace circular sabiendo poco lo que dice. Por ejemplo esto:

----

# Mito 1

## ¡Es algo nuevo, poco probado!

 * Desde **1991**
 * 4 años antes que Java
 * 10 años antes que C#
 * Tan viejo como Visual Basic

.notes: Aunque hay gente que crea que es algo nuevo, solamente porque escucho hablar de el hace poco (dado que no tiene una empresa atrás con un aparato de marketing gigante), pueden ver que es algo tanto o mas viejo y probado como varios lenguajes que nadie clasificaría como "experimental" o "demasiado nuevo"

----

# Mito 2

## Es interpretado

(Y por lo tanto, es tecnología vieja!)

.notes: Este otro mito es tan popular que hasta algunos programadores de Python lo creen

----

# Mito 2

## Es interpretado

* Todas las implementaciones compilan a bytecode (Igual que Java o C#)
* PyPy además compila el bytecode JIT a nativo

Pero... sigue teniendo la flexibilidad de un intérprete

* Compilación casi instantánea, on-the-fly, por módulo
* Uso interactivo
* Introspección masiva y acceso al código desde el programa

.notes: Y lo creen porque Python *parece* interpretado, al tener las cosas buenas de un intérprete. Es decir, un ciclo muy corto de trabajo entre escribir el código y estar probando lo que uno escribió, al punto de poder hacerse de forma interactiva, y poder observar e incluso mutar la estructura del programa mientras se ejecuta, lo que uno no hace todo los días pero permite muchos trucos útiles para debugging y para generación de código.

----

# Mito 3

## Es lento

.notes: Otros "peros" que se escuchan son los peros sobre performance

----

# Mito 3

## Es lento

 * Bueno, sí. Si uno lo trata de programar como si fuera C
 * En la práctica no:
     * Hay que saber usar las herramientas y bibliotecas optimizadas
     * Y en general el cuello de botella no es CPU

.notes: Otros "peros" que se escuchan son los peros sobre performance. Esos están un poco mejor fundados; si uno traduce uno a uno un algoritmo en C, la desventaja de performance se nota mucho. Pero no es la forma en la que los programadores de Python trabajamos. Python trae (tanto en la biblioteca estándar como en bibliotecas externas) una caja de herramientas con la mayoría de los algoritmos que uno necesita, escritos de forma más optimizada de lo que uno podría en C. Con lo cual, si uno conoce y elige estas herramientas, acaba teniendo código más rápido. Esto es algo que en realidad pasa en cualquier lenguaje, pero en Python se nota más; por suerte la disponibilidad de módulos para hacer *lo que sea* es alevosa. De todos modos, aún sin eso la diferencia de performance se nota solo cuando mi sistema es intensivo en CPU; si mi cuello de botella es la red, o el disco, o la base de datos, o el web server, o la interacción con el usuario, todo esto no importa.

----

# Mito 4

## No threadea

* Hay un porcentaje de verdad: sólo en la implementación oficial (CPython), el threading (que si hay) no aprovecha múltiples cores, solamente cuando los threads están corriendo todo código CPU intensivo escrito sin usar bibliotecas externas.
    * No importa en las otras implementaciones
    * No importa si uno no necesita multi-core
    * No importa si uno usa threading para multiplexar cosas bloqueantes (red, disco, UI)
    * No importa si la parte CPU intensiva esta en libs externas (como debería!)
* Ofrece alternativas multi-core más limpias (multiprocessing, sin estado compartido)

.notes: Hay otro comentario popular sobre el soporte de threading. Que se basa en un hecho real que es el punto de arriba, pero en una malainterpretación de este hecho. En realidad el threading esta soportado, pero no se hace por hardware en algunos casos que no son los típicos que necesita un desarrollador de aplicaciones. Si quieren hacer threads paramostrar una barrita de progreso mientras guardan a disco, o para mandar muchos e-mails a la vez, en realidad no van a tener problemas. Y en otros de los casos, se pueden usar las alternativas que se proveen en la biblioteca, que permiten escribir código multi-core con un estilo donde uno tiene que pensar menos en race-conditions y sincronización. El caso real donde el threading puede ser un problema es si están escribiendo código de cálculo numérico de un modo que no está cubierto por ninguna biblioteca numérica de las disponibles; en ese caso probablemente les convenga trabajar en C (al menos para el cálculo. Yo haría el código alrededor de eso en Python). Pero si ustedes se dedican a computo de alta performance... ya sabían esto que les estoy diciendo.

----

# El shell interactivo

Lo que aparece detras de `>>>` es lo que entra el usuario

    !pycon
    $ python
    Python 2.6.5 (r265:79063, Apr 16 2010, 13:09:56) 
    [GCC 4.4.3] on linux2
    Type "help", "copyright", "credits" or "license" for more information.
    >>> print "Hola Python Day!"
    Hola Python Day!
    >>> import socket
    >>> s = socket.socket()
    >>> print s
    <socket._socketobject object at 0xb7732454>
    >>> s.connect( ('www.google.com', 80))
    >>> s.send('GET / HTTP/1.0\r\n\r\n')
    18
    >>> s.recv(80)
    'HTTP/1.0 302 Found\r\nLocation: http://www.google.com.ar/\r\nCache-Control: private\r'

* Práctiquisimo para probar ideas, módulos, aprender

.notes: Suponiendo que ya los limpié de todos los prejuicios que podrían traer, vamos a empezar a ver algo hecho en Python. Una de las cosas prácticas en python es el shell interactivo, donde unopuede ir escribiendo líneas de programa e ir viendo como se ejecutan. Es de lo mejor para aprender, para debuguear y es algo que me gusta mostrar, por que para muchos programadores es algo nuevo. Y es algo que los programadores de python usamos muchísimo y nos permite probar una idea antes de sentarse a escribir código "de verdad" en un archivo. Aca pueden ver como además de mostrar un mensajito, cargo la biblioteca de networking básica (podría haber usado el cliente HTTP pero era más aburrido para este ejemplo),y me conecto al servidor web de google, les mando algo, leo la respuesta. En todo esto yo voy viendo que pasa y eligiendo que hacer cada vez que veo el triple triangulito.


----
# Soporte completo unicode

    !pycon
    >>> data = f.readline().decode('utf-16')
    >>> print data
    u'¡Soy un texto multilingüe! Ես բազմալեզու տեքստ! 我是一个多语种的文字！'
    >>> s.send(data.encode('utf-8'))
    >>> int(u'৪२')
    42

.notes: Para mostrar que es algo moderno y adaptado al mundo globalizado y multilingüe, les quería mostrar que pueden trabajar con texto completamente internacionalizado, que puede venir e irse del programa codificado con distintos estándares, mientras al medio es verdadero texto con acentos en castellano, o armenio, o chino. No solo eso, sino que las funciones estandar, por ejemplo `int` que convierte una cadena a entero, saben trabajar con todo el juego de caracteres, por ejemplo el número 42 de ahi que esta escrito con un 4 bengalí y un 2 devanagari.

----
# Sintáxis piola

    !python
    a = b = 0 # Nada raro aquí... sin punto y coma!
    # Intercambio de valores entre variables
    izq, der = der, izq 
    # Comparaciones de más de 2 cosas
    if 0 <= x < longitud: ... 
    # y sin paréntesis!

.notes: Python se escribe de una forma muy limpita, donde no hay que salpicar el código con simbolitos solo porque si. Si se fijan mi código no tiene puntos y comas; son opcionales, y lo normal es no ponerlos cuando uno pone una instrucción por linea. O sea, el 99% de los casos. Tiene muchas notaciones que no son comunes en otros lenguajes, como el segundo y tercer ejemplo de ahi, pero que si se fijan son bastante obvios de leer sin tener que explicar mucho. Mucha gente dice que escribir python es casi como escribir en pseudocódigo. Eso quiere decir que los mismos atajos prácticos que uno hace al escribir para pensar un programa, en Python son parte del lenguaje y no hace falta ponerse a traducirlos.

----

# Tipos de muy alto nivel

## Listas

    !pycon
    >>> l = [1,2,3,10,47,-1,-96,32]
    >>> l[:4]
    [1, 2, 3, 10]
    >>> l[-3:]
    [-1, 96, 32]
    >>> l.append('hola')
    >>> del l[:-1]
    >>> print l
    ['hola']
    >>> l = l*5
    >>> print l
    ['hola', 'hola', 'hola', 'hola', 'hola']
    >>> l[1:4] = ['al medio']
    >>> print l
    ['hola', 'al medio', 'hola']
    >>> print l[1]
    al medio

.notes: Python soporta tipos de alto nivel. El tipo llamado listas parece a primera vista un arreglo, pero se puede modificar, rebanar, estirar, y guardar cosas de varios tipos (explicar)

----

# Tipos de muy alto nivel

## Conjuntos

    !pycon
    >>> s1 = set([1,2,3,10])
    >>> s2 = set([2,3,5,7])
    >>> s1 | s2
    set([1, 2, 3, 5, 7, 10])
    >>> s1 - s2
    set([1, 10])
    >>> s1 & s2
    set([2, 3])
    >> 6 in s1
    False

.notes: explicar

----

# Tipos de muy alto nivel

## Conjuntos: y esto para que?

Eliminar duplicados en una lista:

    !python
    l = list(set(l))

Revisar permisos:

    !python
    if usuario in registrados-bloqueados:

Se usan más seguido de lo que creen!

----

# Tipos de muy alto nivel

## Diccionarios

    !pycon
    >>> d = {'clave': 17,
             13: 'valor',
             }
    >>> d['clave']
    17
    >>> len(d)
    2
    >>> d['otra'] = []
    >>> del d[13]
    >>> 13 in d
    False
    >>> list(d)
    ['clave', 'otra']
    >>> d.values()
    [17, []]

----

# Más sintaxis piola

    !python
    def nombre(descripcion):
        """Obtiene el nombre a partir de una linea en usuarios.txt"""
        return descripcion.split(',')[0]

    with open('usuarios.txt') as f:
        usuarios = [nombre(linea) for linea in f]
    usuarios.append('admin')
    usuarios.sort()

.notes: son objetos! sin declarar! docstring! whitespace! sin llaves! with! iterando sobre archivos! comprehensions

----

# Sí, como en la primaria

## Comprehensions

    !python
    import itertools
    candidatos = itertools.combinations(range(100), 3)
    ternas = [(c1, c2, h) for c1, c2, h in candidatos if c1**2 + c2**2 == h**2]

----

# Pero lo mejor no está en el lenguaje....

----

# Preguntas?

----

# <http://github.com/dmoisset/slides/> (intro-python)

