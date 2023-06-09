P(ortable) V(irtual)env
=======================

This is Portable conda virtualenv. Just 1. download, 2. unarchive, 3. activate and 4. GO!

* = Works purely in userspace in the dir with just RW access. (No extra admin rights needed.) =
* = Isolated into its directory only. (In install time, not runtime.) =
* = Mutiplatform. (Build on the shoulder of the TITANS - anaconda.com.) =
* = Portable - you can just copy it to next place OR user. * (Until installed non-portable software.) =

/* Non-portable libraries hardcode the PATH where they are, thus making PVenv no more portable, despite works where installed. Read more here.

How to basic use
================

Linux AMD64 (+ docker)
----------------------

(Requires `$ apt install -y wget ca-certificates xz-utils`.)

`
# in the directory you want
# download & unarchive
wget -qO- https://.../venv3.10_lin_amd64.tar.xz | tar xvJf -
# activate
. venv3.10/bin/activate
# ... and go, go, go!
python -m pip install -U pip setuptools
python -m pip install -U matplotlib
python -c "import matplotlib.pyplot as plt; plt.plot(range(10), range(10,0,-1)); plt.show()"
`

Linux ARM64 (+ docker in ARM MacOS)
-----------------------------------

(Requires ```$ apt install -y wget ca-certificates xz-utils```.)

```bash
# in the directory you want
# download & unarchive
wget -qO- https://.../venv3.10_lin_arm64.tar.xz | tar xvJf -
# activate
. venv3.10/bin/activate
# ... and go, go, go!
python -m pip install -U pip setuptools
python -m pip install -U matplotlib
python -c "import matplotlib.pyplot as plt; plt.plot(range(10), range(10,0,-1)); plt.show()"
```

Windows AMD64 powershell (+ docker Win containers)
--------------------------------------------------

(Works for Win8+. You can use even .tar.xz archive instead of self-extracting .exe archive.)

```bash
# in the directory you want
# download
Invoke-WebRequest "https://.../venv3.10_win_amd64.exe" -outfile venv.exe
# unarchive
& .\venv.exe -y -o.
# activate
. venv3.10/bin/activate
# ... and go, go, go!
python -m pip install -U pip setuptools
python -m pip install -U matplotlib
python -c "import matplotlib.pyplot as plt; plt.plot(range(10), range(10,0,-1)); plt.show()"
```

Windows AMD64 cmd (+ docker Win containers)
-------------------------------------------

(Works for Win8+. You can use even .tar.xz archive instead of self-extracting .exe archive.)

```bash
# in the directory you want
# download & unarchive
wget -qO- https://.../venv3.10_win_amd64.tar.xz | tar xvJf -
# activate
venv3.10/bin/activate.bat
# ... and go, go, go!
python -m pip install -U pip setuptools
python -m pip install -U matplotlib
python -c "import matplotlib.pyplot as plt; plt.plot(range(10), range(10,0,-1)); plt.show()"
```

MacOS AMD64
-----------

(Requires just core OS. Maybe check GateKeeper permissions.)

```bash
# in the directory you want
# download & unarchive
curl https://.../venv3.10_mac_amd64.tar.xz | tar xvJf -
# activate
. venv3.10/bin/activate
# ... and go, go, go!
python -m pip install -U pip setuptools
python -m pip install -U matplotlib
python -c "import matplotlib.pyplot as plt; plt.plot(range(10), range(10,0,-1)); plt.show()"
```

MacOS ARM64
-----------

(Requires just core OS. Maybe check GateKeeper permissions.)

```bash
# in the directory you want
# download & unarchive
curl https://.../venv3.10_mac_arm64.tar.xz | tar xvJf -
# activate
. venv3.10/bin/activate
# ... and go, go, go!
python -m pip install -U pip setuptools
python -m pip install -U matplotlib
python -c "import matplotlib.pyplot as plt; plt.plot(range(10), range(10,0,-1)); plt.show()"
```

Try something more advanced
===========================

You can install any package / software (even non-pythonic) in conda.
Check official anaconda (https://anaconda.org/anaconda) OR conda-forge 
(https://anaconda.org/conda-forge) repositories.

Add ruby
--------

```bash
# once in working & activated env
python -m conda install ruby
# we do have ruby now ;-)
ruby -e "print('Hi')"
```

Add QGis
--------

```bash
# once in working & activated env
python -m conda install qgis -c conda-forge
# run qgis
qgis
```

Credits
=======

This is just (mini)conda (https://docs.conda.io/en/latest/miniconda.html) environment made relative-path based. It can be still improved, so write an issue if something spotted, pls. I appreciate it.
