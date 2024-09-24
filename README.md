<<<<<<< HEAD
# TestApiFor-Al-Hilal
# Product API

## Описание проекта

Product API — это REST API для управления продуктами, который поддерживает выполнение CRUD операций, а также экспорт данных в формате CSV. API предоставляет функционал для добавления, чтения, обновления и удаления продуктов с возможностью пагинации и фильтрации данных.

## Возможности API

- Добавление нового продукта.
- Получение списка продуктов с пагинацией.
- Обновление данных продукта по его ID.
- Удаление продукта по его ID.
- Экспорт всех продуктов в формате CSV.

## Требования

- .NET 6 или выше
- MS SQL Server (локальная база данных или контейнер Docker)
- Entity Framework Core

## Настройка проекта

### Шаги по клонированию репозитория

1. Склонируйте репозиторий:

    ```bash
    git clone https://github.com/USEC12/ProductApi.git
    cd ProductApi
    ```

### Установка зависимостей

2. Установите необходимые зависимости:

    ```bash
    dotnet restore
    ```

### Настройка строки подключения

3. Откройте файл `appsettings.json` и настройте строку подключения к MS SQL Server:

    ```json
    "ConnectionStrings": {
        "DefaultConnection": "Server=(localdb)\\mssqllocaldb;Database=ProductDb;Trusted_Connection=True;"
    }
    ```

    - Или настройте Docker-контейнер с MS SQL:

      ```json
      "ConnectionStrings": {
          "DefaultConnection": "Server=localhost,1433;Database=ProductDb;User Id=sa;Password=password123;"
      }
      ```

### Выполнение миграций

4. Примените миграции для создания базы данных:

    ```bash
    dotnet ef database update
    ```

## Запуск приложения

5. Запустите приложение с помощью команды:

    ```bash
    dotnet run
    ```

6. Откройте браузер и перейдите по адресу `https://localhost:7019/swagger` для доступа к Swagger UI и тестирования API.

## Использование API

### Примеры запросов с использованием cURL или Postman

#### 1. Добавление нового продукта

**Запрос:**

```bash
POST /api/products
Content-Type: application/json

{
  "name": "Product Name",
  "description": "Product Description",
  "price": 19.99
}

Получение списка продуктов с пагинацией:
GET /api/products?pageNumber=1&pageSize=10

Обновление продукта по ID:
PUT /api/products/{id}
Content-Type: application/json

{
  "id": 1,
  "name": " Product Name",
  "description": "Product Description",
  "price": 29.99
}
Удаление продукта по ID:
DELETE /api/products/{id}

 Экспорт данных в CSV:
GET /api/products/export

Swagger UI доступен по адресу:
https://localhost:7019/swagger
Документация API автоматически генерируется Swagger-ом.
=======
# TestApiFor-Al-Hilal
>>>>>>> 48df6259ff854bf391830c37b7964e5807c97e97
