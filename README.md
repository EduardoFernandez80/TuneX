# TuneX 🎸

Afinador musical para Android con detección de audio en tiempo real y animaciones visuales.

## Características

- Detección de audio mediante el micrófono.
- Guitarra estándar como afinación predeterminada.
- Indicadores visuales para ayudar a afinar.
- Variantes de animaciones originales.
- Proyecto Android compilable desde Termux.

## Requisitos

- Dispositivo Android compatible.
- Permiso de micrófono.
- Java y Gradle para compilar el proyecto.

## Compilación

Desde la carpeta del proyecto, ejecuta:

    ./gradlew assembleDebug

Si no tienes Gradle Wrapper instalado y configurado, puedes utilizar:

    gradle assembleDebug

El APK de depuración normalmente se genera en:

    app/build/outputs/apk/debug/app-debug.apk

## Instalación

Abre el APK desde el administrador de archivos de Android y autoriza la instalación si el sistema lo solicita.

## Estado

TuneX está en desarrollo. La precisión depende de la implementación del detector de audio.

## Autor

EduardoFernandez80
