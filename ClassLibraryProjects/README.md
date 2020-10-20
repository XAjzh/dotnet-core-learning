# A simple Class Library

A class library in StringLibrary directory.

Use `dotnet new classlib` to create library.

```bash
$ dotnet new classlib -o StringLibrary
```

Use `dotnet build` to build library.

```bash
$ dotnet build StringLibrary
```

## use the library in program

For use the library, the ShowCase project should reference the library.

```bash
$ dotnet add ShowCase/ShowCase.csproj \
    reference StringLibrary/StringLibrary.csproj
```

Use `dotnet run` to run the program

## test the library

Use `dotnet new test` to create test project.

```bash
$ dotnet new test -o StringLibraryTest
```

For use the library, reference the library.

```bash
$ dotnet add StringLibraryTest/StringLibraryTest.csproj \
    reference StringLibrary/StringLibrary.csproj
```

Use `dotnet test` for testing.

```bash
dotnet test StringLibraryTest/
```

## sln file

The sln file is not essential. But using the sln file can make management more convenient.
