# <img src="https://app-metrics.io/images/logo.png" alt="App Metrics" width="50px"/> App Metrics Packaging 
[![Official Site](https://img.shields.io/badge/site-appmetrics-blue.svg?style=flat-square)](https://www.app-metrics.io/getting-started/) [![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg?style=flat-square)](https://opensource.org/licenses/Apache-2.0)

## Latest Builds and Packages

|Branch|VSTS|
|------|:--------:|
|dev|[![BuildStatus](https://appmetrics.visualstudio.com/_apis/public/build/definitions/2145f7d1-b59c-4c8c-a5f7-4e977a72764f/2/badge?branchName=dev)](https://appmetrics.visualstudio.com/AppMetrics/_build/index?definitionId=2)
|master|[![BuildStatus](https://appmetrics.visualstudio.com/_apis/public/build/definitions/2145f7d1-b59c-4c8c-a5f7-4e977a72764f/2/badge?branchName=master)](https://appmetrics.visualstudio.com/AppMetrics/_build/index?definitionId=2)|

|Package|Dev Release|Pre-Release|Release|
|------|:--------:|:--------:|:--------:|
|App.Metrics.Packaging|[![MyGet Status](https://img.shields.io/myget/appmetrics/v/App.Metrics.Packaging.svg?style=flat-square)](https://www.myget.org/feed/appmetrics/package/nuget/App.Metrics.Packaging)|[![NuGet Status](https://img.shields.io/nuget/vpre/App.Metrics.Packaging.svg?style=flat-square)](https://www.nuget.org/packages/App.Metrics.Packaging/)|[![NuGet Status](https://img.shields.io/nuget/v/App.Metrics.Packaging.svg?style=flat-square)](https://www.nuget.org/packages/App.Metrics.Packaging/)

## Usage

Add the following package reference to the csproj:

`<PackageReference Include="App.Metrics.Packaging" Version="*" PrivateAssets="All" />`

The package description defaults to the package id, so add the following project to provide a real description:

```xml
  <PropertyGroup>
    <Description>{The package's description}</Description>
  </PropertyGroup>
```

## How to Build

```csharp
./build.ps1 -Target Local
```

Package will be output to `/.artifacts/packages/App.Metrics.Packaging.{Version}.nupkg`

## Versioning

To version bump, edit the `VersionPrefix` and/or `VersionSuffix` in `./version.props`

> When on non-release branches the `VersionSuffix` will always be set to `alpha` with the build number appended.
