fedmsg-koji-consumer
====================

An example of using `fedmsg <http://fedmsg.com>`_ to monitor `koji <http://koji.fedoraproject.org>`_, the `Fedora <http://fedoraproject.org>`_ Build System.

Running
-------

.. code-block:: bash

   sudo yum install fedmsg-hub
   # Required to configure the entry point for fedmsg-hub
   python setup.py egg_info
   # fedmsg-hub reads fedmsg-config.py from the current working directory and
   # enables kojiconsumer
   PYTHONPATH=$(pwd) fedmsg-hub
