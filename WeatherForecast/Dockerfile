FROM mcr.microsoft.com/dotnet/sdk:7.0

WORKDIR /workshop

COPY . ./

WORKDIR /workshop/WeatherForecast
RUN dotnet build

ENTRYPOINT dotnet run
