FilesStorage
Overview
FilesStorage is a proof-of-concept (POC) file-sharing application built with C# .NET 9 (backend) and intended for integration with a ReactJS frontend. The backend provides a REST API to allow authenticated users to upload, store, and retrieve files (images and documents, up to 100MB each) in a PostgreSQL database, with a per-user storage limit of 10MB. If the limit is exceeded, the API returns an error message, which the frontend can use to display a popup. The project follows Clean Architecture, SOLID principles, and best practices like async operations, dependency injection, and secure JWT-based authentication.
This project is designed to help learn the complete flow of a .NET backend, including database integration, file handling, and API development, while preparing for future scalability (e.g., adding cloud storage like MinIO or Azure Blob Storage later).
Features

User Authentication: JWT-based authentication with user registration and login.
File Upload: Upload files (PNG, JPEG, PDF, DOCX) up to 100MB, stored as blobs in PostgreSQL.
Storage Limit: Enforces a 10MB per-user limit, returning an error if exceeded.
File Retrieval: List user files with metadata (excluding blobs for performance).
API Notifications: Returns messages (e.g., "Uploaded to database" or "Storage limit exceeded") for frontend popups.
Clean Architecture: Organized into Controllers, Services, Repositories, Entities, and DTOs.
Best Practices: Async I/O, streaming file uploads, input validation, and secure file handling.

Tech Stack

Backend: C# .NET 9.0.2019
Database: PostgreSQL (local)
Authentication: ASP.NET Core Identity with JWT
Tools: Visual Studio Code, pgAdmin 4, Postman (for testing)
Frontend: ReactJS (to be integrated by the user)

Prerequisites

.NET SDK: 9.0.2019 (install via sudo apt install dotnet-sdk-9.0)
PostgreSQL: Version 12 or higher (default port: 5432)
pgAdmin 4: For database management
Ubuntu: Tested on Ubuntu (other OSes may work with adjustments)
Node.js: For the React frontend (not covered here)

Contributing
Feel free to submit issues or pull requests on GitHub. Ensure code follows Clean Architecture and SOLID principles.
License
MIT License (or your preferred license).
