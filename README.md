# Web Config Transform Core

Inspired by https://github.com/erichexter/WebConfigTransformRunner.

This is a cross-platform command line tool to run an ASP .NET Web.config transformation

## Supported .NET SDKs

- `netcoreapp3.1`
- `net6.0`

## Used dependencies

- `Microsoft.Web.Xdt`

## Command to build and publish

- `dotnet publish "WebConfigTransformCore/WebConfigTransformCore.csproj" --self-contained --runtime win-x64 -c Release -o ./publish.win-x64 -p:PublishTrimmed=true -p:PublishSingleFile=true`
- `dotnet publish "WebConfigTransformCore/WebConfigTransformCore.csproj" --self-contained --runtime linux-x64 -c Release -o ./publish.linux-x64 -p:PublishTrimmed=true -p:PublishSingleFile=true`
- `dotnet publish "WebConfigTransformCore/WebConfigTransformCore.csproj" --self-contained --runtime osx-x64 -c Release -o./publish.osx-x64 -p:PublishTrimmed=true -p:PublishSingleFile=true`

## To Test

- Build using above commands
- Run `.\WebConfigTransformCore.exe "../TestData/SetAttributesExample/Web.config" "../TestData/SetAttributesExample/Web.Debug.config" "../TestData/SetAttributesExample/NewWeb.Debug.config"`
- Run `.\WebConfigTransformCore.exe "../TestData/HRBExample/NASS.ThirdPartyUploadScheduler.config" "../TestData/HRBExample/NASS.ThirdPartyUploadScheduler.Prod.config" "../TestData/HRBExample/NewNASS.ThirdPartyUploadScheduler.config"`

## Documentation

- https://learn.microsoft.com/en-us/previous-versions/aspnet/dd465326(v=vs.110)
- https://learn.microsoft.com/en-us/aspnet/core/host-and-deploy/iis/transform-webconfig?view=aspnetcore-7.0