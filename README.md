📌 About the Project
This project provides full CRUD operations for customer management, including:
✅ Create customer
📄 List active customers
🔍 Find customer by ID
✏️ Update customer data
❌ Logical deletion (soft delete)
The application uses the soft delete approach, meaning records are not physically removed from the database but marked as inactive instead.
🧱 Architecture
The project follows a layered architecture:
controller → service → repository → entity
Controller → Handles HTTP requests
Service → Contains business logic
Repository → Database communication (JPA)
DTOs → Data transfer between layers
🛠️ Technologies Used
Java 17+
Spring Boot
Spring Data JPA
Lombok
Maven
H2 / PostgreSQL (configurable)
📂 Project Structure
cadastroCliente
 └── controller
 └── dto
 └── service
 └── persistence
      ├── entities
      └── repositories
🔗 Endpoints
➕ Create Customer
POST /cliente
Body:
{
  "nome": "João",
  "telefone": "81999999999"
}
📄 List Customers
GET /cliente
🔍 Get Customer by ID
GET /cliente/{id}
✏️ Update Customer
PUT /cliente/{id}
Body:
{
  "nome": "New Name",
  "telefone": "88888888"
}
❌ Delete Customer (Soft Delete)
DELETE /cliente/{id}
⚙️ How to Run the Project
# Clone the repository
git clone https://github.com/your-username/your-repo.git

# Navigate to the folder
cd your-repo

# Run the application
./mvnw spring-boot:run
🧠 Best Practices Applied
✔️ Layered architecture
✔️ Separation of concerns
✔️ DTO usage
✔️ Soft delete implementation
✔️ Exception handling with Optional
✔️ Clean and readable code
📈 Future Improvements
🔐 Validation with Bean Validation (@Valid)
📊 Pagination and filtering
📦 Docker support
📑 API documentation with Swagger (OpenAPI)
🔒 Authentication with JWT
👨‍💻 Author
Developed by Lucas Neves 🚀
Feel free to reach out if you want to talk about backend development!
