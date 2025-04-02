# MedMatch Backend

💊 A Node.js + Express API for comparing brand-name and generic medication prices.

This is the backend for **MedMatch**, a full-stack healthcare web app built for **Hackatopia 2025**. It allows users to search for medications, view cheaper generic alternatives, and compare prices across pharmacies like GoodRx and Blink Health (mocked for demo purposes).

---

## 🧠 Features

- REST API to search for medications
- Returns generic equivalents
- Simulates pharmacy price comparison
- Seeded with mock medication and pricing data
- Built with Express and MongoDB (via Mongoose)

---

## ⚙️ Tech Stack

- **Backend**: Node.js, Express.js
- **Database**: MongoDB + Mongoose
- **Environment**: dotenv for secure secrets
- **Deployment**: Render (or can be hosted on any Node-compatible platform)

---

## 🚀 Getting Started

### 1. Clone the Repo

```bash
git clone https://github.com/yourusername/medmatch-backend.git
cd medmatch-backend
```
### 2. Install Dependencies
```bash
npm install
```
3. Create a .env File
```bash
MONGO_URI=your_mongodb_connection_string
PORT=5000
```
4. Seed the Database
```bash
node seed.js
```
5. Run the Server
```bash
npm run dev
```

The API will be live at: http://localhost:5000/api/medications/:name

📂 API Example
Endpoint:
```bash
GET /api/medications/Lipitor
```
Response:
```bash
{
  "name": "Lipitor",
  "generic": ["Atorvastatin"],
  "prices": [
    {
      "pharmacy": "GoodRx",
      "price": 12.99,
      "link": "https://www.goodrx.com/lipitor"
    },
    {
      "pharmacy": "Blink Health",
      "price": 10.49,
      "link": "https://www.blinkhealth.com/lipitor"
    }
  ]
}
```
📁 Folder Structure
medmatch-backend/
├── controllers/
│   └── medicationController.js
├── models/
│   └── Medication.js
├── routes/
│   └── medicationRoutes.js
├── seed.js
├── server.js
└── .env
✍️ Authors
Created by Harsha Priya and Sankarraj for Hackatopia 2025.
