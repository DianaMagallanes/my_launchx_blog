---
title: "Errores en el camino"
date: 2022-04-23
description: 'Post 1 de los errores que he tenido durante el curso de Backend en Launch X'
---
<h3>Hola. Este blog lo utilizare como una bitácora de los errores que voy teniendo durante el curso de Backend. </h3>

En los ejercicios de la semana 3 estuvimos realizando proyectos de js con sus respectivas pruebas. Especificamente en el ejercicio 5 tuve un error que fue descuido mío 
ya que no preste atención a la estructura de código (básicamente tuve que refactorizar SI o SI 😅 )

Este ejercicio tenía 4 requerimientos en los cuales hacíamos diversas pruebas para corroborar que la información
que proporcionaba el usuario fuera válida.
En el requerimiento 3 al leer el título de la prueba (*regresar un error si no faltaban propiedades*) decidi revisar
que métodos js tiene para revisar si un objeto tiene una propiedad y encontre el método hasOwnProperty, el cual al 
darle el nombre de la key revisa si existe.

Esto no funcionaba bien para la prueba 4 (de hecho para la 3 tampoco ya que analizandolo bien debía verificar que se contara con todas las propiedades no con alguna, asi que
en lugar de utilizar O debí utilizar Y ( ||  >  && ) y dentro del else poner el mensaje de error).

Pero bueno, el error lo encontré al realizar la prueba 4. En la prueba 4 dabamos todas las propiedades así que se cumplían con las condiciones de hasOwnProperty y por lo 
tanto entraba a esa parte de código y arrojaba el error de "necesitan un valor válido" en lugar de crear el objeto user.

¿Cómo lo corregí?

En lugar de verificar si se contaba con la propiedad revisaba si no estaba indefinida, básicamente lo contrario a lo que hacía. Para esto utilice compare si las propiedades 
eran iguales a undefined.

En fin, a veces nuestro cerebro cree que tenemos una idea buena pero resulta luego resulta que no la pensamos a profundidad. Para dar con la idea de como codificar la prueba
no tarde tanto pero vieran como tarde para corregirlo donde no sabía que estaba fallando de la prueba 4 (revisando que escribi todo bien, que tenía todo guardado, etc.)
