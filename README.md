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


