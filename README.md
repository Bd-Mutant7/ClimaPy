# 🌤️ ClimaPy

A Django-based weather information application that fetches weather data from OpenWeather API.

## Setup

1. Clone the repository
```bash
git clone <repository-url>
cd climapy
python -m venv venv
# On Windows
venv\Scripts\activate
# On Unix or MacOS
source venv/bin/activate
pip install -r requirements.txt
OPENWEATHER_API_KEY=your_api_key_here
DJANGO_SECRET_KEY=your_django_secret_key_here
DEBUG=True
ALLOWED_HOSTS=localhost,127.0.0.1
python manage.py migrate
python manage.py getweather "city name" [--units metric|imperial]
# Get weather in Celsius (default)
python manage.py getweather "London"

# Get weather in Fahrenheit
python manage.py getweather "New York" --units imperial
```
## Features:
```text
Temperature in both Celsius (metric) and Fahrenheit (imperial)

Feels-like temperature

Humidity percentage

Weather conditions

Wind speed (m/s for metric, mph for imperial)

Response caching (10-minute cache to avoid repeated API calls)

Input validation for city names

Detailed error messages
```
## Security Notes
```text
Never commit the .env file to version control

Keep your API keys and secret keys secure

In production, set DEBUG=False and configure ALLOWED_HOSTS appropriately
```
