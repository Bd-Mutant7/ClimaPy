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
# 🔑 API Key Setup Guide

## Getting Your OpenWeather API Key

### Step 1: Sign Up for a Free Account
1. Visit [OpenWeather Signup Page](https://home.openweathermap.org/users/sign_up)
2. Fill in your email, password, and details
3. Verify your email address (check your inbox)

### Step 2: Generate Your API Key
1. Log in to your [OpenWeather account](https://home.openweathermap.org/)
2. Navigate to **"API Keys"** tab in the top menu
3. You'll see a default API key, or click **"Generate"** to create a new one
4. Your key will look like: `a1b2c3d4e5f6g7h8i9j0k1l2m3n4o5p6`

### Step 3: Set Up Your `.env` File

In your ClimaPy project root, create a `.env` file:
```env
# Required: Your OpenWeather API Key
OPENWEATHER_API_KEY=your_actual_api_key_here

# Required: Django secret key (generate a new one!)
DJANGO_SECRET_KEY=generate_with_command_below

# Optional: Debug mode (True for development)
DEBUG=True

# Optional: Allowed hosts (for local development)
ALLOWED_HOSTS=localhost,127.0.0.1
```
## Step 4
```bash
python -c "from django.core.management.utils import get_random_secret_key; print(get_random_secret_key())"
```
## 🚀 Testing Your Setup
```bash
curl "https://api.openweathermap.org/data/2.5/weather?q=London&appid=YOUR_API_KEY"
```
## Create Your .env File
```text
OPENWEATHER_API_KEY=your_actual_api_key_here
DJANGO_SECRET_KEY=generate_a_secure_random_string_here
DEBUG=True
ALLOWED_HOSTS=localhost,127.0.0.1
```
## Generate Django Secret Key
```bash
python -c "from django.core.management.utils import get_random_secret_key; print(get_random_secret_key())"
```
## Testing Your Setup
```bash
python manage.py getweather "Nairobi"
python manage.py getweather "London" --units imperial
```
```bash
# Linux/Mac
touch .env

# Windows (Command Prompt)
type nul > .env

# Windows (PowerShell)
New-Item .env -Type File
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
python manage.py getweather "Kenya" --units imperial
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
## 🌟 About ClimaPy

**ClimaPy** is a Django-based command-line weather application that provides real-time weather information for cities worldwide. Originally developed as a learning project, it has evolved into a practical tool for developers and weather enthusiasts.

### 🎯 Project Vision
To create an accessible, developer-friendly weather tool that demonstrates:
- Clean Django architecture and management commands
- Professional API integration patterns
- Secure configuration management
- User-friendly command-line interfaces

### ✨ What Makes ClimaPy Special

| Feature | Benefit |
|---------|---------|
| **Dual Unit Support** | Switch between Celsius (°C) and Fahrenheit (°F) with a simple flag |
| **Smart Caching** | 10-minute cache reduces API calls and improves response times |
| **Input Validation** | Clean error messages for invalid city names or API issues |
| **Production-Ready** | Follows Django best practices and security guidelines |

### 🔧 Technical Highlights
- **Built with Django 4.2.7** - Leverages Django's robust management command system
- **OpenWeather API Integration** - Uses industry-standard weather data
- **Environment-Based Configuration** - Secure API key management via `.env` files
- **Cross-Platform Compatibility** - Works on Windows, macOS, and Linux

### 📚 Learning Value
ClimaPy serves as an excellent example of:
- Django management command implementation
- Third-party API integration patterns
- Environment variable configuration
- Error handling and user feedback
- Project structure and documentation

### 🚀 Project Journey
- **Origin**: Started as a PLP Python Week 8 Assignment
- **Evolution**: Refactored with professional coding practices
- **Rebranding**: Transitioned from "Weather Project" to "ClimaPy"
- **Future**: Open to community contributions and feature enhancements

### 👥 Who Is This For?
- **Python/Django Learners** - Study a real-world Django application
- **Weather Enthusiasts** - Quick command-line weather checks
- **Developers** - Example of API integration and CLI tools
- **Educators** - Teaching tool for API and Django concepts

### 📈 Project Status
✅ **Core Features Complete** - Weather fetching, caching, unit conversion  
✅ **Documentation Ready** - Clear setup and usage instructions  
✅ **Security Implemented** - Proper API key management  
🔜 **Future Potential** - Web interface, historical data, more APIs

---

### 🏗️ Architecture Overview
ClimaPy Structure:
climapy/ # Django project
├── settings.py # Configuration (supports .env)
├── urls.py # URL routing
└── wsgi.py # WSGI entry point

weather/ # Django app
├── management/
│ └── commands/
│ └── getweather.py # Core weather command
└── models.py # Data models (if expanded)


### 🌍 Real-World Application
ClimaPy demonstrates practical skills used in:
- SaaS product development
- API-based microservices
- Developer tools creation
- Open-source project maintenance

### 🤝 Contributing
While primarily a personal project, ClimaPy welcomes:
- Bug reports and issue tracking
- Documentation improvements
- Code optimizations and best practices
- Educational use and adaptation

---

*ClimaPy represents the journey from a classroom assignment to a polished, practical tool — demonstrating how foundational programming concepts evolve into usable software.*



