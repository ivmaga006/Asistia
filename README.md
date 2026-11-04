# Asistia

Aplicación de escritorio para estudiantes que junta en un solo sitio el horario, el control de faltas, la agenda de exámenes y trabajos, y las notas del curso.

> **Estado actual:** prototipo visual en HTML y CSS; la funcionalidad con JavaScript está pendiente. Nació como práctica de 2º DAM (Desarrollo de Interfaces) y la idea es seguir desarrollándola hasta convertirla en una aplicación real.

## Por qué existe

En muchas modalidades de estudio, superar el 15 % de faltas de asistencia te mete en problemas. Llevar esa cuenta de cabeza, o en una libreta, es un coñazo y es fácil que se te pase. Asistia lo hace por ti y, de paso, te organiza las entregas y calcula tu nota media.

La idea es que el estudiante sepa en todo momento cuántas faltas tiene, cuántas le quedan y qué tiene que entregar, sin miedo a llegar tarde a descubrirlo.

## Para quién es

- Pensada para estudiantes de modalidades no obligatorias, aunque la puede usar cualquier estudiante.
- En el caso de menores, también pueden usarla sus padres o tutores.

## Cómo se usa (flujo típico)

1. Creas tu horario a mano o lo importas desde un archivo JSON.
2. Al terminar el día, la app te recuerda que indiques a qué clases has asistido y a cuáles no.
3. Las clases a las que no has asistido suman una falta.
4. Vas añadiendo tus exámenes y trabajos en la agenda, y las notas conforme las recibes.
5. En el panel principal ves de un vistazo el horario de la semana, las próximas tareas, tu % de faltas y tu nota media.

## Funcionalidades

### Horario (vista principal)
- Horario semanal creado a mano o importado desde un archivo JSON.
- Al hacer clic en un módulo de un día se marca como falta y aparece en rojo. Se puede revertir volviendo a hacer clic.
- Navegación entre semanas, incluidas las anteriores.
- Muestra las próximas tareas y el % de calificación.
- Menú hamburguesa (arriba a la derecha) para acceder al resto de vistas.

### Faltas
- Faltas totales permitidas, faltas acumuladas hasta la fecha y faltas restantes hasta el límite.
- Detalle de las faltas de todos los módulos.
- Aviso al llegar al 50 % de las faltas permitidas y al quedarte sin ellas.
- Si superas el límite, la app sigue contando para que mantengas el registro.

### Agenda
- Alta y baja de exámenes y trabajos, indicando el módulo al que pertenecen (parecido a Google Calendar, pero por asignatura).
- Datos de cada tarea: fecha (o fecha límite), módulo y nota si es evaluable.
- Vista de próximos 7 días, 1 mes o el año entero.
- Marcar tareas como finalizadas y anotar la nota.
- Aviso con antelación para que te prepares.

### Notas
- Alta y consulta de notas.
- Cálculo automático de la media cuando están todas las notas de una evaluación.
- Desglose del % de calificación total: cuánto viene de exámenes, cuánto de trabajos y de qué módulos, para ver en cuál vas fuerte y en cuál flojeas.

### Configuración
- Límite de faltas (%).
- Modo claro y oscuro.
- Idioma.
- Mostrar u ocultar el % de calificación en el inicio.

## Datos que maneja

| Elemento | Datos |
|---|---|
| Examen | Fecha, módulo, nota |
| Trabajo | Fecha límite, módulo, nota (si es evaluable) |
| Falta | Fecha, módulo |
| Nota | Nota |
| Horario | Módulo, horas, profesor |

## Estructura de la interfaz

```
Panel Princial (vista principal)
├── Tareas
├── Faltas
├── Notas
└── Configuración
```

Desde el Horario se accede al resto con el menú hamburguesa. Desde cualquier otra vista se vuelve al Horario con un botón de volver.

## Estructura del proyecto

```
asistia/
├── index.html
├── pages/
│   └── tareas.html
├── css/
│   ├── styles.css
│   └── pages/
│       └── tareas.css
├── js/
│   └── app.js
└── img/
    └── .gitkeep
```

## Hoja de ruta

- [x] Estructura HTML semántica (Práctica 1)
- [x] Estilos con CSS (diseño del dashboard y listado de tareas)
- [ ] Funcionalidad con JavaScript
- [ ] Decidir qué entra en la primera versión real y qué se queda como ampliación
- [ ] Empaquetado como aplicación de escritorio

## Por decidir

Cosas que todavía no están definidas y hay que cerrar antes de desarrollar de verdad:

- Tecnología para empaquetar la app de escritorio.
- Plataformas objetivo (Windows, macOS, Linux).
- Dónde se guardan los datos (local o en la nube).
- Formato exacto del JSON de importación del horario.
- Licencia del proyecto.
- Modelo de distribución (gratuita, de pago, etc.).

## Autor

Iván Marín Gayete
