# AXM

## Contexto del proyecto

Este proyecto consiste en desarrollar una aplicación web para el registro y administración de movimientos contables de una caja fuerte. Su objetivo es permitir el almacenamiento de un historial auditable en Google Sheets, eliminando la necesidad de mantener un servidor dedicado en funcionamiento permanente.

El sistema debe permitir registrar transacciones desde cualquier dispositivo con acceso a Internet y sincronizarlas cuando el software de procesamiento esté disponible.

En otras palabras, la aplicación funciona como una capa web de captura y sincronización de datos contables, con integración a servicios de Google y Firebase para facilitar el acceso, la autenticación y el almacenamiento.

## Dependencias instaladas

Las siguientes librerías se instalaron con `pip` para cubrir las necesidades principales del proyecto:

- `flask`: se usa para construir la aplicación web y exponer rutas HTTP que permitan registrar y consultar movimientos.
- `firebase-admin`: se usa para conectarse a Firebase desde el backend y administrar servicios como autenticación, Firestore o Storage.
- `gspread`: se usa para trabajar con Google Sheets desde Python y guardar el historial contable en una hoja de cálculo.
- `google-auth`: se usa para autenticar peticiones contra APIs de Google de forma segura.
- `python-dotenv`: se usa para cargar variables de entorno desde archivos `.env` y evitar escribir credenciales directamente en el código.

## ¿Por qué se instalaron?

Se instalaron porque el proyecto necesita una base web con Flask y también integración con servicios externos de Google y Firebase. En particular, estas dependencias permiten:

- crear endpoints y lógica web con Flask;
- autenticar el acceso a APIs y recursos de Google;
- conectar la aplicación con Firebase y sus servicios;
- leer y escribir datos en Google Sheets;
- gestionar configuración sensible mediante variables de entorno.

## ¿Para qué sirven en el proyecto?

En conjunto, estas dependencias permiten que la aplicación pueda recibir solicitudes, procesar datos, autenticarse contra servicios externos y almacenar o consultar información en plataformas de Google/Firebase. Esto encaja con la necesidad de registrar transacciones desde cualquier dispositivo y dejar trazabilidad de cada movimiento en un historial centralizado.

## Archivo `requirements.txt`

El archivo `requirements.txt` guarda la lista exacta de dependencias instaladas junto con sus versiones. Sirve para:

- reproducir el mismo entorno en otra máquina;
- instalar todo el proyecto con un solo comando;
- evitar diferencias de versión entre desarrollo, pruebas y despliegue.

Para instalar todo lo que aparece en ese archivo, se usa:

```bash
pip install -r requirements.txt
```

## Nota

Algunas dependencias que aparecen en `requirements.txt` no se instalaron de forma manual, sino que llegaron como dependencias secundarias de los paquetes principales. Eso es normal cuando se exporta el entorno completo con `pip freeze`.
