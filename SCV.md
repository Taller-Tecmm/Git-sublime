### Sistema de control de versiones. Software que administra el acceso a un conjunto de ficheros, y mantiene un historial de cambios realizados. El control de versiones es �til para guardar cualquier documento que cambie con frecuencia, como c�digo fuente, documentaci�n o ficheros de configuraci�n. [1]
Contenido

    1 Caracter�sticas
    2 Clasificaci�n
        2.1 Centralizados
        2.2 Distribuidos
    3 Control de versiones
        3.1 Ejemplos
        3.2 Forma habitual de trabajo
    4 Funcionamiento
        4.1 Exclusivos
        4.2 Colaborativos
    5 Procedimiento de uso habitual de un sistema de control de versiones
    6 Subversi�n como evoluci�n de CVS
    7 Clientes e integraci�n con IDEs
    8 Sistemas de Control de Versiones Libres
        8.1 CVS
        8.2 Subversion
        8.3 SVK
        8.4 Mercurial
        8.5 GIT
        8.6 Bazaar
    9 Referencias
    10 Fuentes

Caracter�sticas
Sistema de control de versiones

Un sistema de control de versiones debe proporcionar:

    Mecanismo de almacenamiento de los elementos que deba gestionar.
    Posibilidad de realizar cambios sobre los elementos almacenados.
    Registro hist�rico de las acciones realizadas con cada elemento o conjunto de elementos.

Clasificaci�n

Los sistemas de control de versiones se pueden clasifica en 2 grandes grupos:
Centralizados

En un sistema de control de versiones centralizado todos nuestros fuentes y sus versiones est�n almacenados en un �nico directorio (llamado repositorio de fuentes) de un ordenador (un servidor). Todos los desarrolladores que quieran trabajar con esos fuentes, deben pedirle al sistema de control de versiones una copia local para trabajar. En ella realizan todos sus cambios y cuando est�n listos y funcionando, le dicen al sistema de control de versiones que guarde los fuentes modificados como una nueva versi�n.Algunos ejemplos son CVS y subversi�n.
Distribuidos

En un sistema de control de versiones distribuido no hay un repositorio central. Todos los desarrolladores tienen su propia copia del repositorio, con todas las versiones y toda la historia. Por supuesto, seg�n van desarrollando y haciendo cambios, sus fuentes y versiones van siendo distintas unas de otras. Sin embargo, los sistemas de control de versiones distribuidos permiten que en cualquier momento dos desarrolladores cualesquiera puedan "sincronizar" sus repositorios. Si uno de los desarrolladores ha tocado determinados fuentes y el otro no, los modificados se convierten en la versi�n m�s moderna.Ejemplos:Git y Mercurial.
Control de versiones

Normalmente consiste en una copia maestra en un repositorio central, y un programa cliente con el que cada usuario sincroniza su copia local. Esto permite compartir los cambios sobre un mismo conjunto de ficheros. Adem�s, el repositorio guarda registro de los cambios realizados por cada usuario, y permite volver a un estado anterior en caso de necesidad. [2]
Ejemplos

    Guardar distintas copias de los ficheros nombr�ndolos adecuadamente.
    Hacer scripts para automatizar las copias.
    Usar un software espec�fico para realizar el control de versiones.

Forma habitual de trabajo

    Mantener una copia en local y modificarla.Despu�s actualizarla en el repositorio. Esto nos brinda grandes ventajas,ya que,no necesita acceso continuo al repositorio y asegurarse de que lo actualizado est� bien.

    Con algunos sistemas de control de versiones es posible trabajar directamente contra el repositorio.Esto aunque tiene una ventaja muy grande es que nos facilita la transparerencia de las versiones tambi�n provoca como inconveniente el bloqueo de ficheros.

Funcionamiento

Todos los sistemas de control de versiones se basan en disponer de un repositorio, que es el conjunto de informaci�n gestionada por el sistema. Este repositorio contiene el historial de versiones de todos los elementos gestionados.

Cada uno de los usuarios puede crearse una copia local duplicando el contenido del repositorio para permitir su uso. Es posible duplicar la �ltima versi�n o cualquier versi�n almacenada en el historial. Este proceso se suele conocer como checkout o desproteger. Para modificar la copia local existen dos sem�nticas b�sicas:
Exclusivos

Para poder realizar un cambio es necesario marcar en el repositorio el elemento que se desea modificar y el sistema se encargar� de impedir que otro usuario pueda modificar dicho elemento.
Colaborativos

