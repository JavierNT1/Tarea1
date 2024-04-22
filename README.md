
# # Tarea1 Sistema de Gestión de Pacientes en Hospital

## Descripción

Este sistema facilita la gestión de la atención hospitalaria, permitiendo a los usuarios registrar nuevos pacientes, asignarles prioridades y visualizar la lista de espera, entre otras funciones. Diseñado para optimizar la eficiencia en la atención médica, garantiza que los pacientes con prioridades más altas reciban atención prioritaria de manera ágil.

## Cómo compilar y ejecutar

Para ejecutar el `main`, primero debemos compilar los archivos fuente. Desde la carpeta raíz del proyecto, ejecuta el siguiente comando en tu terminal:

```bash
gcc tdas/*.c main.c -Wno-unused-result -o main
```
Y luego ejecutar:

```bash
./main
```

## Funcionalidades

### Funcionando correctamente:
- Registrar pacientes con sus datos y una prioridad inicial(Baja = 3).
- Asignar o modificar la prioridad de los pacientes.
- Ver la lista de espera de pacientes, ordenada por prioridad y hora de registro.

### Problemas conocidos:

- Atender al siguiente paciente, respetando el orden de prioridad. La función me permite atender al siguiente paciente, pero no por hora; está desordenado.
  Esto puede ocurrir por un ordenamiento inconsistente: Si la función de ordenamiento (lower_than) no está bien implementada o no se llama en el lugar adecuado, la lista podría no estar ordenada correctamente.

### A mejorar:

- Implementar una interfaz de usuario más amigable.
- Permitir la edición de los datos de los pacientes.
- Permitir ingresar el nombre con letras en mayúsculas, minúsculas e intercaladas.
- Mejorar el sistema de hora.

## Ejemplo de uso

**Paso 1: Registrar un Nuevo Paciente**

Se comienza registrando un nuevo paciente que acaba de llegar al hospital. Se le piden nombre, edad, sintomas y hora de llegada.

```
Ingrese su opción: 1
Registrar nuevo paciente
Ingrese el nombre del paciente: Gabriel
Ingrese la edad del paciente: 25
Ingrese los síntomas del paciente: Tos
Ingrese la hora de llegada del paciente: 12
```

El sistema registra a Gabriel con una prioridad inicial "Bajo" y guarda la hora actual de registro. La prioridad inicial puede ser ajustada más tarde basada en una evaluación médica más detallada.

**Paso 2: Asignar Prioridad a un Paciente**

Tras una evaluación inicial, el médico determina que el estado de Gabriel requiere atención prioritaria.

```
Ingrese su opción: 2
Asignar prioridad paciente
Ingrese el nombre del paciente: Gabriel
Ingrese la nueva prioridad del paciente:
1- Alta
2- Media
3- Baja
2
La nueva prioridad de Gabriel es Media
```

El sistema actualiza la prioridad de Gabriel a "Media", asegurando que será una de las próximas pacientes en ser atendida.

**Paso 3: Ver la Lista de Espera**

El usuario revisa la lista de espera para ver todos los pacientes y sus prioridades.

```
Ingrese su opción: 3
Mostrar lista de espera
Pacientes en espera: 
Nombre paciente: Gabriel
Edad paciente: 25
Sintomas paciente: Tos
Hora llegada paciente: 12 Hrs
Prioridad paciente: Media
```

La lista muestra a Gabriel en la parte superior, indicando su prioridad Media y que es la siguiente en línea para recibir atención.

**Paso 4: Ver la Lista de pacientes según prioridad**

El usuario puede consultar la lista de pacientes filtrada por prioridad, mostrando únicamente aquellos pacientes que coincidan con la prioridad seleccionada.

```
Ingrese su opción: 5
Mostrar lista pacientes por prioridad
Ingrese la prioridad, para mostrar los pacientes a los correspondientes
1-Alta
2-Media
3-Baja
2
Nombre paciente: Gabriel
Edad paciente: 25
Sintomas paciente: Tos
Hora llegada paciente: 12 Hrs
Prioridad paciente: Media
```

La lista muestra a Gabriel en la parte superior, indicando su prioridad como Media y que es el único paciente con esa prioridad en la lista.

**Paso 5: Atender al Siguiente Paciente**

Gabriel es llamado para ser atendido basándose en su prioridad.

```
Ingrese su opción: 4
Atender siguiente paciente
Paciente atendido:
Nombre paciente: Gabriel
Edad paciente: 25
Sintomas paciente: Tos
Hora llegada paciente: 12 Hrs
Prioridad paciente: Media
```

El sistema muestra que Gabriel está siendo atendido y la elimina de la lista de espera.

##

**Paso 6: Salir del sistema**

Gabriel abandona el sistema para finalizar su hospitalización.

```
Ingrese su opción: 6
Saliendo del sistema de gestión hospitalaria...
```

## Contribuciones

Javier Nuñez
