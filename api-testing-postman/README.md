# API Testing con Postman y Newman

Suite automatizada de pruebas de API REST contra JSONPlaceholder, validando el ciclo CRUD (GET, POST, PUT, DELETE) y manejo de errores (404 Not Found) mediante Newman y reportes HTML.

## Ejecucion
1. Instalar dependencias: npm install
2. Ejecutar pruebas: npx newman run jsonplaceholder-tests.postman_collection.json -r cli,htmlextra --reporter-htmlextra-export reports/reporte-api.html

## Cobertura
- GET /users/1 (200 OK y validacion de estructura)
- POST /posts (201 Created)
- PUT /posts/1 (200 OK)
- DELETE /posts/1 (200 OK)
- GET /users/99999 (Caso negativo 404 Not Found)
