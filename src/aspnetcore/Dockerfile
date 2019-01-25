FROM microsoft/dotnet:2.2-aspnetcore-runtime AS base
WORKDIR /app
EXPOSE 80

FROM microsoft/dotnet:2.2-sdk AS build
WORKDIR /src
COPY ["aspnetcore.csproj", "./"]
RUN dotnet restore "./aspnetcore.csproj"
COPY . .
WORKDIR "/src/."
RUN dotnet build "aspnetcore.csproj" -c Release -o /app

FROM build AS publish
RUN dotnet publish "aspnetcore.csproj" -c Release -o /app

FROM base AS final
WORKDIR /app
COPY --from=publish /app .
ENTRYPOINT ["dotnet", "aspnetcore.dll"]
