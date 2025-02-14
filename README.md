# JWT Authentication API - .NET 8

Este proyecto es una API en **.NET 8** que implementa autenticación mediante **JWT (JSON Web Token)**. Incluye endpoints para autenticación y protección de rutas.

## 🚀 Tecnologías utilizadas

- **.NET 8**
- **ASP.NET Core Web API**
- **JWT Bearer Authentication**
- **Microsoft IdentityModel.Tokens**

## 📦 Instalación

### 1️⃣ Clonar el repositorio
```sh
git clone https://github.com/tu_usuario/AuthApp.git
cd AuthApp
```

### 2️⃣ Instalar paquetes necesarios
Ejecuta los siguientes comandos:
```sh
dotnet add package Microsoft.AspNetCore.Authentication.JwtBearer
dotnet add package Microsoft.IdentityModel.Tokens
```

### 3️⃣ Configurar `appsettings.json`
Edita el archivo `appsettings.json` para definir los valores de autenticación JWT:
```json
{
  "Jwt": {
    "Key": "clave_super_secreta_para_firmar_tokens",
    "Issuer": "tu-api",
    "Audience": "tus-clientes"
  }
}
```
## 🚀 Estructura

![Estructura](https://raw.githubusercontent.com/tu_usuario/tu_repositorio/main/img/autenticacion.png)

## 🚀 Cómo probar

1️⃣ **Obtener un token:**
- Realiza una solicitud `POST` a `api/auth/login` con JSON:

```json
{
  "username": "admin",
  "password": "password123"
}
```

- Recibirás un **token JWT** en la respuesta.

2️⃣ **Usar el token:**
- En cualquier endpoint protegido (`api/secure`), usa el token en **Authorization Header**:

```
Authorization: Bearer TU_TOKEN_AQUI
```

## 📜 Licencia
Este proyecto está bajo la licencia MIT. ¡Siéntete libre de usarlo y modificarlo! 🚀

