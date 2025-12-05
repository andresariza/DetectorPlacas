# DetectorPlacas

Proyecto: Detección de placas vehiculares usando YOLO. Repositorio con backend (modelo/API) y aplicación móvil (frontend) que consume la API y muestra las detecciones.

## Integrantes
- pendiente — Andres Ariza
- U00185389 — Cristian Camilo Valencia

## Estructura del repositorio
- backend/ — código del servidor, modelo y scripts
- mobile/ — aplicación móvil
- evidencias/ — capturas y vídeos de evidencia (3 imágenes backend, 2 vídeos frontend)
- README.md — este archivo

## Requisitos
- Python 3.8+
- Node.js / npm (para la app móvil)
- Entorno virtual para Python (venv)

## Instalación y ejecución (Backend)
1. Clonar el repositorio:
   git clone https://github.com/cristianvalencia22/DetectorPlacas.git
2. Entrar a la carpeta del backend:
   cd DetectorPlacas/backend
3. Crear y activar entorno virtual e instalar dependencias:
   python -m venv venv
   source venv/bin/activate   (Windows: venv\\Scripts\\activate)
   pip install -r requirements.txt
4. Colocar el modelo YOLO en backend/models/ (o la ruta que indique el código).
5. Iniciar la API:
   python app.py
6. Verificar salud del servicio:
   curl http://localhost:5000/health

## Endpoints principales
- POST /detect — enviar imagen y recibir detecciones (JSON)
- GET /health — estado del servicio

## Instalación y ejecución (Aplicación móvil)
1. Entrar a la carpeta mobile:
   cd DetectorPlacas/mobile
2. Instalar dependencias:
   npm install
3. Configurar la URL del backend en el archivo de configuración de la app (ej. src/config.js o constantes).
4. Ejecutar la app en emulador o dispositivo:
   npm run android   (o el comando correspondiente según el proyecto móvil)

## Prueba rápida (ejemplo)
1. Enviar una imagen de prueba al endpoint de detección:
   curl -X POST -F "image=@ruta/a/imagen.jpg" http://localhost:5000/detect
2. Resultado esperado: JSON con bounding boxes y clase "placa" y/o imagen con anotaciones devuelta por la API.

## Evidencia (capturas y vídeos)
Las evidencias se encuentran en la carpeta `evidencias/` del repositorio. Se incluyen (ejemplos de nombres de archivo, actualizar si difieren):
- evidencias/backend1.png
- evidencias/backend2.png
- evidencias/backend3.png
- evidencias/frontend1.mp4
- evidencias/frontend2.mp4

Vistas previas relativas (si GitHub las muestra):

![Evidencia Backend 1](evidencias/backend1.png)
![Evidencia Backend 2](evidencias/backend2.png)
![Evidencia Backend 3](evidencias/backend3.png)

- Vídeo 1 (Frontend): evidencias/frontend1.mp4
- Vídeo 2 (Frontend): evidencias/frontend2.mp4

> Nota: Si los nombres reales de los archivos difieren, actualice las rutas en este README o renombre los archivos en `evidencias/`.

## Descripción de las evidencias
- imágenes backend: consola con el servicio corriendo, logs de detección y configuración del servidor.
- vídeos frontend: interacción de la app mostrando la detección sobre imágenes o video en tiempo real.

## Entrega
- Este repositorio contiene la aplicación móvil, el backend y la evidencia solicitada por la práctica.

## Contacto
- Andres Ariza — (ID: pendiente)
- Cristian Camilo Valencia — (ID: U00185389)

---

Commit realizado automáticamente para actualizar README con instrucciones y rutas de evidencia.