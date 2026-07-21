# Jay Swimmys Tide Guide

A simple, interactive web-based tide prediction tool for NOAA tide stations with real-time water temperature data.

## Features

- **Live Tide Predictions**: View detailed tide predictions for any NOAA monitoring station
- **Water Temperature**: Current water temperature from multiple sources (station sensors, satellite data, or nearby sensors)
- **Sun & Moon Info**: Sunrise/sunset times and current moon phase for your location
- **Wind Speed and Direction**: Prevailing wind speed with arrow/cardinal direction
- **Interactive Charting**: Beautiful SVG tide charts with high/low tide markers
- **Favorites**: Save your preferred tide stations for quick access
- **Date Navigation**: View tides for any date with easy navigation
- **Responsive Design**: Works on desktop and mobile devices

## Usage

1. Open `tide-guide.html` in any modern web browser
2. Search for your favorite NOAA tide station
3. Save it to your favorites for quick access
4. View tide predictions, water temperature, wind speed/direction and celestial data
5. Navigate between dates or jump to today's tides

## Data Sources

- **Tide Predictions**: NOAA CO-OPS API (MLLW predictions)
- **Water Temperature**: 
  - NOAA sensors (when available)
  - Open-Meteo marine API (satellite/model SST)
  - Nearest NOAA sensor (fallback)
- **Sun Times**: Computed using NOAA solar calculation algorithm
- **Moon Phase**: Lunisolar calendar calculation

## Browser Compatibility

Works on all modern browsers that support:
- ES6 JavaScript
- SVG rendering
- Fetch API
- LocalStorage

## License

MIT License - see LICENSE file for details
