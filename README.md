# Steps to check C# project coverage using local Sonar Qube

Make sure you have sonar-scanner installed and environment set
OBS: to check it just run
```
sonar-scanner -v
```
## 1. Run the Sonar qube container
```
docker compose up -d
```
## 2. Login and set password to Sonar qube running instance at
```
http://localhost:9000
```
## 3. Create a sonar project and token to push coverage

## 4. Go to the C# project and build the project
```
dotnet build
```
## 4. Test the C# project exporting the coverage result on opencover format
```
dotnet test --collect:"XPlat Code Coverage;Format=opencover"
```
## 3. Copy the sonar-project.properties to the root of the solution

## 4. Run sonar scanner
```
sonar-scanner
```
