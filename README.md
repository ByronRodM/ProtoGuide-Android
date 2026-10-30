# ProtoGuide

Aplicación para Android que reconoce los componentes de un diagrama de circuito fotografiado y genera
su montaje en una protoboard, con una guía de armado paso a paso.

Proyecto de graduación. La versión publicada es un prototipo en fase beta.

Sitio: https://protoguide.dev

## Descarga

La versión más reciente está en [Releases](../../releases/latest), como `ProtoGuide.apk`.

## Requisitos

- Android 7.0 o posterior.
- Cámara, o una foto del diagrama guardada en el teléfono. También se puede armar un circuito sin
  foto, sobre un lienzo en blanco.
- Conexión a internet solo para la cuenta, la copia en la nube y compartir circuitos. Sin cuenta, la
  aplicación funciona sin conexión.

## Instalación

1. Descargar `ProtoGuide.apk` desde el teléfono.
2. Abrir el archivo. Android pide permitir la instalación desde el navegador o el gestor de archivos,
   porque la aplicación no se distribuye por Google Play. Por el mismo motivo puede aparecer un aviso
   de Google Play Protect.

Para actualizar desde una versión anterior, se instala el archivo nuevo encima, sin desinstalar: los
circuitos guardados se conservan.

## Funciones

- Detección de diez tipos de componentes en la foto de un diagrama dibujado a mano.
- Trazado de las conexiones sobre el diagrama, o armado del circuito sobre un lienzo en blanco.
- Montaje en protoboard en 2D, esquemático y vista 3D.
- Guía de armado paso a paso, dentro de la aplicación y en PDF.
- Tutorial «Primeros pasos» y una ayuda en cada pantalla.
- Cuenta opcional, con copia de los circuitos en la nube.
- Compartir circuitos por código o QR.

## Limitaciones conocidas

- La aplicación reconoce componentes, no conexiones: las conexiones las traza el usuario.
- No distingue un transistor NPN de uno PNP; el tipo se elige en el editor. El orden de las patas
  puede variar según el fabricante y conviene comprobarlo en la hoja de datos.
- **Interruptores:** se colocan siempre como un pulsador táctil de cuatro patas que cruza el canal
  central. Un interruptor de dos patas o uno deslizante se monta adaptando esa colocación, como
  explica su ficha en la biblioteca.
- No hay recuperación de contraseña desde la aplicación.

## Licencias

La aplicación incluye bibliotecas, tipografías y un modelo de detección de terceros. Los avisos y los
textos completos de sus licencias están en la aplicación, en «Acerca de ProtoGuide».

El modelo de detección se entrenó con Ultralytics YOLO11 sobre el conjunto de datos CGHD: Thoma, F.,
Bayer, J., Li, Y. y Dengel, A. (2021). *A Public Ground-Truth Dataset for Handwritten Circuit Diagram
Images*. International Conference on Document Analysis and Recognition (ICDAR), Springer, pp. 20–27.
