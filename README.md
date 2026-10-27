# n8n · Recordatorios de cita desde Google Sheets (gratis)

Free n8n workflow that emails each client a reminder 24 h before their appointment, reading bookings from a Google Sheet. Built for hair salons and barbershops in Spain, works for any appointment-based business.

**ES:** Flujo gratuito de n8n que envía un recordatorio por email 24 h antes de cada cita, leyendo la agenda de una hoja de Google.

## Files
- `recordatorio_citas_email_ES.json`: Spanish version (node names and notes in Spanish)
- `send-appointment-reminders-google-sheets_EN.json`: English version (English node names, sheet columns and email text; also handles MM/DD/YYYY dates, 12-hour times and failed sends)
- `Citas.csv`: sample tab for the Spanish version (columns: id, fecha, hora, cliente, email, telefono, servicio, profesional, estado, recordatorio_enviado)
- `appointments_sample_EN.csv`: sample tab for the English version, named **Appointments** (columns: id, date, time, client_name, email, service, staff, status, reminder_sent)

## Setup (15 min)
1. Import the JSON in n8n (Workflows → Import from file).
2. Upload `Citas.csv` (Spanish version) as a tab named **Citas**, or `appointments_sample_EN.csv` (English version) as a tab named **Appointments**.
3. Fill in the settings node (sheet ID, business name, sender, phone, address, links).
4. Attach Google Sheets and SMTP credentials, run it once, then activate.

## Notes
- Runs hourly from 8:00 to 21:00 and never double-sends (it writes a timestamp to the row).
- Handles `YYYY-MM-DD`, `DD/MM/YYYY` and Sheets serial dates in your timezone.
- You are responsible for your clients' consent (GDPR/LOPDGDD).

License: MIT · Provided as is, without warranty. · Automatiza.es · automatizaes.soporte@gmail.com
