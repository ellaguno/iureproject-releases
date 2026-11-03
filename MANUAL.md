# IureProject: guía de uso

*[English version](MANUAL.en.md)*

IureProject planea proyectos como Microsoft Project (Gantt, recursos, costos, seguimiento, líneas
base) y se integra con Iurefficient. Abre y guarda los planes de MS Project, así que puedes
compartirlos con quien lo use.

## Instalar
- **Linux:** el `.deb` (Ubuntu, Debian y derivadas) o el `.rpm` (Fedora, openSUSE…) lo instala con
  su icono en el menú. El `.tar.gz` sirve en cualquier distribución: descomprímelo y abre
  `iureproject`.
- **Windows 10/11:** abre el instalador `.msi` y acepta el aviso de administrador: queda en el
  menú Inicio y en el escritorio, los archivos `.iurp` se abren con IureProject y `iureproject-cli` queda en el
  `PATH`. Se desinstala desde Configuración › Aplicaciones. Para usarlo sin instalar, descomprime
  el `.zip` y abre `iureproject.exe`. Si Windows avisa (la app aún no está firmada): «Más
  información» › «Ejecutar de todas formas».
- **macOS 11 o posterior:** abre el `.dmg` y arrastra `IureProject.app` a Aplicaciones (o
  descomprime el `.zip`). La primera vez: clic derecho › «Abrir» › «Abrir».

Descargas y notas de cada versión: <https://github.com/ellaguno/iureproject-releases/releases>.

## Primeros pasos
1. **Archivo › Nuevo:** un plan en blanco, el de ejemplo o una plantilla (también las de tu
   despacho en Iurefficient).
2. **Escribe las tareas** en la hoja: nombre, duración («3d», «4h», «2s»…). Insert agrega una
   tarea; Supr la elimina.
3. **Esquema:** Alt+Mayús+→ aplica sangría (la tarea queda dentro de la de arriba, que se vuelve
   resumen); Alt+Mayús+← la quita.
4. **Vínculos:** selecciona dos o más tareas y Ctrl+F2 las encadena (fin a comienzo). En la columna
   Predecesoras puedes escribir tipos y posposiciones: `3CC+1d`, `5FF`, `2FC-50%`.
5. **Recursos:** en Recurso › Hoja de recursos agrega personas (tasa por hora), materiales o
   costos; en la columna «Nombres de los recursos» de la tarea escribe `Ana` o `Ana[50%];Luis`.
6. **Fechas:** IureProject calcula comienzo y fin con los vínculos y los calendarios. Escribir una
   fecha a mano pone una restricción, como en MS Project.
7. **Guardar:** Ctrl+S guarda en `.iurp` (el formato propio, con todo). Para MS Project, Archivo ›
   Guardar como › MS Project XML.

## Seguimiento
- **Línea base:** Proyecto › Establecer línea base guarda el plan aprobado para compararlo.
- **Avance:** en la cinta, 0 %, 25 %, 50 %, 75 % o 100 %; o «Actualizar tareas» con fechas y
  duración reales.
- **Fecha de estado** y **Actualizar proyecto** (pestaña Proyecto): da por hecho lo programado hasta
  una fecha.
- **Informes** (pestaña Informe): costos, trabajo, recursos y valor acumulado; en pantalla, PDF o
  impresos.

## Vistas
En la pestaña Vista: Diagrama de Gantt, Gantt de seguimiento, Uso de tareas, Uso de recursos,
Hoja de recursos, Gráfico de recursos, Diagrama de red, Calendario, Planificador de equipo,
Tablero (Kanban) y Sprints. Ctrl+F1 pliega la cinta para tener más espacio.

## Archivos de Microsoft Project
- **Abrir:** `.mpp` y plantillas `.mpt` (de MS Project 2010 en adelante), MS Project XML (`.xml`) y
  MPX. Una plantilla se abre como plan nuevo sin nombre.
- **Guardar para MS Project:** como MS Project XML; MS Project lo abre con tareas, vínculos,
  recursos, calendarios, líneas base y avance. (Guardar como `.mpp` todavía no está disponible.)
- **Exportar:** PDF, Excel, CSV (el de Iurefficient), agenda `.ics` e imagen del Gantt.

