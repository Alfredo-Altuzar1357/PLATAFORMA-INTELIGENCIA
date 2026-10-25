# Actualizar a Situación · Chiapas 0.2.0

Esta actualización amplía la aplicación existente. Conserva la cuenta, los acontecimientos, las cifras capturadas, las revisiones, los PIN y el directorio de datos de la versión 0.1.0. No requiere contratar alojamiento ni una API de pago.

## En Windows

1. Abre la versión que ya tienes. En **Ajustes** —**Mi aplicación** en la versión anterior— descarga un respaldo y guárdalo en una carpeta privada.
2. Cierra la aplicación mediante **Detener Situacion Chiapas**, en el menú Inicio.
3. Descarga el [instalador 0.2.0](https://github.com/Alfredo-Altuzar1357/PLATAFORMA-INTELIGENCIA/raw/refs/heads/installer-download/descargas/0.2.0/Situacion-Chiapas-0.2.0-Instalador.zip). Si viene en ZIP, pulsa **Extraer todo** y ejecuta `Situacion-Chiapas-Windows-0.2.0-Instalador.exe`.
4. Instálalo en la misma carpeta de programa que utilizabas. **No borres la carpeta de datos y no necesitas desinstalar primero.**
5. El instalador comprueba que la instancia anterior esté detenida y crea un respaldo SQLite consistente antes de reemplazar sus archivos. Si no puede verificarlo, detiene la actualización y conserva la instalación anterior.
6. Abre el mismo acceso del escritorio e inicia sesión con tu usuario y contraseña habituales.

Los datos continúan en `%LOCALAPPDATA%\SituacionChiapas`; el programa se instala por defecto en `%LOCALAPPDATA%\Programs\SituacionChiapas`. El respaldo automático previo queda dentro de la carpeta privada `Backups`, con el prefijo `Antes-de-actualizar-0.2.0-`. El instalador no envía estos archivos a GitHub ni a otro servicio.

## Cambios de esta versión

- En **Fuentes y cobertura → Iniciar barrido completo**, inicia la búsqueda, observa el progreso y pulsa **Ver hallazgos en el mapa**. Se ejecutan los canales directos y búsquedas públicas indexadas por municipio y fuente; las fuentes inaccesibles no se presentan como revisadas.
- En **H.D. y fallecimientos**, ejecuta el barrido específico y revisa las publicaciones detectadas antes de incorporarlas como casos. Su listado, gráficas y mapa se separan de las cifras confirmadas para evitar conteos indebidos.
- **Consultar fuentes oficiales** muestra los intentos del Gabinete y SESNSP. Las gráficas de cifras cargadas separan organismos y unidades. La nueva carga del CSV municipal original del SESNSP evita convertirlo manualmente a JSON cuando su esquema sea compatible. Las fuentes primarias consultadas devolvieron 403/503: no hay descarga vigente verificada y el lector de PDF del Gabinete sigue pendiente.
- En **Ajustes**, cambia el intervalo automático (5, 15, 30 o 60 minutos), fuentes habilitadas, intensidad del barrido, búsquedas de agenda/fallecimientos, pantalla inicial, puntos o calor, notificaciones y registros pendientes visibles. Los cambios permanecen guardados en el equipo. El barrido ampliado periódico se activa expresamente; el valor inicial conserva la actualización de canales directos.

La recopilación requiere equipo, programa e Internet activos. Un resultado indexado no equivale a leer directamente una red social ni a corroborar una noticia. Las estadísticas oficiales dependen de la publicación primaria y de su disponibilidad; el programa debe conservar su fuente, unidad, periodo y estado de consulta.

## Si necesitas regresar

Conserva la versión anterior y el respaldo previo. Detén la aplicación antes de restaurar. Utiliza **Restaurar respaldo** y selecciona la copia correspondiente; las credenciales vuelven a ser las de esa copia. La restauración conserva un archivo de seguridad de la base que sustituye.

Este procedimiento no ejecuta automáticamente un retroceso de versión. No borres datos para resolver un error: conserva el mensaje y el respaldo para revisar la causa.

## Comprobación de esta entrega

El instalador se genera con su versión y los SHA256 de sus distribuciones. La construcción y las pruebas disponibles se realizan en Linux; la ejecución del instalador en Windows todavía requiere comprobación en el equipo de destino. La compilación no tiene una firma comercial de editor. No desactives las protecciones de Windows.
