# DevOps Project

## Opis
Aplikacja webowa .NET z endpointami / i /products, uruchamiana w Dockerze, z testami jednostkowymi.

## Uruchomienie lokalnie
1. docker build -t devopsapp:latest .
2. docker run -d -p 5055:80 --name devopsapp-container devopsapp:latest
3. Sprawdü w przeglπdarce:
   - http://localhost:5055/
   - http://localhost:5055/products

## Testy jednostkowe
dotnet test