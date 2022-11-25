# Tabla de contenidos
<ol type="1">
  <li>Introduccion</li>
  <li>Descripcion general</li>
  <li>Requerrimientos externos</li>
  <li>Funcionalidades del sistema</li>
  <li>Otros requerrimientos no funcionales</li>
</ol>

## 1. Introduccion
<ul>
  <li>Objetivo</li>
  Se explican los requerrimientos del sistema de software que son necesarios <br />
  para que la aplicacion funcione de forma correcta asi como una explicacion <br />
  integral de las funcionalidades de la aplicacion y como dar un uso correcto.
  <li>Convenciones</li>
  Este documento sigue el estandar propuesto por la IEEE. Al leer este documento <br />
  tome en cuenta que el usuario puede usar la aplicacion desde la modalidad tanto <br />
  de asesor como de alumno que toma asesorias. Cuando nos refiramos a que el usuario <br />
  esta impariendo asesorias le llamaremos "asesor", mientras que si el usuario esta <br />
  tomando la asesoria le diremos "estudiante".
  <li>Audiencia</li>
  Este documento esta dirigido a estudiantes del ITAM que buscan sacar el maximo <br />
  provecho a esta aplicacion, pues se indica como explorar todas las funcionalidades <br />
  ademas se perimite conocer un poco sobre la estructura interna de la aplicacion y <br />
  los requisitos para usarla.
  <li>Enfoque del producto</li>
  La aplicacion fue disenada para alumnos del ITAM, por ahora el uso esta limitado <br />
  a este sector de la comunidad, pues no ofrecemos soporte a maestros ni se imparten <br />
  asesorias sobre materias ajenas al ITAM.
  <li>Referencias</li>
  IEEE template for software requirement specification.
</ul>

## 2. Descripcion general
<ul>
  <li>Prespectiva del producto</li>
  La aplicacion es para facilitar la vida a los estudiantes del ITAM, tanto a los que buscan <br />
  aprender como a los que buscan impartir conocimiento. La aplicacion ofrece un espacio seguro <br />
  para adquirir conocimientos y generar dinero, la interfaz es facil de usar y cualquier alumno <br />
  tiene acceso a esta herramienta, ya que la trasnparencia es vital toda asesoria muestra el <br />
  contenido que cubre y su costo. Para que sea facil de usar la aplicacion, desde tu misma <br />
  cuenta puedes dar asesorias o tomarlas.
  <li>Funcionalidades</li>
  <ol>
    <li>Inicio de sesion</li>
    Se necesita un nombre de usuario y contrasena,<br /> 
    con esto basta para darse de alta y acceder <br />
    a la aplicacion.
    <li>Crear asesoria</li>
    Si buscas compartir tus conocimientos puedes dar de alta un curso en la modalidad <br />
    de asesor de alguna o varias materias que imparte el ITAM, al crear una asesoria <br />
    deberas dar una descripcion y el temario que vas a cubrir, ademas de establecer un <br />
    costo.
    <li>Subir multimedia</li>
    La aplicacion ofrece un espacio dnde puedes subir links a multimedia, ya sea <br />
    desde ka modalidad de asesor o estudiante, este contenido solo podra ser visto <br />
    por miembros de la asesoria.
    <li>Inscribirte a asesorias</li>
    Desde la modalidad de estudiante podras meterte a cuantas asesorias quieras, <br />
    siempre y cuando estas existan, esten disponibles y estes dispuesto a pagar.
    <li>Pagar</li>
    En la modalidad de estudiante ofrecemos metodos de pago
  </ol>
  <li>Casos de uso</li>
Crear: Contiene los ids de los usuarios y de los cursos.
Usuario: Contiene la id del usuario junto con su nombre, teléfono y correo.
Inscrito: Contiene los ids de los usuarios y de los cursos.
Curso: Contiene la id del curso junto con su nombre, materia, precio.
Temario: Contiene la id del temario junto con su nombre y la id del curso.
Multimedia: Contiene la id del multimedia, su nombre, su link junto con la id del temario y la id del curso
  ![Imagen1](https://user-images.githubusercontent.com/116897605/203907008-d37903c0-4b84-4b17-adaa-ac3425697cc8.png)
  <li>Operating enviroment</li>
  Se uso el framework django que ofrece python y so hosteo en una web.
  <li>Design and implementation constraints</li>
    <ol>
      <li>Tiene que seguir siendo desarrollada en Django ya que usamos muchas características del lenguaje para diseñar el proyecto</li>
      <li>La IP tiene que ser redirigida a un host externo y tiene que tener la capacidad mínima de 10 gbs para la base de datos.</li>
      <li>Se recomendaría tener pocos cursos agregados para que los tiempos de espera sean adecuados, esto debido a la forma en que esta hecho la aplicación, optimiza el diseño y la forma grafica a costa de la velocidad de respuesta.</li>
   </ol>
  <li>Supuestos y dependencias</li>
 Esta aplicación no esta asociada con el ITAM, los cursos son impartidos por alumnos en salones previamente pedidos a la institución.
</ul>

## 3. Requerrimientos externos
3.1 User interface <br />
3.2 Hardware interfaces: <br />
  Se utiliza solamente una computadora para un host temporal local con las siguientes especificaciones: <br />
  ![Imagen2](https://user-images.githubusercontent.com/116897605/203908193-35312aa2-beea-461b-8b39-b940da81972c.png)
<br />
3.4 Softwate interface <br />
HOST: AWS Lambda <br />
Lenguaje: Django versión 2.1 <br />
IDE: Visual Studio Code versión 1.73 <br />
Ejecutable: Google Chrome o Cualquier navegador <br />
3.5 Communiaction interface: <br />
Se utiliza una conexión desde Visual Studio Code hacia el navegador predeterminado del usuario para empezar a correr la aplicación. Además todas las solicitudes hacia la aplicación para ver cursos y agregar cursos los maneja los servicios de Amazon (AWS) <br />

## 4. Funcionalidades del sistema



  
