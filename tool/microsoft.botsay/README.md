# create and use tool

## create tool

Add the following nodes to the end of <PropertyGroup>.

```xml
<PackAsTool>true</PackAsTool>
<ToolCommandName>botsay</ToolCommandName>
<PackageOutputPath>./nupkg</PackageOutputPath>
```

Then use `dotnet pack` to create a NuGet package.

## install the tool as a global tool

Use `dotnet tool install` to install the tool.

```bash
$ dotnet tool install --global --add-source ./nupkg microsoft.botsay
```

The bellow command can invoke the tool 

```bash
$ botsay <arguments>
```

The bellow command can remove the tool

```bash
$ dotnet tool uninstall -g microsoft.botsay
```

## Use the tool as a global tool installed in a custom location

Use `--tool-path` option to specifiy a custom location

```bash
$ dotnet tool install --tool-path ~/bin --add-source ./nupkg microsoft.botsay
```

Invoke the tool

```bash
$ ~/bin/botsay hello from the bot
```

Remove the tool

```bash
$ dotnet tool uninstall --tool-path ~/bin microsoft.botsay
```
