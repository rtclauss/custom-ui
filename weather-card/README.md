## Lovelace animated weather card

Originally created for the [old UI](https://community.home-assistant.io/t/custom-ui-weather-state-card-with-a-question/23008) [converted](https://community.home-assistant.io/t/custom-ui-weather-state-card-with-a-question/23008/291) by @arsaboo and @ciotlosm to Lovelace and now converted to Lit to make it even better.

Thanks for all picking this card up.

# Configuration:

1. Download the [weather-card.js](https://raw.githubusercontent.com/bramkragten/custom-ui/master/weather-card/weather-card.js) to /config/www/custom-lovelace/weather-card/.
2. Save, the [amcharts](https://www.amcharts.com/free-animated-svg-weather-icons/) 1.9k icon under www\icons\weather_icons\animated

Add the following to resources in your lovelace config:
```yaml
resources:
  - url: /local/custom-lovelace/weather-card/weather-card.js
    type: module
```

And add a card with type `custom:weather-card`:
```yaml
  - type: custom:weather-card
    entity: weather.yourweatherentity
```