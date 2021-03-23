# FlightSurety

Udacity Blockchain Developer Nanodegree project Flight Surety.


## Installation

To install, download or clone this repo, then run:

`npm install`


## DApp Build and Deployment

1. **Compile contracts**:
```
truffle compile
```

2. **Run Ganache CLI**:
```
ganache-cli -m "seed words" --accounts=50 --deterministic --gasLimit 500000000 --gasPrice 30000000000
```

3. **Deploy contracts**:
```
truffle migrate --reset --network development
```



## DApp Testing

1. **Run Ganache CLI**:
    ```
    ganache-cli --accounts=50 --gasLimit 500000000 --gasPrice 30000000000
    ```

2. **Run flightSurety and oracles truffle tests (separately)**:
    ```
    truffle test ./test/flightSurety.js

    truffle test ./test/oracles.js
    ```

## Launching FlightSurety DApp

1. **Import accounts**

    Import contract owner, airline and passengers accounts from Ganache to Metamask using private keys.
Here is how to import accounts to Metamask:

    |# | Account  | Default| Metamask|
    |-- | ---- | --------- | --------|
    |1  |owner | |   |
    |2  |airline | 5 airline accounts| import|
    |3  |airline | ||
    |4  |airline |  ||
    |5  |airline |   ||
    |6  |airline |||
    |7  |passenger | 3 passenger accounts|import|
    |8  |passenger | ||
    |9  |passenger | ||
    |10 |oracle | 40 oracles | don't import|
    |.. |.. | .. |..|
    |50 |oracle |  ||
    
    
    Airline and passenger default numbers of accounts are defined and can be changed in master_data.js: **NUMBER_OF_AIRLINES** and **NUMBER_OF_PASSENGERS** constants).
    
    Oracle accounts will not be imported to Metamask. The number of oracle accounts is defined and can be changed in server.js: **NUMBER_OF_ORACLES**.


2. **Run Ganache CLI**:
    ```
    ganache-cli -m "seed words" --accounts=50 --deterministic --gasLimit 500000000 --gasPrice 30000000000
    ```
3. **Start the server**:
    
    Wait until oracles have been registered before starting the DApp
    ```
    npm run server
    ```

4. Start the DApp:
    ```
    npm run dapp
    ```

5. Go to http://localhost:8000



## Resources

* [Truffle Framework](http://truffleframework.com/)
* [Ganache Local Blockchain](http://truffleframework.com/ganache/)
* [Solidity Language Reference](http://solidity.readthedocs.io/en/v0.4.24/)
* [Web3Js Reference](https://github.com/ethereum/wiki/wiki/JavaScript-API)