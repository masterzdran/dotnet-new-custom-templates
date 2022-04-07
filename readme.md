# ![dotnet-new Templates](./icon.64.png "dotnet-new templates") dotnet-new templates
# Download

https://www.nuget.org/packages/LeanArchitecture.Dotnet.Templates.Project/

## Lean Architecture

```
├───class-xunit-lib
│   ├───src
│   │   └───LeanArchitecture.Project
│   │           LeanArchitecture.Project.csproj
│   │
│   └───tests
│       └───LeanArchitecture.Project.Tests
│               LeanArchitecture.Project.Tests.csproj
│
├───sln
│   │   azure-pipelines.yml
│   │   editorconfig
│   │   gitignore
│   │   global.json
│   │   LeanArchitecture.Solution.sln
│   │   nuget.config
│   │
│   ├───src
│   │       readme.md
│   │
│   └───tests
│           readme.md
│
└───xunit
    └───LeanArchitecture.Project.Tests
            LeanArchitecture.Project.Tests.csproj
```

## Clean Architecture

```
│   azure-pipelines.yml
│   CleanArchitecture.Solution.sln
│   editorconfig
│   gitignore
│   global.json
│   nuget.config
│   readme.md
│
├───src
│   │
│   ├───Application
│   │
│   ├───Infrastructure
│   │
│   └───Presentation
│
└───tests
    │
    ├───Application
    │
    ├───Infrastructure
    │
    └───Presentation

```

# Usage

## Create new solution:

**Lean Solution Template**

```
dotnet new mz-clean-architecture-sln -n [Solution Name] -o [Solution Name Location]
```

**Clean Solution Template**

```
dotnet new mz-lean-architecture-sln -n [Solution Name] -o [Solution Name Location]
```

## Create new lib project:

**Lean Test project Template**

```
$> cd [Solution Name Location]
$> dotnet new new mz-lean-architecture-xunit -n [Project Name] -o .
```

**Lean Class Library and Test Project Template**

```
$> cd [Solution Name Location]
$> dotnet new mz-lean-architecture-class-xunit-lib -n [Project Name] -o .
```

## Add New Projects to Solution

**Libraries Project**

```
$> cd [Solution Name Location]
$> dotnet sln add .\src\[Project Name]\[Project Name].csproj --solution-file tests\[Project Name]
```

**Test Project**

```
$> cd [Solution Name Location]
$> dotnet sln add .\tests\[Project Name].Tests\[Project Name].Tests.csproj --solution-file tests\[Project Name].Tests
```

# Credits

<a href="https://www.flaticon.com/free-icons/digital-book" title="digital book icons">Digital book icons created by Freepik - Flaticon</a>
