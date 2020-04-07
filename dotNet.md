# DotNet Core, C#
Resources, learnings and best practices in all things .net, including dotnet core, C#, EF core, ASP.Net
## OpenAPI
OpenAPI a standard way of documenting an API. It was previouslly called Swagger and the names are often used interchangably. NSwag and Swashbuckle are the two most popular libraries to implement OpenAPI in .net core applications. 
### Resources
* https://github.com/KevinDockx/DocumentingAspNetCoreApisWithOpenAPI - provides a best practices example of an OpenAPI implementation in a dotnet core app

#### ApiExplorer
Both Swashbuckle and NSwag build the OpenApi document based on information provided by the runtime system. This information is collected through the ApiExplorer. This will need to be configured first.

For versioend endpoints, the configuration would look like this:
```csharp
services.AddVersionedApiExplorer(setupAction =>
{
  setupAction.GroupNameFormat = "'v'VV";
});
```
This will group your documentation into *Groups* by version, with the format "v1.0" or "v2". 
