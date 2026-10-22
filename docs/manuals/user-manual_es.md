# Manual de usuario

## Versión 0.38.0.0 — recordatorios y combinación fiable

Las fechas como «28.10» se reconocen por separado del resumen y se guarda un recordatorio opcional en UTC. Las tareas con una fecha y hora futuras reconocidas reciben un recordatorio; si solo hay fecha, se utiliza la hora guardada del resumen diario de tareas. Si no está configurada, elige una hora. No se reprograman registros anteriores automáticamente.

Las sugerencias para combinar priorizan los temas comunes y después la relevancia del texto; excluyen registros archivados. Se conserva el ID y el título del destino y se concatena el texto completo sin reescritura por IA, conservando adjuntos distintos y recordatorios programados. El original se archiva para recuperarlo; sus comentarios permanecen allí.

Los títulos de los resúmenes y del texto extraído aparecen en negrita y se omiten secciones de análisis idénticas. El título de la nota breve ya no muestra el límite de palabras. Se conservan los guiones bajos de los usuarios. La propuesta de compartir ofrece una sola acción para abrir el registro, en lugar de controles de retorno duplicados. Los avisos de creación no añaden relleno invisible; el dispositivo controla los saltos del aviso nativo.

Los importes de los bonos no cambian. Los reintentos de notificación persisten sin abonar el saldo de nuevo. OAuth de Google sigue aplazado. La aceptación de un adjunto por Telegram no confirma su descarga en el dispositivo; se siguen investigando los retrasos de las imágenes.

## Versión 0.37.0.3 — bonos y mensajes del sistema

Un día local activo aporta 0,50 puntos; los tres días siguientes sin actividad válida, 0,30, 0,15 y 0,05. El cuarto día se detienen con un aviso. Cuenta crear una entrada o comentario de más de 100 caracteres visibles, o compartir o asignar una entrada a otra persona; consultar, editar y recibir copias no cuenta. Si ya se abonó el bono de inactividad, la actividad solo completa el total diario hasta 0,50. No hay abonos retroactivos ni recálculo de saldos. El proceso se ejecuta durante la primera hora local; una incidencia puede retrasar o impedir el aviso ese día.

Ajustes → Ocultar mensajes del sistema: 5, 10 o 30 segundos, 1 minuto o Nunca; por defecto, 30 segundos. Se aplica a nuevos avisos temporales, no a la limpieza de navegación ni a la sincronización técnica del teclado. Los botones de borradores pendientes se conservan hasta actuar. Google OAuth queda aplazado; ICS y los enlaces de Google siguen costando 0,10 puntos, sin precio en el botón.

## Correcciones de 0.37.0.3

Las confirmaciones de creación usan espacios normales, sin saltos de línea forzados. Telegram y el sistema operativo determinan el diseño final de la notificación.

En la propuesta de compartir una nota, Compartir y Abrir nota aparecen en la misma fila; Atrás sigue separado y solo cierra la propuesta. En la ficha, Comentarios y Calendario comparten fila cuando el calendario está disponible.

El borrador conserva el enlace original antes de terminar el resumen. Guardar un resumen alternativo conserva su fuente. Los nuevos cargos de enriquecimiento con IA y justificantes de exportación incluyen la referencia a la entrada para enlazarla desde el historial; no se adivinan ni reescriben referencias antiguas.

Las expresiones con una hora sin minutos, como «сегодня в 19», incluyen una hora, no solo una fecha. Un enlace compatible de videollamada se exporta como ubicación en ICS y Google. La convención regional configurable CET/CEST usa Europe/Madrid, con horario de verano, no un desfase fijo UTC+01:00. Varios lugares distintos requieren aclaración.

## Versión 0.37.0.1

Los botones del calendario ya responden correctamente y no muestran el precio. Si no se confirma el envío del ICS, el bot ofrece un enlace independiente de Google Calendar dentro de la misma exportación de 0,10 puntos. Direcciones como `av. Aragon nº4-bis` conservan el número del edificio; se excluyen teléfono y correo de la consulta. No es necesario conectar una cuenta de Google.

## Versión 0.37.0.0

La exportación al calendario aparece en la ficha si se detecta una fecha u hora, y siempre en Más. El botón no incluye el precio en su nombre; la exportación cuesta 0,10 puntos. Al pulsarlo recibes directamente un archivo de evento .ics, sin vista previa intermedia en el bot, y un enlace alternativo a Google Calendar. Abre el archivo con tu calendario y confirma la importación; Telegram o el sistema pueden pedirte elegir una aplicación. No se garantiza la apertura automática del calendario predeterminado en iOS, Android ni en ordenador.

Si Telegram no confirma el envío del ICS, el bot envía un mensaje independiente con el enlace preparado de Google Calendar. La confirmación es un ID de mensaje y de archivo devuelto por Telegram, no la descarga o importación en el dispositivo. El enlace no requiere conectar el bot mediante OAuth.

Una fecha sin hora crea un evento de día completo; una hora sin fecha usa el día de hoy en tu zona horaria guardada, aunque ya haya pasado. Con fecha y hora se usa ese momento. La duración predeterminada es de 60 minutos. El título empieza con el icono de nota/tarea y usa el título del registro; la descripción incluye un enlace al registro en el bot, no su texto privado. Si falta la fecha o es inválida o ambigua, Más solicita una sola fecha/hora de inicio; Atrás cancela, y los archivos o reenvíos crean un borrador nuevo.

Se cobra una sola entrega correcta por usuario para el mismo evento. Volver a obtenerlo es gratis, incluso tras reiniciar el bot; los fallos de envío se reembolsan. Un título, fecha u hora diferente crea otro evento. El bot no confirma el guardado en el calendario. Reimportar puede crear duplicados; no hay sincronización con cambios posteriores. El archivo desaparece del chat al cerrar los adjuntos del registro. No hace falta conectar una cuenta de calendario ni usar análisis de IA de pago.

La lectura en voz alta conserva los enlaces del autor y de la fuente, incluso al convertir una nota en tarea o viceversa. Los enlaces sin esquema, como Tambur.pub, se abren mediante HTTPS y no se muestran como Markdown.

