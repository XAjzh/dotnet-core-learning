# create and use tool

## create tool

Add the following nodes to the end of <PropertyGroup>.

```xml
<PackAsTool>true</PackAsTool>
<ToolCommandName>botsay</ToolCommandName>
<PackageOutputPath>./nupkg</PackageOutputPath>
```

Then use `dotnet pack` to create a NuGet package.