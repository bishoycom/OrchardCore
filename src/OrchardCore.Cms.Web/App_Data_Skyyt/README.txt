
Build Solution

global.json
from: "version": "9.0.201",
to: "version": "9.0.103"

OrchardCore.Cms.Web > Edit Project File
from: <AspNetCoreHostingModel>InProcess</AspNetCoreHostingModel>
to: <AspNetCoreHostingModel>OutOfProcess</AspNetCoreHostingModel>

\OrchardCore.Build\TargetFrameworks.props
from: <CommonTargetFrameworks Condition="'$(CommonTargetFrameworks)' == ''">net8.0;net9.0</CommonTargetFrameworks>
to: <CommonTargetFrameworks Condition="'$(CommonTargetFrameworks)' == ''">net9.0</CommonTargetFrameworks>

Publish OrchardCore.Cms.Web project to folder

Fix multiple frameworks error
in: \src\OrchardCore.Cms.Web\Properties\PublishProfiles\FolderProfile.pubxml
add: <TargetFramework>net9.0</TargetFramework>
inside: <PropertyGroup>

Publish OrchardCore.Cms.Web project to folder

New Website
Proceed with installation steps
