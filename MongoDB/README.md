General process in small steps for quick MongoDB setup.

# Installation  

Consult the official documentation for suitable OS.
https://docs.mongodb.com/manual/administration/install-community/

MongoDB stores its:
- Configuration in `/etc/mongod.conf`
- Data in `/var/lib/mongodb`
- Log files in `/var/log/mongodb`

This is for Ubuntu environment, other environments may differ.
# Get it running  

## Start

> sudo service mongod start

## Status

> sudo service mongod status

## Stop

> sudo service mongod stop

## Using mongoDB shell

> mongo --host 127.0.0.1:27017

# Shell command  

[Quick guide for frequently used commands](Shell-command.md)

Full documentation: [official mongoDB Shell guide](https://docs.mongodb.com/manual/mongo/)
