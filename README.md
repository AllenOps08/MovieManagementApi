```

# Movie Management API

This is a simple RESTful API built with Go (Golang) using the Gorilla Mux router. It provides endpoints to manage movies, including retrieving all movies, retrieving a single movie by ID, creating a new movie, updating an existing movie, and deleting a movie.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/MovieManagementApi.git
   ```

2. Navigate to the project directory:
   ```bash
   cd MovieManagementApi
   ```

3. Build the Go application:
   ```bash
   go build
   ```

4. Run the executable:
   ```bash
   ./MovieManagementApi
   ```

## Usage

### Endpoints

- **GET /movies**: Retrieve all movies.
- **GET /movies/{id}**: Retrieve a single movie by ID.
- **POST /movies**: Create a new movie.
- **PUT /movies/{id}**: Update an existing movie.
- **DELETE /movies/{id}**: Delete a movie.

### Sample Movie JSON Format

```json
{
  "id": "1",
  "isbm": "438227",
  "title": "Movie One",
  "director": {
    "firstname": "Ak",
    "lastname": "Doe"
  }
}
```

### Example Usage

- Retrieve all movies:
  ```bash
  curl http://localhost:8000/movies
  ```

- Retrieve a single movie by ID:
  ```bash
  curl http://localhost:8000/movies/1
  ```

- Create a new movie:
  ```bash
  curl -X POST -H "Content-Type: application/json" -d '{"isbm": "123456", "title": "New Movie", "director": {"firstname": "John", "lastname": "Doe"}}' http://localhost:8000/movies
  ```

- Update an existing movie:
  ```bash
  curl -X PUT -H "Content-Type: application/json" -d '{"isbm": "123456", "title": "Updated Movie", "director": {"firstname": "Jane", "lastname": "Doe"}}' http://localhost:8000/movies/1
  ```

- Delete a movie:
  ```bash
  curl -X DELETE http://localhost:8000/movies/1
  ```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
```

