==================
flatpak-claws-mail
==================

|Travis| |License|

.. |Travis| image:: https://img.shields.io/travis/karras/flatpak-claws-mail.svg?style=flat-square
   :target: https://travis-ci.org/karras/flatpak-claws-mail
.. |License| image:: https://img.shields.io/github/license/karras/flatpak-claws-mail.svg?style=flat-square
   :target: LICENSE

This repository contains a manifest to create a Flatpak build of Claws Mail.

Claws Mail will have the following permissions:

* Access X11 and DBUS
* Access the network
* Map configurations to ``~/.claws-mail``

Usage
=====
Follow the steps described below to build XChat from scratch. All steps are
executed within the user context:

1. Install ``flatpak`` with your package manager
2. Clone this repository and switch into the created directory
3. Download the required runtimes: ::

   $ flatpak install --user flathub org.gnome.Platform//3.28
   $ flatpak install --user flathub org.gnome.Sdk//3.28

4. Build and install the app in a local repository: ::

   $ flatpak-builder --user --install org.clawsmail.Claws.json

5. Run the app: ::

   $ flatpak run org.clawsmail.Claws/x86_64/stable

License
=======
GNU GENERAL PUBLIC LICENSE Version 3

See the `LICENSE`_ file.

.. _LICENSE: LICENSE
