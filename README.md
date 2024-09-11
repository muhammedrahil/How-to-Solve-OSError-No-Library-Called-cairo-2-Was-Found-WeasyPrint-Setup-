
# How to Solve OSError: No Library Called "cairo-2" Was Found (WeasyPrint Setup)

## Problem:
Encountering the error: `OSError: no library called "cairo-2" was found` while trying to use **WeasyPrint** in a Python project.

## Solution:

Follow these steps to resolve the issue:

1. **Create a virtual environment**  
   Run the following command to create a virtual environment:
   ```bash
   python -m venv env
   ```

2. **Activate the virtual environment**  
   On Windows:
   ```bash
   env\Scripts\activate
   ```
   On macOS/Linux:
   ```bash
   source env/bin/activate
   ```
3. **Install WeasyPrint**  
   Use pip to install WeasyPrint:
   ```bash
   pip install weasyprint
   ```
   You can check more about the installation and other details here:  
   [WeasyPrint on PyPI](https://pypi.org/project/weasyprint/)


5. **Set up the system environment variables**  
   After installation, add the GTK3 Runtime binary path to the system environment variables.  
   Example path:
   ```
   C:\Program Files\GTK3-Runtime Win64\bin
   ```
   To do this, follow these steps:
   - Right-click on 'This PC' or 'My Computer' and select 'Properties'.
   - Click 'Advanced system settings'.
   - Under the 'Advanced' tab, click on 'Environment Variables'.
   - Find the 'Path' variable, select it, and click 'Edit'.
   - Add the path to the GTK3 `bin` folder to the list.


4. **Download and install the GTK3 Runtime for Windows**  
   Download the latest version of the GTK3 Runtime for Windows from the following link:  
   [Download GTK3 Runtime](https://github.com/tschoonj/GTK-for-Windows-Runtime-Environment-Installer/releases)  
   Choose and install the latest version (e.g., `gtk3-runtime-3.24.31-2022-01-04-ts-win64.exe`).
