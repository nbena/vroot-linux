# vroot-linux

Docker template files for IMUNES virtual nodes when running on Linux.

This repository provides different base images for IMUNES virtual nodes. Each
version is in its own folder.

Currently supported Linux distributions for the base image can come in two
different variations:
 - __full__ - includes all packages that are needed to run the
   [imunes-examples](https://github.com/imunes/imunes-examples) and even a
   greater variety of networking tools. Bigger and slower.
 - __minimal__ - includes a smaller set of packages and is designed to be
   faster and have a smaller footprint.

## Versions

Currently supported versions is the following.

| Folder            | Distribution and version | Image name                       | Comment                              |
| ----------------- | ------------------------ | -------------------------------- | ------------------------------------ |
| ubuntu-16.04      | Ubuntu 16.04 LTS         | imunes/template:ubuntu-16.04     | ubuntu release, needs testing        |
| ubuntu-16.04-min  | Ubuntu 16.04 LTS minimal | imunes/template:ubuntu-16.04-min | minimal edition                      |

## Credits

This image is based on [Phusion](http://www.phusion.nl/) baseimage-docker and
slightly modified to run a different distro version along with some new
packages.

You can use it as a base for your own Docker images. For more info on this
please check the [basedocker-image](https://github.com/phusion/baseimage-docker)
README or the source code.

-----------------------------------------
[<img src="http://imunes.tel.fer.hr/images/imunes_logo.png">](http://www.imunes.net/)
