# DotNetCoreAngularTemplate
A basic implementation of the default project that Visual Studio creates to get you started with a .NET Core Web Application using an Angular SPA. A few extra steps were taken to get the solution to the point where you can start working without having to go through the same startup steps every time.

## Goals
- To clone this solution, press `Ctrl+F5`, and have a working Angular SPA with a .NET Core backend
- To have an up-to-date set of dependencies that have no (or only low severity) vulnerabilities
- To reduce the amount of set-up time needed when the urge to whip up a new SPA occurs
- To keep as light as possible, so that a new project can be taken any number of directions; this is not meant to be a fully-fledged startup project (with existing tests, configured logging or dependency injection, continuous integration, etc.)

## Actions Taken
- Created a .NET Core 3.1 Web Application with Angular, configured for HTTPS
- Created projects for Web (Angular SPA), Core, Infrastrucutre, and Unit Tests (XUnit)
- Created a folder structure for the solution (`src` and `tests` folder)
- All class library projects are .NET Standard 2.0
- All projects are configured to treat warnings as errors
- NPM dependencies were altered via `npm audit fix` to fix vulnerabilities that, as of this project creation, are still the default out of the box behavior for this Visual Studio project template
  - Manually downgraded `@angular-devkit/build-angular` as per [this known issue with Angular](https://github.com/angular/angular-cli/issues/16902)
