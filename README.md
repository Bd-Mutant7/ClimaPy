# 🌤️ ClimaPy

A Django-based weather information application that fetches weather data from OpenWeather API.

## Setup

1. Clone the repository
```bash
git clone https://github.com/Bd-Mutant7/ClimaPy
cd climapy

python -m venv venv
```

## On Windows
```bash
venv\Scripts\activate
```
## On Unix or MacOS
```bash
source venv/bin/activate
```
```bash
pip install -r requirements.txt
OPENWEATHER_API_KEY=your_api_key_here
```
```bASH
DJANGO_SECRET_KEY=your_django_secret_key_here
DEBUG=True
ALLOWED_HOSTS=localhost,127.0.0.1
```
```bash
python manage.py migrate
python manage.py getweather "city name" [--units metric|imperial]
# Get weather in Celsius (default)
python manage.py getweather "Kenya"
```
## Get weather in Fahrenheit
```bash
python manage.py getweather "New York" --units imperial
```
## Features:

Temperature in both Celsius (metric) and Fahrenheit (imperial)

Feels-like temperature

Humidity percentage

Weather conditions

Wind speed (m/s for metric, mph for imperial)

Response caching (10-minute cache to avoid repeated API calls)

Input validation for city names

Detailed error messages

## Security Notes
```text
Never commit the .env file to version control

Keep your API keys and secret keys secure

In production, set DEBUG=False and configure ALLOWED_HOSTS appropriately
```

