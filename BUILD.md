# BUILD — MINI COMPANY IN A BOX GENERATOR

## CLIENT NAME
Sarah

## BUILD LOCATION
/Departments/Sarah/

## PURPOSE
This BUILD.md creates a complete mini-company-in-a-box for the client.  
The system must include:
- Business department modules (MFCF)
- Backend (offline-first capable)
- Frontend (mobile-first, PWA-ready)
- Local-first data layer
- Sync logic
- Analytics

This build must follow COPILOT_INSTRUCTIONS.md exactly.

---

# 1. BUSINESS LAYER (DEPARTMENTS)

Create folder:
/Departments/Sarah/

Inside it, create these 8 modules:

Intake.md  
Qualification.md  
Payment.md  
Booking.md  
Delivery.md  
ContentEngine.md  
AdsEngine.md  
Analytics.md  

Each module must follow the MFCF structure:

# Mission  
# Function  
# Components  
# Flow  

---

# 2. BACKEND (OFFLINE-FIRST READY)

Create folder:
/apps/Sarah/backend/

Create these files:

main.py  
models.py  
storage.py  
requirements.txt  

Backend rules:
- Use FastAPI structure
- Use SQLite for local-first storage
- Include sync hooks for future cloud sync
- Mirror business logic from Departments modules
- Expose REST endpoints:
  /intake  
  /qualification  
  /payment  
  /booking  
  /delivery  
  /content  
  /ads  
  /analytics  

---

# 3. FRONTEND (MOBILE-FIRST, OFFLINE-FIRST)

Create folder:
/apps/Sarah/frontend/

Create these files:

src/App.tsx  
src/screens/IntakeScreen.tsx  
src/screens/BookingScreen.tsx  
src/screens/SessionsScreen.tsx  
src/screens/PaymentsScreen.tsx  
src/store/state.ts  
src/offline/db.ts  
src/service-worker.ts  
index.html  
vite.config.ts  
tsconfig.json  

Frontend rules:
- Must be mobile-first layout
- Must work offline using IndexedDB/localStorage
- Must include a service worker for caching
- Must sync with backend when online
- Must allow:
  - Intake
  - Booking
  - Viewing sessions
  - Drafting notes
  - Viewing payments

---

# 4. OFFLINE-FIRST DATA MODEL

Rules:
- Local DB is the primary write target
- When offline: queue writes
- When online: replay queue to backend
- Conflict strategy: last-write-wins

---

# 5. ANALYTICS

Create:
- Local analytics log
- Sync to backend when online
- Track:
  - Leads
  - Sessions
  - Payments
  - Conversions
  - Performance metrics

---

# 6. EXECUTION RULES

- Build ONLY what is listed here
- Place files ONLY where specified
- Use MFCF for all modules
- Do not create extra files
- Do not modify other directories
- Follow COPILOT_INSTRUCTIONS.md exactly

---

# END OF BUILD