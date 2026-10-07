# Asistia

Aplicación de escritorio para estudiantes que reúne horario, control de faltas, agenda de entregas y notas en un solo sitio.

## ¿Qué problema resuelve?

Llevar la cuenta de las faltas durante el curso para no llegar al 15 % de inasistencia, donde empiezan los problemas. Además centraliza las fechas de exámenes y trabajos y calcula la nota media.

## ¿Para quién es?

Para estudiantes de modalidades no obligatorias, aunque cualquier estudiante puede usarla. En menores, también pueden usarla sus padres o tutores.

## Funcionalidades previstas

- **Horario:** se crea a mano o se importa desde un archivo JSON. Al hacer clic en un módulo de un día se marca como falta (en rojo), y se puede revertir volviendo a hacer clic.
- **Faltas:** muestra las faltas acumuladas, las que quedan hasta el límite y el límite configurado. Si superas el límite, la app sigue contando para que mantengas el registro.
- **Avisos:** recordatorio al final del día para indicar a qué clases has asistido, y avisos al llegar al 50 % de las faltas permitidas y al quedarte sin ellas.
- **Agenda:** alta y baja de exámenes y trabajos, indicando el módulo al que pertenecen. Se pueden ver los próximos 7 días, 1 mes o el año completo, marcar tareas como finalizadas y anotar la nota si son evaluables.
- **Notas:** desglose de la calificación total por exámenes, trabajos y módulos, para ver en cuál vas mejor y en cuál peor. La media se calcula automáticamente.
- **Configuración:** límite de faltas, modo claro/oscuro, idioma y opción de mostrar u ocultar el % de calificación en el inicio.

## Estructura de la interfaz

La vista principal es el **Horario**, que muestra también las próximas tareas y el % de calificación. Desde ahí se accede a Agenda, Faltas, Notas y Configuración. Desde cualquier otra vista se vuelve al Horario con un botón de volver.

## Estado del proyecto

Versión 1.0. Por ahora solo existe la estructura HTML semántica (Práctica 1). Los estilos con CSS y la funcionalidad con JavaScript se añadirán en prácticas posteriores.

## Estructura del proyecto

```
asistia/
├── index.html
├── css/
│   └── styles.css
├── js/
│   └── app.js
└── img/
    └── .gitkeep
```

## Autor

Iván Marín Gayete, 2º DAM.
