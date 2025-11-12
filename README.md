# AppCreator24 - ClanWarzonocturno (Plantilla)

Proyecto preparado para publicarlo con branding "AppCreator24".

Cambios aplicados:
- applicationId: com.appcreator24.clanwarzonocturno
- namespace: com.appcreator24.clanwarzonocturno
- android:label actualizado a "AppCreator24 - Clan Warzonocturno"
- index.html actualizado con marca AppCreator24

Cómo compilar y generar APK:
1. Clona o descarga el repo:
   git clone https://github.com/manuelmartinez00029-afk/ClanWarzonocturno.git
   cd ClanWarzonocturno

2. Abre en Android Studio o usa la terminal:
   ./gradlew assembleDebug
   APK debug: app/build/outputs/apk/debug/app-debug.apk

3. Para un APK release firmado:
   - Genera un keystore localmente:
     keytool -genkeypair -v -keystore release-keystore.jks -alias clan_release -keyalg RSA -keysize 2048 -validity 10000
   - Añade signingConfigs a app/build.gradle (usa variables de entorno para contraseñas).
   - ./gradlew assembleRelease

Publicación:
- Si quieres que cree la Release con el APK por ti, necesito autorización desde la interfaz para operar en tu repo; una vez autorizada crearé el workflow y subiré el APK como asset.