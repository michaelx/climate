# Climate JSON

A JSON file with the monthly climate data of over one-hundred destinations and counting. It includes the average high and low temperature, dry days, snow days, and rainfall, for every month.

## Why?

Friends asked me to provide a JSON of my [Climate Sheet](http://michaelxander.com/climate-data/), so I wrote a conversion script, but first a note about the data!

>Source of the complete weather data is the excellent [Forecast.io API](https://developer.forecast.io/) which you might know from the Dark Sky app. 

I never had the intention to create a climate data file in the first place, but I see how it can be useful to play around with. If you’d like to create a serious weather application however, I highly recommend building your own solution directly connected to the Forecast.io API. They offer historical data, but you’ve to aggregate it yourself, so in order to get the monthly data you need to request every single day of a month, and it might be a good idea to do that for a few years to improve data quality.

Anyhow, if you just would like to play around, feel free to check it out.

>**Note:** The temperature data is in **Celsius**, and rainfall in **mm**.

>**Tip:** Divide `rainfall` by the number of days of the month, to calculate the average daily rainfall.

## Structure

I included an id to easily hook it up with matching data. Otherwise the JSON should be pretty self explanatory. Just remember to access the monthlyAvg array with the correct index (month number - 1).

```json
[
  {
    "id": 1,
    "city": "Amsterdam",
    "country": "Netherlands",
    "monthlyAvg": [
      {
        "high": 7,
        "low": 3,
        "dryDays": 19,
        "snowDays": 4,
        "rainfall": 68
      },
      {
        "high": 6,
        "low": 3,
        "dryDays": 13,
        "snowDays": 2,
        "rainfall": 47
      },
      …
    ]
  },
  {
    "id": 2,
    "city": "Athens",
    "country": "Greece",
    "monthlyAvg": [
      {
        "high": 12,
        "low": 7,
        "dryDays": 21,
        "snowDays": 1,
        "rainfall": 53
      },
      …
    ]
  },
  …
]
```

## Credits

* [Forecast.io API](https://developer.forecast.io/)
* [That Michael Xander fellow](http://michaelxander.com)