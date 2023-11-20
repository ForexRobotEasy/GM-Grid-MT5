# GM Grid MT5

GM Grid MT5 is a trading robot developed by the Forex Robot Easy Team. It is designed to implement a trading strategy based on Price Action signals. This code can be used as a sample to understand how the robot works.

## Requirements

To use this code, you need to have the following libraries installed:

- Trade.mqh
- ArrayObj.mqh

## Constants

The code defines the following constants:

- `SYMBOLS_ALLOWED`: An array of symbols allowed for trading. Only symbols present in this array will be considered for trading.
- `MIN_DEPOSIT_WITH_SL`: The minimum account balance required with a stop loss.
- `MIN_DEPOSIT_WITHOUT_SL`: The minimum account balance required without a stop loss.

## Global Variables

The code defines the following global variables:

- `trade`: An instance of the `CTrade` class used for trading operations.
- `symbolList`: An array to store the allowed symbols for trading.
- `accountBalance`: The current account balance.

## Initialization

The `OnInit` function is called when the robot is initialized. It performs the following tasks:

1. Checks if the symbol is allowed for trading.
2. Adds the allowed symbol to the `symbolList` array.
3. Checks the account balance.
4. If stop loss is required, checks if the account balance is sufficient.
5. If stop loss is not required, checks if the account balance is sufficient.

If the account balance is insufficient, an error message is printed and the initialization fails.

## Stop Loss Requirement

The `IsStopLossRequired` function is called to determine if stop loss is required for trading. The logic to determine this requirement should be implemented in this function. The function should return `true` if stop loss is required, and `false` otherwise.

## Trading Strategy

The `TradePriceAction` function is called to implement the trading strategy based on Price Action signals. The trading strategy should be implemented in this function. It should determine entry and exit points, stop loss and take profit levels, and position sizing calculations.

In this sample code, the `Buy` and `Sell` functions of the `CTrade` class are used to place trade orders. The symbol, volume, stop loss, and take profit levels are set to default values.

## Trading Operations

The `OnTick` function is called on each tick of the market. It checks if the current symbol is in the `symbolList` array, and if so, calls the `TradePriceAction` function to execute the trading strategy.

## Deinitialization

The `OnDeinit` function is called when the robot is deinitialized. It performs any necessary cleanup and finalizes the trading robot.

Note: ForexRobotEasy is not the official developer of this product. This code is provided as a sample that can work as described in the product. To find the official developer of this product, please use MQL5.

For detailed reviews and trading results of this product, please visit [Forex Robot Easy - GM Grid MT5 Review](https://forexroboteasy.com/forex-robot-review/gm-grid-mt5-review-high-win-low-spread-forex-robot/).
