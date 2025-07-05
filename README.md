# Proyecto de POO 

## Descripción

Este proyecto es un sistema de gestión de contenido audiovisual creado con las siguientes clases:

#### Clases Base:

- `ContenidoAudiovisual` (clase abstracta base, Esta seria la super clasegeneral)

#### Clases de Contenido:

- `Pelicula` (extiende ContenidoAudiovisual)
- `SerieDeTV` (extiende ContenidoAudiovisual)
- `Documental` (extiende ContenidoAudiovisual)

#### Clases de Relación (Desprenden de las clases de contenido):

- `Actor` - Esta directamente relacionada con la clase de contenido llamada Película (Asociación)
- `Temporada` - Esta directamente relacionada con la clase de contenido llamada SerieDeTV (Composición)
- `Investigador` - Esta directamente relacionada con la clase de contenido llamada Documental (Asociación)

### Las relaciones Implementadas son:

1. **Actor ↔ Película (Asociación)**

   - Una película puede tener varios actores
   - Un actor puede participar en varias películas
   - Los actores existen sin dependencia de las películas

2. **Temporada ↔ SerieDeTV (Composición)**

   - Una serie de TV puede tener varias temporadas
   - Las temporadas no existen sino existe la serie
   - La eliminación de la serie elimina con sigo todas sus temporadas

3. **Investigador ↔ Documental (Asociación)**
   - Un documental puede ser hecho por varias investigadores
   - Un investigador puede trabajar en varios documentales
   - Los investigadores existen sin necesidad de la existencia del documental

### Estructura del Proyecto

```
poo_unidad1/
├── src/
│   ├── uni1a/
│   │   ├── ContenidoAudiovisual.java
│   │   ├── Pelicula.java
│   │   ├── SerieDeTV.java
│   │   ├── Documental.java
│   │   ├── Actor.java
│   │   ├── Temporada.java
│   │   └── Investigador.java
│   └── poo/
│       ├── PruebaAudioVisual.java
│       └── PruebaRelaciones.java
└── README.md
```

### Compilación y Ejecución

## Como requisitos fundamentales para la ejecución del programa se necesita:

- Java JDK 8 o superior
- Terminal o línea de comandos

## Los pasos para compilar el código son:

1. Abrir terminal en la carpeta raíz del proyecto
2. Ejecutar el comando de compilación:
   ```bash
   javac -d . src/uni1a/*.java src/poo/*.java
   ```

## Los pasos para ejecutar el programa son:

1. Ejecutar la clase de prueba principal:

   ```bash
   java poo.PruebaRelaciones
   ```

2. O ejecutar la clase de prueba original:
   ```bash
   java poo.PruebaAudioVisual
   ```

## Características de las Clases

#### Actor

- Atributos: nombre, apellido, edad, nacionalidad, especialidad
- Métodos: getters/setters, mostrarInformacion(), getNombreCompleto()

#### Temporada

- Atributos: número de temporada, número de episodios, duración promedio, fechas
- Métodos: gestión de episodios, cálculo de duración total, mostrarInformacion()

#### Investigador

- Atributos: nombre, apellido, especialidad, institución, años de experiencia, título académico
- Métodos: getters/setters, mostrarInformacion(), getCredenciales()

## Ejemplo de Uso

El archivo `PruebaRelaciones.java` contiene ejemplos completos de cómo usar todas las relaciones implementadas, incluyendo:

- Creación de actores y asociación con la clase películas
- Creación de temporadas y composición con la clase series de TV
- Creación de investigadores y asociación con la clase documentales

### Notas de Implementación

- Con las clases se incluyen métodos para agregar, eliminar y mostrar las entidades relacionadas
- Se utilizan `List<Actor>`, `List<Temporada>` y `List<Investigador>` para manejar las relaciones uno-a-muchos
