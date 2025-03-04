[![CI](https://github.com/ReeganExE/bcrypt-cli/actions/workflows/main.yml/badge.svg)](https://github.com/ReeganExE/bcrypt-cli/actions/workflows/main.yml)

> The original [bitnami/bcrypt-cli](https://github.com/bitnami/bcrypt-cli) is not maintained and lacked binary build for latest OS versions.
> This fork aims to provide latest pre-built binary and improved a bit of user-experience.

# bcrypt

This tool allows generating the bcrypt hash for the provided password through stdin 

# Install

Download the pre-built binary from https://github.com/ReeganExE/bcrypt-cli/releases/latest

> *Supported: Linux, macOS, Windows, Raspberry Pi family*

# Basic usage

~~~bash
$> bcrypt --help
Usage:
  bcrypt [OPTIONS]

Application Options:
  -c, --cost=COST    The cost weight, range of 4-31 (default: 10)

Help Options:
  -h, --help         Show this help message
~~~

# Examples

## Hash the provided password with default cost (10)

~~~bash
$> echo -n supersecret | bcrypt
$2a$10$m8hh/nNMb.2krzysVyoRVOS3LoSZha7rwV4lfBnCvasTBKAGC.X4i
~~~

## Hash the provided password with higher cost

~~~bash
$> echo -n supersecret | bcrypt --cost=16
$2a$16$qYLz4PvNXK4tS3LZeud0OutgUDE3yX0KwJgMq3zlg/uOKjaUnrdwy
~~~
