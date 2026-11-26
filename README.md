# FacaLab — estudio móvil de filtros faciales

Prototipo web instalable (PWA) para probar accesorios 2D y modelos GLB en vivo desde la cámara frontal del teléfono.

## Qué incluye
- Vista en directo y tracking facial con MediaPipe Face Landmarker.
- Filtros demo 2D (lentes y corona), accesorios propios PNG/JPG/WEBP y carga de modelos 3D GLB con Three.js.
- Controles para tamaño, posición vertical/horizontal y opacidad.
- Captura PNG, instalación como PWA y guardado local de los ajustes.
- El video y la detección facial se procesan dentro del navegador; esta versión no transmite la cámara a un servidor.

## Probar en teléfono
El acceso a cámara requiere HTTPS y permiso del navegador. Publica el contenido de esta carpeta como sitio estático (por ejemplo GitHub Pages), abre la URL segura y permite cámara. La PWA guarda el cascarón de la interfaz para abrirlo sin conexión, pero el tracking usa bibliotecas y el modelo descargados por Internet. Requiere conexión a Internet para descargar las bibliotecas y el modelo de tracking.

## Importante
Es un MVP: el anclaje 3D usa una aproximación 2D de los puntos del rostro; los GLB de distintas orientaciones pueden necesitar ajustes o una configuración de anclaje por tipo de accesorio. Los archivos importados no se guardan en servidor; el preset local guarda solo ajustes. Esta versión no crea APK nativa ni publica filtros en redes.
