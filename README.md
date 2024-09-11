
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


4. **Download and install the GTK3 Runtime for Windows**  
   Download the latest version of the GTK3 Runtime for Windows from the following link:  
   [Download GTK3 Runtime](https://github.com/tschoonj/GTK-for-Windows-Runtime-Environment-Installer/releases)  
   Choose and install the latest version (e.g., `gtk3-runtime-3.24.31-2022-01-04-ts-win64.exe`).
