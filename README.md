# ElectroFusion Libre

Proyecto independiente de ejemplo para una aplicación Android/Web offline que reúne:
- Visor básico DXF ASCII (LINE, CIRCLE, ARC, LWPOLYLINE, TEXT, MTEXT).
- Crear planos nuevos; dibujar líneas, rectángulos, círculos, polilíneas y textos.
- Seleccionar y mover entidades, eliminar y deshacer.
- Guardar/abrir proyectos editables JSON.
- Zoom, desplazamiento, capas, medición, exportación DXF y PDF mediante diálogo de impresión.
- Calculadora de ley de Ohm.
- Potencia monofásica y trifásica equilibrada.
- Relación ideal de transformadores.

## Sin registro / sin conexión
La aplicación no tiene login, backend, anuncios, telemetría ni llamadas de red. Todos los cálculos se ejecutan localmente.

## Crear APK
1. Comprimir el contenido de la carpeta `www` en un ZIP (o importar la carpeta del proyecto).
2. Abrir un empaquetador HTML-to-APK que permita importar un proyecto/ZIP local.
3. Seleccionar `www/index.html` como página inicial.
4. Configurar el nombre `ElectroFusion Libre`, identificador de paquete propio e icono.
5. Compilar y probar el APK en un dispositivo.

También puede abrirse `www/index.html` directamente en un navegador moderno.

## Alcance y limitaciones
Este es un punto de partida funcional, no un CAD profesional ni un dimensionador reglamentario. Solo interpreta DXF ASCII y las entidades indicadas. No implementa bloques, SPLINE, cotas, referencias externas ni todas las variantes DXF. La exportación crea un DXF ASCII nuevo y no conserva metadatos avanzados. Las calculadoras son orientativas y no sustituyen normas locales ni revisión de un profesional matriculado.

## Sobre los APK de referencia
El APK ElectroCAD examinado es un contenedor Trusted Web Activity que abre `https://electrocad.ar/app.html`; no incluye el código fuente de ese sitio. El otro APK contiene una herramienta CAD web de DXF. Por eso este ZIP es una implementación independiente de funciones generales, no una copia ni una fusión binaria de las aplicaciones originales. Para reproducir funciones específicas de ElectroCAD hace falta una lista de funciones o su código fuente con permiso de reutilización.

## Licencia
MIT para el código original incluido en este proyecto. Las bibliotecas de terceros no se incluyen. El uso de esta licencia no concede derechos sobre las marcas, código o recursos de las aplicaciones de referencia.


## Edición y exportación
- Para terminar una polilínea, hacé doble toque/clic en el área de dibujo.
- Seleccioná una entidad para moverla; eliminá la selección con el botón correspondiente.
- Guardar proyecto crea un archivo JSON editable por esta aplicación.
- Exportar DXF genera DXF ASCII con entidades compatibles.
- Exportar PDF abre la impresión del navegador; elegí **Guardar como PDF**. En algunos empaquetadores Android, la impresión depende del WebView y del servicio de impresión instalado.
- El término CAD puede referirse a formatos propietarios como DWG. Esta versión exporta DXF, un formato CAD de intercambio; no exporta DWG.
