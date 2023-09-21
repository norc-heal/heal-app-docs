# Running the Desktop Application Tool for Mac

For Mac users, there are currently two options for running the tool. You can:

1. Run the application locally (from source code)
2. Run the application locally (from an application file)

*Both require that you first follow the instructions in the 'Initial Set-Up' section below.*

### Running the application locally from source code vs. from application file:
    
If you choose to run the app locally (from source code), set-up is a bit easier and shorter as you cut out one layer of set-up. However, you must always use the command line to open the app if you choose this option. On the other hand, if you choose to run the app locally (from application file), set-up is a bit more involved as you will need to follow instructions to package the tool into an application file locally first. However, once you have done this, you will have the option to open the app either using the command line, or by using the GUI file explorer on your Mac to first navigate to the application file, then double click on the file to launch.

=== "Running the application locally<br>(from source code)"

    If you choose to run the app locally (from source code), once you have completed the steps in the ‘Initial Set-up’ section, you can just follow the instructions in the ‘Run the app locally (from source code)’ section below each time you want to run the app

=== "Running the application locally<br>(from application file)"

    If you choose to run the app locally (from an application file), once you have completed the steps in the ‘Initial Set-up’ section you will need to follow the instructions in the ‘Package app locally’ section below one time. Then you can just follow the instructions in the ‘Run the app locally (from application file)’ section below each time you want to run the app.

***

### Instructions

1. Initial Set-Up
    1. Check if you have python 3 installed; if not, install it (if installing from scratch, make sure you select the option to install pip at the same time).
    2. Check if you have pip installed; if not, install it.
    3. Download DSC Desktop Application Tool zipped source code directory from [here](https://github.com/norc-heal/heal-data-pkg-tool/releases/latest/).
        1. Expand "Assets" and click to download "Source code (zip)". *Note: Disregard the dsc-pkg-tool-mac.zip for now, as that is still in development.*
        1. Extract from zipped archive to a drive location that makes sense for you.
    4. Open terminal.
        1. Navigate to the extracted DSC Desktop Application Tool directory
            1.	The extracted dir name will start with ‘heal-dsc-gui-dev-‘
            2.	Within this directory is a single directory that also starts with ‘heal-dsc-gui-dev’
            3.	Navigate into this second layer
            4.	Within this directory will be many files
        2.	Make sure the following files exist in this directory
            1.	Requirements.txt
            2.	Dsc_pkg_tool.py
        3. Create a new python virtual environment (name it something unique, memorable and relevant – e.g. dsc-pkg-env) and activate your new virtual environment
        4. Install required packages into python virtual environment from the requirements.txt file: ‘pip install -r requirements.txt’ 

#### If running the application locally from source code:

2.	Run app locally (from source code)
    1. Navigate to the DSC Desktop Application Tool directory (dir with requirements.txt and dsc_pkg_tool.py files)
    2. Activate the python virtual environment you created during initial set-up steps above
    3. Run the app from the command line: ‘python3 dsc_pkg_tool.py’
    4. This should launch a multi-tab GUI; 
        1. If it does this – Success! 
        2. If it does not do this – Please contact us and we will help you to troubleshoot
3.	Package app locally
    1. Navigate to the DSC Desktop Application Tool directory (dir with requirements.txt and dsc_pkg_tool.py files)
    2. Activate the python virtual environment you created during initial set-up steps above
    3. Package the app into an executable from the command line: ‘pyinstaller --icon=heal-icon.ico --add-data="heal-icon.ico:." --collect-all pipe --hidden-import pipe --hidden-import pyreadstat._readstat_writer --hidden-import pyreadstat.worker --paths=. --debug=all dsc_pkg_tool.py’
    4. This should create a subdirectory within the DSC Desktop Application Tool directory called ‘dist’, 
        1. Within the ‘dist’ directory will be a subdirectory called ‘dsc_pkg_tool’
        2. Within the ‘dsc_pkg_tool’ directory will be an application file called ‘dsc_pkg_tool.app’
        3. This is your application file – HOWEVER, don’t move this application file; it will only work in the context of the larger dsc_pkg_tool directory 


#### If running the application locally from application file:

1. Run app locally (from application file)
    1. From command line
        1. Use command line to navigate to application file parent directory (dist/dsc_pkg_tool directory)
        2. Use command line to open application: ‘open dsc_pkg_tool.app’
    2. From GUI file explorer
        1. Use GUI file explorer to navigate to application file (dsc_pkg_tool.app)
        2. Double click on file to open
