# 🚗 GreenCarWash API

![.NET](https://img.shields.io/badge/.NET-9.0-blue) ![Build Status](https://img.shields.io/badge/build-passing-brightgreen) ![License](https://img.shields.io/badge/license-MIT-green) ![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)

> **Modern ASP.NET Core 9.0 Car Wash Management API** with JWT Authentication, Entity Framework, Real-time Features, and Production-Ready Architecture

## 🌟 Features

### 🔐 **Authentication & Security**
- **JWT Bearer Authentication** with enhanced security
- **Role-based Authorization** (Customer, Admin, Washer)
- **Global Exception Handling** with structured error responses
- **Input Validation** using FluentValidation
- **Security Best Practices** implementation

### 🚗 **Core Functionality**
- **User Management** - Registration, login, profile management
- **Car Management** - Multiple cars per user, car details
- **Package System** - Various wash packages with pricing
- **Order Management** - Place, track, and manage wash orders
- **Add-on Services** - Additional services and customization
- **Review System** - Customer feedback and ratings
- **Promo Codes** - Discount and promotional campaigns

### 🔧 **Technical Excellence**
- **ASP.NET Core 9.0** with modern C# features
- **Entity Framework Core 9.0** with SQL Server
- **Clean Architecture** with repository pattern
- **AutoMapper** for object mapping
- **Performance Indexes** for database optimization
- **Health Checks** for monitoring
- **Swagger/OpenAPI** documentation

### 🚀 **DevOps & Deployment**
- **GitHub Actions** CI/CD pipeline
- **Docker Ready** containerization support
- **Environment Configuration** management
- **Logging & Monitoring** implementation
- **Production Deployment** ready

## 📚 API Documentation

### 🔗 **Main Endpoints**

| Category | Endpoint | Description |
|----------|----------|-------------|
| **Auth** | `POST /api/auth/register` | User registration |
| **Auth** | `POST /api/auth/login` | User login |
| **Cars** | `GET /api/cars` | Get user's cars |
| **Orders** | `POST /api/orders/place` | Place new order |
| **Packages** | `GET /api/packages` | Get available packages |
| **Reviews** | `POST /api/reviews` | Submit review |
| **Health** | `GET /health` | Health check endpoint |

### 📖 **Swagger Documentation**
Access interactive API documentation at: `http://localhost:5053/swagger`

## 🛠️ Installation & Setup

### **Prerequisites**
- .NET 9.0 SDK
- SQL Server (LocalDB or Full)
- Visual Studio 2022 / VS Code

### **Quick Start**

1. **Clone the repository**
```bash
git clone https://github.com/YOUR_USERNAME/GreenCarWash-API.git
cd GreenCarWash-API
```

2. **Configure Database**
```bash
# Update connection string in appsettings.json
# Run migrations
dotnet ef database update
```

3. **Run the Application**
```bash
dotnet run
```

4. **Access the API**
- API: `http://localhost:5053`
- Swagger UI: `http://localhost:5053/swagger`
- Health Check: `http://localhost:5053/health`

### **Configuration**

#### **Database Setup**
```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=YOUR_SERVER;Database=GreenWashDB;User Id=YOUR_USER;Password=YOUR_PASSWORD;TrustServerCertificate=True;"
  }
}
```

#### **JWT Configuration**
```json
{
  "Jwt": {
    "Key": "YOUR_SECRET_KEY_MINIMUM_32_CHARACTERS",
    "Issuer": "GreenCarWashAPI",
    "Audience": "GreenCarWashClient",
    "ExpiresInDays": 7
  }
}
```

## 🏗️ Architecture

### **Project Structure**
```
├── Controllers/          # API Controllers
├── Models/              # Entity Models
├── Data/                # DbContext & Configuration
├── Repository/          # Data Access Layer
├── Services/            # Business Logic Layer
├── DTO/                 # Data Transfer Objects
├── Interfaces/          # Contracts & Abstractions
├── Middleware/          # Custom Middleware
├── Validators/          # Input Validation
├── Common/              # Shared Components
└── Migrations/          # Database Migrations
```

### **Technology Stack**
- **Backend**: ASP.NET Core 9.0, C# 12
- **Database**: SQL Server, Entity Framework Core 9.0
- **Authentication**: JWT Bearer Tokens
- **Validation**: FluentValidation
- **Mapping**: AutoMapper
- **Documentation**: Swagger/OpenAPI
- **Testing**: Unit Tests (Future)
- **DevOps**: GitHub Actions, Docker

## 🔄 CI/CD Pipeline

### **GitHub Actions Workflow**
- ✅ **Build & Test** on every push/PR
- ✅ **Security Scanning** with CodeQL
- ✅ **Automated Deployment** to staging/production
- ✅ **Docker Image** building and publishing

### **Quality Gates**
- Code compilation
- Unit test execution  
- Security vulnerability scanning
- Code quality analysis

## 🌐 Deployment

### **Environment Support**
- **Development**: Local development with SQL LocalDB
- **Staging**: Test environment with full SQL Server
- **Production**: Cloud deployment ready (Azure/AWS)

### **Docker Deployment**
```dockerfile
# Build and run with Docker
docker build -t greencarwash-api .
docker run -p 5053:80 greencarwash-api
```

### **Cloud Deployment**
Ready for deployment to:
- Azure App Service
- AWS ECS/Elastic Beanstalk  
- Google Cloud Run
- Any container platform

## 🤝 Contributing

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/AmazingFeature`)
3. **Commit** your changes (`git commit -m 'Add some AmazingFeature'`)
4. **Push** to the branch (`git push origin feature/AmazingFeature`)
5. **Open** a Pull Request

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Ritik Singh**
- GitHub: [@YOUR_GITHUB_USERNAME](https://github.com/YOUR_GITHUB_USERNAME)
- LinkedIn: [Your LinkedIn Profile](https://linkedin.com/in/YOUR_PROFILE)

## 🙏 Acknowledgments

- Built with modern .NET 9.0 framework
- Inspired by clean architecture principles
- Follows industry best practices for API development

---

⭐ **Star this repository** if you find it helpful!

🐛 **Report issues** [here](https://github.com/YOUR_USERNAME/GreenCarWash-API/issues)

💡 **Request features** [here](https://github.com/YOUR_USERNAME/GreenCarWash-API/issues)
