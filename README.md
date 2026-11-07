# Alimentadores SMD (app Android con Capacitor)

El HTML esta en `www/index.html`. Cualquier cambio se hace ahi y luego:

    npm install
    npx cap sync android

## Opcion A: Android Studio
1. `npx cap open android` (o abrir la carpeta `android` en Android Studio).
2. Esperar a que termine Gradle y pulsar Build > Build APK(s).
3. El APK queda en `android/app/build/outputs/apk/debug/app-debug.apk`.

## Opcion B: GitHub Actions (sin instalar nada)
1. Subir esta carpeta a un repositorio de GitHub (rama `main`).
2. Pestana Actions > "Compilar APK" > Run workflow.
3. Descargar el artefacto `AlimentadoresSMD-apk` y pasar el APK al movil.

## Instalar en el movil
Copiar el APK al telefono, abrirlo y permitir "instalar apps de origen desconocido".

## Notas
- Los datos se guardan en el almacenamiento local de la app (como en el navegador). Exporta el CSV de vez en cuando como copia de seguridad.
- Exportar CSV abre el menu Compartir de Android (Drive, correo, Excel...).
- El boton de camara usa el escaner de Google (necesita Google Play Services). Un lector fisico por teclado funciona igual que antes.
- El APK "debug" sirve para uso interno. Para Play Store hay que firmar un release.
