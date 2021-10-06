# Forex-Python-SDK
Python SDK (Software Development Kit) to help get live and historical forex data in one line of code.

### Install
pip install tradermade

### Signup

Signup for Free at https://marketdata.tradermade.com/signup. 

You can find your key at https://marketdata.tradermade.com/myAccount

### Set API KEY

` tm.set_rest_api_key("api_key") `


### get currency codes

` tm.currency_list() `

_gets list of all currency codes available add two codes to get code for currencypair ex EUR + USD gets EURUSD_

### Get Live Rates

` tm.live(currency='EURUSD,GBPUSD',fields=["bid", "mid", "ask"]) `

### Get Historical Rates

` tm.historical(currency='EURUSD,GBPUSD', date="2011-01-20",interval="daily", fields=["open", "high", "low","close"]) `

_returns historical data for the currency requested interval is daily, hourly, minute - fields is optional_

### Get Timeseries 
 
` tm.timeseries(currency='EURUSD,GBPUSD', start="2021-04-26",end="2021-04-27",interval="minute",fields=["close"],period=15) `

_returns 15 min bar for two currencies - you may need to adjust date to two days back or function will return an error that only two days of data is allowed for minute interval_
