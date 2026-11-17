# Política de privacidad de IureProject / IureProject privacy policy

*Última actualización / Last updated: 2026-11-17* · [Español](#español) · [English](#english)

## Español

IureProject es una aplicación de escritorio de gestión de proyectos publicada por Eduardo Llaguno
Velasco («nosotros»). Esta política explica qué datos maneja la aplicación (incluidas la línea de
comandos `iureproject-cli` y su servidor MCP).

**Resumen:** IureProject no tiene telemetría, analítica ni reportes automáticos de fallos, y no nos
envía tus planes ni tus datos. Lo que sale de tu equipo va a GitHub (solo para saber si hay una
versión nueva) o a la instancia de Iurefficient que tú elijas.

### Qué sale de tu equipo
1. **Aviso de versión nueva.** Al abrir la aplicación (si la opción está activa, que es lo
   predeterminado) o cuando lo pides, la app consulta `api.github.com` para conocer la última
   versión publicada. No envía datos tuyos; GitHub recibe, como en cualquier conexión, tu dirección
   IP y la versión de la app en el agente de usuario. Se desactiva en Archivo › Opciones › Actualizaciones. En la
   versión de la Microsoft Store y en el snap esta consulta no se hace (la tienda actualiza la app).
2. **Iurefficient (opcional).** Si inicias sesión en una instancia de Iurefficient, la app envía a
   *esa* instancia tu correo y contraseña (y el código de verificación en dos pasos, si lo usas) y,
   después, los datos que trabajes con ella: expedientes, tareas, recursos, horas, presupuesto,
   riesgos, comentarios, documentos y las preguntas que escribas en el chat del expediente. El chat
   lo responde el asistente de la instancia de Iurefficient (que puede usar inteligencia artificial
   generativa); la app no se conecta directamente con ningún proveedor de IA. El tratamiento de esos
   datos lo rige la política de privacidad de quien opera esa instancia (normalmente tu
   organización).
3. **Enlaces que abres.** «Reportar un problema», la guía de uso y los enlaces a documentos solo
   abren tu navegador; nada se envía hasta que tú lo hagas en esa página.

### Qué se guarda en tu equipo
- Tus planes (`.iurp` y otros formatos), donde tú los guardes.
- Preferencias y la lista de archivos recientes, en la carpeta de configuración de tu usuario.
- Una copia de recuperación del plan abierto mientras tiene cambios sin guardar (se borra al
  guardar o cerrar normalmente), y un registro de arranque con la versión, el sistema y la tarjeta
  de video, para diagnosticar fallos; nunca se envía solo.
- Si marcas «Recordar la sesión» de Iurefficient: las cookies de la sesión (no la contraseña) en el
  llavero del sistema (Credential Manager de Windows, Llavero de macOS o Secret Service en Linux), y
  el dominio y el correo de la cuenta activa. Cerrar sesión los borra.
- Archivos temporales de documentos descargados, notas e impresión, en la carpeta temporal.

### Servidor MCP
`iureproject-cli mcp` se comunica solo por su entrada y salida estándar con el programa que lo
inicia (por ejemplo, un asistente de IA); no abre puertos de red. Si hay una sesión de Iurefficient
recordada, ese programa puede usarla para consultar y guardar planes en tu instancia.

### Niños
IureProject es una herramienta de trabajo y no está dirigida a menores de 13 años.

### Tus opciones y contacto
Puedes usar IureProject sin cuenta y sin conexión, apagar el aviso de versión y cerrar la sesión de
Iurefficient en cualquier momento. Para preguntas sobre esta política, abre un *issue* en
<https://github.com/ellaguno/iureproject-releases/issues>. Si la política cambia, la nueva versión
se publica en esta misma página con su fecha.

## English

IureProject is a desktop project-management application published by Eduardo Llaguno Velasco
("we"). This policy explains what data the application handles (including the `iureproject-cli`
command line and its MCP server).

**Summary:** IureProject has no telemetry, analytics or automatic crash reporting, and it does not
send your plans or your data to us. What leaves your computer goes to GitHub (only to find out
whether a new version exists) or to the Iurefficient instance you choose.

### What leaves your computer
1. **New-version notice.** When the app starts (if the option is on, which is the default) or when
   you ask, it queries `api.github.com` for the latest published version. It sends no personal
   data; like any connection, GitHub sees your IP address and the app version in the user agent.
   Turn it off in File › Options › Updates. The Microsoft Store and snap versions do not make this check (the
   store updates the app).
2. **Iurefficient (optional).** If you sign in to an Iurefficient instance, the app sends *that*
   instance your email and password (and your two-step verification code, if you use one) and then
   the data you work on with it: cases, tasks, resources, hours, budget, risks, comments, documents
   and the questions you type in the case chat. The chat is answered by the Iurefficient instance's
   assistant (which may use generative AI); the app does not connect directly to any AI provider.
   That data is governed by the privacy policy of whoever operates the instance (usually your
   organization).
3. **Links you open.** "Report a problem", the user guide and document links only open your
   browser; nothing is sent until you do so on that page.

### What is stored on your computer
- Your plans (`.iurp` and other formats), wherever you save them.
- Preferences and the recent-files list, in your user configuration folder.
- A recovery copy of the open plan while it has unsaved changes (deleted on a normal save or exit),
  and a startup log with the app version, operating system and graphics adapter, for diagnosing
  crashes; it is never sent automatically.
- If you check "Remember the session" for Iurefficient: the session cookies (not your password) in
  the system keychain (Windows Credential Manager, macOS Keychain or Secret Service on Linux), plus
  the active account's domain and email. Signing out deletes them.
- Temporary files for downloaded documents, notes and printing, in the temporary folder.

### MCP server
`iureproject-cli mcp` talks only over standard input and output with the program that starts it
(for example, an AI assistant); it opens no network ports. If an Iurefficient session is
remembered, that program can use it to read and save plans on your instance.

### Children
IureProject is a work tool and is not directed at children under 13.

### Your choices and contact
You can use IureProject without an account and offline, turn off the new-version notice and sign
out of Iurefficient at any time. For questions about this policy, open an issue at
<https://github.com/ellaguno/iureproject-releases/issues>. If the policy changes, the new version
is published on this same page with its date.
