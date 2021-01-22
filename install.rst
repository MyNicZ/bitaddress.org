
Installing Electron Cash
========================

Installing on Linux
-------------------
To avoid dependency issues, you can use the Electron Cash "AppImage", a self-contained app bundle with everything you need already inside. Just download the AppImage file and set it as executable with "chmod +x <fileName>".

Alternatively, Linux users can run Electron Cash directly from the source code:

1. You will need Python version 3.4.0 or higher. Check your python version with ``python3 --version``.
#. Install the dependencies:

  - ``sudo apt-get install python3-setuptools``
  - ``sudo pip3 install PyQt5``

3. You should have already :doc:`downloaded and verified <verifydownload>` a gzipped tar of the source. The file will be named something like
   ``ElectronCash-3.1.2.tar.gz``.
#. Extract the files using ``tar -xvzf ElectronCash-3.1.2.tar.gz`` and ``cd`` into the directory.
#. Install using ``sudo python3 setup.py install``
#. You can now run Electron Cash using ``./electron-cash``

Some common issues are:

- ``No local packages or working download links found for pyqt5`` - you will need to install PyQt5 before installing Electron Cash. See step 2 above.
