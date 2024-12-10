# LabelImg

[![PyPI Version](https://img.shields.io/pypi/v/labelimg.svg)](https://pypi.python.org/pypi/labelimg)
[![GitHub Workflow Status](https://img.shields.io/github/workflow/status/tzutalin/labelImg/Package?style=for-the-badge)](https://github.com/tzutalin/labelImg)
[![Language English](https://img.shields.io/badge/lang-en-blue.svg)](https://github.com/tzutalin/labelImg)
[![Language Chinese](https://img.shields.io/badge/lang-zh-green.svg)](https://github.com/tzutalin/labelImg/blob/master/readme/README.zh.rst)
[![Language Japanese](https://img.shields.io/badge/lang-jp-green.svg)](https://github.com/tzutalin/labelImg/blob/master/readme/README.jp.rst)

LabelImg is an image annotation tool written in Python and QT.

Supported annotation formats include PASCAL VOC format, YOLO, and createML.

![Demo Image](https://raw.githubusercontent.com/tzutalin/labelImg/master/demo/demo3.jpg)
![Demo Image](https://raw.githubusercontent.com/tzutalin/labelImg/master/demo/demo.jpg)

[Demo Video](https://youtu.be/p0nR2YsCY_U)

---

## Installation

### Install from Source Code

#### Linux/Ubuntu/Mac

Requires Python and [PyQt5](https://pypi.org/project/PyQt5/).

##### Ubuntu Linux

```bash
sudo apt-get install pyqt5-dev-tools
sudo pip3 install -r requirements/requirements-linux-python3.txt
make qt5py3
python3 labelImg.py
python3 labelImg.py [IMAGE_PATH] [PRE-DEFINED CLASS FILE]

### macOS
----------

brew install qt  # Install qt-5.x.x via Homebrew
brew install libxml2

# Or use pip
pip3 install pyqt5 lxml

make qt5py3
python3 labelImg.py
python3 labelImg.py [IMAGE_PATH] [PRE-DEFINED CLASS FILE]
---------------
Python 3 Virtualenv (Recommended)
-----------------------------------
brew install python3
pip3 install pipenv
pipenv run pip install pyqt5==5.15.2 lxml
pipenv run make qt5py3
pipenv run python3 labelImg.py
# [Optional]
rm -rf build dist
python setup.py py2app -A
mv "dist/labelImg.app" /Applications
------------------------------------

Windows
Install Python, PyQt5, and lxml.

Navigate to the labelImg directory and run:
pyrcc4 -o libs/resources.py resources.qrc
# For pyqt5
pyrcc5 -o libs/resources.py resources.qrc

python labelImg.py
python labelImg.py [IMAGE_PATH] [PRE-DEFINED CLASS FILE]
---------------------------------------------------------
Windows + Anaconda
Download and install Anaconda (Python 3+).

Open Anaconda Prompt, navigate to the labelImg directory, and run:
conda install pyqt=5
conda install -c anaconda lxml
pyrcc5 -o libs/resources.py resources.qrc
python labelImg.py
python labelImg.py [IMAGE_PATH] [PRE-DEFINED CLASS FILE]
---------------------------------------------------------
Install from PyPI
Requires Python 3.0 or above.
pip3 install labelImg
labelImg
labelImg [IMAGE_PATH] [PRE-DEFINED CLASS FILE]

-------------------------
Use Docker
docker run -it \
--user $(id -u) \
-e DISPLAY=unix$DISPLAY \
--workdir=$(pwd) \
--volume="/home/$USER:/home/$USER" \
--volume="/etc/group:/etc/group:ro" \
--volume="/etc/passwd:/etc/passwd:ro" \
--volume="/etc/shadow:/etc/shadow:ro" \
--volume="/etc/sudoers.d:/etc/sudoers.d:ro" \
-v /tmp/.X11-unix:/tmp/.X11-unix \
tzutalin/py2qt4

make qt4py2
./labelImg.py
---------------------------------------
## Usage

### Generate Labels

To define the labels for annotation, edit the file `data/predefined_classes.txt`.  
This file contains the list of predefined classes you will use for labeling images. Each line in the file represents one class.

For example:

```txt
dog
cat
car
person
---------------------------------------
## Keyboard Shortcuts

Here is a list of keyboard shortcuts to speed up the annotation process:

| Shortcut           | Action                                    |
|--------------------|------------------------------------------|
| `Ctrl + U`         | Load all images from a directory         |
| `Ctrl + R`         | Change the output directory for annotations |
| `Ctrl + S`         | Save the annotation                      |
| `Ctrl + D`         | Duplicate the current label and bounding box |
| `Ctrl + Shift + D` | Delete the current image                 |
| `Space`            | Mark the current image as verified       |
| `W`                | Create a new bounding box               |
| `D`                | Move to the next image                  |
| `A`                | Move to the previous image              |
| `Delete`           | Delete the selected bounding box        |
| `Ctrl + +`         | Zoom in on the image                    |
| `Ctrl + -`         | Zoom out of the image                   |
| `↑` `→` `↓` `←`    | Move the selected bounding box          |
-----------------------------------------------------------------

Contribution
Contributions are welcome! Feel free to submit code directly.


This version is fully translated into English and formatted as Markdown. Let me know if you need further adjustments!




