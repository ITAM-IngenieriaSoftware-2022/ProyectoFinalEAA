# Plan de calidad siguiendo estandar IEEE 829
## 1. Test plan identifier
  Primera version, plan de calidad de la aplicacion de asesorias. 
## 2. Introduction
El objetivo del plan de calidad es no pronasticar y marcar tiempos factibles parea poder entregar un producto de alta calidad y que culpa con todos los requisitos. El plan toma en cuenta el alcance que nuestra aplicacion va a tener y los recursos con los que contamos. Debido a que somos estudiantes y al mismo tiempo trabajamos el tiempo es en extremo limitado por esto es necesario planear etapas del proyecto y tener un intinerario. La aplicacion solo cubre materias que imparte el ITAM y solo contempla a estudiantes del ITAM.
## 3. Test items
<ul>
  <li>botones</li>
  <li>Conexion a bases de datos</li>
  <li>Inicio de sesion</li>
  <li>vista</li>
</ul>

## 4. Features to be tested
Vamos a probar las siguientes funcionalidades y que interactuen de forma correcta con la base de datos <br />
<ol>
  <li>Probaremos el inicio de sesion</li>
  Probando casos validos e invalidos
  <li>Crear asesorias</li>
  Pruebas exhaustivas
  <li>Subir multimedia</li>
  Diferentes links a diferetes herramientas exteriores
  <li>Inscripcion a cursos</li>
  Multiples altas
</ol>
## 5. Features not to be tested
La funcionalidad el pago no sera probada <br />
## 6. Approach
Usaremos pruebas de regresion que  nos permite acceso a la documentacion de estructuras de datos internas y a los algoritmos utilizados. Este metodo nos va a permitir identificar errores rapidamente. Dados ciertos datos de arranque vamos a monitorear el estado de proyecto en cada etapa hasta que lleguemos a outputs deseados. Ademas haremos pruebas de regresion cada vez que hagamos cambios, probaremos as clases y sus metodos asi como cada boton, esto inmediatamente despues de que este listo. Es decir, no vamos a esperar a que eset toda la aplicacion lista, sino que haremos pruebas modulares, pues de esta forma sabremos que parte de la aplicacion falla y en que momento. Al final haremos pruebas globales, pero solo si los componentes estan fucnionando. En ningun caso seguiremos avanzando si no corre algun cacho del codigo sin importar que ese cacho del codigo no afecte a otras partes, esto porque no queremos que se acumulen errores ni que nos sea complicado encontralos. <br /> 
## 7. Item pass/fail criteria
Toda funcionalidad recibira una calificacion discreta del 1 al 3, 1 siendo que no cumple, 2 siendo satisfactorio y 3 listo para entrega. Se pone atencion a que la funcionalidad corra y sea rapida, si corre pero tarda sera un 2 si no cumple ninguna sera un 1. 
<ul>
  <li>Inicio de sesion</li>
  Aqui no basta con entrar a la sesion, el acceso debe ser rapido, ademas en caso de usuario invalido o contrasena incorrecta se debe desplegar un mnesaje adecuado
  <li>Crear curso</li>
  Crear un curso debe ser rapido, y se deben poder agregar elementos al temario y poner una descripcion. Solo si se cumplen todos estos requisitos recibira un 3 y tendra el visto bueno.
  <li>Subir multimedia</li>
  En esta funcionalidad la escala es olo 1 o 3, pues es subir un link a una herramienta externa
  <li>Inscribirse a curso</li>
  Se da 1 si no se puede realizar esta accion, 2 si se puede realizar pero es tardado, o si no prevee casos extremos como inscribirte al mismo curso dos veces (que se le podria atribuir al usuario el error). 
</ul>

## 8. Suspension criteria and resumption requirements

No hay criterio por el cual algo sea exepto a pruebas, salvo falta de recursos

## 9. Test deliverables

En forma de capturas de pantalla 

## 10. Testing tasks
Para probar crearemos un usuario y dentro de la aplicacion llevaremos acabo todas las funcionalidades. Para el inicio de sesion intentaremos acceder con usarios incorrectos y/o contrasenas incorrectas. Siempre las pruebas seran exhaustivas para cada funcionalidad, es decir, vamos a robar los casos extremos.
Defectos reccurentes
<ul>
  <li>Connection timeout</li>
  <li>Undefined behaviour</li>
  <li>No se actualiza base de datos</li>
</ul>

## 11. Enviromental needs
Solo usamos una computadora externa y nos metimos a la pagina web y usamos la app desde ahi, no se usaron softwares externos ni hardware especifico para hacer las pruebas, no se necesito equipo extra.

## 12. Responsabilities
Esteban se encargo de probar el inicio de sesion, Alejandro se encargo de que los botones dentro de la aplicacion fucnionaran correctamente,m mientras que Alan se encargo de la conexion de la aplicacion a la base de datos (SQL) y que esta base de datos funcinara correctamente. Todos los integrantes crearon un usuario y usaron todas las funcionalidades.
## 13. Staffing and training needs
El equipo ya contaba con las habilidades necesarias para hacer las pruebas
## 14.Schedule
## Risks and contingencies
Los riesgos son en su mayoria de mal uso de la aplicacion, como subir contenido inapropiado o falso. Riesgos internos son que elinicio de sesion falle y puedas entrar a la cuenta de otros usarios, tambien existe el riesgo de que el pago no se efectue. 
