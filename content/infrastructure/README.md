# Software

---

| <CENTER>OS</CENTER>    | | <CENTER>Status</CENTER> |
| ------- | ----- | -----------------|
| Linux & macOS  | | [![Build Status](https://travis-ci.org/darribas/gds19.svg?branch=master)](https://travis-ci.org/darribas/gds19) |
| Windows |  | [![Build status](https://ci.appveyor.com/api/projects/status/k9cbbpt03goyo3hd?svg=true)](https://ci.appveyor.com/project/darribas/gds19) |

---

This course is best followed if you can reproduce the examples and tutorials provided with it. To do so, you will need to install in your machine a series of software packages. These are all open-source and available for free to download. 

**NOTE-1** There are several ways to install software requirements for this course in your machine. I only support the one described below but, if you know what you're doing, you may find alternatives that suit your setup better.

**NOTE-2** Before proceeding, make sure you have a good internet connection and at least about 10GB of space in your hardrive free.

## Main Requirement: Docker

The recommended way to install Python for this course is through a software
package called [`Docker`](https://www.docker.com/). You will need a recent
version of Docker installed and working on your computer to be able to install
everything else. Here are a couple of links to guides for installing Docker
under different platforms:

- `Windows10 Pro/Enterprise`: [Install Docker Desktop for Windows](https://docs.docker.com/docker-for-windows/install/)
- `Other Windows`: [Docker Toolbox](https://docs.docker.com/toolbox/overview/)
- `macOS`: [Get started with Docker Desktop for Mac](https://docs.docker.com/docker-for-mac/)

**IMPORTANT**: Installing Docker requires administrative rights on the
computer you will install it.

Once Docker is successfully installed, make sure to enable access to your main
drive (e.g. `C:\\`): 

- `Windows10 Pro/Enterprise`: Open the preferences for Docker and click the
  "Shared Drives" tab; click on the drive you want to add and then "Apply"
- `Other Windows`: this feature should be automatically enabled
- `macOS`: this feature is automatically enabled

## Installation

Once you have Docker up and running, open up a (Docker) terminal:

- `macOS`: Open `/Applications/Utilities/Terminal.app`
- `Windows10 Pro/Enterprise`: Powershell
- `Other Windows`: Docker terminal (open through "Docker QuickStart" app)

Then, type on the terminal the following command and hit `Enter`:

```
> docker pull darribas/gds:3.0
```

This will take a while to download but, once finished, you will be all ready
to go.

## Launch

Once the command above has finished installing your GDS stack, you are ready
to go! To get a Jupyter session started, you can follow these steps:

1. Run on the same terminal as above the following command:

    ```
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

   ```
    (base) dh073236:gds19 dani$ docker run --rm -ti -p 8888:8888 -v ${PWD}:/home/jovyan/work darribas/gds:3.0
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
