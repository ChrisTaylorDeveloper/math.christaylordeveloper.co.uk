# math.christaylordeveloper.co.uk

Development
```
docker run -it --volume $(pwd):/source --workdir /source mcr.microsoft.com/dotnet/sdk:7.0
dotnet build
```

Delete build files
```
rm -rf aspnetapp/bin/ aspnetapp/obj/
```

Production
```
docker build -t aspnetapp .
docker run --env ASPNETCORE_ENVIRONMENT=Development -d -it --rm -p 80:80 --name math_ctd_co_uk aspnetapp
```
