python-cloudfiles-hubic
=======================

Python language bindings for Cloud Files API, modified to add HubiC Authentication support

## Goal
Being able to use tools already compatible with Cloud Files with HubiC, OVH's own cloud storage service.
HubiC is based on the same underlying protocol as RackSpace's Cloud Files: OpenStack Object Storage aka [*Swift*](http://docs.openstack.org/developer/swift/). Only authentication is different.
This is a modified version of the official Cloud Files python bindings which add support for HubiC authentication.

## Use Case: Duplicity
From wikipedia:
> Duplicity is a software suite that provides encrypted, digitally signed, versioned, remote backup of files requiring little of the remote server.
Duplicity has the ability to store encrypted backups on Cloud Files using python-cloudfiles. With this modified version of python-cloudfiles, it gains the ability to connect to HubiC.

### Example
    export CLOUDFILES_USERNAME="YOUR_HUBIC_EMAIL"
    export CLOUDFILES_APIKEY="YOUR_HUBIC_PASSWORD"
    export CLOUDFILES_AUTHURL='hubic'
    duplicity /local/dir/to/backup cf+http://default
