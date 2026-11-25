# Air Quality Lookup

A small Django app that shows the current air quality for a US ZIP code. It calls the [AirNow API](https://docs.airnowapi.org/) and explains the result with the official AQI category and a matching colour.

## Features

- Enter a US ZIP code and get the current Air Quality Index (AQI) for that area
- Shows the AQI category (Good, Moderate, Unhealthy for Sensitive Groups, Unhealthy, Very Unhealthy, Hazardous) with a short health explanation
- Colour-coded result card for each category
- Opens with a default ZIP code so the page is never empty
- About page

## Built with

- Python 3, Django
- `requests` for the AirNow API call
- Django templates and Bootstrap

## Run it locally

```bash
git clone https://github.com/hamzakhalem/weatherappdjango.git
cd weatherappdjango
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
pip install django requests
export DJANGO_SECRET_KEY="any-long-random-string"   # PowerShell: $env:DJANGO_SECRET_KEY="..."
python manage.py migrate
python manage.py runserver
```

Then open http://127.0.0.1:8000.

## Project structure

```
weather/   Django project settings and root URLs
lookup/    The app: views that call AirNow, templates (home, about)
```
