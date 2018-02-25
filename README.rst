Introduction
============
NOTE: this is a fork of the psphere master branch (v0.5.3) that attempts to add Python 3 compatibility to the psphere library

psphere is a Python interface for the `VMware vSphere Web Services SDK`_, a 
powerful API for programatically managing your VMware infrastructure:

* Provision, clone and snapshot virtual machines
* Query and configure clusters, host systems and datastores
* Programatically configure ESXi hosts (i.e. for automation)

psphere can be used to create standalone Python scripts or used as a library
in larger Python applications (e.g. Django).

Usage
=====

    >>> from psphere.client import Client
    >>> #uncomment next two lines to ignore self-signed certificate error
    >>> #import ssl
    >>> #ssl._create_default_https_context = ssl._create_unverified_context
    >>> client = Client("your.esxserver.com", "Administrator", "strongpass")
    >>> servertime = client.si.CurrentTime()
    >>> print(servertime)
    2010-09-04 18:35:12.062575
    >>> client.logout()

Installation
============

To install, download or clone this to a local directory and run the following command from the psphere directory:

# python setup.py install