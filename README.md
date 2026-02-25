# Weather Dashboard 
This is a React + Vite weather dashboard that fetches and displays **global** weather data.

It supports:

- Search by location (city name, airport code, or `lat,long`)
- Current conditions (temperature, humidity, wind, condition)
- Forecast display when available

## Setup / run instructions

### Prerequisites

- Node.js (LTS recommended)
- An IndianAPI key for the Weather API

### 1) Install dependencies

From the `frontend/` folder:

```bash
npm install
```

### 2) Configure environment variables

Create a `.env` file inside `frontend/`:

```env
VITE_INDIANAPI_KEY=YOUR_API_KEY_HERE
```

### 3) Start the dev server

```bash
npm run dev
```

### Provider

- IndianAPI Weather: https://indianapi.in/weather-api

### Base URL

```text
https://weather.indianapi.in
```

### Authentication

All requests include:

```text
x-api-key: <your api key>
```

### Endpoints used by this project

- `GET /global/weather?location=<string>&days=<1-3>`
- `GET /global/current?location=<string>` (used as a fallback if `/global/weather` is unavailable)

### Implementation location

- API client: `src/api/weatherApi.js`
- UI: `src/Home.jsx`
