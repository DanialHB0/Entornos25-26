### Requisitos Tecnicos TapatAPP
# Arquitectura

[Client Servidor](charts/mvc-generic.mermaid)

### 1. Backend (Servidor 1 Gestion de Datos)

El backend sera el corazon del sistema, encargado de gestionar datos y usuarios.
1. La logica del sistema

## a. Requisitos del Servidor
-Alojamiento: Hosting Compartido
-Base de datos: Mysql o MariaDB
-Sistema Operatrivo: Linux o Windows
-WebService: RESTful llibreria Python Flask

## b. Lenguajes de Programacion
Python o Java

## c. Seguridad
-Autentificacion y autorizacion de usuarios
-Cifrado de datois HTTPS
-Copias de seguridad automaticas

### 2. Frontend

## a. Tipos de Clientes
- App Mobil: Android
- Consola Python
- Framework Multiplataforma: Flutter (Apps, IOS,, Android, Web, Desktop)

## b. Almacenamiento local y sincronizacion
- Datos guardados en local: Token, nickname
- Seguridad: HTTPS, autentificacion servicios por Token

## c. Gestion de Accesibilidad
- Niveles A, AA, AAA de accesibilidad

# 3. Requisitos Generales de Infraestructura

## a. Gestion de Usuarios
- Roles de Usuario: Tutores y Cuidador
- Seguridad: Contraseña, md5m, sha256 o sha512

## b. Requisitos de Infraestructura
- Xarxa: Internet
- Espacio de almacenamiento al Servidor: 1TB
- APIs a terceros: No se usan

### 4. Requisitos del Proceso de Desarrollo
- IDEs: VSCode, Python, Android Studio, PyCharm
- Controles de versiones: Github
- Metodologia de desarollo: SCRUM
- Testing y provas de calidad: Tests y pruebas unitarias