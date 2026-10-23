# CareOps — Quarantine Facility Operations Prototype

## Run locally
Open `index.html` in Chrome, or run `python -m http.server 8000` in this folder and visit `http://localhost:8000`.

## Deploy to Vercel
1. Upload this folder to a GitHub repository.
2. Import the repository in Vercel.
3. Select Framework Preset: Other; leave Build Command blank and set Output Directory to `.`.
4. Deploy. Use the generated `.vercel.app` URL in your assessment document.

## Implemented demo workflows
- Overview dashboard with capacity, pending temperature and doctor-round counts, discharge queue and workflow completion.
- Patient registration with active capacity guard at 74.
- Nurse temperature recording/editing, one reading per patient per day; readings >=38.0°C are flagged for doctor review.
- Doctor round documentation is blocked until today's temperature exists.
- Admin discharge queue requires 3 full consecutive recorded days below 38.0°C and updates bed occupancy.
- Quality metrics against 85% success / 15% mortality benchmarks and CSV export.
- Role selector for Admin/Nurse/Doctor; it is a demo selector, not authentication.
- Responsive UI and browser localStorage persistence.

## Limitations
Demo data is local to the browser, not shared or backed by a database. This is a prototype, not a clinical system. The 38.0°C threshold is an explicit demo assumption, not medical advice. Missing readings reset the consecutive-day fever-free count. No mortality-entry workflow or real authentication is implemented. Do not enter real patient data.
