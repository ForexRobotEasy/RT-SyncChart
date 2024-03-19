# RT SyncChart.mq5

This code is a custom indicator for MetaTrader 5 (MT5) that allows for synchronization of symbols and timeframes across multiple charts. It is designed to enhance forex analysis by ensuring that all charts display the same symbol and timeframe.

### Global Variables
- SyncSymbol: Specifies the symbol to be synced across charts (default: EURUSD).
- SyncTimeframe: Specifies the timeframe to be synced across charts (default: H1).

### Custom Indicator Initialization Function (OnInit)
- Sets the symbol and timeframe for the current chart using ChartSetSymbolPeriod().
- Loops through all open charts and syncs them to display the same symbol and timeframe.

### Custom Indicator Deinitialization Function (OnDeinit)
- Resets the symbol and timeframe for all charts to empty values.

### Custom Indicator Iteration Function (OnCalculate)
- Performs symbol monitoring and analysis for each bar of data.
- Example analysis logic is provided in the code to calculate a simple moving average (SMA) using the iMA() function.
- Displays the moving average on all synced charts using ObjectCreate() and ObjectSetInteger().

### Custom Event Handling Function (OnChartEvent)
- Handles drawing object synchronization across charts.
- For CHARTEVENT_OBJECT_CREATE, syncs the created object across all charts using ObjectCreate().
- For CHARTEVENT_OBJECT_CHANGE, syncs the modified object across all charts using ObjectMove().
- For CHARTEVENT_OBJECT_DELETE, syncs the deleted object across all charts using ObjectDelete().

Please note that Forex Robot Easy is not the official developer of this product. We only provide a sample code that can work as described in the product. To find the official developer of this product, please refer to MQL5.

For detailed reviews and trading results of this product, please visit [Forex Robot Easy - RT SyncChart Review](https://forexroboteasy.com/forex-robot-review/rt-syncchart-review-enhance-forex-analysis-with-timeframe-syncing/).
