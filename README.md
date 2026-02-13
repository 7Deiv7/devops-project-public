DevOps Project
Opis
Aplikacja webowa .NET z endpointami / i /products, uruchamiana w Dockerze, z testami jednostkowymi.

Aplikacja ma dwa endpointy:

'/' → zwraca tekst: Hello DevOps!
'/products' → zwraca listę produktów w formacie JSON:
[
{ "id": 1, "name": "Laptop" },
{ "id": 2, "name": "Phone" }
]

Wymagania
Docker Desktop uruchomiony w tle
.NET SDK 9.x
PowerShell (Windows) lub terminal (Linux/Mac)
Uruchomienie lokalnie
docker build -t devopsapp:latest .
docker run -d -p 5055:80 --name devopsapp-container devopsapp:latest
Sprawdz w przegladarce:
http://localhost:5055/
http://localhost:5055/products
Testy jednostkowe
Uruchom testy poleceniem:

dotnet test ./DevopsApp.Tests/DevopsApp.Tests.csproj --logger "trx;LogFileName=test_results.trx"
