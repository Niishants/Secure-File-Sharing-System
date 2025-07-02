## Secure File Sharing System
<hr>

### Features

#### Technology Stack
- **Framework**: Flask
- **Database**: MongoDB
- **Authentication**: JWT (JSON Web Tokens)
- **File Type Detection**: python-magic
  - The file type is determined not only by the file extension but also by analyzing its contents.
<hr>

### Security Considerations
- File types are verified by content, not just extension
- Download URLs are encrypted and have a short expiration time
- User passwords are hashed before storage
<hr>

### API Endpoints
#### Authentication
- **POST** `/signup`: Sign up a new user
- **GET** `/verify-email/<token>`: Verify user's email
- **POST** `/login`: Log in a user

#### File Operations
- **POST** `/upload`: Upload a file (Operation Users only)
- **GET** `/files`: List all uploaded files
- **GET** `/download/<file_id>`: Generate a download link for a file
- **GET** `/secure-download/<token>`: Download a file using a secure token
<hr>

### Testing
To run the test suite:
```shell
pytest -v tests/
```
You can check out a previous pytest log at [tests/test_results.log](tests/test_results.log) <br>

View the postman tests run summary at [assets/Secure File Sharing System.postman_test_run.json](assets/Secure%20File%20Sharing%20System.postman_test_run.json) <br>

<p align="center">
  <img width="700" src="assets/Postman%20Test%20Summary.png">
</p>

You can also import the Postman collection at [assets/Secure File Sharing System.postman_collection.json](assets/Secure%20File%20Sharing%20System.postman_collection.json)
<hr>
