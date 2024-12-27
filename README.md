# Spring Boot JWT Authentication 🔐

Implementación de autenticación JWT con Spring Boot y Spring Security.

## 🛠️ Tecnologías
- Java 17
- Spring Boot 3.2.3
- Spring Security
- JWT
- MySQL 8

## ⚙️ Configuración
```properties
spring.application.name=SpringJwt
spring.datasource.url=jdbc:mysql://localhost:3306/jwtSB?createDatabaseIfNotExist=true
spring.datasource.username=root
spring.datasource.password=rootroot
```

## 🔒 Endpoints

### Autenticación
| Método | Ruta | Descripción | Roles |
|--------|------|-------------|-------|
| GET | /auth/index | Endpoint público | - |
| POST | /auth/register | Registro de usuario | - |
| POST | /auth/login | Inicio de sesión | - |

### Rutas Protegidas
| Método | Ruta | Descripción | Roles |
|--------|------|-------------|-------|
| GET | /auth/admin/test | Acceso solo admin | ADMIN |
| GET | /auth/user/test | Acceso general | ADMIN, USER |

### Ejemplo Login
```json
{
  "username": "usuario",
  "password": "contraseña"
}
```

## 📁 Estructura
```
SpringJwt/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── springjwt/
│   │   │       ├── config/
│   │   │       ├── control/
│   │   │       ├── entity/
│   │   │       ├── filter/
│   │   │       ├── repository/
│   │   │       ├── service/
│   │   │       └── SpringJwtApplication.java
│   │   └── resources/
│   └── test/
└── pom.xml
```

## 🚀 Instalación
```bash
./mvnw clean install
./mvnw spring-boot:run
```

## 🔑 Uso

1. Registrar usuario
2. Obtener token JWT
3. Incluir token en header: `Authorization: Bearer {token}`
