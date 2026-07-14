# Arquitectura MVC - SGBD Biblioteca Puebla

Este documento detalla la implementación del patrón Arquitectura Modelo-Vista-Controlador (MVC) para el sistema.

## Capas del Sistema
* **Modelo (Model):** Gestión de la lógica de negocio y mapeo de las tablas de la base de datos (Usuarios, Libros, Préstamos).
* **Controlador (Controller):** Intermediario que recibe las peticiones del frontend, procesa las reglas de negocio y actualiza los modelos.
* **Vista (View):** Interfaz de usuario implementada en la carpeta `frontend` para la interacción con el sistema bibliotecario.