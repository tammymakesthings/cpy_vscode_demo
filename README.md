# cpy_vscode_demo: CircuitPython/VSCode Tasks Demo

This demo project shows how I manage CircuitPython projects in Visual Studio
Code. The build tasks are defined in the `.vscode/tasks.json` file, which
may be hidden by default.

The following tasks are defined:

- Maintenance: run Black formatter on code.py file
- Maintenance: run pylint on code.py file
- CPY: Copy code.py to CircuitPython Device
- CPY: circup: Install libraries
- CPY: circup: update libraries
- CPY: discotool: Serial console

The "CPY: Copy code.py to CircuitPython Device" task is configured as the
default build task for the project.

## Important Notes

I've tried to make this demo simple and generic, but you'll have to edit the
`.vscode/tasks.json` file to (at a minimum) confirm the drive letter/mount
points for your CircuitPython device and the libraries you want the
"CPY: circup: Install libraries" task to install.

Also, I use [Poetry][poetry] to manage my Python environments. If you don't
use Poetry, you'll need to remove the appropriate references from the
`.vscode/tasks.json` file. You'll also have to make sure you install the
tools which the build tasks depend on manually:

- [discotool][discotool]
- [circup][circup]

[Poetry]:       https://python-poetry.org/
[discotool]:    https://pypi.org/project/discotool/
[circup]:       https://docs.circuitpython.org/projects/circup/en/latest/index.html
