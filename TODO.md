# WeatherWise — feature tracker

Use this as the single source of truth until a GitHub Project board is set up. Check items off as you ship.

## Core pipeline

- [ ] Connect to a weather API (Open-Meteo or OpenWeatherMap)
- [ ] Build a data normalizer (raw weather JSON → structured format)
- [ ] Build a recommendation engine (LLM prompt → 1–3 short tips)

## Product surface

- [ ] Create tip categories: Clothing, Umbrella, Go outside?, Travel, Evening plans
- [ ] “My Day” hourly timeline view (icons + one-liner per hour)
- [ ] “Should I?” quick query feature (e.g. walk to work? run outside?)

## Personalization & resilience

- [ ] User persona setup (commute type, cold sensitivity, outdoor plans)
- [ ] Graceful degraded-data mode (still works with incomplete forecast)

## Social & distribution

- [ ] Social feed layer (friends’ weather, share your own tip)
- [ ] Frontend mini-app or widget (clean, mobile-friendly, one screen)

## Engineering & ops

- [ ] REST API with Postman-testable endpoints
- [ ] Docker setup for easy deployment and judging
