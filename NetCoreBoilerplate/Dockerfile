FROM mcr.microsoft.com/dotnet/core/sdk:3.0-alpine3.10 as build

WORKDIR /src
COPY . .
RUN dotnet publish -c Release -r linux-musl-x64 -o ./deploy /p:ShowLinkerSizeComparison=true

FROM mcr.microsoft.com/dotnet/core/runtime-deps:3.0-alpine3.10 as runtime

WORKDIR /app
COPY --from=build /src/deploy .

CMD ["./NetCoreBoilerplate"]