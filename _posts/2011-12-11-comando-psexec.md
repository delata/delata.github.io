---
layout: post
title: COMANDO PSEXEC
date: 2011-12-11 12:39
author: agarciaizquierdo
comments: true
categories: [COMANDOS, EJECUCIONES REMOTAS, PSEXEC.EXE, Sin categoría, WINDOWS]
---
Buenas, en este post os voy a hablar de un comando muy útil, el cual he tenido que usar bastante en las ultimas semanas, es el comando <b>psexec.exe, </b>pero,  ¿para que sirve este comando? muy sencillo, es un comando el cual nos permite conectamos de forma remota a otro equipos y lanzarle scripts, comandos...<br /><br />Por defecto no viene con el sistema operativo y es necesario descargárselo de la web de Microsoft. Cuando lo tengamos descargado simplemente debemos dejarlo en la ruta donde lo queramos ejecutar (<b>C:\Windows\System32</b> es una buena ruta)<b> </b> y ya podemos empezar a "jugar" con este comando, aqui os dejo unos ejemplos:<br /><br /><br /><ul><li>psexec @\\srvdatos\equipos.txt -u dominio\usuario -p password -n 15 -e cmd /C \\srvdatos\comandos.bat</li></ul><div><br /></div><div>Aquí lo que estamos haciendo es lanzar el script "comandos.bat" a un listado de equipos que se encuentra en el txt "equipos.txt", como este comando ejecuta comando de forma remota debemos de meter los credenciales para conectarnos a esos equipos, , y por ultimo es recomendable fijar un "time out" de intento por conexión, ya que puede daré el caso que alguno de los equipos de nuestro listado este apagado o tengamos problemas de conectividad, yo le he fijado un "time out" de 15 segundos.</div><div><br /></div><div><ul><li>psexec \\pc-administracion -u dominio\usuario -p password -n 15 -e cmd /C xcopy /z /y "\\srvdatos\conf.ini" "C:/program files/"</li></ul><div><br /></div><div>En este ejemplo mas simple lo que estamos haciendo es conectarnos directamente al un PC llamado "pc-administracion" y le estamos copiando un archivo desde un servidor a local.</div></div><div><br /></div><div>Como siempre aquí os dejo un poco de literatura de Microsoft y la descarga. Espero que os sea útil! </div><div><br /></div><div><ul><li><a href="http://technet.microsoft.com/en-us/sysinternals/bb897553">PsExec v1.98</a></li></ul></div><div><br /></div><div>Un saludo</div><div><br /></div>