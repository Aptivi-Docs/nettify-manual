---
description: Welcome to Nettify!
---

# 👋 Welcome

Welcome to Nettify! It's a C# library that allows you to use various Internet-based tools, such as getting your city's weather forecast at the current time, reading and viewing all RSS feed articles, and getting your favorite SHOUTcast-powered internet radio information.

To use this library, go to any page in the left side of the screen.

## Installation

This library is very easy to install. It's available at [NuGet](https://www.nuget.org/packages/SpecProbe/). Just follow these steps:

1. Open your project file (`.csproj` or `.fsproj`)
2. Place the `PackageReference` line on a property group like so:
   * `<PackageReference Include="Nettify" Version="x.x.x" />`
   * ...where `Version` is the current version of the library
3. Run a package restore using `dotnet restore`

If you follow these steps correctly, you should be able to use Nettify functions.
