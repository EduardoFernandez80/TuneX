# TuneX (APK)

Envoltorio Android (WebView) de TuneX, la app de afinación. La app completa vive en `app/src/main/assets/index.html`.

## Compilar con Android Studio
1. Abre esta carpeta con **File > Open** y espera a que termine el *Gradle sync* (necesita internet la primera vez).
2. **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
3. El APK queda en `app/build/outputs/apk/debug/app-debug.apk`.

## Instalar por ADB
    adb install -r app/build/outputs/apk/debug/app-debug.apk

## Por línea de comandos (si ya tienes Gradle 8.7+ y el SDK de Android)
    gradle assembleDebug

## Notas
- Android 8.0 (API 26) o superior.
- Al primer uso pedirá permiso de micrófono.
- Para actualizar la app, reemplaza `app/src/main/assets/index.html` y vuelve a compilar.

## Icono
El icono es adaptativo: primer plano en `app/src/main/res/drawable-nodpi/ic_fg.png` (432x432) y color de fondo `ic_bg` en `res/values/colors.xml`.
