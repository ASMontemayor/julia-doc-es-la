.. _man-introduction:

**************
Introducción   
**************

La Computación científica ha requerido tradicionalmente el más alto rendimiento,sin embargo, 
los expertos en este ambito se han cambiado en gran parte a lenguajes dinámicos más lentos 
para el trabajo diario. Creemos que hay muchas buenas razones para preferir lenguajes dinámicos 
para estas aplicaciones, y no esperamos que su uso disminuya. Afortunadamente, las técnicas modernas para
la creación de lenguajes y las de compilador hacen posible eliminar, casi en su totalidad, el problema del 
desempeño de los lenguajes dinámicos y proporcionar un ambiente productivo para la creación de prototipos y 
lo suficientemente eficiente para el despliegue de aplicaciones con gran rendimiento. El lenguaje de programación 
Julia cumple este papel: es un lenguaje dinámico flexible, apropiado para cálculo científico y numérico, con un 
rendimiento comparable a los tradicionales lenguajes de tipo estático.

Julia presenta la mecanografía opcional,envío múltiple, y un buen rendimiento, alcanzado con el uso de 
inferencia de tipos y la compilación justo a tiempo *just-in-time* (JIT),
implementada usando `LLVM <http://en.wikipedia.org/wiki/Low_Level_Virtual_Machine>`_.
Es un multi-paradigma, que combina características 
de programación imperativa, funcional y orientado a objetos.  La sintaxis de Julia es similar a la de 
`GNU Octave <http://en.wikipedia.org/wiki/GNU_Octave>`_ o `MATLAB(R) <http://en.wikipedia.org/wiki/Matlab>`_
y por consiguiente los programadores de MATLAB deberían sentirse inmediatamente cómodos con Julia.
 Mientras que MATLAB es muy eficaz para el prototipado y la exploración de álgebra lineal numérica, tiene 
limitaciones para la programación de tareas fuera de este alcance relativamente estrecho.
Julia mantiene la facilidad y expresividad del MATLAB(R) para el cálculo numérico de alto nivel, 
sino que trasciende sus limitaciones generales de programación. Para lograr esto, Julia se basa 
en el linaje de los lenguajes de programación matemática, pero también toma mucho de lenguajes populares dinámicos, 
incluyendo 
`Lisp <http://en.wikipedia.org/wiki/Lisp_(programming_language)>`_,
`Perl <http://en.wikipedia.org/wiki/Perl_(programming_language)>`_,
`Python <http://en.wikipedia.org/wiki/Python_(programming_language)>`_,
`Lua <http://en.wikipedia.org/wiki/Lua_(programming_language)>`_, and
`Ruby <http://en.wikipedia.org/wiki/Ruby_(programming_language)>`_.

Las características mas significativas de Julia en relación a los lenguajes
dinámicos típicos son:

-  El núcleo del lenguaje impone muy poco, la biblioteca estándar está escrita 
   en el propio lenguaje Julia, incluidas las operaciones primitivas como las operaciones
   aritmética de enteros
-  Una variedad grande de tipos para construir y describir objetos, que también,
   puede utilizarse opcionalmente, para hacer declaraciones de tipos
-  La capacidad de definir el comportamiento de funciones a través de la combinación
   de varios tipos de argumentos via *multiple dispatch* [#MD-en]_, [#MD-pt]_
-  Generación automática de código eficiencia y especializado para diferentes 
   tipos de argumentos
-  Buen rendimiento, acercándose a la de los lenguajes estáticamente e compilados como C

Embora alguns por vezes digam que linguagens dinâmicas não são tipadas,
elas definitivamente são: todo objeto, seja primitivo ou definido pelo usuário,
possui um tipo. A ausência na declaração do tipo na maioria das linguagens
dinâmicas, entretanto, significa que não podemos instruir o compilador sobre o
tipo dos valores, e comumente não podemos falar sobre tipos. Em linguagens
estáticas, em oposição, enquanto podemos - e usualmente precisamos -
especificar tipos para o compilador, tipos existem apenas em tempo de
compilação e não podem ser manipulados ou expressos em tempo de execução. Em
Julia, tipos são objetos em tempo de execução, e podem também ser utilizados
para convenientemente informar o compilador.

Embora o programador casual não precise explicitamente utilizar tipos ou
*multiple dispatch*, estas são características principais de Julia: funções são
definidas para diferentes combinações de tipos de argumentos, e utilizadas de
acordo com as especificações mais semelhantes. Este modelo ser para programação
matemáticas, onde não é natural o primeiro argumento "possuir" uma operação
como é tradicional em linguagens orientadas a objetos. Operadores são apenas
funções com uma função especial - para estender a adição para um novo tipo
definido pelo usuário, você define um novo método para a função ``+``. Codes já
existentes são aplicados para novos tipos sem problemas.

Parcialmente por causa da inferência de tipos em tempo de execução (aumentado
pela opcionalidade da declaração de tipo), e parcialmente por causa do grande
foco em desempenho existente no início do projeto, a eficiência computacional
de Julia é maior que a de outras linguagens dinâmicas, e até rivaliza com
linguagens estáticas e compiladas. Para problemas numéricos de larga escala,
velocidade sempre foi, continua sendo, e provavelmente sempre será crucial: a
quantidade de dados sendo processada tem seguido a Lei de Moore na década
passada.

Julia anseia criar uma combinação sem precedente de facilidade de uso, força e
eficiência em uma única linguagem. Em adição ao dito acima, algumas das
vantagens de Julia em comparação com outros sistemas são:

-  Livre e open source (`Licença MIT
   <https://github.com/JuliaLang/julia/blob/master/LICENSE>`_)
-  Tipos definidos pelo usuário são rápidos e compactos como tipos nativos
-  Ausência da necessidade de vetorizar códigos por desempenho; códigos não
   vetorizados são rápidos
-  Projetado para computação paralela e distribuída
-  *Lightweight "green" threading coroutines* [#COR-en]_, [#COR-pt]_
-  Sistemas de tipos no obstrutivos mas poderosos
-  Conversão e promoção de tipos numéricos e outros de forma elegante e
   extensível
-  Soporte eficiente para
   `Unicode <http://en.wikipedia.org/wiki/Unicode>`_, incluyendo pero no
   limitado ao `UTF-8 <http://en.wikipedia.org/wiki/UTF-8>`_
-  Llamadas de funciones en C de forma directa (sin necessidad de *wrappers* o
   *API* especial)
-  Capacidad semejante a  una poderosa *shell* para gerenciar otros
   procesos
-  Macros de forma similar a Lisp y otras facilidades de metaprogramación

.. rubric:: Notas de rodapé

.. [#JIT-en] http://en.wikipedia.org/wiki/Just-in-time_compilation
.. [#JIT-pt] http://pt.wikipedia.org/wiki/JIT
.. [#LLVM-en] http://en.wikipedia.org/wiki/Low_Level_Virtual_Machine
.. [#LLVM-pt] http://pt.wikipedia.org/wiki/Low_Level_Virtual_Machine
.. [#MD-en] http://en.wikipedia.org/wiki/Multiple_dispatch
.. [#MD-pt] http://pt.wikipedia.org/wiki/Despacho_m%C3%BAltiplo
.. [#COR-en] http://en.wikipedia.org/wiki/Coroutine
.. [#COR-pt] http://pt.wikipedia.org/wiki/Corotina

