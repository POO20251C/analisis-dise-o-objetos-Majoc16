[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/vTkcPn0-)
# 2.-Dise-o-Orientado-a-Objetos
Primer acercamiento y prácticas guiadas e individuales de POO
#Diagrama UML - Proyecto

```mermaid
classDiagram
direction TB
 class Clinica {
	    -list  citas
	    -list duenos
	    -list mascotas <Mascota>
	    +registrarDueño()
        +registrarMascota(Mascotam): void
	    +agendarCita()
        +listarCitas(): List<Cita>
    }

    class Dueno {
	    -String id
	    -Date fechaR
	    -list  mascotas <Mascota>
	    +registrarMascota()
	    +gets()
	    +sets()
    }

    class Cita {
	    -mascotatendida Mascota
	    -Date fechacita
	    -String hora
	    -Boolean estado
	    +registrarCita()
	    +cambiarEstado()
	    +registrarHora()
    }

    class Mascota {
	    -String nombre
	    -String especie
	    -Date fechaNacimiento
	    +registrarNombre()
	    +gets()
	    +sets()
    }

   

    Cita "1" --o "many" Clinica
    Mascota "1" --o "many" Cita
    Mascota "1" --o "many" Dueno
    Mascota "1" --o "many" Dueno
    Cita "1" --> "1" Mascota : Atiende
    Clinica "1" --o "many" Dueno : Tiene
    Clinica "1" --o "many" Mascota : Atiende

#Diagrama UML- clases de musica 

```mermaid
classDiagram
    direction TB
    class Escuela {
        -List cursos
        -List estudiantes
        -List inscripciones
        +registrarEstudiante()
        +registrarCursos()
        +crearInscripciones()
        +RegistrarEstadosCursos()
        +listarEstudiantes(): List<Estudiante>
        +listarCursos(): List<Curso>
        +listarInscripciones(): List<Inscripcion>
    }

    class Curso {
        -String nombre
        -int duracion
        -list inscripcion 
        +getduracion()
        +setduracion()
    }

    class Estudiante {
        -string id 
        -list cursos
        +listarCursos(): List<Curso>
        +get()
        +set()
        +cursosPresenta()
    }

    class Inscripcion {
        -String curso 
        -String estudiante
        -Boolean estado
        -Date fechainscripcion
        +registrarEstudiante()
        +get()
        +set()
        +registrarCurso()
        +registrarFecha()
    }

    
    Estudiante "1" --o "many" Curso: participan
    Escuela "1" --o "many" Estudiante: tiene
    Escuela "1" --o "many" Curso: ofrece
    Estudiante "1"  --o "many" Inscripcion: puede tener
    Inscripcion "1" --> "1" Estudiante: tiene
    Inscripcion "1" --> "1" Curso: correponde a
    Curso "1" --o "many" Inscripciones: tiene

    
