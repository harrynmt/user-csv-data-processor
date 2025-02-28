# user-csv-data_processor
Processes user data from CSV files via a Django REST Framework API with validation.

This will execute all the unit tests defined in the `csv_handler` app.

## API Endpoints

*   **POST `/api/upload/`**: Uploads a CSV file and processes the user data.

    *   **Request**: `multipart/form-data` with a file field named `file`.
    *   **Response**: JSON object summarizing the upload results (total saved, total rejected, detailed errors).
    *   Test endpoint can be accessed via UI for uploading CSV files on the path `/upload_form/`.
*   **GET `/admin/`**: Django Admin interface for manually managing the users data models. Requires superuser credentials.
    *   Test endpoint can be accessed via UI on the home page `/`.

### Admin Interface
- **GET /admin/**: Provides access to the Django Admin interface for managing user data models.
  - Requires superuser credentials.

## Running Tests

To run all unit tests for the `csv_handler` app, use the following command:
python manage.py test csv_handler
python manage.py test --verbosity=2

## Contributing

Contributions are welcome! To contribute, please follow these steps:

1.  Fork the repository.
2.  Create a new branch for your feature or bug fix.
3.  Make your changes and commit them with descriptive messages.
4.  Submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE) - see the `LICENSE` file for details.
