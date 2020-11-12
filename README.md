# Sonar - a Docker utility tool

[![Build Status](https://circleci.com/gh/felicianotech/sonar.svg?style=shield)](https://circleci.com/gh/felicianotech/sonar) [![Software License](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/felicianotech/sonar/master/LICENSE)

`sonar` is a Docker utility tool useful for when you want to learn more about your Docker images.
You can list and compare Docker images, their tags, and pull metrics from Docker Hub.


## Table of Contents

- [Installing](#installing)
- Configuring
- Features


## Installing

### Debian Package (.deb) Instructions

Download the `.deb` file to the desired system.

For graphical systems, you can download it from the [GitHub Releases page][gh-releases].
Many distros allow you to double-click the file to install.
Via terminal, you can do the following:

```bash
wget https://github.com/felicianotech/sonar/releases/download/v0.8.0/sonar_0.8.0_amd64.deb
sudo dpkg -i sonar_0.8.0_amd64.deb
```

`0.8.0` and `amd64` may need to be replaced with your desired version and CPU architecture respectively.

### Linux Snap
Sonar can be installed via snap for users of `Ubuntu`, `Pop!_OS`, Debian, Fedora, and more.
It's an easy installation that always stays up-to-date which is great.
You can install it by running:

```bash
sudo snap install sonar
```

### macOS / Brew

```bash
brew install sonar
```


## Configuring

Most commands don't need authentication.
Some, such as `sonar set description`, require Docker / Docker Hub credentials.
These can be set via the environment variables `DOCKER_USER` and `DOCKER_PASS`.

You can also set the password specifically with the global `--password` flag.
Please be careful with this, you don't want a password in your shell history.
The suggestion is to pass an environment variable (that isn't already `DOCKER_PASS`) by doing something like this:

```bash
sonar set readme my/image --password=$THE_PASSWORD_ENVAR ./file.md
```


## Features

*Lists* - List images belonging to a namespace and tags belonging to an image.

*Metadata* - Set your image's Docker Hub description from the command-line.

Run `sonar help` to see all commands available.


## License

This repository is licensed under the MIT license.
The license can be found [here](./LICENSE).



[gh-releases]: https://github.com/felicianotech/sonar/releases
