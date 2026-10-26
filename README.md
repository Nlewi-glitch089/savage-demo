![21 Savage](public/21savage.jpg)

## Installation

1. Clone repo
2. run `npm install`
3. Copy `.env.example` to `.env` and fill in your own values (see below)

## Usage

1. run `npm run savage`
2. Navigate to `localhost:3000`

## Environment variables

| Variable | Required | Purpose |
| --- | --- | --- |
| `MONGODB_URI` | yes | MongoDB connection string. |
| `MONGODB_DB_NAME` | no | Database to use. Defaults to `demo`. |
| `PORT` | no | Port to listen on. Defaults to 3000; Render sets it automatically. |

The server exits with an error if `MONGODB_URI` is missing or it can't connect to MongoDB. `.env` is ignored by Git; never commit real credentials.

## Deploying to Render

1. Create a **Web Service** from this repo.
2. Build command: `npm install`
3. Start command: `npm start`
4. Under **Environment**, add `MONGODB_URI` (and optionally `MONGODB_DB_NAME`).
5. In MongoDB Atlas, allow connections from Render under **Network Access** (Render's outbound IPs, or `0.0.0.0/0` for a class project) and create a database user for the app.
