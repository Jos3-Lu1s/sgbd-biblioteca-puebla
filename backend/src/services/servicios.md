# Servicios del Backend (services/servicios) - Simulación

Este documento describe la lógica de servicios y utilidades reutilizables enfocadas en el procesamiento de datos y notificaciones.

## Servicios Previstos

### 1. Servicio de Notificaciones por Correo (`emailService`)
Lógica para notificar a los usuarios mediante correos electrónicos automáticos en los siguientes eventos:
- Registro exitoso en la plataforma.
- Confirmación de solicitud de préstamo de libros.
- Alertas de retraso en la devolución (programado mediante tareas en segundo plano).

### 2. Servicio de Estadísticas y Reportes (`reporteService`)
Generación de datos agregados para la sección de reportería del administrador:
- Listado de libros más solicitados.
- Gráficas de volumen de préstamos semanales.
- Historial de actividad de usuarios.

_Boceto de arquitectura para el flujo de Git — Sin código ejecutable._
