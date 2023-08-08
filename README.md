# Web Config Transform Runner

Inspired by https://github.com/erichexter/WebConfigTransformRunner.

This is a commandline tool to run an ASP.Net web.config transformation.

## Used dependencies

- `Microsoft.Web.Xdt`

## Command to build and publish

- `dotnet publish "WebConfigTransformRunner/WebConfigTransformRunner.csproj" --self-contained --runtime win-x64 -c Release -o ./publish.win-x64 -p:PublishTrimmed=true -p:PublishSingleFile=true`
- `dotnet publish "WebConfigTransformRunner/WebConfigTransformRunner.csproj" --self-contained --runtime linux-x64 -c Release -o ./publish.linux-x64 -p:PublishTrimmed=true -p:PublishSingleFile=true`
- `dotnet publish "WebConfigTransformRunner/WebConfigTransformRunner.csproj" --self-contained --runtime osx-x64 -c Release -o./publish.osx-x64 -p:PublishTrimmed=true -p:PublishSingleFile=true`

## To Test
