
Установка Helm
**************
В этом руководстве рассказывается, как установить Helm CLI. Helm может быть установлен как из
исходного кода, так и из собранных binary релизов.


Из Проекта Helm
===============
Проект Helm предоставляет два способа получения и установки Helm. Это
официальные методы получения релизов Helm. В дополнение к этому сообщество Helm
предоставляет методы установки Helm через различные менеджеры пакетов.
Установка с помощью этих методов может быть найдена ниже официальных методов.


Из Binary Релизов
-----------------


Каждый  `релиз`_ Helm предоставляет различные binary сборки под разные операционные системы (OSes). Эти binary версии могут быть загружены и установлены вручную.

.. _релиз: https://github.com/helm/helm/releases/


Скачайте нужную вам версию и распакуйте. Найдите `helm` binary файл в директории из распаковки, и переместите в нужное место


.. code-block:: console

  wget https://get.helm.sh/helm-v3.14.3-linux-amd64.tar.gz

  tar -zxvf helm-v3.14.3-linux-amd64.tar.gz

  mv linux-amd64/helm /usr/local/bin/helm

Из Скрипта
----------

 У Helm теперь есть скрипт установки, которая будет автоматически загружать последнюю версию Helm и `устанавливать его локально`_ .

.. _устанавливать его локально: https://github.com/helm/helm/releases/

Через Менеджеров Пакетов
------------------------

Используя Homebrew (macOS)
--------------------------

.. code-block:: console

  brew install helm

Используя Chocolatey (Windows)
------------------------------

Используя Apt (Debian/Ubuntu)
-----------------------------

.. code-block:: console

  curl https://baltocdn.com/helm/signing.asc | gpg --dearmor | sudo tee /usr/share/keyrings/helm.gpg > /dev/null
  sudo apt-get install apt-transport-https --yes
  echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/helm.gpg] https://baltocdn.com/helm/stable/debian/ all main" | sudo tee /etc/apt/sources.list.d/helm-stable-debian.list
  sudo apt-get update
  sudo apt-get install helm


Используя Snap
--------------
.. code-block:: console

  sudo snap install helm --classic
