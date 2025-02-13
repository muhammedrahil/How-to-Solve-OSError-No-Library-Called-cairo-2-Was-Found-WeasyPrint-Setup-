
# How to Solve OSError: No Library Called "cairo-2" Was Found (WeasyPrint Setup)

## Problem:
Encountering the error: `OSError: no library called "cairo-2" was found` while trying to use **WeasyPrint** in a Python project.

![image](https://github.com/user-attachments/assets/df6954e4-75e6-40df-bc57-517b87101952)

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

6. **Restart your computer**  
   This is an **important step** to ensure all changes take effect.

7. **Test WeasyPrint**  
   Run the following command to test WeasyPrint:
   ```bash
   python -m weasyprint http://weasyprint.org weasyprint.pdf
   ```

8. **Run your project**  
   Now you can start your project:
   ```bash
   python manage.py runserver
   ```

## Additional Resources:
- [StackOverflow Solution](https://stackoverflow.com/questions/59481394/django-oserror-no-library-called-cairo-was-found-on-windows)
- [WeasyPrint Installation Guide](https://pypi.org/project/weasyprint/)
- [YouTube Installation Guide for WeasyPrint](https://www.youtube.com/watch?v=l58EK6zfCJQ)
