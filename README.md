# Scoop Bucket for [REZ](https://rez.readthedocs.io)

<!-- Uncomment the following line after replacing placeholders -->
[![Tests](https://github.com/MichaelHaussmann/scoop-play/actions/workflows/ci.yml/badge.svg)](https://github.com/MichaelHaussmann/scoop-play/actions/workflows/ci.yml) 
[![Excavator](https://github.com/MichaelHaussmann/scoop-play/actions/workflows/excavator.yml/badge.svg)](https://github.com/MichaelHaussmann/scoop-play/actions/workflows/excavator.yml)

This repo is a bucket for [Scoop](https://scoop.sh), the Windows command-line installer.

It allows to install [rez](https://rez.readthedocs.io), a cross-platform package manager. 

```pwsh
scoop bucket add scoop-play https://github.com/MichaelHaussmann/scoop-play
scoop install scoop-play/rez
```

This will install REZ as a scoop app:

```pwsh
rez -V
Rez 3.2.1 from ~\scoop\apps\rez\3.2.1\install\Lib\site-packages\rez (python 3.11)

rez3 -V
Rez 3.2.1 from ~\\scoop\apps\rez\3.2.1\install\Lib\site-packages\rez (python 3.11)
```

It is possible to install a separate version of rez-2

```pwsh
scoop bucket add scoop-play https://github.com/MichaelHaussmann/scoop-play
scoop install scoop-play/rez2
```

It will be usable with a `rez2` command.
```
rez2 -V
Rez 2.114.0 from ~\scoop\apps\rez\2.112.0\install\Lib\site-packages\rez (python 3.11)
```

### Note:

The installed rez can coexist with another installation, and therefore exposes the shim `rez3` (or `rez2` for the rez-2 version).

The installations were not totally tested, and are not production proof.  
It is merely to play around with a local installation of rez.


## Todo

To make this repo complete:

2. Allow all GitHub Actions:
   - Navigate to `Settings` - `Actions` - `General` - `Actions permissions`.
   - Select `Allow all actions and reusable workflows`.
   - Then `Save`.
3. Allow writing to the repository from within GitHub Actions:
   - Navigate to `Settings` - `Actions` - `General` - `Workflow permissions`.
   - Select `Read and write permissions`.
   - Then `Save`.
8. If you'd like your bucket to be indexed on `https://scoop.sh`, add the
   topic `scoop-bucket` to your repository.


## How do I contribute new manifests?

To make a new manifest contribution, please read the [Contributing
Guide](https://github.com/ScoopInstaller/.github/blob/main/.github/CONTRIBUTING.md)
and [App Manifests](https://github.com/ScoopInstaller/Scoop/wiki/App-Manifests)
wiki page.
