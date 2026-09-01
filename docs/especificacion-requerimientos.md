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


### RF-03 - [Inscripción a una tutoría]

#### Resumen
Permitir que un estudiante solicite y registre su inscripción en una tutoría disponible utilizando su código estudiantil y el identificador de la tutoría.

#### Entradas

| Entrada                     | Tipo de dato | Descripción                                                                 |
| --------------------------- | ------------ | --------------------------------------------------------------------------- |
| Código estudiantil          | String       | Código que identifica al estudiante que desea inscribirse.                  |
| Identificador de la tutoría | String       | Identificador único de la tutoría a la que el estudiante desea inscribirse. |


#### Reglas o condiciones
-El estudiante debe encontrarse activo en la Universidad.
-La tutoría debe existir en el sistema.
-La tutoría debe tener al menos un cupo disponible.
-El estudiante no debe estar previamente inscrito en la tutoría.
-Si todas las condiciones se cumplen, se debe registrar la inscripción y disminuir en uno la cantidad de cupos disponibles.
-Si alguna condición no se cumple, la inscripción no debe realizarse y el sistema debe informar el motivo.

#### Salidas

| Salida                         | Tipo de dato | Descripción                                                                       |
| ------------------------------ | ------------ | --------------------------------------------------------------------------------- |
| Confirmación de inscripción    | String       | Mensaje que informa que la inscripción fue realizada exitosamente.                |
| Mensaje de error               | String       | Mensaje que informa el motivo por el cual no fue posible realizar la inscripción. |
| Cupos disponibles actualizados | Integer      | Cantidad de cupos restantes después de una inscripción exitosa.                   |


#### Resultado esperado
El sistema registra correctamente la inscripción del estudiante, actualiza la cantidad de cupos disponibles de la tutoría y muestra un mensaje de confirmación. Si alguna de las condiciones requeridas no se cumple, no registra la inscripción y muestra el motivo correspondiente.


### RF-04 - Cancelación de inscripción a tutoría

#### Resumen

Permitir que un estudiante que se encuentre inscrito en una tutoría pueda cancelar su participación.

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|
| código estudiantil | String | Código que identifica al estudiante que desea cancelar su inscripción. |
| identificador de la tutoría | String | Identificador único de la tutoría en la que el estudiante desea cancelar su participación. |

#### Reglas o condiciones

- El estudiante debe tener una inscripción previa en la tutoría.
- La tutoría debe existir.
- La tutoría no debe haber comenzado.
- Si alguna de las condiciones no se cumple, la cancelación no deberá realizarse.

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|
| mensaje de confirmación | String | Informa al estudiante que la cancelación fue realizada correctamente. |
| mensaje de error | String | Informa el motivo por el cual no fue posible realizar la cancelación. |

#### Resultado esperado

La inscripción del estudiante es eliminada, se libera nuevamente el cupo correspondiente de la tutoría y se informa al estudiante que la cancelación fue realizada correctamente.
