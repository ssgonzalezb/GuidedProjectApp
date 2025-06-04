# Library App


## Description

Library App is a console-based library management system built with .NET 8.0. It allows users to search for patrons, view and manage book loans, and handle membership renewals. The application uses a clean architecture approach, separating core logic, infrastructure, and presentation layers, and persists data in JSON files for easy setup and portability.

## Project Structure

- GuidedProjectApp.sln
- readme.md
- AccelerateDevGitHubCopilot/
  - src/
    - Library.ApplicationCore/
      - Library.ApplicationCore.csproj
      - Entities/
      - Enums/
      - Interfaces/
      - Services/
    - Library.Console/
      - appSettings.json
      - CommonActions.cs
      - ConsoleApp.cs
      - ConsoleState.cs
      - Library.Console.csproj
      - Json/
      - Program.cs
    - Library.Infrastructure/
      - Library.Infrastructure.csproj
      - Data/
  - tests/
    - UnitTests/
      - UnitTests.csproj

## Key Classes and Interfaces

- **Library.ApplicationCore**
  - `Entities/`  
    Core domain models such as `Patron`, `Loan`, `Book`, `BookItem`, and `Author`.
  - `Enums/`  
    Enumerations for domain-specific states and actions.
  - `Interfaces/`  
    - `IPatronRepository`  
    - `ILoanRepository`  
    - `IPatronService`  
    - `ILoanService`  
    Abstractions for repositories and services.
  - `Services/`  
    Business logic implementations for library operations.

- **Library.Infrastructure**
  - `Data/JsonData.cs`  
    Handles loading, saving, and populating entities from JSON files.
  - `Data/JsonPatronRepository.cs`  
    Implements `IPatronRepository` for patron data access.
  - `Data/JsonLoanRepository.cs`  
    Implements `ILoanRepository` for loan data access.

- **Library.Console**
  - `ConsoleApp.cs`  
    Main interactive loop and state management for the console UI.
  - `Program.cs`  
    Application entry point; configures dependency injection and starts the app.
  - `CommonActions.cs`, `ConsoleState.cs`  
    Define user actions and application states.

## Usage

1. **Build the project:**
   ```sh
   dotnet build GuidedProjectApp.sln
   ```

2. **Run the console application:**
   ```sh
   dotnet run --project AccelerateDevGitHubCopilot/src/Library.Console/Library.Console.csproj
   ```

3. **Follow the on-screen prompts** to search for patrons, view details, manage loans, and renew memberships.

## License

This project is licensed under the MIT License. See the LICENSE file for details.