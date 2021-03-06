# dotnet-nuget-gc

[![Build Status](https://terrajobst.visualstudio.com/dotnet-nuget-gc/_apis/build/status/terrajobst.dotnet-nuget-gc?branchName=master)](https://terrajobst.visualstudio.com/dotnet-nuget-gc/_build/latest?definitionId=15)

This `dotnet` extension is designed to clean-up the NuGet cache. It's a
(hopefully) temporary workaround for the [missing cache-expiration
policy][nuget-issue] Code written by [@dotmorten] as outlined in [his
comment][code-origin].

[![](docs/thumbnail.png)](https://www.youtube.com/watch?v=2nNJly4uim0)

[@dotmorten]: https://githun.com/dotMorten
[nuget-issue]: https://github.com/NuGet/Home/issues/4980
[code-origin]: https://github.com/NuGet/Home/issues/4980#issuecomment-432512640

## Installation

    $ dotnet tool install dotnet-nuget-gc -g

## Usage

    $ dotnet nuget-gc [minimum-days]

* `minimum-days`. Number of days a package must not be used in order to be
  purged from the cache. Defaults to `30`.
