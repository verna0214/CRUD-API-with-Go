# Movie API

This is a simple Movie API built with Go using the [Gorilla Mux](https://github.com/gorilla/mux) router. It provides basic CRUD functionality to manage a list of movies.

## Features

- **Get all movies**: Retrieve a list of all movies.
- **Get a specific movie**: Retrieve details of a specific movie by its ID.
- **Create a movie**: Add a new movie to the list.
- **Update a movie**: Update details of an existing movie by its ID.
- **Delete a movie**: Remove a movie from the list by its ID.

## Prerequisites

To run this project, you will need:

- Go 1.22.5
- Gorilla Mux package (`github.com/gorilla/mux`)

## Installation

1. Clone the repository:
  ```bash
  git clone https://github.com/yourusername/movie-api.git
  ```

2. Navigate to the project directory:
  ```bash
  cd Go-movies-crud
  ```

3. Install the dependencies:
  ```bash
  go mod tidy
  ```


## Running the API
The server will start on port 8000. You can test the API using tools like Postman or curl.
  ```bash
  go run main.go
  ```

## API Endpoints

#### Get All Movies
This endpoint returns a list of all movies.
  ```bash
  GET /movies
  ```

#### Get a Single Movie
This endpoint returns the details of a specific movie by ID.
  ```bash
  GET /movies/{id}
  ```

#### Create a  Movie

  ```bash
  POST /movies
  ```
This endpoint allows you to create a new movie. The request body should contain JSON data in the following format:
```
{
  "isbn": "movie-isbn",
  "title": "movie-title",
  "director": {
    "firstname": "director-firstname",
    "lastname": "director-lastname"
  }
}
```

#### Update a Movie
This endpoint allows you to update an existing movie by ID. The request body should contain JSON data in the same format as the create request.
  ```bash
  PUT /movies/{id}
  ```

#### Delete a Movie
This endpoint deletes a movie by its ID.
  ```bash
  DELETE /movies/{id}
  ```



## Example Movie Data
Here is an example of the movie data used by the API:
```
{
  "id": "1",
  "isbn": "438227",
  "title": "Movie One",
  "director": {
    "firstname": "John",
    "lastname": "Doe"
  }
}
```