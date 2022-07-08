##steps


### Setup
* git clone https://github.com/freqtrade/freqtrade.git

* uncomment build in docker-compose file

* docker-compose build
 
* docker-compose up

* docker-compose run --rm freqtrade create-userdir --userdir user_data
 
* docker-compose run --rm freqtrade new-config --config user_data/config.json

* docker-compose run --rm freqtrade new-strategy -s ZigZag_strategy --template minimal

### Setup new Strategy

* 

### Downloading data

* in config.json set `"method": "StaticPairList",`

  * whitelist in the config.json under exchange: 
    `"pair_whitelist": [
              "BTC/USDT",
              "ETC/USDT",
              "BNB/USDT",
              "BNB/USDT",
              "XRP/USDT",
              "ADA/USDT",
              "SOL/USDT",
              "DOGE/USDT",
              "DOT/USDT",
              "DAI/USDT",
              "TRX/USDT",
     ],
* `

* docker-compose run --rm freqtrade download-data

### Backtesting 

* docker-compose run --rm freqtrade  backtesting --strategy SampleStrategy