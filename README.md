
# Weather Dashboard

## Overview

The Weather Dashboard is a web application for monitoring and managing real-time weather data across multiple cities. It provides current weather conditions, daily summaries, and temperature alerts with options to receive notifications when certain temperature thresholds are exceeded.

## Features

- **Real-Time Weather Data**: Displays current weather information for multiple cities.
- **Temperature Conversion**: Toggle between Celsius and Fahrenheit.
- **Daily Summaries**: View daily summaries of temperature and weather conditions.
- **Temperature Alerts**: Set alerts based on user-defined temperature thresholds and receive notifications via email.
- **Past Alerts**: View a history of past alerts sent.

## Technologies

- **Frontend**: ReactJS
- **Backend**: Node.js with Express
- **Database**: MongoDB (using Mongoose)
- **Email Service**: Nodemailer (Gmail)
- **Weather API**: OpenWeatherMap

## Setup

### Prerequisites

- Node.js and npm installed
- MongoDB installed and running
- An API key for OpenWeatherMap
- Gmail account for sending email notifications

### Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/weather-dashboard.git
   cd weather-dashboard
   ```

2. **Install dependencies:**

   For the weather-monitoring:

   ```bash
   cd weather-monitoring
   npm install
   ```

   For the weather-monitoring-ui:

   ```bash
   cd weather-monitoring-ui
   npm install
   ```

3. **Configure environment variables:**

   Create a `.env` file in the `backend` directory and add the following variables:

   ```
   EMAIL_USER=your-email@gmail.com
   EMAIL_PASS=your-email-password
   OPENWEATHER_API_KEY=your-openweather-api-key
   MONGODB_URI=your-MongoDB-URI
   ```

4. **Start the server:**

   In the `weather-monitoring` directory:

   ```bash
   npm start
   ```
   the server will be running at ```http://localhost:3001```

5. **Start the frontend:**

   In the `weather-monitoring-ui` directory:

   ```bash
   npm run dev
   ```
   The application will be running at ```http://localhost:5173```

6. **Access the application:**

   Open your web browser and go to `http://localhost:3000` to view the dashboard.

## API Endpoints

- **GET `/api/weather`**: Fetch current weather data for multiple cities.
- **GET `/api/summaries`**: Fetch daily summaries of temperature and weather conditions.
- **POST `/api/alerts`**: Set an alert with a temperature threshold and optional email address.
- **GET `/api/alerts`**: Retrieve a list of past alerts.

## Usage

1. **Setting Alerts:**

   - Enter a temperature threshold in Celsius.
   - Optionally provide an email address to receive alerts.
   - Click "Set Alert" to configure.

2. **Viewing Weather Data:**

   - The dashboard will display weather data for each city in a grid layout.
   - Use the "Toggle to Fahrenheit" button to switch temperature units.

3. **Viewing Past Alerts:**

   - Navigate to the "Past Alerts" section to see a history of alerts.
