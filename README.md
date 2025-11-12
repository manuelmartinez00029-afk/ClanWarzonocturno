# Clan Warzonocturno - App Android (Plantilla)

Esta es una plantilla mínima para crear una app Android que muestre el contenido del clan Warzonocturno en un WebView cargando un HTML local (assets/index.html).

Contenido:
- index.html con la descripción/marketing del clan.
- MainActivity.kt carga el HTML.
- Instrucciones para compilar y generar APK.

Advertencia legal y de marca:
- "Warzone" es una marca registrada. Si esta app pretende ser oficial de un juego comercial, revisa las políticas de marca y derechos del propietario. Te recomiendo usar nombres y marca del clan que no infrinjan derechos de terceros, o pedir permiso oficial si fuera necesario.

Requisitos para compilar:
- Android Studio (recomendado) con SDK Android 34.
- JDK 17.
- Conexión a Internet para descargar dependencias la primera vez.

Cómo compilar en Android Studio:
1. Abre Android Studio -> "Open an existing project" y selecciona la carpeta raíz con settings.gradle.
2. Espera a que Gradle sincronice.
3. Ejecuta Run -> selecciona un emulador o dispositivo físico.
4. Para generar APK release: Build -> Generate Signed Bundle / APK... y sigue los pasos para firmar con tu keystore.

Cómo compilar desde línea de comandos:
- Ejecuta:
  ./gradlew assembleDebug    # genera app/build/outputs/apk/debug/app-debug.apk
  ./gradlew assembleRelease  # genera release (necesita signingConfigs para ser instalable sin firmar)

Firmado y distribución:
- Para publicar en Google Play necesitas firmar la app con una keystore y seguir las reglas de Play Console.
- Si solo quieres distribuir un APK para miembros:
  - Pruébalo en tu dispositivo (habilita "Instalar apps desconocidas" para la app que uses).
  - Sube el APK a GitHub Releases, tu web, o servicios como Firebase App Distribution.

Agregar funcionalidades futuras (ideas):
- Noticias dinámicas desde una API (reemplazar assets por WebView remota o un Activity con Retrofit).
- Chat de comunidad (WebSocket o integrar servicio existente).
- Integración de vídeos/TikTok embebido.
- Pantalla de configuración y consentimiento de privacidad.

Si quieres, puedo:
- Añadir un icono personalizado y nombres.
- Generar un gradle signingConfigs de ejemplo y explicar cómo crear una keystore.
- Preparar un repo en GitHub con README listo para descargar y generar releases (necesitaría permiso para crear el repo o que me indiques el owner/repo).