## Iurefficient
- **Archivo › Iurefficient:** inicia sesión con tu cuenta del despacho, abre el plan de un
  expediente y guárdalo de vuelta (las tareas, fechas y estados quedan en Iurefficient).
- Los **documentos del expediente** están a un clic en la barra de estado.
- **Plantillas del despacho:** Archivo › Nuevo las lista; «Guardar como plantilla en Iurefficient»
  agrega o reemplaza una.

## Buscar y hacer cualquier cosa
La barra superior tiene la **búsqueda de comandos y tareas** (Ctrl+K): escribe «línea base»,
«vincular», el nombre de una tarea o de un recurso, elige con las flechas y Enter.

## Atajos de teclado
| Teclas | Qué hace |
|---|---|
| Ctrl+K | Buscar comandos y tareas |
| Ctrl+S, Ctrl+O, Ctrl+P | Guardar, abrir, imprimir |
| Ctrl+Z, Ctrl+Y | Deshacer, rehacer |
| Ctrl+C, Ctrl+X, Ctrl+V | Copiar, cortar y pegar tareas |
| Ctrl+F, Ctrl+H | Buscar tarea, reemplazar |
| Insert, Supr | Insertar, eliminar tarea |
| Alt+Mayús+→ / ← | Aplicar o quitar sangría |
| Alt+Mayús++ / − | Expandir o contraer resúmenes |
| Ctrl+F2 | Vincular las tareas seleccionadas |
| Mayús+F2 | Información de la tarea |
| F9 | Calcular el proyecto |
| Ctrl+F1 | Plegar o mostrar la cinta |
| Flechas, Inicio, Fin, F2, Intro | Moverse y editar en la hoja y en las vistas de uso |
| Alt+← / →, Alt+Inicio / Fin | Desplazar el Gantt; ir al comienzo o al fin del proyecto |
| Ctrl+Mayús+F5 | Ir a la barra de la tarea seleccionada |
| Ctrl+← / → (Tablero) | Pasar la tarjeta al estado anterior o siguiente |
| Ctrl+↑ / ↓ (Planificador) | Reasignar la tarea al recurso de arriba o de abajo |
| Re Pág / Av Pág (Calendario) | Mes anterior o siguiente |

Todo se puede usar con el teclado y con un lector de pantalla.

## Ajustes
Archivo › Opciones: tema (claro, oscuro, alto contraste o el del sistema), densidad, tamaño de la
interfaz, idioma, fuente y la barra de título del sistema en lugar de la integrada.

## Asistentes de IA (MCP)
`iureproject-cli mcp plan.iurp` ofrece el plan a Claude Desktop, Claude Code u otro cliente MCP:
puede leerlo, cambiarlo con los mismos comandos y guardarlo. En Claude Desktop (Ajustes ›
Desarrollador › Editar configuración):

```json
{
  "mcpServers": {
    "iureproject": { "command": "iureproject-cli", "args": ["mcp", "/ruta/plan.iurp"] }
  }
}
```

En Windows, la ruta completa a `iureproject-cli.exe` con barras dobles (con el instalador `.msi`,
`"C:\\Program Files\\IureProject\\iureproject-cli.exe"`); en macOS, la de `iureproject-cli`, que
viene junto a `IureProject.app`. En Claude Code: `claude mcp add iureproject -- iureproject-cli mcp
/ruta/plan.iurp`.

## Si algo falla
Archivo › Información › **Reportar un problema…** abre un reporte con la versión y el sistema ya
escritos (no envía nada de tu plan). Adjunta el **registro de arranque**, que dice qué tarjeta
gráfica se usó y si hubo errores: `%LOCALAPPDATA%\iureproject\arranque.log` en Windows,
`~/.local/share/iureproject/arranque.log` en Linux y
`~/Library/Application Support/iureproject/arranque.log` en macOS.

Si la ventana se abre **en blanco**, es la tarjeta gráfica (pasa en máquinas virtuales): ábrela
eligiendo otro motor de gráficos, p. ej. en PowerShell `$env:WGPU_BACKEND="dx12"; .\iureproject.exe`
(o `vulkan`, `gl`). En Windows ya se usa DirectX 12 por omisión. Si una sesión se cerró sin guardar, al volver a abrir
IureProject ofrece recuperar la copia automática.
