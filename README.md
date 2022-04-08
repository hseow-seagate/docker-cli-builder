# docker-cli-builder
[![Build status](https://ci.appveyor.com/api/projects/status/5mn0j7adf8xtoawn/branch/master?svg=true)](https://ci.appveyor.com/project/StefanScherer/docker-cli-builder/branch/master)

Build Docker CLI for Windows from upstream repo https://github.com/docker/cli and publish the `docker.exe` to GitHub releases https://github.com/StefanScherer/docker-cli-builder/releases.

**Build with Powershell (Admin)**
```powershell
choco install -y golang -version 1.13.15
choco install -y git
choco install -y mingw

GOPATH C:\gopath
git clone -q --branch=v20.10.14 --single-branch https://github.com/docker/cli.git C:\gopath\src\github.com\docker\cli
powershell -File .\scripts\make.ps1 -Binary
```
