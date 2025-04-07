# Scoop Bucket for [rez](https://rez.readthedocs.io)

<!-- Uncomment the following line after replacing placeholders -->
[![Tests](https://github.com/MichaelHaussmann/scoop-play/actions/workflows/ci.yml/badge.svg)](https://github.com/MichaelHaussmann/scoop-play/actions/workflows/ci.yml) [![Excavator](https://github.com/MichaelHaussmann/scoop-play/actions/workflows/excavator.yml/badge.svg)](https://github.com/MichaelHaussmann/scoop-play/actions/workflows/excavator.yml)

This repo is a bucket for [Scoop](https://scoop.sh), the Windows command-line installer.

It allows to install [rez](https://rez.readthedocs.io), a cross-platform package manager.

## Usage

In powershell enter

```pwsh
scoop bucket add play https://github.com/MichaelHaussmann/scoop-play
scoop install play/rez
```

This will install rez as a scoop app.

### Notes

The installed rez can coexist with another installation, usable with commands `rez` and `rez3`.<br>
The installations are not production proven. It is merely to play around with a local installation of rez.

## Python version

The installer will call `python3`.<br>
Whatever python version is run for `python3` will become res's python version.<br>

If needed, install a specific python version before installing rez, for example:

```pwsh
scoop bucket add versions
scoop install versions/python311
```

## Result

```pwsh
rez -V
Rez 3.2.1 from <scoop-install-path>\scoop\apps\rez\3.2.1\install\Lib\site-packages\rez (python 3.11)

rez3 -V
Rez 3.2.1 from <scoop-install-path>\scoop\apps\rez\3.2.1\install\Lib\site-packages\rez (python 3.11)
```

## Rez-2

It is possible to install a separate version of rez-2, usable with commands `rez2`.<br>
This version is just for testing purposes.

```pwsh
scoop bucket add play https://github.com/MichaelHaussmann/scoop-play
scoop install play/rez2
```

It will be usable with a `rez2` command.

```pwsh
rez2 -V
Rez 2.114.0 from <scoop-install-path>\scoop\apps\rez\2.112.0\install\Lib\site-packages\rez (python 3.11)
```


