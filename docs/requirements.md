# Requirements
# Requirements

ClinicQ Phase 1 serves a single walk-in clinic with one doctor, where patients are seen in order of arrival.

## Users

### Patient
- Needs: know their turn and waiting time without sitting in the waiting room
- Uses: a link or QR code on their phone, plus SMS
- Technical level: low; many use basic smartphones

### Receptionist
- Needs: run the queue fairly and quickly; add patients without smartphones
- Uses: staff screen on a clinic computer or tablet, all day
- Technical level: basic computer skills

### Doctor
- Needs: see who is next and signal when a consultation is finished
- Uses: large "Call next" and "Done" buttons
- Technical level: busy; must work in seconds

## Features

### Core (product is useless without these)
- Patient self-joins by clinic link or QR code (name and phone, no login)
- Token number with live position and estimated wait
- Receptionist can add a patient manually
- Call next and mark done
- Duplicate protection (one active entry per name and number)

### High priority (90/100)
- SMS with tracking link and "your turn is near" message
- Skip and rejoin with grace timer and staff override
- Staff login with roles (receptionist, doctor)
- Queue open and close window
- Status history (audit log)
- Patient can cancel their own entry

### Stretch (10/100)
- "I'm on my way" and Joined/Arrived states
- Multiple clinics and dashboards (Phase 2)

### Out of scope
- Appointments, prescriptions, inventory, analytics, billing, medical records

## Screens

| Screen | Patient | Receptionist | Doctor |
|---|---|---|---|
| Join page | Yes | | |
| Tracking page | Yes | | |
| Staff login | | Yes | Yes |
| Queue board | | Yes | View |
| Add patient manually | | Yes | |
| Call next, done, skip, rejoin override | | Yes | Call next, done |
| Open/close queue, clinic QR code | | Yes | |
| History view | | Yes | |

## Quality priorities
- **Ease of use (primary):** joining takes under 30 seconds, with no app and no login
- **Integrity (primary):** fair, correct queue order; no duplicates, no lost turns, every change recorded
- **Availability:** important during clinic hours; staff can fall back to paper during short outages
- **Security:** staff actions need login; patient pages show only minimum data
