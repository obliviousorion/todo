# Todo Application

This is a simple Todo application built with the Gin web framework and GORM for SQLite database interaction.

## Prerequisites

- Go 1.16 or later
- GCC (for CGO support)
- SQLite

## Installation

1. Clone the repository:

    ```sh
    git clone https://github.com/obliviousorion/todo.git
    cd todo
    ```

2. Install dependencies:

    ```sh
    go mod tidy
    ```

3. Ensure `gcc` is installed:

    ```sh
    sudo apt update
    sudo apt install build-essential
    ```

## Running the Application

1. Set the `CGO_ENABLED` environment variable to `1`:

    ```sh
    export CGO_ENABLED=1
    ```

2. Build and run the application:

    ```sh
    go run main.go
    ```

## API Endpoints

### Create a Todo

- **URL**: `/todos`
- **Method**: `POST`
- **Request Body**:

    ```json
    {
        "title": "Sample Todo",
        "description": "This is a sample todo item"
    }
    ```

- **Response**:

    ```json
    {
        "ID": 1,
        "CreatedAt": "2023-01-20T00:56:14Z",
        "UpdatedAt": "2023-01-20T00:56:14Z",
        "DeletedAt": null,
        "title": "Sample Todo",
        "description": "This is a sample todo item"
    }
    ```

### Get All Todos

- **URL**: `/todos`
- **Method**: `GET`
- **Response**:

    ```json
    [
        {
            "ID": 1,
            "CreatedAt": "2023-01-20T00:56:14Z",
            "UpdatedAt": "2023-01-20T00:56:14Z",
            "DeletedAt": null,
            "title": "Sample Todo",
            "description": "This is a sample todo item"
        }
    ]
    ```

## License

This project is licensed under the MIT License.
