# Code Coverage with .Net Core and Cobertura

Already I have some routine activity to provide code coverage report for my .Net Core projects to CI. An issue turned out more complex then I appreciate so I decide to provide here the most important steps from the journey

## Prerequisites

So, let's assume that we have some codebase

```sh
dotnet new classlib -n MyBuisLogic
```

and two test projects: one with unit and another with integration tests

```sh
dotnet new xunit -n MyBuisLogic.Unit.Tests
dotnet new xunit -n MyBuisLogic.Integration.Tests
```

## Add Coverlet

First of all we should add `coverlet.collector` to both test projects
```sh
cd MyBuisLogic.Unit.Tests && dotnet add package coverlet.collector && cd ..
cd MyBuisLogic.Integration.Tests && dotnet add package coverlet.collector && cd ..
```

then you should check that your csproj contains something like this:
```xml
<ItemGroup>
    <PackageReference Include="coverlet.collector" Version="1.3.0"/>
    ...
</ItemGroup>
```

> If you add coverlet package using Visual Studio it will be installed with assets filters and your csproj will contain
>  ```xml
> <ItemGroup>
>   <PackageReference Include="coverlet.collector" Version="1.3.0">
>      <PrivateAssets>all</PrivateAssets>
>       <IncludeAssets>runtime; build; native; contentfiles; analyzers; buildtransitive</IncludeAssets>
>    </PackageReference>
>    ...
> </ItemGroup>
> ```
> In this case you should remove this additional elements manualy. Otherwise you will have an error `"Could not find data collector 'XPlat Code Coverage'"`

If you done this right than you can run 
```sh
dotnet test --collect:"XPlat Code Coverage"
```




