# SignificantTrades [![Build Status](https://travis-ci.org/Tucsky/SignificantTrades.svg?branch=master)](https://travis-ci.org/Tucsky/SignificantTrades)
Live trades visualizer.<br>
Currently supporting Bitstamp, Kraken, Huobi, Hitbtc, Okex, Bitmex, Binance, Bitfinex, Gdax ([see server/src/exchanges/](server/src/exchanges))

![screenshot](https://i.imgur.com/j3iP8ds.gif)

## How it works
- The repo contains a server part to gather & format exchanges data and broadcast it to many clients through websocket (mostly) communication.
- The client part is written in vue.js, show live trades in a list based on settings (short timeframe row stacking by amount) and allow to visualize session's buys/sells/price in a little chart (which tick from 10s to 1d depending on zoom, so mostly 10s). It also can control the server so it knows which pair to track.

## What it do
- Aggregate trades from exchanges on a specific pair (default BTCUSD)
- Filter trades by amount (by stacking them up)
- Show realtime BUY & SELL volume & average price on a chart
- Load previous trade data on the chart
- Range selection (`shift + clic` the chart)

Check out [the demo](https://tucsky.github.io/SignificantTrades/)
