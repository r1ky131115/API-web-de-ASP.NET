# API-web-de-ASP.NET
En esta ocasión, he creado una API web de ASP.NET Core que se ejecuta en .NET. La API web crea, lee, actualiza y elimina pizzas desde una caché en memoria. Se ha usado una caché en memoria. Esto para poder permitir centrarse en el aprendizaje de conceptos de API web, pero tiene algunas limitaciones obvias para las aplicaciones reales: si la aplicación se detiene o se bloquea, se pierden todos los cambios.


Datos a tener en cuenta: 
En este módulo se usa el SDK de .NET 6.0. Antes de comenzar el módulo, asegúrese de que tiene instalado .NET 6.0 mediante la ejecución del siguiente comando en el terminal que prefiera:

CLI de .NET

dotnet --list-sdks
Verá un resultado similar al siguiente:

Consola:
3.1.100 [C:\program files\dotnet\sdk]
5.0.100 [C:\program files\dotnet\sdk]
6.0.100 [C:\program files\dotnet\sdk]


Compilación y prueba de la API web.

1- Ejecute el comando siguiente de la CLI de .NET Core en el shell de comandos:
  dotnet run

2-Abra un explorador web y vaya a: 
  https://localhost:{PORT}/pizza
 
3- Abra un nuevo terminal integrado desde Visual Studio Code. Para ello, seleccione Terminal > Nuevo terminal en el menú principal y ejecute el siguiente comando:
  dotnet tool install -g Microsoft.dotnet-httprepl
  
4- Conéctese a la API web mediante el comando siguiente:
  httprepl https://localhost:{PORT}
    Para ver el punto de conexión de pizzas ya disponible, ejecute el siguiente comando:
        ls

5- Vaya al punto de conexión Pizza ejecutando el siguiente comando:
  cd Pizza

6- Realice las solicitudes GET, POST, PUT, DELETE en HttpRepl usando el comando siguiente:
  get o get "id"
  post -c "{"name":"Pizza", "isGlutenFree":false}"
  put 3 -c  "{"id": 3, "name":"PizzaNueva", "isGlutenFree":false}"
  delete "id"