La duración del audio generado se mide y se conserva al volver a abrir la entrada. Repetir la lectura del mismo texto con la misma voz y modelo reutiliza el archivo guardado, sin otro cargo de generación con IA ni un adjunto duplicado. Al cambiar el texto leído se crea una versión nueva. Los archivos de audio antiguos de origen desconocido no se eliminan automáticamente.

## Versión 0.36.0.1

Los adjuntos y los mensajes reenviados crean un borrador nuevo en vez de interpretarse como una fecha de recordatorio, aunque el resumen de la tarde espere respuesta. Una sugerencia de recordatorio no activa la introducción de fechas; abre Recordatorio expresamente para escribir una fecha.

Las acciones Nota con IA y Tarea con IA aparecen siempre en los borradores nuevos y reabiertos, incluidos los de solo texto. El acceso a la IA y el saldo se comprueban al pulsar; el guardado normal sigue disponible.

En la sugerencia de enviar o asignar una entrada a las personas mencionadas, Atrás cierra solo la sugerencia y conserva la pantalla, la página y los adjuntos anteriores. Volver a la entrada sigue siendo una acción independiente.

## Versión 0.36.0.0

El bono diario se abona con la primera acción válida, no a medianoche. Crear un elemento o comentario —también al completar una tarea— exige más de 100 caracteres visibles; compartir o asignar a otra persona no exige una longitud mínima. No se repite en el mismo día local ni se recalculan saldos anteriores. Las recompensas de bienvenida y por compartir mantienen sus propias reglas.

La búsqueda muestra todas las coincidencias por relevancia, con paginación estándar. Volver desde un elemento recupera la consulta y la página anteriores sin cobrar de nuevo el resumen de IA.

El audio AAC se empaqueta localmente en M4A sin recodificar antes de transcribirlo. El adjunto original no cambia. Un borrador sin texto con un archivo Markdown muestra una descripción clara y el número de documentos.

Los botones de un borrador pendiente permanecen en su tarjeta principal hasta que se usan, aunque se abra otro borrador. Al guardar, cerrar o eliminar un elemento se retiran las copias de adjuntos mostradas por el bot, incluso durante el envío; se conservan los mensajes originales.

Los sitios no repiten su fuente y los enlaces del texto se conservan. Cada segmento reenviado se muestra como «autor: mensaje», con enlace al mensaje original cuando Telegram lo proporciona; puede no estar disponible en reenvíos privados u ocultos. Se conservan los enlaces de los párrafos numerados. Los borradores antiguos no se reescriben en bloque.

## Versión 0.35.0.9

Al establecer recordatorios se vuelve a una sola pantalla de tareas, sin listas duplicadas. Al cerrar un elemento se retiran sus archivos adjuntos del chat; al volver a abrir el mismo elemento se reutilizan los archivos ya mostrados.

Los ID de los resultados de búsqueda enlazan con el elemento correspondiente y cada línea utiliza el icono de su encabezado.

Los mensajes reenviados combinados conservan el remitente de cada segmento. El análisis con IA genera un único resumen del texto, el OCR y el contenido de los adjuntos compatibles, incluida la información visual. Se conservan los párrafos y las listas.

Telegram controla la descarga en el dispositivo; la vista previa puede seguir borrosa mientras se descarga. No se pueden analizar por completo archivos incompatibles o demasiado grandes.

Esta guía explica cómo usar AUNotebot desde Telegram.

Nota de mantenimiento (aclaración del límite de audio v0.25): para el audio subido a Telegram, este bot aplica el límite de descarga de Telegram Bot API.

## 1. Inicio
1. Abre el chat con el bot.
2. Envía `/start`.
3. `/start` siempre vuelve a cargar y aplica tus ajustes guardados, especialmente Idioma y visibilidad del menú inferior.
4. Verás:
   - mensaje de bienvenida:
     - `Bienvenido al bot Telenota.`
     -
     - `📝🗣️🎥🌃➡️🧠✅`
     - `Toma notas donde transcurre tu vida.`
     - `Captura ideas, pensamientos y tareas, y no vuelvas a olvidar nada.`
     -
     - `1️⃣ Escríbeme, envíame un mensaje de voz, una imagen, un video circular o un video normal.`
     - `2️⃣ Lo guardaré y crearé una nota o una tarea. Mi IA lo analizará y hará un breve resumen.`
     - `3️⃣ Déjalo como nota o conviértelo en tarea para compartirlo o poner un recordatorio.`
     -
     - `⚖️ Al usar el bot, aceptas las Condiciones de uso (haz clic en Más -> Legal).`
     - `❓ Haz clic en Más -> Ayuda para abrir la guía de usuario.`
     - `✉️ Ideas o comentarios: @telenota_chat.`
   - la versión actual en la última línea del mensaje de bienvenida
   - contadores y accesos directos inline:
     - fila 1: `Notas`, `Tareas`
     - fila 2: `Borradores`, `Recordatorios`
     - fila 3: `Buscar`, `Más`
     - fila 5: botón opcional `Seguir novedades de Telenota` en el idioma actual de la interfaz
   - menú de comandos de Telegram (menú hamburguesa) con accesos directos
5. Abrir `/start` o cualquier lista oculta las pantallas antiguas de listas/inicio para que solo quede visible la pantalla solicitada.
6. Las listas abiertas desde accesos directos muestran un título compacto encima de los botones en vez de un mensaje vacío de marcador.
7. Si hay un canal de novedades configurado para tu idioma de interfaz, `/start` también muestra un botón opcional con noticias, consejos y ejemplos de Telenota en ese idioma. Seguirlo es opcional y no afecta al uso del bot.

