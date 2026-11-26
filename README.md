# FacaLab

App Android en desarrollo para diseñar y probar accesorios faciales con una cabeza base 3D y cámara en vivo.

## APK automática
Cada cambio publicado en la rama `main` genera una APK instalable y una versión descargable en **Releases**. El workflow también conserva un artefacto de la compilación en Actions. La APK de prueba se firma con la clave debug de Android; no es una firma de publicación para Google Play.

## Incluye
- Vista de una cabeza base 3D y modo cámara.
- Seguimiento facial en el teléfono con MediaPipe Face Landmarker.
- Accesorios de muestra, importación de imágenes y modelos 3D GLB.
- Ajustes de tamaño, posición y opacidad; captura y descarga de foto.
- WebView Android con permiso de cámara solicitado al usarla.

## Permisos y privacidad
Android solicita permiso de cámara cuando la app intenta abrirla. No se usa micrófono. El video y el seguimiento facial se procesan en el dispositivo; no hay un servidor de video. La app necesita Internet para descargar las bibliotecas y el modelo de tracking, y para cargar three.js y accesorios GLB.

## Estado
Es un prototipo funcional en progreso. El tracking se basa en los puntos faciales de MediaPipe; la colocación de modelos 3D es inicial y modelos con orientaciones distintas pueden necesitar ajustes. Generar la APK en Actions no equivale a probarla en un teléfono físico.
