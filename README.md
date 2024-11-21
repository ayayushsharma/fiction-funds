# fiction-funds

The desire here is an applicaiton that is able to:

On a functionality level
- Pull timeseries infomation about any stock and cache them in a database
    - Stock price changes over a range of time
    - Stock perception in general media in a specific timeframe

On a User level
- Start with a base amount of cash to invest in a fake stock market
- Make a choice on type of investment
    - Real time
        In Real time investment, the stocks bought/sold will correspond with the 
        current market price of the stock
    - Historical
        In Historial, investments can be added/made on any timeframe and the stock
        will be registered in one selfs account at that time's value

- [ ] Future inplementations will include
    - Machine learning models that will try to maximize portfolio value based on multiple 
    parameters
    - Parameters can include (based on the timeperiod of investment - very short, short, long)
        - What and how much stocks to buy
        - When to sell individual stocks


## Architecture

This requires a minimum of 2 applcation instances to run 

1. User interaction applicaiton
2. Server Application which will direct stock queries to their appropriate APIs
