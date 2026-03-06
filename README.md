# Taller 1 - Hello Android

## Información del Estudiante

**Nombre:** Freddy Alastre
**Código:** 1100976183
**Fecha:** 05/03/2026

---

# Respuestas

## 1. Función del AndroidManifest.xml

El archivo **AndroidManifest.xml** es uno de los archivos más importantes de una aplicación Android. Su función principal es describir la configuración general de la aplicación para el sistema operativo Android.

En este archivo se definen elementos como:

* El nombre del paquete de la aplicación.
* Las actividades que tendrá la aplicación.
* Los permisos que necesita la aplicación (internet, cámara, ubicación, etc.).
* La actividad principal que se ejecuta cuando se abre la aplicación.
* Información sobre los componentes de la app como servicios, receptores y proveedores de contenido.

En resumen, el **AndroidManifest.xml** le indica al sistema Android cómo debe ejecutarse y qué componentes tiene la aplicación.

---

## 2. Diferencia entre activity_main.xml y MainActivity.kt

El archivo **activity_main.xml** y **MainActivity.kt** cumplen funciones diferentes dentro de una aplicación Android.

**activity_main.xml**

* Define el diseño visual de la pantalla.
* Aquí se crean los elementos de la interfaz gráfica como botones, textos, imágenes y layouts.
* Se usa el lenguaje XML para organizar la interfaz.

**MainActivity.kt**

* Contiene la lógica de programación de la aplicación.
* Está escrito en el lenguaje Kotlin.
* Aquí se controlan las acciones del usuario, como cuando se presiona un botón o se modifica un texto.

En resumen, **activity_main.xml controla la apariencia de la aplicación**, mientras que **MainActivity.kt controla el comportamiento de la aplicación**.

---

## 3. Gestión de recursos en Android

La gestión de recursos en Android consiste en organizar y almacenar elementos que utiliza la aplicación en carpetas especiales dentro del proyecto. Estos recursos pueden ser:

* Imágenes
* Colores
* Textos
* Diseños de interfaz
* Iconos
* Animaciones

Estos archivos se guardan en la carpeta **res** del proyecto.

Por ejemplo:

* **res/layout** → diseños de pantallas
* **res/drawable** → imágenes e iconos
* **res/values** → colores, textos y estilos

La ventaja de este sistema es que permite reutilizar recursos, facilitar la traducción de aplicaciones a diferentes idiomas y adaptar la app a distintos tamaños de pantalla.

---

## 4. Aplicaciones famosas que usan Kotlin

Kotlin es un lenguaje moderno que se usa ampliamente para el desarrollo de aplicaciones Android. Muchas aplicaciones populares utilizan Kotlin en su desarrollo. Algunas de ellas son:

* Netflix
* Pinterest
* Trello
* Evernote
* Uber

Estas empresas utilizan Kotlin porque permite escribir código más limpio, seguro y fácil de mantener, además de ser totalmente compatible con Java y con el ecosistema de Android.

