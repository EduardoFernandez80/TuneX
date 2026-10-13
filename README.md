# TuneX 🎵

**Afinador de instrumentos musicales para Android con visualizaciones animadas intercambiables, paletas de colores personalizables y afinaciones a la medida.**

TuneX escucha tu instrumento con el micrófono, detecta la nota en tiempo real y te muestra qué tan afinada está con animaciones pensadas para que afinar sea un placer visual. Está hecha con HTML, CSS y JavaScript puro, sin librerías externas, y se empaqueta como APK con un envoltorio WebView.

> Hecha por **Eduardo Fernández Jiménez**.

---

## ✨ Lo que hace especial a TuneX

### 🎨 18 visualizaciones intercambiables
La misma lectura de afinación, contada de 18 formas distintas. Cambias de animación con un toque en la barra inferior, y la app recuerda la última que usaste.

| | | |
|---|---|---|
| **Traza**: línea de tiempo con pin, estilo GuitarTuna | **Estela**: partículas y red de polígonos con trazo cian y verde | **Gotas**: agua con simulación de fluidos |
| **Jelly**: gota gelatinosa que se estira y tiembla | **Mirage**: anillos de puntos con ola de tamaños | **Cuerda**: una cuerda que vibra con batido |
| **Enjambre**: luciérnagas que se agrupan al afinar | **Burbuja**: nivel de burbuja con rebote | **Barras**: medidor de barras con picos que caen |
| **Rosa**: flor matemática que se cierra al afinar | **Radar**: barrido con punto que brilla | **Aurora**: cintas de luz que se calman |
| **Balanza**: subibaja con una bolita | **Luna**: fases lunares, llena al afinar | **Órbitas**: dos planetas que se alinean |
| **Estanque**: ondas concéntricas con perspectiva | **Latido**: electrocardiograma que se vuelve rítmico | **Péndulo**: péndulo que oscila con la desafinación |

En todas, el color indica el estado: **afinado**, **cerca** o **lejos**, y cada figura "se calma" cuando la nota queda perfecta.

### 💧 Gotas, con física de agua
- Las gotas se estiran al acelerar y al acercarse a la superficie.
- Al caer, hunden el agua: una simulación de resortes propaga las ondas y rebotan en los bordes.
- Cada impacto lanza gotitas de salpicadura hacia los lados.
- El agua toma el color del estado de afinación y se mezcla poco a poco.
- Controles en pantalla de **frecuencia** y **velocidad** (en porcentaje).

### 🌈 Paletas de colores
- Paleta predeterminada de [Coolors](https://coolors.co): `#0b1020 · #7dd3fc · #22d3ee · #2dd4bf · #8b5cf6`.
- **Importa paletas de sitios como Coolors o Color Hunt** pegando el enlace o los códigos hex. La app reparte los colores por rol automáticamente (fondo, acento, afinado, cerca, lejos).
- Generador de paletas armónicas aleatorias.
- Editor **personalizado** de 5 colores, con aplicación en vivo y **reordenamiento arrastrando** (mantén presionado).
- Historial de las **últimas 10 paletas**, **favoritas** y paletas predefinidas.
- Todo se guarda en el dispositivo.

### 🎸 Instrumentos y afinaciones
- **Guitarra** (15 afinaciones: Estándar, Drop D/C/B, medio tono y un tono abajo, DADGAD, Open D/G/E/A/C, Nashville y más), **Bajo** (4, 5 y 6 cuerdas, Drop D, Piccolo), **Ukelele**, **Violín**, **Violonchelo**, **Cuatro venezolano** y modo **Cromático**.
- Botón ♪ para elegir entre las afinaciones alternativas de cada instrumento.
- **Instrumento Personalizado**: escribe **cualquier cantidad de notas** (`D2 A2 D3 G3 B3 E4`, o con nombres `Re2 La2 Mi3`, con `#` y `b`) y guárdalas con nombre.
- Organiza tu lista de instrumentos: **reordénalos** con ☰, **elimínalos** manteniendo presionado y **restáuralos** cuando quieras.
- Modo **AUTO** que detecta la cuerda, o fija una cuerda tocando su círculo.

### 🎙️ Detección estable
- Detección de tono con el algoritmo **YIN**.
- Filtro de **mediana**, suavizado y rechazo de saltos de octava para que la aguja no brinque.
- Estado "afinado" con **histéresis**, para que no parpadee en el borde.
- Medidor del nivel de entrada del micrófono y mensajes claros si hay un problema de permisos.

### 🔊 Extras
- **Tono de referencia**: mantén presionada una nota para escucharla.
- Vibración al quedar afinado y pantalla encendida mientras afinas.
- Marca de agua del logo, muy tenue, de fondo.
- Interfaz en español, pensada para uso con una mano.

---

## 🛠️ Tecnología
- **App:** un solo archivo `index.html` (HTML + CSS + JavaScript, Canvas 2D y Web Audio API), sin dependencias.
- **Android:** envoltorio **WebView** en Java con `androidx.webkit`, que sirve la app desde un contexto seguro para poder usar el micrófono.
- Android 8.0 (API 26) o superior.

## 📦 Estructura
```
TuneX/
├── app/src/main/
│   ├── assets/index.html      ← toda la aplicación
│   ├── java/.../MainActivity.java
│   ├── res/                   ← icono adaptativo
│   └── AndroidManifest.xml
├── build.gradle
└── settings.gradle
```

## 🚀 Compilar

**Con Android Studio:** abre la carpeta, espera el *Gradle sync* y elige **Build > Build APK(s)**.

**Desde la línea de comandos:**
```bash
gradle assembleDebug
adb install -r app/build/outputs/apk/debug/app-debug.apk
```
El APK queda en `app/build/outputs/apk/debug/`.

**Solo en el navegador:** abre `app/src/main/assets/index.html` en un navegador con permiso de micrófono.

---

## 💜 Apoya el proyecto
Si TuneX te ayuda, dentro de la app hay un botón **♥** (arriba a la izquierda) con las opciones para apoyar con **PayPal**, **XRP** o **Bitcoin**.

## 📄 Licencia
Por definir.
