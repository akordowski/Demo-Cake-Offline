# Demo Cake Offline

A demo for the configuration of [Cake Build](https://github.com/cake-build/cake) for offline scenarios.

1. Set in the file `build.ps1` on line `104` the path to `nuget.exe` in the variable `$NUGET_URL`.
    * `$NUGET_URL = "./nuget/nuget.exe"`
1. Set in the file `build.ps1` on line `121` the path to `packages.config`.
    * `$wc.DownloadFile("./nuget/packages.config", $PACKAGES_CONFIG)`
1. Set in the file `cake.config` in the `[Nuget]` section the path to the NuGet feed.
    * `Source=./nuget/`