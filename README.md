# Arenaweb Booking System

Sistema completo de reservas con Google Calendar, horarios de negocio y API REST.

> Basado en el [workflow de n8n](https://n8n.io/workflows/8635-complete-booking-system-with-google-calendar-business-hours-and-rest-api/)

## 📋 Descripción

Sistema de reservas automatizado que se integra con Google Calendar. Elimina semanas de desarrollo proporcionando dos APIs REST potentes que manejan todo, desde validación de entrada hasta integración con calendario.

A diferencia de formularios básicos, este sistema incluye características de nivel empresarial:
- Detección inteligente de conflictos
- awareness de festivos públicos
- Enforcement de horarios de negocio
- Integración automática con Google Calendar y Meet links

### Beneficios

- 🔐 **Privado y gratis** - No necesitás software caro ni preocuparte por fugas de datos
- 🎯 **Todo en uno** - No requiere envío manual de invitaciones. Google Calendar maneja todo y genera enlaces de Meet automáticamente

## ✨ Características

- ✅ **Integración con Google Calendar** - Crea eventos automáticamente
- ✅ **Google Meet** - Genera enlaces de Meet para cada reserva
- ✅ **Horario de negocio** - Valida horas laborales (9:30 AM - 9:30 PM Madrid)
- ✅ **Control de almuerzos/cenas** - Bloquea 12:30-14:30 y 18:30-20:30
- ✅ **Fines de semana** - No permite reservas
- ✅ **Festivos** - Detecta festivos públicos automáticamente (usa Google Calendar gratis)
- ✅ **Detección de conflictos** - Evita reservas superpuestas
- ✅ **Validación de datos** - Verifica email, teléfono y campos requeridos

## 🔌 APIs REST

| Endpoint | Descripción |
|----------|-------------|
| `/make-booking` | Crear reserva con validaciones multi-capa |
| `/check-booking-date` | Lista disponibilidad en tiempo real |

### Flujo de trabajo

1. Frontend llama a la REST API (ej: botón submit)
2. Workflow valida:
   - Input requerido y formato correcto
   - Fecha/hora dentro del horario de negocio
   - Excluye almuerzos/cenas y festivos
   - Verifica conflictos con reservas existentes
3. Crea evento en Google Calendar con Meet link

## 🎯 Para quién es ideal

- 🏥 **Salud**: Clínicas, dentistas, fisioterapia
- 💼 **Servicios profesionales**: Consultores, abogados, contadores, coaches
- 🎓 **Educación**: Universidades, academias, tutoring
- 🏢 **Pequeños negocios**: Salones, spas, servicios técnicos
- 👨💻 **Desarrolladores**: Para integrar rápido en proyectos de clientes
- 🌐 **Agencias digitales**: Soluciones de booking para múltiples clientes
- 🏨 **Eventos**: Alquiler de salas, venues, coworkings

## 🛠 Tech Stack

- **Frontend:** HTML, CSS, JavaScript (vanilla)
- **Backend:** n8n (webhooks)
- **Calendar:** Google Calendar API

## 🚀 Uso

1. Configura los webhooks en n8n
2. Integra el formulario HTML en tu sitio
3. Las reservas se crean automáticamente en Google Calendar

## 📄 Licencia

MIT
