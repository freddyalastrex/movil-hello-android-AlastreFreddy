# Taller 2 - Hello Android

## Información del Estudiante

**Nombres:** Freddy Alastre, Juan Pablo Gómez 
**Código:** 1100976183
**Fecha:** 05/03/2026

---

# Respuestas



#### 1. ¿Qué problema resuelve el ViewModel en Android?
El ViewModel resuelve principalmente la **pérdida de estado y datos** durante los cambios de configuración (como la rotación del dispositivo). Al tener un ciclo de vida más extenso que la Activity o el Fragment, permite que la aplicación mantenga la información sin necesidad de realizar nuevas cargas o procesos costosos cada vez que la interfaz se recrea.

#### 2. ¿Por qué LiveData es "lifecycle-aware" y qué beneficio trae?
Es "consciente del ciclo de vida" porque observa el estado de los componentes de la UI (LifecycleOwner). Solo envía actualizaciones de datos cuando la vista está en un estado activo (`STARTED` o `RESUMED`). Esto **evita fugas de memoria (memory leaks)** y errores de ejecución (crashes) al intentar actualizar elementos visuales de una pantalla que ya ha sido destruida o está en segundo plano.

#### 3. Explica el flujo de datos en MVVM
El flujo es unidireccional y reactivo:
- La **Vista** observa al **ViewModel**.
- El **ViewModel** solicita datos al **Repositorio**.
- El **Repositorio** entrega los datos al **ViewModel**.
- El **ViewModel** actualiza su **LiveData**.
- La **Vista** reacciona automáticamente al cambio en el LiveData y se refresca.

#### 4. ¿Qué ventaja tiene usar Fragments vs múltiples Activities?
Facilita la implementación de la **Single Activity Architecture**. Las principales ventajas son:
- **Eficiencia:** Menor consumo de recursos al no tener que levantar múltiples instancias de Activity.
- **Modularidad:** Permite reutilizar componentes de interfaz en diferentes partes de la app.
- **Navegación:** Permite transiciones más fluidas y una gestión de la pila de retroceso más sencilla mediante el Navigation Component.

#### 5. ¿Cómo ayuda el Repository Pattern a la arquitectura?
Ayuda proporcionando una **capa de abstracción** sobre las fuentes de datos. El resto de la aplicación no necesita saber si los datos provienen de una base de datos local (Room), una API externa (Retrofit) o memoria volátil. Esto hace que el código sea más fácil de testear, mantener y escalar.

---
