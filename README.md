# n8n · Recordatorios de cita desde Google Sheets (gratis)

Free n8n workflow that emails each client a reminder 24 h before their appointment, reading bookings from a Google Sheet. Built for hair salons and barbershops in Spain, works for any appointment-based business.

**ES:** Flujo gratuito de n8n que envía un recordatorio por email 24 h antes de cada cita, leyendo la agenda de una hoja de Google.

## Files
- `recordatorio_citas_email_ES.json`: Spanish version (node names and notes in Spanish)
- `send-appointment-reminders-google-sheets_EN.json`: English version (same logic)
- `Citas.csv`: sample appointments tab (columns: id, fecha, hora, cliente, email, telefono, servicio, profesional, estado, recordatorio_enviado)

## Setup (15 min)
1. Import the JSON in n8n (Workflows → Import from file).
2. Upload `Citas.csv` to Google Sheets as a tab named **Citas**.
3. Fill in the settings node (sheet ID, business name, sender, phone, address, links).
4. Attach Google Sheets and SMTP credentials, run it once, then activate.

## Notes
- Runs hourly from 8:00 to 21:00 and never double-sends (it writes a timestamp to the row).
- Handles `YYYY-MM-DD`, `DD/MM/YYYY` and Sheets serial dates in your timezone.
- You are responsible for your clients' consent (GDPR/LOPDGDD).

License: MIT · Provided as is, without warranty. · Automatiza.es · automatizaes.soporte@gmail.com
