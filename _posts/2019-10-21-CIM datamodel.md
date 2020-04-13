---
layout: post
title: CIM Datamodel
date: 2019-10-21
author: agarciaizquierdo
comments: true
categories: [CIM, Splunk Apps, Splunk Data Model, Splunk Español]
---
<div class="separator" style="clear: both; text-align: center;">
<img border="0" data-original-height="400" data-original-width="770" height="166" src="https://cdn.apps.splunk.com/media/public/icons/c391c2fc-f0f5-11e9-8aa3-02dfd068cf86.png"/></div>  

Hace ya tiempo hice un  [post](https://agarciaizquierdo.blogspot.com/2019/03/splunk-data-model.html), sobre los **Data Model**, pero me deje una cosa en el tintero, y creo que viene perfecto para poder hacer un post, y explicar uno de los grandes beneficios de los **Data Model**, la **normalización**.

Creo que es uno de los puntos clave cuando nos encontramos un entorno con varias fuentes, por ejemplo dos fabricantes distintos de **firewall** (F1 y F2 en este caso) y nuestro **LDAP**, nos podemos encontrar diferentes campos con el mismo significado pero diferente nombre, por ejemplo, puede que el campo usuario se llame **user\_name** en el F1 **user\_n** en el F2 y en el LDAP sea **account\_name**.

Todo esto **Splunk** lo tiene más que pensado, y para ello dispone de una App llamada **[CIM](https://splunkbase.splunk.com/app/1621/)**, la cual dispone de una estructura de campos bastante grande, donde podemos apoyarnos para esta **normalización**, además dispone de una [documentación](https://docs.splunk.com/Documentation/CIM/latest/User/Overview) bastante completa, donde nos muestra el nombre del campo en función del **Data Model** (Malware, DLP...). 

Por último, es importante tener en cuenta el almacenamiento de la aceleración de los **Data Model**, en este [post](https://yourprodismy.dev/splunk/2019/07/12/splunk_datamodel_acceleration_location.html) lo explican bastante bien.
