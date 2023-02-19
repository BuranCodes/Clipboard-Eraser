# Clipboard Eraser

A Python script that when running, automatically clears your clipboard or your last copied element after a paste.

## How to use

Make sure you have Python packages, pyperclip and keyboard installed. If not, try: `pip install pyperclip` and `pip install keyboard`.

Then you can clone this git repository to get the Python file and remove the rest.

If you want to run the script normally, do `python ClipboardEraser.py` on Windows or `python3 ClipboardEraser.py` on Linux and elsewhere.

To kill the running script, just do KeyboardInterrupt in the terminal where you ran the script normally. That can be done with `CRTL+C` or `Ctrl+\` on Mac.

Otherwise, you can run it in the background by doing `pythonw ClipboardEraser.py`

To kill the script running in the background in different OS:
- Windows: Task Manager, find the process that has the name `Python` and kill it. Or in terminal, do `taskkill /IM <executablename>`
- Linux: In terminal, do `ps -ef | grep python` and look for the Python process running. Then kill with `kill -9 <PID of Python process>`
- Mac: In terminal, do `ps a` and look for the Python process running. Then kill with `kill -9 <PID of Python process>`
