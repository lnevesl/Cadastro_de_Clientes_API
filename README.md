📌 Sobre o Projeto
Este projeto permite realizar operações completas de CRUD de clientes, incluindo:

✅ Cadastro de cliente
📄 Listagem de clientes ativos
🔍 Busca por ID
✏️ Atualização de dados
❌ Exclusão lógica (soft delete)

A aplicação utiliza o conceito de soft delete, mantendo os registros no banco de dados, mas marcando-os como inativos.

🧱 Arquitetura
O projeto segue o padrão em camadas:
controller → service → repository → entity
Controller → Recebe as requisições HTTP
Service → Contém a lógica de negócio
Repository → Comunicação com o banco (JPA)
DTOs → Transferência de dados


🛠️ Tecnologias Utilizadas
Java 17+
Spring Boot
Spring Data JPA
Lombok
Maven
H2 / PostgreSQL (configurável)


📂 Estrutura do Projeto
cadastroCliente
 └── controller
 └── dto
 └── service
 └── persistence
      ├── entities
      └── repositories

🔗 Endpoints
➕ Criar cliente
POST /cliente
Body:
{
  "nome": "João",
  "telefone": "81999999999"
}
📄 Listar clientes
GET /cliente
🔍 Buscar por ID
GET /cliente/{id}
✏️ Atualizar cliente
PUT /cliente/{id}
Body:
{
  "nome": "Novo Nome",
  "telefone": "88888888"
}
❌ Deletar cliente (soft delete)
DELETE /cliente/{id}
⚙️ Como rodar o projeto
# Clonar o repositório
git clone https://github.com/seu-usuario/seu-repo.git

# Entrar na pasta
cd seu-repo

# Rodar a aplicação
./mvnw spring-boot:run
🧠 Boas práticas aplicadas
✔️ Arquitetura em camadas
✔️ Separação de responsabilidades
✔️ Uso de DTOs
✔️ Soft delete
✔️ Tratamento de exceções com Optional
✔️ Código limpo e legível
📈 Melhorias futuras
🔐 Validação com Bean Validation (@Valid)
📊 Paginação e filtros
📦 Dockerização
📑 Documentação com Swagger (OpenAPI)
🔒 Autenticação com JWT
👨‍💻 Autor
Desenvolvido por Lucas Neves 🚀
Se quiser trocar ideia sobre backend, só chegar!
