# MoqLib.Grpc.Testing.SourceGenerator

This package generates Mock setup methods using [Source Generators](https://learn.microsoft.com/en-us/dotnet/csharp/roslyn-sdk/source-generators-overview) to make gRPC tests easier.
The source code generated makes use of the following dependencies:
* [Moq](https://www.nuget.org/packages/Moq)
* [Grpc.Core.Testing](https://www.nuget.org/packages/Grpc.Core.Testing)
* [Google.Api.Gax.Grpc.Testing](https://www.nuget.org/packages/Google.Api.Gax.Grpc.Testing)
* [System.Linq.Async](https://www.nuget.org/packages/System.Linq.Async)

## Setup

Make sure this packages are added to the test project:

```shell
dotnet add package MoqLib.Grpc.Testing.SourceGenerator
dotnet add package Moq
dotnet add package Grpc.Core.Testing
dotnet add package Google.Api.Gax.Grpc.Testing
dotnet add System.Linq.Async
```

Add `Protobuf` property like `Grpc.Tools` recommendations. Example:

```xml
<ItemGroup>
    <Protobuf Include="./Protos/orders-service.proto" Link="Protos/orders-service.proto" />
    <Protobuf Include="./Protos/products-service.proto" Link="Protos/products-service.proto" />
</ItemGroup>
```

Build de project and have fun!
