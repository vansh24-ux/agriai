# KisanWeb Farmer Services

KisanWeb is a farmer support application with local market prices, harvest listings and buyer offers, transport quote requests, price alerts, FPO enquiries, and sponsored partner offers.

## Run locally on Windows

Open two PowerShell windows from the project folder.

In the first window:

```powershell
cd backend
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
.\.venv\Scripts\python.exe -m uvicorn app.main:app --reload
```

In the second window:

```powershell
cd frontend
npm install
npm run dev
```

Open the frontend URL printed by Vite. The backend API runs at `http://127.0.0.1:8000`.

The demo login accepts any farmer name and password `1234`.

## Current service behavior

- Buyer listings and offers are stored in the backend database.
- Transport and FPO forms collect partner enquiries; transport quote matching and paid subscriptions are not connected yet.
- Price alerts are evaluated against a market search made during the current app session. Background SMS and WhatsApp notifications are not connected.
- Sponsored offers submitted by businesses are pending review. Payment processing and an approval dashboard are not connected.
- The demo login is not production authentication. Add user accounts and access controls before deploying with real farmer or business data.