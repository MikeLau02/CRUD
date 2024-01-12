# CRUD

Registrar estudiantes con sus respectivos datos, asignandole a cada uno un Id y además guardando los datos.

CRUD creado en JAVA, utilizando el framework de Spring y sus dependencias, conectándolo a la base de datos MySQL

Utilización de diversos Métodos: 

Entity:
- Se crea la conexión con la base de datos "tbl_student"
      - Se indica cual es la llave primaria con @Id y @GeneratedValue, de tipo Long studentId
      - Demás variables de tipo privada y especificando que el email debe ser unico (unique=true)

Repository:
- Interface

Service:
- Se llama el Repository con @Autowired (studentRepository)
- getStudent = studentRepository.findAll -> Busca los elementos y los retorna.
- getStudent = studentRepository.findById -> Recibe el Id y le envío la infoemación que llega
- saveOrUpdate = Guarda o actualiza la información del estudiante
- delete = Elimina através del id


Controller:
  Se importa @RestController
  path = "api/v1/students" -> Ruta
  @Autowired -> Nos permite enlazar los servicios

  
  
  
