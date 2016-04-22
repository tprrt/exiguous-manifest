..
.. -*- coding: utf-8; tab-width: 4; c-basic-offset: 4; indent-tabs-mode: nil -*-

Tap runtime manifest
--------------------

To get the runtime's source, you need to have `repo` installed and use it as:

Install the `repo` utility:

::

   $ mkdir ~/bin
   $ curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
   $ chmod a+x ~/bin/repo

*Note: make sure ~/bin exists and it is part of your PATH*

Download the runtime source:

::

   $ PATH=${PATH}:~/bin
   $ mkdir Exiguous
   $ cd Exiguous
   $ repo init -u git@github.com:tprrt/exiguous-manifest.git -b <branch> -m <manifest>
   $ repo sync

At the end of the commands you have every metadata you need to start work with.

To start a runtime image build:

::

   $ . exiguous-build-env
   $ bitbake exiguous-image

Maintainer: `Thomas Perrot <thomas.perrot@tupi.fr>`_
