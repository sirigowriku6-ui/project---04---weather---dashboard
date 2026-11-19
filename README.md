# Live Weather Dashboard - Project 04

Live Demo: https://sirigowritudi-ui.github.io/project-04-weather-dashboard/
Repo: https://github.com/sirigowritudi-ui/project-04-weather-dashboard

## What I Built
Search any city to see live temperature and 5-day forecast using Open-Meteo API (no API key needed).

## Features
- City search with validation
- Current weather + 5-day forecast
- °C / °F toggle (saved in localStorage)
- Recent searches (clickable chips, last 5)
- Last city remembered on refresh
- Loading, Empty, Error and Success states
- Responsive on mobile, accessible with aria-live and focus styles

## Tech Used
HTML, CSS, JavaScript (fetch + async/await), Open-Meteo Geocoding + Forecast API, GitHub Pages

## How I Handle Errors
- Empty input: Shows "Type a city name."
- Unknown city: Checks if results are empty, shows "City not found. Check spelling..."
- Network / API failure: Checks response.ok before reading JSON, shows "Service not responding. Please try again."
- User input in URL: Uses encodeURIComponent()
- User text shown with textContent only (never innerHTML) to prevent XSS
- API called only on Search submit, not on every keypress (to respect free API limits)
