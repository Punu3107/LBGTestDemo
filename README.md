# LBGTechTest is Demo application with MVVM Architecture and Swift.  
## Overview  
LBGTechTest is Demo application with MVVM Architecture and Swift. It is an iOS application designed with Clean MVVM Architecture principles and modularity. This project demonstrates a scalable, maintainable, and testable architecture, having dependency injection, protocol-oriented programming, and clear separation of concepts.  

## Project Structure  
This project organised in  different layer structure and each layer have used for specific functionality:

- **AppDelegate:** Handle and manage the way the app is shown.. 
- **Views:** UI components and view lifecycle.
- **ViewModel:** Manage layer between UI and Model.
- **Models:** Model for handling the data.
- **Interface:** handles the Repository and Datasource.
- **Core:** Configuration, network and utilities classes.  

## Responsibilities  
### App
- **APPDelegate.swift:** Entry point of the application, responsible for the application lifecycle and setup.
- **SceneDelegate.swift:** Responsible for what is shown on the screen (Windows or Scenes).

### Views
- **LBGViewContoller.swift:** Main view displaying data on the view.
- **LBGViewContoller+Extensions.swift:** Extension for the viewcontroller class.

### ViewModels
- **LBGViewModel.swift:** View model for managing data presentation logic.

### Interfaces
Defines protocols for repositories and data sources, ensuring a clear contract between layers.
- **DogsDataRepository.swift:** Protocol for data repositories.
- **DogsDataRepositoryClass.swift:** Implementation of data repository.

### UseCaseRepository
Contains business logic and application-specific rules.
- **FetchDataUseCase.swift:** Use case for fetching data.

## Core
**Repositories**
- **DogsFactDataSource.swift:** Implementation of facts data source using remote APIs.

**Remote**: Contains data sources for fetching data from remote APIs.
- **RemoteUserDataSource.swift:** Implementation of remote data source using remote APIs.

 **API:** Contains data sources for fetching data from remote APIs.
- **LBGNetworkManager.swift:** Handles HTTP requests and responses.
- **APIConfiguration.swift:** Constructs URLs for API endpoints.
- **ConfigurationManager.swift:** Manages application configurations.

**Utilities:** Contains shared utilities and helpers.
- **ClientAPIProtocol.swift:** Protocol for API client.
- **ConfigurationProtocol.swift:** Protocol for configuration.  

## Dependency Injection  
The project leverages dependency injection pattern that can significantly enhance the modularity, testability, and maintainability of application. Dependencies are injected through initializers, allowing for easy substitution of implementations during testing.
