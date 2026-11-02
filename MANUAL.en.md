# IureProject: user guide

*[Versión en español](MANUAL.md)*

IureProject plans projects like Microsoft Project (Gantt, resources, costs, tracking, baselines)
and works with Iurefficient. It opens and saves MS Project plans, so you can share them with people
who use it.

## Install
- **Linux:** the `.deb` (Ubuntu, Debian and derivatives) or the `.rpm` (Fedora, openSUSE…) installs
  it with its menu icon. The `.tar.gz` works on any distribution: unpack it and open `iureproject`.
- **Windows 10/11:** unzip the `.zip` and open `iureproject.exe`. If Windows warns you (the app is
  not signed yet): «More info» › «Run anyway».
- **macOS 11 or later:** unzip the `.zip` and drag `IureProject.app` to Applications. The first
  time: right-click › «Open» › «Open».

Downloads and release notes: <https://github.com/ellaguno/iureproject-releases/releases>.

## Getting started
1. **File › New:** a blank plan, the sample or a template (also your firm's templates in
   Iurefficient).
2. **Type the tasks** in the sheet: name and duration («3d», «4h», «2w»…). Insert adds a task;
   Delete removes it.
3. **Outline:** Alt+Shift+→ indents (the task goes under the one above, which becomes a summary);
   Alt+Shift+← outdents.
4. **Links:** select two or more tasks and Ctrl+F2 chains them (finish to start). In the
   Predecessors column you can type types and lags: `3SS+1d`, `5FF`, `2FS-50%`.
5. **Resources:** in Resource › Resource Sheet add people (hourly rate), materials or costs; in the
   task's «Resource Names» column type `Ana` or `Ana[50%];Luis`.
6. **Dates:** IureProject computes start and finish from links and calendars. Typing a date sets a
   constraint, as in MS Project.
7. **Save:** Ctrl+S saves as `.iurp` (the native format, with everything). For MS Project, File ›
   Save As › MS Project XML.

## Tracking
- **Baseline:** Project › Set Baseline keeps the approved plan to compare against.
- **Progress:** 0 %, 25 %, 50 %, 75 % or 100 % in the ribbon, or «Update Tasks» with actual dates
  and duration.
- **Status date** and **Update Project** (Project tab): marks what was scheduled up to a date as
  done.
- **Reports** (Report tab): costs, work, resources and earned value; on screen, as PDF or printed.

## Views
In the View tab: Gantt Chart, Tracking Gantt, Task Usage, Resource Usage, Resource Sheet, Resource
Graph, Network Diagram, Calendar, Team Planner, Board (Kanban) and Sprints. Ctrl+F1 folds the
ribbon for more room.

## Microsoft Project files
- **Open:** `.mpp` and `.mpt` templates (MS Project 2010 and later), MS Project XML (`.xml`) and
  MPX. A template opens as a new, unnamed plan.
- **Save for MS Project:** as MS Project XML; MS Project opens it with tasks, links, resources,
  calendars, baselines and progress. (Saving as `.mpp` is not available yet.)
- **Export:** PDF, Excel, CSV (Iurefficient's), `.ics` calendar and a Gantt image.

## Iurefficient
- **File › Iurefficient:** sign in with your firm's account, open a case's plan and save it back
  (tasks, dates and statuses stay in Iurefficient).
- The **case documents** are one click away in the status bar.
- **Firm templates:** File › New lists them; «Save as template in Iurefficient» adds or replaces
  one.

## Find and do anything
The top bar has the **command and task search** (Ctrl+K): type «baseline», «link», a task or
resource name, pick with the arrows and Enter.

## Keyboard shortcuts
| Keys | What it does |
|---|---|
| Ctrl+K | Search commands and tasks |
| Ctrl+S, Ctrl+O, Ctrl+P | Save, open, print |
| Ctrl+Z, Ctrl+Y | Undo, redo |
| Ctrl+C, Ctrl+X, Ctrl+V | Copy, cut and paste tasks |
| Ctrl+F, Ctrl+H | Find a task, replace |
| Insert, Delete | Insert, delete a task |
| Alt+Shift+→ / ← | Indent or outdent |
| Alt+Shift++ / − | Expand or collapse summaries |
| Ctrl+F2 | Link the selected tasks |
| Shift+F2 | Task information |
| F9 | Calculate the project |
| Ctrl+F1 | Fold or show the ribbon |
| Arrows, Home, End, F2, Enter | Move and edit in the sheet and the usage views |
| Alt+← / →, Alt+Home / End | Scroll the Gantt; go to the project start or finish |
| Ctrl+Shift+F5 | Go to the selected task's bar |
| Ctrl+← / → (Board) | Move the card to the previous or next status |
| Ctrl+↑ / ↓ (Team Planner) | Reassign the task to the resource above or below |
| Page Up / Page Down (Calendar) | Previous or next month |

Everything works with the keyboard and with a screen reader.

## Settings
File › Options: theme (light, dark, high contrast or the system's), density, interface size,
language, font, and the system title bar instead of the integrated one.

## AI assistants (MCP)
`iureproject-cli mcp plan.iurp` offers the plan to Claude Desktop, Claude Code or another MCP
client: it can read it, change it with the same commands and save it. In Claude Desktop (Settings ›
Developer › Edit Config):

```json
{
  "mcpServers": {
    "iureproject": { "command": "iureproject-cli", "args": ["mcp", "/path/plan.iurp"] }
  }
}
```

On Windows, use the full path to `iureproject-cli.exe` with double backslashes
(`"C:\\Programs\\IureProject\\iureproject-cli.exe"`); on macOS, the `iureproject-cli` that
comes next to `IureProject.app`. In Claude Code: `claude mcp add iureproject -- iureproject-cli mcp
/path/plan.iurp`.

## If something goes wrong
File › Info › **Report a problem…** opens a report with the version and system already filled in
(nothing from your plan is sent). If a session closed without saving, IureProject offers to
recover the automatic copy when you open it again.
