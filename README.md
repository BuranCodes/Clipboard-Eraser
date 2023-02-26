# Clipboard Eraser

A Python script that when running, automatically clears your clipboard or your last copied element after a keyboard paste.

## How to use

Make sure you have Python packages, pyperclip and keyboard installed. If not, try: `pip install pyperclip` and `pip install keyboard`.

Then you can clone this git repository to get the Python file and remove the rest.

If you want to run the script in terminal normally, do `python ClipboardEraser.py` on Windows or `python3 ClipboardEraser.py` on Linux and elsewhere.

To kill the running script, just do KeyboardInterrupt in the terminal where you ran the script normally. That can be done with `CRTL+C` or `Ctrl+\` on Mac.

Otherwise, you can run it in the background by doing `pythonw ClipboardEraser.py` in the terminal or rename `ClipboardEraser.py` to `ClipboardEraser.pyw` and then do same as above.

To kill the script running in the background in different OS:
- Windows: Task Manager, find the process that has the name `Python` and kill it. Or in terminal, do `taskkill /IM <executablename>`
- Linux: In terminal, do `ps -ef | grep python` and look for the Python process running. Then kill with `kill -9 <PID of Python process>`
- Mac: In terminal, do `ps a` and look for the Python process running. Then kill with `kill -9 <PID of Python process>`

## Regular use

If you intend to use the script regularly, here's how you can schedule the script in different platforms:

- Windows: Open Task Scheduler, then Create a Basic Task in the Action bar. Set trigger to everytime you log on, choose *start a program*. In the Finish part, you need a path to the program, python or pythonw. To find out where they are, you can go in CMD and do `where python` or `where pythonw`. Copy the first path, or make sure that the path has something like `\Local\Programs\Python\...`. For the arguments part, you need to write `ClipboardEraser.py`. Then for the "Start in", copy the path where the ClipboardEraser.py is. Now you're all set!
- Linux: Add **shebang** line in the Python script: `#!/usr/bin/env python3` at start. Set permissions of the file with `chmod +x ClipboardEraser.py` in the terminal, to allow execution. Then run the script with **nohup** to the path where the ClipboardEraser.py is located: `nohup /path/to/ClipboardEraser.py &`. If you want to kill the script running, find its process ID with `ps ax | grep ClipboardEraser.py`, then kill with `kill <PID of Python process>`.
