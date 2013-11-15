.. highlight:: console

.. index:: ! UNIX

.. _unix:

Unix reference
==============
Elementary survival guide for the UNIX terminal. This guide assumes the bash_ shell is used.

.. _bash: https://en.wikipedia.org/wiki/Bash_(Unix_shell)

Concepts
--------
A good reference for computer terms can be found at `Computer Hope`_.

.. _Computer Hope: http://www.computerhope.com/jargon.htm

.. index::
    shell
    command interpreter
    command-line interface

.. _shell:

Shell
^^^^^
A shell or command-line interpreter is a simple textual interface
allowing users to execute commands on a UNIX system. Typically, a
shell displays the `Command Prompt`_ and allows users to type in
commands which will be execute by the press of the return key.

A commonly used shell is bash_.

.. seealso::
    * http://www.computerhope.com/jargon/s/shell.htm
    * https://en.wikipedia.org/wiki/Shell_(computing)#Text_.28CLI.29_shells

.. index::
    Current Working Directory
    see: Working Directory;Current Working Directory
    see: CWD;Current Working Directory

.. _cwd:

Current Working Directory
^^^^^^^^^^^^^^^^^^^^^^^^^
The current directory or current working directory is the directory
which is currently open in the user's terminal. The value of the
working directory can usually be read from the `command prompt`_::

    drbob@swordfish ~/Development/workflow-reference/unix $

In this example ``~/Development/workflow-reference/unix`` is the
working directory where ``~`` is a common abbreviation for the user's
`home directory`_.

.. note::
    The specific command prompt might look different depending on the
    configuration of your particular computer.

The value of the working directory can be found at any time using the
``pwd`` command::

    drbob@swordfish ~/Development/workflow-reference/unix $ pwd
    /Users/drbob/Development/workflow-reference/unix

.. seealso::
    * `Current Directory on Computer Hope <http://www.computerhope.com/jargon/c/currentd.htm>`_
    * `Current Working Directory Definition <http://www.linfo.org/current_directory.html>`_
    * `Working directory on Wikipedia <https://en.wikipedia.org/wiki/Working_directory>`_

.. _`home directory`:

Home Directory
^^^^^^^^^^^^^^
This is the directory where the user stores all of his or her personal information and files as well as log in scripts and user information. The user's home directory is commonly abbreviated as ``~``.

Returning to the user's home directory from any other directory can be
accomplished with the cd_ command::

    drbob@swordfish ~/Development/workflow-reference $ cd
    drbob@swordfish ~ $

The :ref:`cwd` is now equal to the user's home directory so that the
full `path name`_ to the home directory can be found through pwd_::

    drbob@swordfish ~ $ pwd
    /Users/drbob

.. seealso:: http://www.computerhope.com/jargon/h/homedir.htm

.. _`command prompt`:

Command Prompt
^^^^^^^^^^^^^^

.. seealso:: http://www.computerhope.com/jargon/c/commprom.htm

Path Name
^^^^^^^^^

.. seealso:: http://www.computerhope.com/jargon/p/path.htm

Commands
--------
Some common UNIX commands.

.. _`cd`:

Change Directory (cd)
^^^^^^^^^^^^^^^^^^^^^
Changes into a particular (sub)directory or returns to the user's
home directory when no (sub)directory is specified.

.. seealso:: https://en.wikipedia.org/wiki/Cd_(command)

pwd
^^^
Returns the name of the :ref:`cwd`.
