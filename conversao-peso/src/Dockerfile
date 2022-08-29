FROM mcr.microsoft.com/dotnet/aspnet:5.0 AS base
WORKDIR /app
EXPOSE 80
EXPOSE 443

FROM mcr.microsoft.com/dotnet/sdk:5.0 AS build
WORKDIR /src
COPY ["ConversaoPeso.Web/ConversaoPeso.Web.csproj", "ConversaoPeso.Web/"]
RUN dotnet restore "ConversaoPeso.Web/ConversaoPeso.Web.csproj"
COPY . .
WORKDIR "/src/ConversaoPeso.Web"
RUN dotnet build "ConversaoPeso.Web.csproj" -c Release -o /app/build

FROM build AS publish
RUN dotnet publish "ConversaoPeso.Web.csproj" -c Release -o /app/publish

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "ConversaoPeso.Web.dll"]

# docker build -t isaacgiordani/conversao-peso:v1 .
# docker login
# docker push isaacgiordani/conversao-peso:v1
# docker tag isaacgiordani/conversao-peso:v1 isaacgiordani/conversao-peso:latest
# docker image ls
# docker push isaacgiordani/conversao-peso:latest
# docker container run -d -u 1000 -p 8000:80 --cpus="0.5" isaacgiordani/conversao-peso:v1