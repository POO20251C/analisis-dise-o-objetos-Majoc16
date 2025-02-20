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
