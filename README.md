# Arenaweb Booking System

Sistema de reservas con calendario de Google, horarios de negocio y API REST.

## 📋 Descripción

Sistema de reservas automatizado que se integra con Google Calendar. Elimina semanas de desarrollo proporcionando dos APIs REST potentes que manejan todo, desde validación de entrada hasta integración con calendario.

### Características

- ✅ **Integración con Google Calendar** - Crea eventos automáticamente
- ✅ **Google Meet** - Genera enlaces de Meet para cada reserva
- ✅ **Horario de negocio** - Valida horas laborales (9:30 AM - 9:30 PM)
- ✅ **Control de almuerzos/cenas** - Bloquea 12:30-14:30 y 18:30-20:30
- ✅ **Fines de semana** - No permite reservas
- ✅ **Festivos** - Detecta festivos públicos automáticamente
- ✅ **Detección de conflictos** - Evita reservas superpuestas
- ✅ **Validación de datos** - Verifica email, teléfono y campos requeridos

### APIs REST

| Endpoint | Descripción |
|----------|-------------|
| `/make-booking` | Crear reserva con validaciones |
| `/check-booking-date` | Consultar disponibilidad |

### Uso

1. Configura los webhooks en n8n
2. Integra el formulario HTML en tu sitio
3. Las reservas se crean automáticamente en Google Calendar

### Demo

- [Pruébalo](https://arenabotdo.github.io/booking-form)
- [Código fuente](https://github.com/arenabotdo/booking-form)

## Tech Stack

- **Frontend:** HTML, CSS, JavaScript (vanilla)
- **Backend:** n8n (webhooks)
- **Calendar:** Google Calendar API

## Licencia

MIT
