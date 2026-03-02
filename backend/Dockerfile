# Stage 1: Build
FROM mcr.microsoft.com/dotnet/sdk:7.0 AS build
WORKDIR /app

# Copy csproj and restore dependencies
COPY ./api/*.csproj ./MyApi/
RUN dotnet restore ./MyApi/MyApi.csproj

# Copy the rest of the source code
COPY ./api ./MyApi

WORKDIR /app/MyApi

# Publish the app for production
RUN dotnet publish -c Release -o out

# Stage 2: Runtime
FROM mcr.microsoft.com/dotnet/sdk:10.0 AS dev
WORKDIR /app

# Copy the published output from build stage
COPY --from=build /app/MyApi/out .

# Expose ports
EXPOSE 5000
EXPOSE 5001

# Start the app
ENTRYPOINT ["dotnet", "MyApi.dll"]