En el que cada usuario se descarga la copia, la modifica, y el sistema autom�ticamente combina las diversas modificaciones. El principal problema es la posible aparici�n de conflictos que deban ser solucionados manualmente o las posibles inconsistencias que surjan al modificar el mismo fichero por varias personas no coordinadas. Adem�s, esta sem�ntica no es apropiada para ficheros binarios.
Procedimiento de uso habitual de un sistema de control de versiones

    Descarga de ficheros inicial (Checkout)
    Ciclo de trabajo habitual:

    Modificaci�n de los ficheros
    Actualizaci�n de ficheros en local (Update)
    Resoluci�n de conflictos (si los hay)
    Actualizaci�n de ficheros en repositorio (Commit).

Subversi�n como evoluci�n de CVS

    Renombar, copiar y mover ficheros y directorios sin perdida del hist�rico.
    Commits at�micos.
    Implementaci�n de tres tipos de acceso:
    Stand-alone
    Local
    Apache + webDAV
    Mejorado el sistema de permisos.
    Reducci�n del riesgo de vulnerabilidades por sus distintos RA (repository access).
    Integraci�n con Project Software Manager (Por ejemplo: trac).

Clientes e integraci�n con IDEs

1.Para Concurrent Version Control (CVS):

    Eclipse (integrado)
    Kdevelop (integrado)
    TortoriseCVS. [3]

2.WinCVS[4]

    Cervisia[5]

Para Subversi�n:

    TortoiseSVN [6]
    Plugin para Eclipse (subclipse)

Sistemas de Control de Versiones Libres
CVS

CVS[7] ha estado durante mucho tiempo, y muchos desarrolladores est�n ya familiarizados con �l. En su d�a fue revolucionario: fue el primer sistema de control de versiones de c�digo abierto con acceso a redes de �rea amplia para desarrolladores (que yo sepa), y el primero que ofreci� ""checkouts"" an�nimos de s�lo lectura, los que dieron a los desarrolladores una manera f�cil de implicarse en los proyectos. CVS s�lo versiona ficheros, no directorios; ofrece ramificaciones, etiquetado, y un buen rendimiento en la parte del cliente, pero no maneja muy bien ficheros grandes ni ficheros binarios. Tampoco soporta cambios at�micos.
Subversion

Subversion[8] fue escrito ante todo para reemplazar a CVS�es decir, para acceder al control de versiones aproximadamente de la misma manera que CVS lo hace, pero sin los problemas o falta de utilidades que m�s frecuentemente molestan a los usuarios de CVS. Uno de los objetivos de Subversion es encontrar la transici�n a Subversion relativamente suave para la gente que ya est� acostumbrada a CVS. Aqu� no hay sitio para entrar en detalles sobre las caracter�sticas de Subversion; acceda a su sitio web para m�s informaci�n. [Descargo: Estoy implicado en el desarrollo de Subversion, y es el �nico de estos sistemas que uso habitualmente.]
SVK

Aunque se ha construido sobre Subversion, probablemente SVK[9] se parece m�s a algunos de los anteriores sistemas descentralizados que a Subversi�n. SVK soporta desarrollo distribuido, cambios locales, mezcla sofisticada de cambios, y la habilidad de ""reflejar/clonar"" �rboles desde sistemas de control de versiones que no son SVK. Vea su sitio web para m�s detalles.
Mercurial
Mercurial

Mercurial[10] es un sistemas de control de versiones distribuido que ofrece, entre otras cosas, "una completa ""indexaci�n cruzada"" de ficheros y conjutos de cambios; unosprocotolos de sincronizaci�n SSH y HTTP eficientes respecto al uso de CPU y ancho de banda; una fusi�n arbitraria entre ramas de desarrolladores; una interfaz web aut�noma integrada; [portabilidad a] UNIX, MacOS X, y Windows" y m�s (la anterior lista de caracter�sticas ha sido parafraseada del sitio web de Mercurial).
GIT

GIT[11] es un proyecto empezado por Linus Torvalds para manejar el arbol fuente del ""kernel"" de Linux. Al principio GIT se enfoc� bastante en las necesidades del desarrollo del ""kernel"", pero se ha expandido m�s all� que eso y ahora es usado por otros proyectos aparte del ""kernel"" de Linux. Su p�gina web dice que est� "... dise�ado para manejar proyectos muy grandes eficaz y velozmente; se usa sobre todo en varios proyectos de c�digo abierto, entre los cuales el m�s notable es el ""kernel"" de Linux. GIT cae en la categor�a de herramientas de administraci�n de c�digo abierto distribu�do, similar al, por ejemplo, GNU Arch o Monotone (o bitKeeper en el mundo comercial). Cada directorio de trabajo de GIT es un repositorio completo con plenas capacidades de gesti�n de revisiones, sin depender del acceso a la red o de un servidor central."
Bazaar

Bazaar[12] est� todav�a en desarrollo. Ser� una implementaci�n del protocolo GNU Arch, mantendr� compatibilidad con el procotolo GNU Arch a medida que evolucione, y trabajar� con el proceso de la comunidad GNU Arch para cualquier cambio de protocolo que fuera requerido a favor del agrado del usuario. 