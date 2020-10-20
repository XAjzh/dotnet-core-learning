# install and use local tool

## create a manifest file

To install a tool for local access only (for the current directory and subdirectories), it has to be added to a manifest file.

```bash
$ dotnet new tool-manifest
```

## install botsay as a local tool

```bash
$ dotnet tool install --add-source ./microsoft.botsay/nupkg microsoft.botsay
```

## use the tool

```bash
$ dotnet tool run botsay hello from the bot
```

## remove the tool

```bash
dotnet tool uninstall microsoft.botsay
```