Documentos públicos de términos:
- [Repositorio de documentos legales](https://github.com/panslav/aunotebot_public/tree/main/docs/legal)
- Abre `Más -> Legal` para ver la página de términos en el idioma actual de tu interfaz.
- Políticas de uso de OpenAI (base para funciones de IA):
  - https://openai.com/en-GB/policies/usage-policies/
  - las funciones de IA pueden limitarse o desactivarse si una solicitud infringe estas políticas.
- Nota de seguimiento administrativo:
  - el bot almacena entradas de auditoría de acciones (`moment`, `action_type`) y vínculos de compartición (`source`, `target`, `action_type`) para operaciones y analítica de grafos.

Manuales públicos de usuario:
- [Repositorio de manuales públicos](https://github.com/panslav/aunotebot_public/tree/main/docs/manuals)
- Abre `Más -> Ayuda` para ver el manual en el idioma actual de tu interfaz.

## 2. Idioma
1. En el primer `/start`, el bot intenta detectar tu idioma desde la configuración regional de Telegram.
2. El idioma predeterminado, si no puede detectarlo, es inglés.
3. Para cambiar el idioma manualmente:
   - abre `Más -> Ajustes -> Idioma`
   - elige uno de estos idiomas, en este orden: `English`, `Español`, `Français`, `Português`, `Русский`, `Українська`, `简体中文`, `العربية`
4. Después de seleccionarlo, las etiquetas y botones principales de la interfaz se traducen.

## 2a. Puntos de IA y Telegram Stars
La exportación al calendario cuesta `0,10 puntos` por entregar correctamente el archivo o el enlace alternativo, una vez por usuario y evento sin cambios. Si falla el ICS y se entrega el enlace de Google, se cobra una sola operación. Si no se entrega ninguno, se devuelve la reserva. Repetir la exportación es gratis, incluso tras reiniciar el bot. El botón no muestra el precio.

1. Las acciones con IA usan tu saldo de puntos.
2. Modelo de facturación predeterminado:
   - `1 punto = 1 Telegram Star`
   - `10 puntos gratis` una sola vez cuando empiezas a usar el bot
   - `0,50 puntos` por día local activo; después, `0,30`, `0,15`, `0,05` durante tres días inactivos. El cuarto día se detienen hasta reanudar la actividad válida. Consultar, editar y recibir copias no cuenta.
   - no hay recompensa automática de puntos por crear notas/tareas
   - `1.5 puntos / minuto` para texto a voz
   - `0.25 puntos / minuto` para analizar audio
   - `1 punto / minuto` para convertir en texto audio/vídeo ya adjunto a un elemento guardado
   - `0.1 puntos` por OCR de imagen
   - `0.05 puntos` por análisis de texto/enlace
3. Para `🤖 Analizar con IA` en medios guardados, el bot lee la duración almacenada con el adjunto de Telegram y cobra proporcionalmente por segundos a `1 punto / minuto`.
   - Ejemplo: `125 segundos` cuestan `2.09 puntos`.
   - El cargo se redondea hacia arriba al `0.01 punto` más cercano.
   - Si un adjunto guardado antiguo no tiene duración almacenada, el bot lo trata como `60 segundos`.
   - Si tu saldo es insuficiente, la transcripción no empieza y tu nota/tarea existente no cambia.
4. Abre `Más -> Puntos` para:
   - ver tu saldo actual
   - ver tus últimas 5 operaciones de puntos
   - abrir el historial completo de puntos
   - ver los precios actuales de IA
   - recargar con Telegram Stars
5. Puedes compartir tu propio número de teléfono en `Más -> Ajustes -> Contactos -> Compartir mi teléfono`.
6. `Más -> Ajustes` también incluye una zona peligrosa para borrar los datos de tu cuenta de AUNotebot.
7. Borrar todos los datos elimina permanentemente tus notas, tareas, borradores, recordatorios, contactos, ajustes, historial de puntos y registros de cuentas vinculadas pertenecientes al bot.
8. Cuando compras puntos dentro del bot, las recargas con Telegram Stars se cobran directamente en `XTR`.
9. Si tu saldo es insuficiente:
   - la función de IA se bloquea solo para esa acción
   - el bot muestra una notificación
   - las funciones sin IA siguen funcionando
10. Acciones típicas de IA de pago:
   - resúmenes y etiquetas
   - generación de respuestas en Recall/Find
   - traducción
   - interpretación libre de recordatorios, zona horaria y horarios de digest
   - transcripción y texto a voz

## 3. Crear una nota
1. Envía texto normal al bot.
2. El bot muestra una vista previa de borrador.
3. Pulsa `📝 Guardar como nota`.
4. Se abre la lista de notas.

## 4. Crear una tarea
Opción A:
1. Envía texto.
2. En la vista previa del borrador pulsa `🟧 Guardar como tarea`.
3. Se abre la lista de tareas.

Opción B:
1. Abre cualquier nota.
2. Pulsa `⬛ Convertir en tarea`.

## 5. Reenviar mensajes
1. Reenvía uno o varios mensajes al bot.
2. El bot combina mensajes reenviados cercanos en el tiempo en un solo borrador.
   - El tiempo de combinación predeterminado es `30` segundos.
   - Puedes cambiarlo en `Más -> Ajustes -> Tiempo de combinación de mensajes`.
3. Si añades texto normal justo después de reenviar, el bot lo añade como:
   - `💬 Reenviado con comentario:`
   - `<tu texto>`
   antes de la línea de fuente/pie.
4. En la vista de nota/tarea, las fuentes públicas de usuarios de Telegram se muestran como enlaces clicables `@handle` en lugar de URLs crudas `https://t.me/...`, se mantiene exactamente una línea en blanco antes del pie final `Guardado vía Telenota (...)`, y ese pie también incluye un enlace clicable `tu mensaje` al mensaje exacto del bot desde el que se creó el elemento cuando Telegram todavía lo expone.
5. Si un mensaje reenviado contiene uno o varios enlaces web, el bot usa primero los metadatos de vista previa disponibles de cada página y, cuando no existen, intenta un fallback determinista y seguro del título usando los metadatos de la página (`og:title`, `twitter:title` o HTML `<title>`).
   - Los enlaces redirigidos de Google Maps pueden resolverse al título final de la página cuando la página de destino lo expone.
   - Si no se puede extraer un título seguro, el bot mantiene el fallback existente de guardado con enlace de origen en lugar de mostrar una fuente falsa o un error sin filtrar.
   - En reenvíos combinados, la actualización en segundo plano del resumen del enlace reemplaza solo el bloque pendiente del enlace y conserva los otros mensajes reenviados.
6. El formato de Telegram del texto reenviado se conserva en las notas/tareas guardadas cuando Telegram lo expone al bot:
   - negrita, cursiva estilo Markdown, enlaces y bloques de cita se renderizan en la vista final del elemento.
   - los enlaces conservan su URL de destino completa, incluidos parámetros de consulta como `?g_st=...` o `&foo=...`.
7. Si no se añade un comentario separado después del reenvío, el bot guarda el marcador explícito `Reenviado sin comentarios`; si se envía un comentario justo después, solo ese comentario se guarda en el bloque de comentario.
8. Los medios de Telegram adjuntos al mensaje reenviado se guardan con el borrador y se muestran con la nota/tarea guardada. Si varios adjuntos tienen un enlace de fuente guardado, la vista del elemento los muestra como enlaces compactos separados por comas y agrupados por tipo de medio:
   - las fotos/imágenes permanecen adjuntas cuando Telegram las proporciona como medios descargables por el bot.
   - las imágenes de vista previa de enlaces generadas solo por los clientes de Telegram pueden no estar disponibles mediante Bot API; envía/reenvía la foto real si necesitas retención garantizada de la imagen.
   - si Telegram expone un vídeo o una animación reenviados junto con una foto de vista previa del cliente, el bot conserva el vídeo o la animación reales y oculta la imagen de vista previa duplicada.
   - si Telegram solo informa de un archivo reenviado demasiado grande durante el guardado con IA, el bot guarda el borrador original sin análisis de medios por IA en vez de mostrar un error genérico.
9. Opcional: envía texto solo con hashtags (ejemplo: `#work #idea`) antes de guardar para añadir etiquetas.
10. Abre el borrador y usa:
   - fila 1: `📝 Guardar como nota`, `🟧 Guardar como tarea`
   - fila adicional opcional: `⏰ Guardar como recordatorio` aparece cuando el texto del borrador contiene una fecha/hora reconocible
   - acciones finales: `✏️ Editar`, `❌ Cancelar`
   - las acciones con IA aparecen siempre, también en borradores de solo texto; para imágenes, el elemento conserva primero el contenido original y después muestra el resumen con IA y el texto OCR, manteniendo las listas numeradas y con viñetas legibles
   - el resumen con IA se formatea en tres partes cortas: introducción, parte principal y conclusión
   - `Editar` muestra solo el texto limpio del elemento para copiarlo manualmente; la fuente, el tipo localizado del elemento y el pie del bot permanecen en la plantilla y no forman parte del texto que vuelves a enviar
11. Después de pulsar guardar, el bot muestra inmediatamente un estado de guardado y luego un mensaje de éxito con cuatro accesos directos inline: abrir el elemento creado y Notas en la primera fila, y luego Inicio y Borradores en la segunda fila.
12. Si todos los borradores se consumen/guardan, abrir `Borradores` te devuelve al selector de Inicio.

Los borradores nuevos reciben un título breve generado por IA en el idioma de interfaz seleccionado. El análisis de vídeo con IA describe primero la imagen, incluidas las fechas legibles, y añade la transcripción de audio si está disponible.

## 6. Voz y vídeo
1. Envía un mensaje de voz, archivo de audio (incluido `.m4a` cuando Telegram lo envía como audio o documento de audio), vídeo o videonota.
2. Para mensajes de voz y archivos de audio, el bot muestra inmediatamente un mensaje de procesamiento cuando empieza el análisis.
3. Para vídeos normales, videonotas y documentos de vídeo, el bot primero guarda el medio entrante como borrador; el análisis con IA empieza solo cuando eliges `Nota con IA` o `Tarea con IA`.
4. Cuando se ejecuta el análisis con IA, el bot transcribe y prepara el texto del borrador/elemento. Las transcripciones de audio/vídeo incluyen marcas de tiempo al final de cada párrafo cuando hay datos de timing disponibles.
   - Si la transcripción falla, el bot muestra `Intentar de nuevo`; púlsalo para reintentar con el mismo archivo de Telegram sin volver a subirlo.
5. Pulsa `📝 Guardar como nota` o `🟧 Guardar como tarea`.
   - Después de guardar, el bot muestra un mensaje de éxito con cuatro accesos directos inline: abrir el elemento creado y la lista correspondiente en la primera fila, y luego Inicio y Borradores en la segunda fila.
6. Si el borrador contiene una fecha/hora reconocible, puedes pulsar `⏰ Guardar como recordatorio`.
   - Esto guarda el borrador como tarea y programa el recordatorio inmediatamente.
7. Si un borrador combina varios mensajes reenviados/con pie o análisis de medios por IA, la nota/tarea guardada separa las secciones con divisores horizontales visibles. El formato del texto original y del contenido generado se conserva cuando Telegram lo expone al bot.
8. Los mensajes de voz, archivos de audio y vídeos de Telegram mayores de `20 MB` se rechazan antes del procesamiento porque Telegram Bot API no permite a este bot descargar archivos mayores en este runtime.
9. Si tu grabación o vídeo supera `20 MB`, divídelo o comprímelo manualmente y envía las partes más pequeñas una por una.
10. Los mensajes de error temporales se eliminan automáticamente cuando envías el siguiente mensaje, pulsas el siguiente botón del bot o después de 30 segundos.
11. Los fallos recuperables de Telegram, IA o tiempo de espera muestran un código estable, por ejemplo `E-TIMEOUT-001`. Reenvía ese mensaje a `@telenota_chat` al pedir ayuda; el código no muestra tu contenido.

## 7. Imágenes y capturas de pantalla
1. Envía o reenvía una imagen/captura de pantalla.
2. El bot ejecuta OCR y resume el texto/contenido visible importante.
3. Se crea un borrador; después guárdalo como nota o tarea.
4. Si envías un documento PDF con texto y eliges una acción de guardado con IA, el bot conserva el contenido original del borrador, añade el texto extraído del PDF y después agrega un breve resumen con IA de hasta `300` palabras en el idioma de interfaz seleccionado.
5. El texto extraído se conserva con párrafos legibles y el resumen con IA se renderiza en tres partes cortas: introducción, parte principal y conclusión.
6. Los PDF escaneados o compuestos solo por imágenes pueden fallar en el análisis con IA hasta que exista soporte OCR para PDF.
7. Si guardas un PDF sin IA, el borrador o elemento conserva una línea simple `PDF <nombre del archivo>`. Si después abres el elemento guardado y pulsas `Análisis con IA`, se ejecuta el mismo flujo de resumen del PDF.
8. Telegram Bot API no proporciona a los bots el archivo multimedia de una historia reenviada. El bot guarda la referencia y te pide enviar a continuación una captura, una foto o un vídeo descargado; adjunta ese archivo al mismo borrador.
9. En el análisis con IA de una imagen, el elemento guardado muestra primero el resumen de IA y después el texto OCR reconocido. Las listas numeradas y con viñetas de la imagen conservan su formato.

## 8. Explorar notas y tareas
- Usa el menú de comandos de Telegram (hamburguesa):
  - `🏠 Inicio`
  - `🔎 Buscar`
  - `📝 Notas`
  - `🗂️ Borradores`
  - `🟧 Tareas`
  - `⏰ Recordatorios`
  - `📚 Más`
- Si el menú inferior está activado (`Más -> Ajustes -> Mostrar menú inferior`):
  - fila 1: `📝 Notas` + nueva línea + `(N)`, `⏰ Recordatorios` + nueva línea + `(N)`, `🟧 Tareas` + nueva línea + `(N)`
  - fila 2: `🗂️ Borradores` + nueva línea + `(N)`, `🔎 Buscar`, `📚 Más`
- Los encabezados de listas como `📝 Notas` y `🗂️ Borradores` se muestran en una sola línea visible, sin relleno invisible.
- Cuando abres una tarea desde la página 2 o posterior y luego la marcas como hecha, la eliminas, la conviertes o configuras un recordatorio, el bot vuelve a la misma página de la lista de tareas al mostrar la lista otra vez.
  - cuando está activado, el menú inferior permanece visible hasta que el usuario lo desactiva en ajustes
  - estos botones abren las mismas pantallas que las acciones del menú hamburguesa.
- O usa los contadores inline de la pantalla de inicio:
  - fila 1: `📝 Notas (N)`, `🟧 Tareas (N)`
  - fila 2: `🗂️ Borradores (N)`, `⏰ Recordatorios (N)`
  - fila 3: `🔎 Buscar`, `📚 Más`

## 9. Buscar (búsqueda combinada + Recall)
1. Pulsa `🔎 Buscar` en la pantalla de inicio o en el menú hamburguesa, o usa `/find`.
2. El bot entra en modo Buscar interactivo y muestra:
   - `🔎 ¡Pregúntame lo que quieras! Mi cerebro de IA encontrará y resumirá información para ti.`
3. Envía cualquier consulta/pregunta en formato libre.
4. El bot hace ambas cosas:
   - ranking determinista sobre notas y tareas, incluidos elementos archivados
   - coincidencia sensible a flexiones para variaciones de palabras de la consulta (por ejemplo terminaciones)
   - resumen de IA sobre los resultados relevantes
5. Formato de respuesta cuando se encuentran elementos:
   - texto de resumen
   - `Estos son los elementos más relevantes para tu solicitud:`
   - botones de elementos relevantes, los más relevantes primero
   - `⬅️ Atrás`
6. Si tu consulta de búsqueda es un ID exacto de elemento (por ejemplo `219` o `#219`) y existe, se fija como resultado #1.
7. Para salir del modo Buscar, pulsa `⬅️ Atrás`.
8. `⬅️ Atrás` te devuelve a la pantalla en la que estabas antes del modo Buscar.
9. Si el resumen opcional de IA no está disponible, las coincidencias locales y los botones de resultados siguen disponibles con un resumen alternativo neutro.

## 9a. Sugerencias de recordatorio
1. Si una nota o tarea recién creada contiene una frase probable de fecha/hora, el bot propone automáticamente un recordatorio.
2. Si solo se detecta una fecha, el bot ofrece `Mañana`, `Mediodía`, `Tarde`, además de `Configurar recordatorio` y `Omitir`.
3. Mientras esta pantalla está abierta, puedes escribir directamente tu propia fecha/hora; ya no hay un botón aparte de entrada manual.
4. Si solo se detecta una hora, el bot asume la fecha de hoy salvo que escribas otra fecha.
5. Si el elemento sigue siendo una nota normal y eliges `Configurar recordatorio`, el bot primero la convierte en tarea y luego programa el recordatorio.
6. Después de crear el recordatorio, el bot confirma la hora en tu idioma.
7. Si abres la configuración del recordatorio desde un callback de medio, el bot usa una ruta de edición segura y sigue mostrando la indicación del recordatorio.

## 10. Acciones de notas y tareas

### Acciones de nota
- `✏️ Editar`
- `⬛ Tarea`
- `❌ Eliminar`
- `📚 Más`
- `⬅️ Atrás`
- `📚 Más` abre:
  - fila 1: `🤖 Analizar con IA`, `🔊 Crear voz`
  - fila 2: `🔀 Fusionar`, `📤 Compartir`
  - fila 3: `📌 Fijar` / `📌 Desfijar`, `🏷️ Etiquetas`
  - fila 4: `⬅️ Atrás`

### Acciones de tarea
- `✏️ Editar`
- `✅ Hecho` o `🔄 Rehacer`
- `⏰ Recordatorio`
- `🔁 Convertir en nota`
- `❌ Eliminar`
- `📚 Más`
- `⬅️ Atrás`
- `📚 Más` abre:
  - fila 1: `🤖 Analizar con IA`, `🔊 Crear voz`
  - fila 2: `🔀 Fusionar`, `👥 Asignar` o `👥 Reasignar`
  - fila 3: `📌 Fijar` / `📌 Desfijar`, `🏷️ Etiquetas`
  - fila 4: `⬅️ Atrás`

### Asignación de tareas con Contactos
1. Abre una tarea.
2. Pulsa `👥 Asignar` o `👥 Reasignar`.
3. El bot muestra:
   - tus contactos guardados como botones
   - opción de entrada manual (`@handle` o teléfono)
4. Si escribes un nuevo `@handle`/teléfono válido, se guarda automáticamente en tus Contactos.
5. Si el destinatario ya inició el bot, la asignación se envía y la tarea queda vinculada a ese usuario.
6. Si el destinatario no inició el bot y seleccionaste un `@handle`, el bot crea un mensaje de invitación separado con el enlace oculto bajo “Telenota”. Envía ese mensaje al destinatario: cuando inicie el bot con ese enlace, la tarea se entregará automáticamente si su handle de Telegram coincide. Si otra cuenta abre el enlace, el bot te pedirá aprobar o rechazar el acceso.
7. Puedes usar `↩️ Quitar asignación` desde el selector de asignación para eliminar la asignación actual.

### Compartir notas con Contactos
1. Abre una nota normal.
2. Pulsa `📤 Compartir`.
3. El bot muestra:
   - tus contactos guardados como botones
   - opción de entrada manual (`@handle` o teléfono)
4. Si escribes un nuevo `@handle`/teléfono válido, se guarda automáticamente en tus Contactos.
5. Si el destinatario ya inició el bot, la nota se comparte y se entrega en su chat, incluidos adjuntos.
6. Si el destinatario no inició el bot y seleccionaste un `@handle`, el bot crea un mensaje de invitación separado con el enlace oculto bajo “Telenota”. Envíalo al destinatario: cuando inicie el bot con ese enlace, la nota se entregará automáticamente si su handle de Telegram coincide. Si otra cuenta abre el enlace, el bot te pedirá aprobar o rechazar el acceso.

### Crear voz (texto a voz)
1. Abre cualquier nota o tarea.
2. Pulsa `🔊 Crear voz`.
3. El bot muestra inmediatamente una notificación del sistema indicando que ha empezado la generación de texto a voz.
4. El bot genera un mensaje de voz usando OpenAI (voz `onyx`), lo envía al chat y lo adjunta a ese elemento.

### Medios a texto
1. Abre cualquier nota o tarea.
2. Abre `📚 Más`.
3. Pulsa `🤖 Analizar con IA`.
4. El mismo botón ahora también funciona para elementos de texto normales y para imágenes adjuntas, no solo para audio/vídeo/PDF.
5. El bot calcula el coste según la ruta real de análisis:
   - el enriquecimiento de texto/enlaces usa la tarifa de análisis de texto
   - las imágenes guardadas usan la tarifa de análisis de imagen
   - el audio/vídeo guardado usa la duración almacenada de Telegram a `1 punto / minuto`, redondeada al `0.01 punto` más cercano
6. Si tu saldo es suficiente, el bot reserva los puntos necesarios, ejecuta el análisis con IA, actualiza el elemento y confirma el cargo solo después de un procesamiento correcto.
   - Las transcripciones de audio/vídeo añadidas incluyen marcas de tiempo al final de cada párrafo cuando hay datos de timing disponibles.
7. Si el análisis con IA falla, los puntos reservados se liberan y el elemento queda sin cambios.

## 11. Fusionar elementos (nota/tarea)
1. Abre un elemento.
2. Pulsa `🔗 Fusionar`.
3. El bot muestra hasta 5 elementos del mismo tipo abiertos recientemente.
4. Selecciona el elemento destino o envía el ID del destino como texto.
5. El texto del elemento origen se añade al texto del elemento destino.
6. El elemento origen se elimina y se abre el elemento destino.
7. El aviso de fusión correcta aparece dentro de la pantalla del elemento destino abierto, no como mensaje separado en el chat.

## 11.1 Fijar elementos
1. Abre una nota o tarea.
2. Pulsa `📚 Más`.
3. Pulsa `📌 Fijar` para mantener el elemento arriba de su lista.
4. Pulsa `📌 Desfijar` para devolverlo al orden cronológico normal.

## 12. Etiquetas
1. Abre una nota.
2. Pulsa `🏷️ Etiquetas`.
3. Pulsa una etiqueta para abrir notas con esa etiqueta.
4. Para añadir etiquetas, envía un mensaje con hashtags (ejemplo: `#project #urgent`).
5. Los nombres personales detectados en el texto de la nota se añaden automáticamente como etiquetas con mayúscula inicial.

## 13. Editar una nota
1. Abre una nota/tarea.
2. Pulsa `✏️ Editar`.
3. Copia solo el texto limpio del cuerpo que aparece en la indicación, edítalo y vuelve a enviar el texto completo actualizado.
4. Las líneas de fuente, el tipo localizado del elemento y el pie `Guardado vía Telenota` se vuelven a aplicar desde la plantilla del bot y no deben escribirse manualmente.
5. El bot guarda la edición y añade una marca de tiempo `última edición` en el pie.

## 14. Eliminar o archivar
1. Abre una nota/tarea.
2. Pulsa `❌ Eliminar`.
3. Elige:
   - `🗑️ Eliminar`
   - `🗄️ Archivar`
   - `⬅️ Atrás`
4. Si eliges `🗄️ Archivar`, el bot pide un comentario opcional de archivado.
5. Envía el comentario o pulsa `✅ Sin comentarios`.
6. El bot añade la línea `Comentario de archivado: <comment>` al final del elemento y luego lo archiva.
7. Si la nota/tarea tenía adjuntos de medios mostrados en el chat, esos mensajes de adjuntos se eliminan de la pantalla después de eliminar/archivar.

## 15. Tarea completada y comentarios
1. Abre una tarea.
2. Pulsa `✅ Hecho`.
3. Introduce un comentario opcional o pulsa `✅ Sin comentarios`.
4. Todos los mensajes de adjuntos mostrados actualmente para esa tarea se eliminan del chat mientras se muestra la indicación/lista de completado; los adjuntos guardados permanecen en el elemento.
5. El resultado sigue tus Ajustes:
   - Eliminar
   - Archivar
   - Mantener

## 16. Recordatorios
1. Abre una tarea.
2. Pulsa `⏰ Recordatorio`.
3. Envía una fecha/hora en formato libre:
   - `mañana a la misma hora`
   - `en 2 horas`
   - `2026-02-20 14:30`

## 17. Ajustes
Abre `⚙️ Ajustes` para configurar:
- `🌐 Idioma` (primer elemento)
  - English / Español / Français / Português / Русский / Українська / 简体中文 / العربية
- `🕒 Zona horaria`
  - pulsa `Zona horaria`
  - responde con ciudad, código de zona horaria o texto con la hora actual
  - el bot usa OpenAI para inferir y guardar tu zona horaria
  - la zona horaria guardada se muestra como `UTC±HH:MM · City`
- `Marcar como hecho`
  - Eliminar / Archivar / Mantener
- `Copiar texto para ediciones`
  - Copiar texto de nota / No hacer nada
- `🗓️ Digest diario de tareas`
  - `Configurar hora` con texto libre como `cada día a las 8`, `21:30`, `mañana 7`
  - guardar una hora también activa automáticamente el digest diario
  - `Activar` / `Desactivar`
  - en Ajustes, el estado se muestra solo con un círculo verde/rojo
  - el resumen de Ajustes muestra la hora local sin sufijo de zona horaria
  - el digest se envía una vez al día a la hora local configurada del usuario
  - el digest incluye secciones:
    - `Recordatorios` o `No hay recordatorios hasta el próximo digest`
    - `Tareas`
    - `Notas añadidas desde el último digest`
  - los elementos de todas las secciones son enlaces; al pulsarlos se abre la nota/tarea relacionada en el bot
  - el mensaje de digest incluye botones rápidos: `⏰ Recordatorios`, `🟧 Tareas`
  - el estado está sincronizado entre el resumen de Ajustes y la pantalla de detalle del digest
- `🌙 Resumen de la tarde`
  - `Configurar hora` con el mismo parser de hora libre que el digest matutino
  - guardar una hora también activa automáticamente el resumen de la tarde
  - `Activar` / `Desactivar`
  - en Ajustes, el estado se muestra solo con un círculo verde/rojo
  - el resumen de Ajustes muestra la hora local sin sufijo de zona horaria
  - el digest de la tarde incluye:
    - `Tareas -> Tareas que he completado hoy`
    - `Tareas -> Tareas que he creado hoy`
    - `Notas que he añadido hoy`
  - después del digest, el bot pregunta:
    - `¿Y cómo sientes TÚ que fue tu día hoy?`
    - responde a esa indicación concreta con texto/voz/vídeo
    - el bot guarda tu respuesta como una nota con la etiqueta `daily`
- `⏱️ Tiempo de combinación de mensajes`
  - pulsa el botón
  - envía un número de segundos, por ejemplo `30`, `45`, `120`
  - los mensajes enviados dentro de ese intervalo se combinan en un solo borrador
  - si el intervalo es de `30` segundos o más (con el ajuste predeterminado), se crea un nuevo borrador
- `📱 Mostrar menú inferior`
  - el estado se muestra solo con un círculo verde/rojo
  - predeterminado: activado
  - cuando está activado, el teclado inferior persistente se muestra para este usuario
  - cuando está desactivado, el teclado inferior persistente se oculta para este usuario
  - cambiar este ajuste es silencioso, sin mensajes del sistema sobre visibilidad
- `📚 N.º de elementos`
  - controla cuántos elementos se muestran por página en las pantallas de lista

La gestión de contactos está disponible en `Más -> Ajustes -> Contactos`:
- ver todos los contactos guardados para asignaciones
- `➕ Añadir contacto` (introducir `@handle` o teléfono)
- `📱 Compartir mi teléfono` (compartir tu propio contacto de Telegram con el bot)
- abrir contacto -> `Editar` / `Eliminar`
- editar actualiza el valor de contacto usado en las sugerencias de asignación

## 18. Consejos
- Si una lista es larga, usa los botones de paginación.
- Usa el menú de comandos (`/start`, `Notas`, `Tareas`, etc.) para navegar rápido.
- `Archivar` oculta el elemento de las listas normales de notas/tareas, pero conserva los datos.

## 19. Si algo parece roto (lado del cliente)
Si las acciones parecen bloqueadas (por ejemplo, pulsar un botón envía tu mensaje pero el bot no responde), prueba:
- enviar `/start`
- pulsar un botón inline de la pantalla de bienvenida
- pulsar/enviar `⬅️ Atrás` o `/back`
- cerrar y volver a abrir la app de Telegram
- si sigue bloqueado, borrar el historial del chat y volver a abrir el chat con el bot

## 20. Cómo informar bien de un error
Al informar de un error, incluye:
- el botón/acción exacto que pulsaste
- fecha/hora y zona horaria exactas
- captura de pantalla o grabación corta de pantalla
- la respuesta exacta del bot o que no hubo respuesta
- si `/start` sigue funcionando mientras otros botones no funcionan

## Documentos relacionados
- Condiciones de uso: [repositorio de documentos legales](https://github.com/panslav/aunotebot_public/tree/main/docs/legal)
- Flujo de pantallas: [Flujo de pantallas](/docs/Screenflow.md)
- Instalación: [Instalación](/docs/installation.md)
- Índice de documentación: [Inicio de documentación](/docs/README.md)

## 21. Actualizaciones de compartir y fuente
- `Más -> Compartir` ahora funciona tanto para notas como para tareas.
- En el selector de compartir puedes elegir un contacto guardado o pulsar `Compartir públicamente` para crear un mensaje reenviable con el enlace de inicio del bot.
- Los elementos largos de `Compartir públicamente` se dividen automáticamente en varios mensajes reenviables; cada mensaje termina con el pie normal `Guardado vía Telenota (<fecha y hora local>)`.
- Si alguien inicia el bot por primera vez desde tu enlace de invitación o desde tu enlace privado de compartir, recibirás una notificación persistente del bot indicando que se unió.
- Cuando Telegram aporta suficientes metadatos, `Fuente` abre el mensaje original exacto de Telegram.
- Los borradores, las notas y las tareas muestran la fecha y hora de guardado en tu zona horaria.

## Inicio guiado y borradores con IA
- En el primer inicio, completa tres acciones útiles y recibe el bono de bienvenida en partes: `+2`, `+3` y `+5` puntos.
- `Nota con IA` y `Tarea con IA` conservan el texto original, convierten todos los adjuntos compatibles a texto en orden y añaden un resumen legible de tres párrafos.
- Cada adjunto extraído se etiqueta por tipo y orden original; el texto completo aparece antes del resumen.
- Las menciones nunca asignan ni comparten automáticamente: Telenota te pide elegir la acción.
- `Atrás` recorre el historial de pantallas y `Inicio` vuelve directamente a la pantalla principal.
- Si un elemento ocupa varios mensajes de Telegram, sus botones aparecen bajo el último mensaje.

## Últimas actualizaciones (0.35.2)
- Las fotos y vídeos consecutivos del mismo bloque capturado ahora se muestran como álbum de Telegram cuando Telegram permite ese formato.
- La vista previa del borrador conserva mejor tanto los contadores agrupados de adjuntos como el texto original, sin repetir varias veces el mismo segmento combinado.
- En notas, tareas y borradores el pie es ahora más compacto: autor y fuente se muestran en una sola línea localizada, y la fecha guardada se muestra solo como fecha y hora locales.
- Al abrir una nota o borrador pesado ya no hace falta esperar a que terminen de cargar todos los adjuntos para usar la tarjeta principal; los medios siguen cargándose en segundo plano.
- Las pantallas de Contactos, Temas e Historial de puntos ahora tienen una fila final explícita con `Atrás` / `Inicio`, y los selectores grandes de páginas navegan por ventanas en lugar de una sola cuadrícula enorme.
- Las líneas del Historial de puntos ahora pueden mostrar la Nota/Tarea relacionada y un enlace profundo al elemento cuando el movimiento está vinculado a un elemento guardado que todavía existe.

## Últimas actualizaciones (0.36)
- Las notas y tareas ahora admiten comentarios. Abre un elemento y toca `Comentarios (N)` para ver los comentarios existentes como mensajes separados de Telegram con botones `Comentar` / `Eliminar`.
- Cuando el modo de comentario está activo, el siguiente texto/medio enviado o reenviado se muestra primero como vista previa con `Comentar`, `Crear borrador`, `Atrás` e `Inicio`; solo después de confirmarlo se guarda debajo del elemento como `Comentario N`.
- Los borradores y elementos guardados mantienen más compactas las líneas de servicio del reenvío: `Reenviado sin comentarios`, autor/fuente y hora de guardado quedan juntos sin líneas vacías extra.
- Las vistas previas de borrador muestran los contadores de adjuntos cerca del final de la tarjeta, encima de los metadatos de reenvío/fuente, y conservan el formato de Telegram siempre que sea posible.
- Ejecutar `Análisis con IA` sobre una nota o tarea ya guardada ahora añade el resultado debajo del contenido existente bajo `Resultados del análisis con IA:` en lugar de sustituir tu contenido guardado.
- Marcar una tarea como hecha ahora cancela sus recordatorios programados, y las sugerencias de recordatorio usan el idioma de interfaz guardado para reconocer meses y días localizados.
- `Más` ya no incluye un botón duplicado de `Ajustes`; abre Ajustes desde la pantalla de inicio.
- `Puntos` incluye un enlace directo a la documentación pública de puntos.
- Las sugerencias de `Combinar` ahora priorizan elementos con etiquetas similares sin IA; el ranking semántico con IA no está activado por defecto porque añadiría coste y latencia.

## Últimas actualizaciones (0.36.2.phase4-5)
- La vista previa del borrador puede mostrar un interruptor rojo/verde de traducción antes de guardar. Rojo conserva el idioma original; verde traduce el borrador al idioma de tu interfaz al guardar una nota o tarea normal.
- Los resúmenes de IA de notas y tareas ahora usan el idioma de interfaz elegido, aunque el texto original esté en otro idioma.
- Los mensajes reenviados rápidamente se fusionan respetando el orden de llegada.
- Las pantallas de combinación abiertas desde mensajes con medios ahora usan una reserva segura en lugar de mostrar un error de edición de Telegram.
- Los álbumes reenviados se guardan de forma serializada para conservar cada imagen, vídeo y pie de foto en su orden original. Las encuestas reenviadas guardan una copia textual de sus opciones y resultados disponibles; si no hay resultados, se añade una nota para votar en la encuesta original.
- Para líneas de dirección explícitas, el bot puede proponer coincidencias exactas de OpenStreetMap. Solo tras confirmación se añaden como comentarios de ubicación al guardar la nota o tarea.

## Últimas novedades (0.36.4)
- Los comentarios conservan el formato de Telegram y usan `Guardar`, `❌ Eliminar` y `Atrás`; al volver o eliminar también desaparece la pantalla de comentarios anterior.
- Las capturas de encuestas muestran los votos por opción y el total solo si Telegram los proporciona. En caso contrario, Telenota indica expresamente que los resultados son desconocidos y nunca inventa ceros.
- Las direcciones claras se detectan tanto en mensajes directos como reenviados, incluidas abreviaturas de calles en varios idiomas. Solo se envía a OpenStreetMap el candidato extraído y no se añaden coincidencias ambiguas.
- En los bloques de contacto, `Контакты: av. Aragon nº4-bis` se extrae como `Avenida Aragon, 4-bis`. Se normalizan las abreviaturas de vía y los indicadores del número sin perder `-bis` ni las letras del edificio. Los teléfonos, correos y enlaces contiguos se excluyen de la consulta. Se conserva la ciudad indicada, sin inventar una ciudad ni una ubicación aproximada.

## Versión 0.35.0.4
- Los títulos con IA usan el texto disponible, el resumen del enlace y el análisis de adjuntos compatibles. Un borrador que solo contiene un adjunto conserva un título por tipo de archivo hasta que se analice.
- El análisis con IA de un elemento guardado combina el texto actual con el texto extraído de todos los adjuntos compatibles antes de añadir el resultado.
- En reenvíos combinados, cada segmento muestra su autor antes del texto. La sugerencia de recordatorio desaparece tras cualquier acción; `Omitir` solo omite el recordatorio.

## Versión 0.35.0.5
- En un elemento combinado, cada autor aparece antes del texto de su mensaje reenviado.
- El resumen de IA aparece antes del texto OCR o extraído de los adjuntos.
- Ajustes usa un encabezado localizado y breve; Telegram controla la alineación de las etiquetas de los botones.
- Solo una respuesta explícita al aviso de reflexión nocturna se guarda como reflexión. Un texto, enlace o archivo enviado de forma independiente después del resumen crea un borrador normal y no queda atrapado en un modo de entrada anterior.
