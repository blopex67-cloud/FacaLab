# FacaLab

App Android para probar accesorios faciales en realidad aumentada móvil. Importas una imagen o un modelo GLB, eliges qué punto de la cara lo ancla (ojos, frente, nariz, boca, barbilla u orejas) o tocas la cabeza para fijarlo en un punto personalizado; luego el tracking facial mantiene el accesorio siguiendo ese punto al mover la cabeza.

## APK automática
Cada cambio publicado en la rama `main` genera una APK instalable y una versión descargable en **Releases**. El workflow también conserva un artefacto de la compilación en Actions. La APK de prueba se firma con la clave debug de Android; no es una firma de publicación para Google Play.

## Incluye
- Vista de una cabeza base 3D interactiva para ensayar el anclaje y modo cámara.
- Seguimiento facial en el teléfono con MediaPipe Face Landmarker, que mantiene el accesorio unido al punto facial elegido.
- Importador Android de GLB binarios mediante lectura directa del archivo (sin blob URL), imágenes y selector de puntos faciales.
- Gizmos 3D táctiles de mover, girar y escalar con ejes XYZ o por eje; el modelo mantiene su transformación cuando el tracking actualiza el anclaje.
- Ajustes de tamaño, posición y opacidad; captura y descarga de foto.
- Android empaqueta localmente Three.js, MediaPipe y la interfaz en un solo script WebView; evita depender de que carguen módulos CDN al iniciar. El modelo de seguimiento facial y el runtime de MediaPipe aún se descargan por Internet.

## Permisos y privacidad
Android solicita permiso de cámara cuando la app intenta abrirla. No se usa micrófono. El video y el seguimiento facial se procesan en el dispositivo; no hay un servidor de video. La app necesita Internet para descargar las bibliotecas y el modelo de tracking, y para cargar three.js y accesorios GLB.

## Estado
Es una primera versión de realidad aumentada facial, no una app para casco VR ni seguimiento espacial del cuarto. El tracking se basa en los puntos faciales de MediaPipe; la orientación 3D de modelos con pivote/ejes distintos puede requerir ajuste. Importa GLB binario (no un .gltf externo con texturas separadas). Generar la APK en Actions no equivale a probarla en un teléfono físico.
