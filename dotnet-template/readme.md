# dotnet-new templates

## Lean Architecture Strutucture

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

## Clean Architecture Structure

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

# Test Projects Dependencies

- Microsoft.NET.Test.Sdk, Version: 17.1.0
- coverlet.collector, Version: 3.1.2
- coverlet.msbuild, Version: 3.1.2
- Moq, Version: 4.17.2
- Shouldly, Version: 4.0.3
- xunit, Version: 2.4.1
- xunit.runner.visualstudio, Version: 2.4.3

# Azure Devops Pipeline

- Checkout
- Nuget Restore
- Build
- Test with Code Coverage
- Install ReportGenerator tool (version 5.0.4)
- Generate Coverage Reports
- Publish Test Results in Azure Devops.
- Publish Code Coverage Results in Azure Devops.
- Publish Artifacts in Azure Devops.

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

# Contributors

- @masterzdran

# Attribution

<a href="https://www.flaticon.com/free-icons/digital-book" title="digital book icons">Digital book icons created by Freepik - Flaticon</a>
