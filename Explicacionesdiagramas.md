#Diagrama de clinica de mascotas
En este diagrama se observaron solo 4 clases, y aunque se pueda pensar que la clinica no es necesaria, decidi dejarla ya que reoresenta  el lugar principal
de toda la sitaucion, por lo que las clases quedaron: Clinica, Cita, Dueño (escrito como dueno porq la ñ no se lee) y Mascota
Luego en el diagrama con el icono - que representa lo privado, se escribieron lo que defini como atributos de cada clase. Por ejemplo: Dueno -String id
Tambien van los metodos con el icono de publico +, por ejemplo, en citas es importante que se realice un registro de la cita --> registrarCita()
Por ultimo, las relaciones: 
1. Sabemos q los dueños pueden tener mas de una mascota por eso el rombo
2. Clinica tiene una relación con mascota, dueño y citas  ya que gestiona toda la información y es el lugar donde se enfoca la situacion.
3.  A pesar de que citas solo pueda atender a 1 mascota, las mascotas pueden tener mas de una cita en rangos de tiempos, por eso las dos relacioneshechas en el diagrama
4. La relación entre la clase Clínica y Mascota era necesaria en la jerarquía, al principio  no estaba segura, pero considero que es importante incluirla porque es una de las relaciones más generales
 en el sistema, y eso es que la clinica puede atender a varias mascotas. Además, esta relación permite que sigan las otras relaciones: Las mascotas puedan tener citas dentro de la clínica

#diagrama de clase musica 
En este diagrama hay 4 clases: Escuela, Curso, Estudiante e Inscripción. Aunque la escuela podría parecer innecesaria, la dejé porque es el centro de todo el sistema.

Las relaciones las organice de esta manera:
- Escuela tiene varios Estudiantes y ofrece varios Cursos.
- Estudiantes pueden inscribirse en varios cursos y un curso tiene varios estudiantes.
- Inscripción conecta a estudiantes y cursos porque no todos los estudiantes toman los mismos cursos al mismo tiempo.
- Cada inscripción pertenece a un estudiante y un curso.
- Sobre los atributos y métodos:
Tambien: 
Usé List en Escuela porque maneja varios datos.
De nuevo el simbolo de privado (-) para atributos
Métodos como registrarEstudiante() y listarCursos() son clave para manejar la informacion y sus estados
En Inscripción, puse estado (booleano) para saber si sigue activa o se completo el curso y fechainscripcion para tener registro.

Las clases en mayúscula porque son entidades principales.
Al principio dudé si Escuela debía conectarse con Inscripción, pero vi que no era necesario porque la relación se da a través de los estudiantes. Con esto, el sistema queda claro y organizado. 
