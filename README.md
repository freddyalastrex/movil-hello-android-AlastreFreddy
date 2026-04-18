Realizado por Freddy Alejandro Alastre
HelloAndroid - Alastre Freddy
Proyecto Android desarrollado en los Talleres 1, 2 y 3 de la asignatura de Desarrollo de Aplicaciones Móviles.

Taller 3 – Lista de Tareas con Fragments, Persistencia y Recordatorios
¿Qué se implementó?
En este taller se construyó una aplicación de lista de tareas (To-Do App) completa, utilizando una arquitectura moderna de Android con los siguientes componentes:
Arquitectura

Single Activity + Fragments: toda la app corre dentro de una sola MainActivity que actúa como contenedor de los fragments.
MVVM (Model - View - ViewModel): se separó la lógica de datos de la interfaz gráfica usando ViewModel y LiveData.
Navigation Component: se usó nav_graph.xml para manejar la navegación entre fragments de forma declarativa.

Pantallas (Fragments)

TaskListFragment: muestra la lista de tareas guardadas. Incluye un botón flotante para agregar nuevas tareas y permite tocar una tarea existente para editarla.
TaskDetailFragment: formulario para crear o editar una tarea. Contiene campo de título, descripción, y un switch para activar el recordatorio.

Persistencia de datos

Las tareas se guardan localmente en el dispositivo usando SharedPreferences.
Se usa la librería Gson para serializar y deserializar la lista de tareas en formato JSON.
Las tareas persisten aunque se cierre y vuelva a abrir la aplicación.

Modelo de datos
Cada tarea (Task) contiene:

id: identificador único
title: título de la tarea
description: descripción opcional
hasReminder: indica si tiene recordatorio activo

Recordatorio

Se utilizó un BroadcastReceiver (TaskReminderReceiver) para recibir la alarma.
Se utilizó AlarmManager para programar el recordatorio.
Opción elegida: Notificación local — al guardar una tarea con el switch de recordatorio activado, se programa una notificación que aparece en la barra de estado del dispositivo 30 segundos después.
Se creó un canal de notificación (task_reminder_channel) compatible con Android 8.0 (API 26) en adelante.

Interfaz gráfica mejorada

Diseño con colores corporativos en azul (#3F51B5).
Barra superior con título y subtítulo en cada pantalla.
Tarjetas (CardView) con sombra y bordes redondeados para cada tarea en la lista.
Ícono de campana 🔔 visible en cada tarea que tiene recordatorio activo.
Formulario de detalle organizado dentro de una tarjeta con separadores visuales.
Botón flotante extendido (ExtendedFloatingActionButton) con texto e ícono.


Dependencias agregadas
En build.gradle (Module: app):
gradleimplementation("com.google.code.gson:gson:2.10.1")

Permisos requeridos
En AndroidManifest.xml:
xml<uses-permission android:name="android.permission.POST_NOTIFICATIONS"/>
<uses-permission android:name="android.permission.SCHEDULE_EXACT_ALARM"/>
<uses-permission android:name="android.permission.RECEIVE_BOOT_COMPLETED"/>

Opción de recordatorio utilizada
✅ Notificación local
Al guardar una tarea con el switch de recordatorio activado, el sistema programa una alarma con AlarmManager que dispara el TaskReminderReceiver 30 segundos después. El receiver construye y muestra una notificación en la barra de estado con el título de la tarea.
