========
Сборка проекта используя Sphinx-doc
========

Linux
-----

Debian/Ubuntu
~~~~~~~~~~~~~

Установите пакет ``python3-sphinx`` используя apt-get:

::

   $ apt-get install python3-sphinx

Если python не был до этого установлен, команда установит Python на компьютер.

RHEL, CentOS
~~~~~~~~~~~~

Установите пакет ``python-sphinx`` используя yum:

::

   $ yum install python-sphinx

Если python не был до этого установлен, команда установит Python на компьютер.

Другие дистрибутивы
~~~~~~~~~~~~~~~~~~~

Большинство дистрибутивов Linux имеют Sphinx в своих репозиториях пакетов. Обычно пакет называется ``python3-sphinx``, ``python-sphinx`` или ``sphinx``.


macOS
-----

Sphinx обычно устанавливают используя `Homebrew`__, `MacPorts`__, или через pip, используя пакет поставки `Anaconda`__.

__ https://brew.sh/
__ https://www.macports.org/
__ https://www.anaconda.com/download/#macos

Homebrew
~~~~~~~~

::

   $ brew install sphinx-doc

Для получения дополнительной информации: `package overview`__.

__ https://formulae.brew.sh/formula/sphinx-doc

MacPorts
~~~~~~~~

Установите пакет ``python3x-sphinx`` используя `port`:

::

   $ sudo port install py38-sphinx

Установите пути до исполняемых файлов, используя комманду ``port select``:

::

   $ sudo port select --set python python38
   $ sudo port select --set sphinx py38-sphinx

Для получения дополнительной информации: `package overview`__.

__ https://www.macports.org/ports.php?by=library&substr=py38-sphinx

Anaconda
~~~~~~~~

::

   $ conda install sphinx

Windows
-------

Sphinx можно установить используя менеджер пакетов `Chocolatey`__ или
установить используя pip.

__ https://chocolatey.org/

Chocolatey
~~~~~~~~~~

::

   $ choco install sphinx

Для этого предварительно надо установить менеджер пакетов `install Chocolatey
<https://chocolatey.org/install>`_.

Для получения дополнительной информации: `chocolatey page`__.

__ https://chocolatey.org/packages/sphinx/

.. _windows-other-method:

Установка используя pip
~~~~~~~~~~~~~

У большинства пользователей Windows python не установлен по умолчанию, поэтому мы начнем с
установка самого Python. Если у вас не установлен Python, обратитесь к `Hitchhikers
Guide to Python's`__ в раздел Python on Windows. Вам необходимо установить
`Python 3`__.

После установки Python можно установить теперь Sphinx с помощью комманды`pip`. Описанному далее ниже в разделе `Установка используя PyPI`.

__ https://docs.python-guide.org/
__ https://docs.python-guide.org/starting/install3/win/


Установка используя PyPI
----------------------

Sphinx packages are published on the `Python Package Index
<https://pypi.org/project/Sphinx/>`_.  The preferred tool for installing
packages from *PyPI* is :command:`pip`.  This tool is provided with all modern
versions of Python.

On Linux or MacOS, you should open your terminal and run the following command.

::

   $ pip install -U sphinx

On Windows, you should open *Command Prompt* (:kbd:`⊞Win-r` and type
:command:`cmd`) and run the same command.

.. code-block:: doscon

   C:\> pip install -U sphinx

After installation, type :command:`sphinx-build --version` on the command
prompt.  If everything worked fine, you will see the version number for the
Sphinx package you just installed.

Installation from *PyPI* also allows you to install the latest development
release.  You will not generally need (or want) to do this, but it can be
useful if you see a possible bug in the latest stable release.  To do this, use
the ``--pre`` flag.

::

   $ pip install -U --pre sphinx

Using virtual environments
~~~~~~~~~~~~~~~~~~~~~~~~~~

When installing Sphinx using pip,
it is highly recommended to use *virtual environments*,
which isolate the installed packages from the system packages,
thus removing the need to use administrator privileges.
To create a virtual environment in the ``.venv`` directory,
use the following command.

::

   $ python -m venv .venv

You can read more about them in the `Python Packaging User Guide`_.

.. _Python Packaging User Guide: https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/#creating-a-virtual-environment

.. warning::

   Note that in some Linux distributions, such as Debian and Ubuntu,
   this might require an extra installation step as follows.

   .. code-block:: console

      $ apt-get install python3-venv

Docker
------

Docker images for Sphinx are published on the `Docker Hub`_.  There are two kind
of images:

- `sphinxdoc/sphinx`_
- `sphinxdoc/sphinx-latexpdf`_

.. _Docker Hub: https://hub.docker.com/
.. _sphinxdoc/sphinx: https://hub.docker.com/r/sphinxdoc/sphinx
.. _sphinxdoc/sphinx-latexpdf: https://hub.docker.com/r/sphinxdoc/sphinx-latexpdf

Former one is used for standard usage of Sphinx, and latter one is mainly used for
PDF builds using LaTeX.  Please choose one for your purpose.

.. note::

   sphinxdoc/sphinx-latexpdf contains TeXLive packages. So the image is very large
   (over 2GB!).

.. hint::

   When using docker images, please use ``docker run`` command to invoke sphinx
   commands.  For example, you can use following command to create a Sphinx
   project:

   .. code-block:: console

      $ docker run -it --rm -v /path/to/document:/docs sphinxdoc/sphinx sphinx-quickstart

   And you can use the following command to build HTML document:

   .. code-block:: console

      $ docker run --rm -v /path/to/document:/docs sphinxdoc/sphinx make html

For more details, please read `README file`__ of docker images.

.. __: https://hub.docker.com/r/sphinxdoc/sphinx


Installation from source
------------------------

You can install Sphinx directly from a clone of the `Git repository`__.  This
can be done either by cloning the repo and installing from the local clone, on
simply installing directly via :command:`git`.

::

   $ git clone https://github.com/sphinx-doc/sphinx
   $ cd sphinx
   $ pip install .

::

   $ pip install git+https://github.com/sphinx-doc/sphinx

You can also download a snapshot of the Git repo in either `tar.gz`__ or
`zip`__ format.  Once downloaded and extracted, these can be installed with
:command:`pip` as above.

.. highlight:: default

__ https://github.com/sphinx-doc/sphinx
__ https://github.com/sphinx-doc/sphinx/archive/master.tar.gz
__ https://github.com/sphinx-doc/sphinx/archive/master.zip


