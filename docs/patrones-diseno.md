# Patrones de Diseño - SGBD Biblioteca Puebla

Este documento describe los patrones de diseño de software aplicados para resolver problemas comunes en el desarrollo del sistema.

## Patrones Implementados
* **Singleton:** Utilizado en la conexión a la base de datos para asegurar que exista una única instancia del pool de conexiones en todo el backend.
* **Data Access Object (DAO):** Aplicado para separar la lógica de acceso a datos de la lógica de negocio de usuarios, libros y préstamos.