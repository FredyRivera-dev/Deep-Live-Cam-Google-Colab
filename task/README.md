# Run Deep-Live-Cam on Windows using Google Colab as GPU Provider

## Set up local machine

First, to run all of this (on your local machine), you need to have `uv, git, python, ffmpeg, and Visual Studio 2022 Build Tools (Windows)` installed.

If you don't have `ffmpeg` installed, run this command:
```bash
winget install ffmpeg
```

If you don't have `Visual Studio 2022 Build Tools (Windows)`:

Go to this link and [download the installer](https://visualstudio.microsoft.com/visual-cpp-build-tools/). When installing, make sure to select the "Desktop development with C++" option, and verify that these components are selected in the right panel:

- MSVC v143 - VS 2022 C++ x64/x86 build tools (or any version above v143)
- Windows 11 SDK (or Windows 10 SDK)
- C++ CMake tools for Windows

Click "Install while downloading". When the installation completes, it will prompt you to restart your computer. Do so, and everything should work correctly.

Clone the repository:
```bash
https://github.com/Thankgod20/Deep-Live-Cam-Google-Colab.git
cd Deep-Live-Cam-Google-Colab
```

If you don't have Python 3.10 installed (the recommended version), run the following command:

```bash
uv python install 3.10
```

Create your virtual environment:

```bash
uv venv --python 3.10
```

Start env:
```bash
.venv\Scripts\activate
```

Run this command before executing the requirements.txt installation because it will give an error indicating that it needs to be installed:
```bash
uv pip install tqdm==4.66.4
```

To install all the necessary dependencies, you can run this command:
```bash
uv pip install -r requirements.txt
```

To install all the necessary dependencies, you can run this command:
```bash
uv pip install -r requirements.txt
```

If you encounter errors with tensorflow, you can run these commands.
```bash
uv pip install --upgrade pip setuptools wheel
uv pip uninstall tensorflow 
uv pip install tensorflow==2.12.0
```

Run the GUI with this command: 
```bash
python run.py
```


## Set up Google Colab

Upload the `task/Deep_Live_Cam.ipynb` file to your Colab environment and start running it cell by cell, and everything should work.