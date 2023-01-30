========
Сборка проекта используя Sphinx-doc
========

Linux
-----

Debian/Ubuntu
~~~~~~~~~~~~~

Установите пакет ``python3-sphinx`` используя ``apt-get``:

::

   $ apt-get install python3-sphinx

Если python не был до этого установлен, команда установит Python на компьютер.

RHEL, CentOS
~~~~~~~~~~~~

Установите пакет ``python-sphinx`` используя ``yum``:

::

   $ yum install python-sphinx

Если ``Python`` не был до этого установлен, команда установит ``Python`` на компьютер.

Другие дистрибутивы
~~~~~~~~~~~~~~~~~~~

Большинство дистрибутивов Linux имеют Sphinx в своих репозиториях пакетов. Обычно пакет называется ``python3-sphinx``, ``python-sphinx`` или ``sphinx``.


macOS
-----

``Sphinx`` обычно устанавливают используя `Homebrew`__, `MacPorts`__, или через ``pip``, используя пакет поставки `Anaconda`__.

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

Установите пакет ``python3x-sphinx`` используя ``port``:

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
установить используя ``pip``.

__ https://chocolatey.org/

Chocolatey
~~~~~~~~~~

::

   $ choco install sphinx

Для этого предварительно надо установить менеджер пакетов `install Chocolatey
<https://chocolatey.org/install>`_.

Для получения дополнительной информации: `chocolatey page`__.

__ https://chocolatey.org/packages/sphinx/

Установка используя pip
~~~~~~~~~~~~~

У большинства пользователей Windows ``Python`` не установлен по умолчанию, поэтому мы начнем с
установка самого ``Python``. Если у вас не установлен ``Python``, обратитесь к `Hitchhikers
Guide to Python's`__ в раздел Python on Windows. Вам необходимо установить
`Python 3`__.

После установки ``Python`` можно установить теперь ``Sphinx`` с помощью комманды ``pip``. Описанному далее ниже в разделе ``Установка используя PyPI``.

__ https://docs.python-guide.org/
__ https://docs.python-guide.org/starting/install3/win/


Установка используя PyPI
----------------------

Пакет ``Sphinx`` опубликован в `Python Package Index
<https://pypi.org/project/Sphinx/>`_.  Для установки пакета из *PyPI* используется комманда ``pip``, которая поставляется сейчас со всеми пакетами ``Python``.

В Linux или MacOS необходимо открыть терминал и выполнить следующую команду.

::

   $ pip install -U sphinx

В Windows необходимо открыть *Командная строка* (:kbd:'⊞Win-r' и ввести *cmd*) и выполните ту же команду.

.. code-block:: doscon

   C:\> pip install -U sphinx

После установки введите команду *sphinx-build --version* в командной строке.  Если установка прошла нормально, вы увидите номер версии для пакета Sphinx, который вы только что установили.


Использование виртуальных сред
~~~~~~~~~~~~~~~~~~~~~~~~~~

При установке Sphinx с помощью pip,
настоятельно рекомендуется использовать *виртуальные среды*,
которые изолируют установленные пакеты от системных пакетов,
тем самым устраняя необходимость использования прав администратора.
Чтобы создать виртуальную среду в каталоге ``.venv``,
используйте следующую команду.

::

   $ python -m venv .venv

Подробнее о этом можно прочитать в разделе `Python Packaging User Guide`_.

.. _Python Packaging User Guide: https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/#creating-a-virtual-environment

.. Предупреждение::

   Обратите внимание, что в некоторых дистрибутивах Linux, таких как Debian и Ubuntu,
   для этого может потребоваться дополнительный шаг установки, как показано ниже.

   .. code-block:: console

      $ apt-get install python3-venv