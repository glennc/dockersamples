FROM microsoft/aspnetcore:1.0.1
ENTRYPOINT ["dotnet", "API.dll"]
ARG source=.
WORKDIR /app
ENV ASPNETCORE_URLS=http://+:80;http://localhost:8080
HEALTHCHECK --interval=1m --timeout=3s CMD curl -f http://localhost:8080 || exit 1
EXPOSE 80
COPY $source .
