# Server Architecture

## Deciding on Database

It would be beneficial to use a timeseries database but for now we can stick to a SQLite instance


## Data pulling structure

Server will not pull all the data from stock api servers at once. What we can do is letting the user
search a stock and then pull it's data. We can ask all the APIs about the stock and whichever one 
sends the data first, is sent as a response to maintain fast API responses. We save all the servers 
that sent a successful response in a database table to maintain a cache of right servers.

In case a stock's has multiple API we can fetch it's information from. We can save it list and save
the default API endpoint in another column.


## API structure

- /stocks/{stock_name}?market={market_name}
  `stock_name` - (string) Name of the stock 
  `market_name` - (string, not required) If a market_name is not supplied, the default market is picked.
  Else market_name is used to pull data of the desired stock
