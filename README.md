# Equipo Rosado - Caso de Estudio: FurniStore

##### Autor:

* Julián Santiago Ramírez Urueña

---

### Tecnologías y dependencias configuradas en el proyecto:

* Lenguaje: Java 17
* Framework: Spring Boot + Lombok
* Calidad de código: SonarQube y JaCoco
* Gestión de dependencias: Maven
* Control de versiones: GiHub


##### Evidencia de la compilación del ambiente de trabajo:

* Incluyendo las dependencias de Lombok y SonarQube

![img.png](docs/images/BUILDSUCCESS.png)


#### Estrategia de Versionamiento y Branches

- `main`: versión estable para producción.
- `develop`: rama de desarrollo principal.
- `feature/*`: nuevas funcionalidades.
- `bugfix/*`: correcciones de errores.
- `release/*`: preparación de versiones.  

#### Notación de los commits:

***Cada commit realizado debe seguir el siguiente template: “feat: Equipo Rosado Parte n - Acción realizada”.***

---

### Caso de Estudio FurniStore:
Se estará trabajando en el desarrollo de una solución tecnológica que permita digitalizar la operación de la reconocida tienda de muebles ***FurniStore***. Dicha solución tecnológica sentará las bases de la programación orientada objetos en conjunto a la implementación de buenas prácticas, como lo son los patrones de diseño y/o los principios SOLID. De este modo se garantiza que FurniStore reciba el varias veces mencionado ***recurso tecnológico, robusto, escalable y profesional***.

### Justificación Patrones de Diseño y principios SOLID:

* Patrones de Diseño

Se identificó el patrón de diseño Abstract Factory Method. De modo que FurniStore maneja un catálogo amplio de mueblería, se optó por generalizar la abstracción de los muebles a través de una clase abstracta llamada ***Furniture***. Esta clase asbtracta contiene varios atributos y métodos que serán compartidos por las subclases (muebles en sí) que la extiendan, de ese modo, se gestionan los diferentes artículos de forma 'independiente'. 

Bajo este mismo orden de ideas, se decidió implementar el patrón Abstract Factory, a través del cual se dividirán los varios tipos de muebles según su estilo visual. Consecuentemente se irán estableciendo los gremios bajo los cuales se irán agrupando cada uno de los muebles; así, se definen entonces las ***familias del catálogo***.

* SOLID

En cuanto a los principios SOLID, tenemos que el SRP es cumplido pues, Furniture (modelo base con atributos y getters), Catalog(gestiona la colección de muebles disponibles), ShoppingCart(gestiona los ítems a agregar o remover del carrito), Billing (toma las riendas de la facturación), FurnitureFactory (fábrica de los objetos agremiados) y User (según cada tipo de usuario) se encargan de una y solamente una única responsabilidad.
También, OCP se hace presente pues, el sistema no requiere de modificaciones, sin embargo, cuenta con extensibilidad. Esto porque se pueden agregar nuevas familias de objetos, nuevos objetos como tal y también, nuevos tipos de usuario.

Por parte de LSP las subclases de Furniture (Chair, Table, Sofa) pueden reemplazar a Furniture sin problemas y cualquier familia concreta de FurnitureFactory sustituye a la interfaz sin romper el sistema. ISP se cumple a través de FurnitureFactory pues se enfoca únicamente en la creación de artículos haciendo que cada implementación cree únicamente aquello que le corresponde.

Finalmente, DIP se satisface porque los clientes dependen de abstracciones y no de implementaciones concretas. 

---

### DIAGRAMACIÓN:

* Diagrama de Contexto:

![Contexto FurniStore.png](docs/uml/Contexto%20FurniStore.png)

URL al DCT - https://lucid.app/lucidchart/3c7e970a-5d55-479e-86c3-a6f86f0c373e/edit?viewport_loc=-659%2C-169%2C3476%2C1631%2CHWEp-vi-RSFO&invitationId=inv_e6326696-8a7c-4b09-a66b-359f4415f0ca

* Diagrama de Clases:

![Inicial FurniStore.png](docs/uml/Inicial%20FurniStore.png)

URL al DC - https://lucid.app/lucidchart/1bf0b5d2-d569-4900-88bb-5eaa509e0114/edit?viewport_loc=-73%2C-228%2C4222%2C2036%2CHWEp-vi-RSFO&invitationId=inv_1a24da31-8ed7-44f6-83a3-b4d82121f8ab

* Diagrama de Casos de Uso:

![Casos de Uso FurniStore.png](docs/uml/Casos%20de%20Uso%20FurniStore.png)

URL al DCU - https://lucid.app/lucidchart/0f1d32bc-fd34-45b3-980e-c12877d7f0d0/edit?viewport_loc=350%2C504%2C2564%2C2119%2C.Q4MUjXso07N&invitationId=inv_d90147c2-6560-4400-9224-590d79dcfb7f

