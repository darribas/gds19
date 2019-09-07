# Software

---

| <CENTER>OS</CENTER>    | | <CENTER>Status</CENTER> |
| ------- | ----- | -----------------|
| Linux & macOS  | | [![Build Status](https://travis-ci.org/darribas/gds19.svg?branch=master)](https://travis-ci.org/darribas/gds19) |
| Windows |  | [![Build status](https://ci.appveyor.com/api/projects/status/k9cbbpt03goyo3hd?svg=true)](https://ci.appveyor.com/project/darribas/gds19) |

---

This course is best followed if you can reproduce the examples and tutorials provided with it. To do so, you will need to install in your machine a series of software packages. These are all open-source and available for free to download. 

There are two main pathways to install required Python libraries on your own machine. A minimalist one is less stable and will only provide Python resources, while a more comprehensive one will install not only a Python stack but also several useful R libraries.

## 1) A comprehensive approach: the GDS Docker container (recommended)

This is the recommended approach if you meet the following requirements:

1. You have admin rights over your machine
1. You are running either Windows 10 Pro, macOS, or Linux

In that case, [Docker](https://www.docker.com/) is the preferred alternative. It provides a stable platform to run complex software setups like that required in this context. Docker is a containerisation technology that allows to run pre-packaged (containerised) software under controlled environments. Relying on Docker, the [`gds_env`](https://github.com/darribas/gds_env) project provides a containerised platform for Geographic Data Science.

The steps to install this (given you meet the requirements above) include:

- Obtain a copy of Docker and install it:
    - `Windows10 Pro/Enterprise`: [Install Docker Desktop for Windows](https://docs.docker.com/docker-for-windows/install/)
    - `macOS`: [Get started with Docker Desktop for Mac](https://docs.docker.com/docker-for-mac/)
- Once Docker is successfully installed, make sure to enable access to your main drive (e.g. `C:\\`): 
    - `Windows10 Pro/Enterprise`: Open the preferences for Docker and click the
      "Shared Drives" tab; click on the drive you want to add and then "Apply"
    - `macOS`: this feature is automatically enabled
- Once you have Docker up and running, open up a (Docker) terminal:
    - `macOS`: Open `/Applications/Utilities/Terminal.app`
    - `Windows10 Pro/Enterprise`: Powershell

    Then, type on the terminal the following command and hit `Enter`:

    ```
    > docker pull darribas/gds:3.0
    ```

    This will take a while to download but, once finished, you will be all ready
    to go.
    
* Once the command above has finished installing your GDS stack, you are ready to go! To get a Jupyter session started, you can follow these steps:
    1. Run on the same terminal as above the following command:

        ```shell
        > docker run --rm -ti -p 8888:8888 -v ${PWD}:/home/jovyan/work darribas/gds:3.0
        ```

    This will start a Python session, please do not quite the window until you are
    done using Python! 

    2. Open your favorite browser (preferably Firefox or Chrome) and point it to
       `localhost:8888`
    3. You will be asked for a password or a token. To find the correct one, check
       the terminal where you started the `docker run ...` command in 1) and look
       for the long token in the logs. Your prompt should look something (albeit
       not exactly) like this:

       ```shell
        > docker run --rm -ti -p 8888:8888 -v ${PWD}:/home/jovyan/work darribas/gds:3.0
        Executing the command: jupyter notebook
        [I 11:38:40.234 NotebookApp] Writing notebook server cookie secret to /home/jovyan/.local/share/jupyter/runtime/notebook_cookie_secret
        [I 11:38:41.328 NotebookApp] Loading IPython parallel extension
        [I 11:38:41.612 NotebookApp] JupyterLab extension loaded from /opt/conda/lib/python3.7/site-packages/jupyterlab
        [I 11:38:41.612 NotebookApp] JupyterLab application directory is /opt/conda/share/jupyter/lab
        [I 11:38:43.091 NotebookApp] Serving notebooks from local directory: /home/jovyan
        [I 11:38:43.091 NotebookApp] The Jupyter Notebook is running at:
        [I 11:38:43.091 NotebookApp] http://ee20e7549b49:8888/?token=4dc814ee44c64383d5d32dfd439fe62bbc17d9803d9ae434
        [I 11:38:43.091 NotebookApp]  or http://127.0.0.1:8888/?token=4dc814ee44c64383d5d32dfd439fe62bbc17d9803d9ae434
        [I 11:38:43.091 NotebookApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
        [C 11:38:43.114 NotebookApp]

            To access the notebook, open this file in a browser:
                file:///home/jovyan/.local/share/jupyter/runtime/nbserver-6-open.html
            Or copy and paste one of these URLs:
                http://ee20e7549b49:8888/?token=4dc814ee44c64383d5d32dfd439fe62bbc17d9803d9ae434
             or http://127.0.0.1:8888/?token=4dc814ee44c64383d5d32dfd439fe62bbc17d9803d9ae434
       ```

       The token you want to copy is the long series of letter and numbers right
       after `?token=`, starting by `4dc814ee`.
    4. The token should let you into your Jupyter Lab session. Congratulations!
       You can then access the files in your computer through the `work` directory
       on the left-side pane.

## 2) A minimalist approach: `conda`

If you just want a more minimalist installation that *only* includes the barebones of what's needed in this context, and/or you are not running Windows 10 Pro, macOS or Linux, the recommended approach is to do a `conda` installation. This route will install natively a Python distribution with the libraries we will need. Please note that no interactive extensions or R packages are installed in this case, and also be aware the installation is less stable as it relies on the specific versions for your OS and latest releases (in most cases it should be fine, and this particular stack is regularly tested, but some failures nevertheless happen sometimes).

To install Python and required libraries through this approach, please follow these steps:

- Install [`miniconda`](https://docs.conda.io/en/latest/miniconda.html) for your OS version from the [official link](https://docs.conda.io/en/latest/miniconda.html). Make sure to install the Python 3 (e.g. 3.7) version, not Python 2.
- Once you have miniconda installed, we need to setup an independent environment that isolates all the functionality we need. Open up a terminal ("Anaconda Command Prompt" in Windows, "Applications --> Utilities --> Terminal" in macOS and  "ctr+alt+T" in Linux) and run the following commands:
    - Download the installer file from [here](https://raw.githubusercontent.com/darribas/gds19/master/content/infrastructure/install_gds_stack.yml) and place it in a folder you can access (e.g. Downloads)
    - Navigate to the folder where this file is (e.g. Downloads):

        ```
        cd /path/to/Downloads
        ```

    - Execute the following command (note you will need a good and stable internet connection and will take a while to complete):

        ```
        conda-env create -f install_gds_stack.yml
        ```

    - Once this has run, you should be able to activate the environment:

        ```
        conda activate gds
        ```
    - If you want to test the results, you can download [this file](https://github.com/darribas/gds19/raw/master/content/infrastructure/check_gds_stack.ipynb), place it in the same folder and run:
    
        ```
        jupyter nbconvert --execute --to html
        ```
        
        When this completes, it will create a `.html` file in the same folder that you can inspect. If no error messages are present, the installation was successful!
