# Smart Home and Device Management Backend 

## Project Overview

The purpose of our project is to revolutionize the management of smart home ecosystems by creating an integrated mobile application and website. Our aim is to empower users to control and monitor their Internet of Things (IoT) devices effortlessly, thereby enhancing convenience, energy efficiency, and security within their homes. 

## Technology Stack

### ASP.NET Core
- **Purpose**: Build the web API for handling client requests.
- **Benefits**: High performance, cross-platform, and supports dependency injection for better testability.

### Clean Architecture
- **Purpose**: Structuring the codebase to be maintainable, scalable, and testable.
- **Benefits**: Separation of concerns, independent of frameworks, and facilitates test-driven development.

### C#
- **Purpose**: Primary programming language for backend development.
- **Benefits**: Strongly typed, object-oriented, and integrated seamlessly with the .NET framework.

### SQL Server
- **Purpose**: Database management.
- **Benefits**: High performance, robust transaction processing, and integration with Azure services.

### Azure App Service
- **Purpose**: Hosting the web API.
- **Benefits**: Easy deployment, scaling, and management.

## Database Design

The project uses **SQL Server** hosted on **Azure**. Key tables include:

- **AspNetUsers**: Stores user information such as IDs, names, usernames, emails, and password hashes.
- **Devices**: Stores information about IoT devices, including smart sockets, security sensors, and smart lights. Key attributes include device IDs, names, types, room IDs, and statuses.
- **Rooms**: Stores information about different rooms in the smart home. Key attributes include room IDs, names, and home IDs.
- **Homes**: Stores information about homes, including home IDs, owner IDs, names, and addresses.
- **Users**: Stores additional user details such as user IDs, names, emails, passwords, and associated home IDs.
- **HomeOwners**: Join table for homes and users, facilitating a many-to-many relationship.

### Entity Relationships

The database schema ensures robust relationships between entities:
- **Home-Room Relationship**: Each home can have multiple rooms, and deleting a home cascades deletions to its rooms.
- **Room-Device Relationship**: Each room can have multiple devices, and deleting a room cascades deletions to its devices.
- **User-Home Relationship**: Many-to-many relationship managed through the `HomeOwners` join table, linking users to homes. This allows a single user to own multiple homes and multiple users to access the same home as homeowners.

## API Endpoints

The backend includes several controllers to manage different aspects of the smart home system. Below are the primary endpoints, derived from the 

<img width="1094" alt="Screenshot 2024-07-05 at 18 12 28" src="https://github.com/busecoban/SmartHomeandDeviceManagementBackEnd/assets/73944611/b8aa85ce-1770-472b-8045-a6e092545d9e">

<img width="1085" alt="Screenshot 2024-07-05 at 18 12 38" src="https://github.com/busecoban/SmartHomeandDeviceManagementBackEnd/assets/73944611/be19a1f9-ad89-4b2f-b350-72822dc79f80">

<img width="1084" alt="Screenshot 2024-07-05 at 18 12 45" src="https://github.com/busecoban/SmartHomeandDeviceManagementBackEnd/assets/73944611/a39ccbe7-e96e-492a-91e7-38780bd07e94">

<img width="1086" alt="Screenshot 2024-07-05 at 18 12 51" src="https://github.com/busecoban/SmartHomeandDeviceManagementBackEnd/assets/73944611/d78efef2-8c9e-4223-bbba-8bd1014a5757">

<img width="1083" alt="Screenshot 2024-07-05 at 18 12 59" src="https://github.com/busecoban/SmartHomeandDeviceManagementBackEnd/assets/73944611/6b82c2ac-c9df-4a18-a4e6-e1517b58236e">

<img width="1084" alt="Screenshot 2024-07-05 at 18 13 06" src="https://github.com/busecoban/SmartHomeandDeviceManagementBackEnd/assets/73944611/23406a50-d544-45f6-addd-d88f70865e4f">



### DeviceController

- **GET /api/devices**: Retrieves a list of all devices.
- **GET /api/devices/{id}**: Retrieves a specific device by its ID.
- **POST /api/devices**: Adds a new device.
- **PUT /api/devices/{id}**: Updates an existing device by its ID.
- **DELETE /api/devices/{id}**: Deletes a device by its ID.

### HomeController

- **GET /api/home**: Retrieves information about the home setup.
- **PUT /api/home**: Updates home configuration.

### ProductController

- **GET /api/products**: Retrieves a list of all products.
- **GET /api/products/{id}**: Retrieves a specific product by its ID.
- **POST /api/products**: Adds a new product.
- **PUT /api/products/{id}**: Updates an existing product by its ID.
- **DELETE /api/products/{id}**: Deletes a product by its ID.

### RoomController

- **GET /api/rooms**: Retrieves a list of all rooms.
- **GET /api/rooms/{id}**: Retrieves a specific room by its ID.
- **POST /api/rooms**: Adds a new room.
- **PUT /api/rooms/{id}**: Updates an existing room by its ID.
- **DELETE /api/rooms/{id}**: Deletes a room by its ID.

### UserController

- **GET /api/users**: Retrieves a list of all users.
- **GET /api/users/{id}**: Retrieves a specific user by their ID.
- **POST /api/users**: Adds a new user.
- **PUT /api/users/{id}**: Updates an existing user by their ID.
- **DELETE /api/users/{id}**: Deletes a user by their ID.

## Configuration

- **Database Connection**: Update the connection strings in `appsettings.json` to match your Azure SQL Database credentials.
- **IoT Device Setup**: Configure your IoT devices to communicate with the backend APIs.

## Future Enhancements

- Implement AI-based energy consumption optimization.
- Integrate more types of IoT devices.
- Enhance security features with advanced image and video processing.

## PROJECT TEAM:
- Ibrahim Duman              Back-End Lead
- Buse Çoban                           
- Meryem Ahıskalı            
- Özge Havva Şahin

      
<img width="374" alt="Screenshot 2024-07-05 at 18 46 20" src="https://github.com/busecoban/SmartHomeandDeviceManagementBackEnd/assets/73944611/80b9f2b3-8d20-41a8-b079-b6dc50e56c54">


  
