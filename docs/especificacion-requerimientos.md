# Especificación de Requerimientos

## 1. Descripción del sistema

## 2. Integrantes

- Nombre: Juan David Delgado
- Nombre: Jeronimo Mazo Diez
- Nombre: Juan José Ortega Aguilera

## 3. Requerimientos Funcionales

### RF-01 - [Registro tutoria]

#### Resumen
El sistema deberá permitir que un profesor registre una nueva tutoría académica, proporcionando la información necesaria para que posteriormente los estudiantes puedan consultarla e inscribirse.
#### Entradas

| Entrada                        | Tipo de dato | Descripción                                                       |
| ------------------------------ | ------------ | ----------------------------------------------------------------- |
| Código del profesor            | String       | Código que identifica al profesor que ofrece la tutoría.          |
| Tema de la tutoría             | String       | Tema o contenido académico que será tratado en la tutoría.        |
| Fecha                          | Date         | Fecha en la que se realizará la tutoría.                          |
| Hora de inicio                 | Time         | Hora en la que comenzará la tutoría.                              |
| Cantidad máxima de estudiantes | Integer      | Número máximo de estudiantes que podrán participar en la tutoría. |


#### Reglas o condiciones
La fecha de la tutoría no puede ser anterior a la fecha actual.
La cantidad máxima de estudiantes debe estar entre 1 y 10.
El sistema deberá asignar automáticamente un identificador único a la tutoría.
El registro solo se realizará si todas las condiciones son válidas.
#### Salidas

| Salida                      | Tipo de dato   | Descripción                                                  |
| --------------------------- | -------------- | ------------------------------------------------------------ |
| Identificador de la tutoría | Integer/String | Identificador único asignado a la tutoría.                   |
| Mensaje de confirmación     | String         | Informa al profesor que la tutoría fue creada correctamente. |


#### Resultado esperado
La tutoría queda registrada correctamente en el sistema con un identificador único y el profesor recibe un mensaje de confirmación.


### RF-02 - [consulta-tutorias]

#### Resumen
El sistema deberá permitir a los estudiantes consultar las tutorías disponibles para una fecha determinada y, opcionalmente, filtrar los resultados por asignatura o tema de interés.
#### Entradas


| Entrada           | Tipo de dato | Descripción                                                                            |
| ----------------- | ------------ | -------------------------------------------------------------------------------------- |
| Fecha de consulta | Date         | Fecha para la cual el estudiante desea consultar las tutorías.                         |
| Asignatura o tema | String       | Criterio opcional utilizado para filtrar las tutorías según el interés del estudiante. |


#### Reglas o condiciones
La fecha de consulta es obligatoria.
La asignatura o tema es opcional.
Si se proporciona un tema, solo deberán mostrarse las tutorías que correspondan con este.
Solo deberán mostrarse tutorías que correspondan con los criterios de búsqueda.
Si no existen tutorías que coincidan con la búsqueda, el sistema deberá informar al estudiante.
#### Salidas

| Salida                   | Tipo de dato   | Descripción                                                          |
| ------------------------ | -------------- | -------------------------------------------------------------------- |
| Identificador de tutoría | Integer/String | Identificador de la tutoría encontrada.                              |
| Tema                     | String         | Tema de la tutoría.                                                  |
| Profesor responsable     | String         | Profesor encargado de la tutoría.                                    |
| Fecha                    | Date           | Fecha de realización de la tutoría.                                  |
| Hora                     | Time           | Hora de inicio de la tutoría.                                        |
| Cupos disponibles        | Integer        | Cantidad de estudiantes que aún pueden inscribirse.                  |
| Mensaje                  | String         | Informa si no se encontraron tutorías que coincidan con la búsqueda. |


#### Resultado esperado
El estudiante recibe una lista de las tutorías disponibles que coinciden con los criterios de búsqueda, mostrando su información y los cupos disponibles. Si no existen coincidencias, recibe un mensaje informativo.


### RF-03 - [Nombre del requerimiento]

#### Resumen

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|

#### Reglas o condiciones

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|

#### Resultado esperado


### RF-04 - [Nombre del requerimiento]

#### Resumen

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|

#### Reglas o condiciones

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|

#### Resultado esperado


## 4. Gestión de Versiones

### Ramas utilizadas

### Proceso de integración

### Conflictos encontrados
