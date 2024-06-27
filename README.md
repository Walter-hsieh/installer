# installer

To use PyInstaller to create an executable for your `smart_pdf_renamer.py` script, follow these steps:

1. **Install PyInstaller**: If you haven't installed PyInstaller, you can do so using pip:
    
    ```
    pip install pyinstaller
    
    ```
    
2. **Prepare Your Script**: Ensure your script is working correctly and all dependencies are installed.
3. **Create the Executable**: Run PyInstaller with your script. You can do this from the command line:
    
    ```
    pyinstaller --onefile smart_pdf_renamer.py
    
    ```
    
    The `--onefile` flag bundles everything into a single executable file. Without this flag, PyInstaller will create a folder with dependencies and the executable.
    
4. **Check the Output**: PyInstaller will create a `dist` directory containing your executable. Navigate to this directory to find your `smart_pdf_renamer` executable.

Here are the steps in detail:

### Step-by-Step Guide

1. **Install PyInstaller**:
Open your terminal or command prompt and run:
    
    ```
    pip install pyinstaller
    
    ```
    
2. **Prepare Your Script**:
Make sure all necessary libraries used in your script (`tkinter`, `langchain_google_genai`, `langchain_community.document_loaders`, etc.) are installed in your environment. You can install these libraries using pip:
    
    ```
    pip install <library_name>
    
    ```
    
3. **Run PyInstaller**:
Open your terminal or command prompt in the directory where `smart_pdf_renamer.py` is located and run:
    
    ```
    pyinstaller --onefile smart_pdf_renamer.py
    
    ```
    
    This command tells PyInstaller to bundle everything into a single executable file. The process will create several directories and files, including a `dist` directory where the final executable will be placed.
    
4. **Check the Output**:
After the process completes, navigate to the `dist` directory:
    
    ```
    cd dist
    
    ```
    
    You should see the executable file named `smart_pdf_renamer` (or `smart_pdf_renamer.exe` on Windows).
    

### Additional Options

- **Include Data Files**: If your script requires additional data files, you can include them using the `-add-data` option:
    
    ```
    pyinstaller --onefile --add-data "path/to/datafile;destination/folder" smart_pdf_renamer.py
    
    ```
    
- **Specify Icon**: You can also specify an icon for your executable using the `-icon` option:
    
    ```
    pyinstaller --onefile --icon=path/to/icon.ico smart_pdf_renamer.py
    
    ```
    
- **Hidden Imports**: If PyInstaller misses some imports, you can specify them with the `-hidden-import` option:
    
    ```
    pyinstaller --onefile --hidden-import=<module_name> smart_pdf_renamer.py
    
    ```
    

### Example Command

Here’s an example command combining some of these options:

```
pyinstaller --onefile --icon=myicon.ico --add-data "config.yaml;." smart_pdf_renamer.py

```

This command creates a single executable with an icon and includes a `config.yaml` file in the same directory as the executable.

By following these steps, you should be able to create a standalone executable for your `smart_pdf_renamer.py` script using PyInstaller.
