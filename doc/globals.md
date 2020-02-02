[@tinkoff/invest-openapi-js-sdk](README.md) › [Globals](globals.md)

# @tinkoff/invest-openapi-js-sdk

## Index

### Classes

* [OpenAPI](classes/openapi.md)

### Interfaces

* [UserAccount](interfaces/useraccount.md)
* [UserAccounts](interfaces/useraccounts.md)

### Type aliases

* [BrokerAccountType](globals.md#brokeraccounttype)
* [Candle](globals.md#candle)
* [CandleResolution](globals.md#candleresolution)
* [CandleStreaming](globals.md#candlestreaming)
* [Candles](globals.md#candles)
* [CandlesResponse](globals.md#candlesresponse)
* [Currencies](globals.md#currencies)
* [Currency](globals.md#currency)
* [CurrencyPosition](globals.md#currencyposition)
* [Depth](globals.md#depth)
* [Dict](globals.md#dict)
* [Empty](globals.md#empty)
* [Error](globals.md#error)
* [ErrorPayload](globals.md#errorpayload)
* [HttpMethod](globals.md#httpmethod)
* [InstrumentId](globals.md#instrumentid)
* [InstrumentType](globals.md#instrumenttype)
* [Interval](globals.md#interval)
* [LimitOrderParams](globals.md#limitorderparams)
* [LimitOrderRequest](globals.md#limitorderrequest)
* [LimitOrderResponse](globals.md#limitorderresponse)
* [MarketInstrument](globals.md#marketinstrument)
* [MarketInstrumentList](globals.md#marketinstrumentlist)
* [MarketInstrumentListResponse](globals.md#marketinstrumentlistresponse)
* [MarketInstrumentResponse](globals.md#marketinstrumentresponse)
* [MoneyAmount](globals.md#moneyamount)
* [Operation](globals.md#operation)
* [OperationStatus](globals.md#operationstatus)
* [OperationTrade](globals.md#operationtrade)
* [OperationType](globals.md#operationtype)
* [OperationTypeWithCommission](globals.md#operationtypewithcommission)
* [Operations](globals.md#operations)
* [OperationsResponse](globals.md#operationsresponse)
* [Order](globals.md#order)
* [OrderResponse](globals.md#orderresponse)
* [OrderStatus](globals.md#orderstatus)
* [OrderType](globals.md#ordertype)
* [Orderbook](globals.md#orderbook)
* [OrderbookResponse](globals.md#orderbookresponse)
* [OrderbookStreaming](globals.md#orderbookstreaming)
* [OrdersResponse](globals.md#ordersresponse)
* [PlacedLimitOrder](globals.md#placedlimitorder)
* [Portfolio](globals.md#portfolio)
* [PortfolioCurrenciesResponse](globals.md#portfoliocurrenciesresponse)
* [PortfolioPosition](globals.md#portfolioposition)
* [PortfolioResponse](globals.md#portfolioresponse)
* [SandboxCurrency](globals.md#sandboxcurrency)
* [SandboxSetCurrencyBalanceRequest](globals.md#sandboxsetcurrencybalancerequest)
* [SandboxSetPositionBalanceRequest](globals.md#sandboxsetpositionbalancerequest)
* [SocketEventType](globals.md#socketeventtype)
* [TradeStatus](globals.md#tradestatus)

### Variables

* [WebSocket](globals.md#const-websocket)

### Functions

* [getQueryString](globals.md#getquerystring)
* [once](globals.md#once)

## Type aliases

###  BrokerAccountType

Ƭ **BrokerAccountType**: *"Tinkoff" | "TinkoffIis"*

*Defined in [src/domain.d.ts:238](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L238)*

___

###  Candle

Ƭ **Candle**: *object*

*Defined in [src/domain.d.ts:93](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L93)*

#### Type declaration:

* **c**: *number*

* **figi**: *string*

* **h**: *number*

* **interval**: *[CandleResolution](globals.md#candleresolution)*

* **l**: *number*

* **o**: *number*

* **time**: *string*

* **v**: *number*

___

###  CandleResolution

Ƭ **CandleResolution**: *object*

*Defined in [src/domain.d.ts:104](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L104)*

#### Type declaration:

___

###  CandleStreaming

Ƭ **CandleStreaming**: *object*

*Defined in [src/OpenAPI.ts:46](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L46)*

#### Type declaration:

* **c**: *number*

* **figi**: *string*

* **h**: *number*

* **interval**: *[Interval](globals.md#interval)*

* **l**: *number*

* **o**: *number*

* **time**: *string*

* **v**: *number*

___

###  Candles

Ƭ **Candles**: *object*

*Defined in [src/domain.d.ts:87](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L87)*

#### Type declaration:

* **candles**: *[Candle](globals.md#candle)[]*

* **figi**: *string*

* **interval**: *[CandleResolution](globals.md#candleresolution)*

___

###  CandlesResponse

Ƭ **CandlesResponse**: *object*

*Defined in [src/domain.d.ts:81](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L81)*

#### Type declaration:

* **payload**: *[Candles](globals.md#candles)*

* **status**: *string*

* **trackingId**: *string*

___

###  Currencies

Ƭ **Currencies**: *object*

*Defined in [src/domain.d.ts:29](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L29)*

#### Type declaration:

* **currencies**: *[CurrencyPosition](globals.md#currencyposition)[]*

___

###  Currency

Ƭ **Currency**: *object*

*Defined in [src/domain.d.ts:229](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L229)*

#### Type declaration:

___

###  CurrencyPosition

Ƭ **CurrencyPosition**: *object*

*Defined in [src/domain.d.ts:33](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L33)*

#### Type declaration:

* **balance**: *number*

* **blocked**? : *undefined | number*

* **currency**: *[Currency](globals.md#currency)*

___

###  Depth

Ƭ **Depth**: *1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10*

*Defined in [src/OpenAPI.ts:36](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L36)*

___

###  Dict

Ƭ **Dict**: *object*

*Defined in [src/OpenAPI.ts:39](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L39)*

#### Type declaration:

* \[ **x**: *string*\]: T

___

###  Empty

Ƭ **Empty**: *object*

*Defined in [src/domain.d.ts:1](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L1)*

#### Type declaration:

* **payload**: *any*

* **status**: *string*

* **trackingId**: *string*

___

###  Error

Ƭ **Error**: *object*

*Defined in [src/domain.d.ts:7](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L7)*

#### Type declaration:

* **payload**: *[ErrorPayload](globals.md#errorpayload)*

* **status**: *string*

* **trackingId**: *string*

___

###  ErrorPayload

Ƭ **ErrorPayload**: *object*

*Defined in [src/domain.d.ts:233](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L233)*

#### Type declaration:

* **code**? : *undefined | string*

* **message**? : *undefined | string*

___

###  HttpMethod

Ƭ **HttpMethod**: *"get" | "post"*

*Defined in [src/OpenAPI.ts:37](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L37)*

___

###  InstrumentId

Ƭ **InstrumentId**: *object | object*

*Defined in [src/OpenAPI.ts:45](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L45)*

___

###  InstrumentType

Ƭ **InstrumentType**: *object*

*Defined in [src/domain.d.ts:231](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L231)*

#### Type declaration:

___

###  Interval

Ƭ **Interval**: *"1min" | "2min" | "3min" | "5min" | "10min" | "15min" | "30min" | "hour" | "2hour" | "4hour" | "day" | "week" | "month"*

*Defined in [src/OpenAPI.ts:22](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L22)*

___

###  LimitOrderParams

Ƭ **LimitOrderParams**: *object*

*Defined in [src/OpenAPI.ts:65](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L65)*

#### Type declaration:

* **figi**: *string*

* **lots**: *number*

* **operation**: *[OperationType](globals.md#operationtype)*

* **price**: *number*

___

###  LimitOrderRequest

Ƭ **LimitOrderRequest**: *object*

*Defined in [src/domain.d.ts:156](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L156)*

#### Type declaration:

* **lots**: *number*

* **operation**: *[OperationType](globals.md#operationtype)*

* **price**: *number*

___

###  LimitOrderResponse

Ƭ **LimitOrderResponse**: *object*

*Defined in [src/domain.d.ts:162](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L162)*

#### Type declaration:

* **payload**: *[PlacedLimitOrder](globals.md#placedlimitorder)*

* **status**: *string*

* **trackingId**: *string*

___

###  MarketInstrument

Ƭ **MarketInstrument**: *object*

*Defined in [src/domain.d.ts:217](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L217)*

#### Type declaration:

* **currency**? : *[Currency](globals.md#currency)*

* **figi**: *string*

* **isin**? : *undefined | string*

* **lot**: *number*

* **minPriceIncrement**? : *undefined | number*

* **name**: *string*

* **ticker**: *string*

___

###  MarketInstrumentList

Ƭ **MarketInstrumentList**: *object*

*Defined in [src/domain.d.ts:206](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L206)*

#### Type declaration:

* **instruments**: *[MarketInstrument](globals.md#marketinstrument)[]*

* **total**: *number*

___

###  MarketInstrumentListResponse

Ƭ **MarketInstrumentListResponse**: *object*

*Defined in [src/domain.d.ts:200](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L200)*

#### Type declaration:

* **payload**: *[MarketInstrumentList](globals.md#marketinstrumentlist)*

* **status**: *string*

* **trackingId**: *string*

___

###  MarketInstrumentResponse

Ƭ **MarketInstrumentResponse**: *object*

*Defined in [src/domain.d.ts:211](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L211)*

#### Type declaration:

* **payload**: *[MarketInstrument](globals.md#marketinstrument)*

* **status**: *string*

* **trackingId**: *string*

___

###  MoneyAmount

Ƭ **MoneyAmount**: *object*

*Defined in [src/domain.d.ts:52](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L52)*

#### Type declaration:

* **currency**: *[Currency](globals.md#currency)*

* **value**: *number*

___

###  Operation

Ƭ **Operation**: *object*

*Defined in [src/domain.d.ts:123](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L123)*

#### Type declaration:

* **commission**? : *[MoneyAmount](globals.md#moneyamount)*

* **currency**: *[Currency](globals.md#currency)*

* **date**: *string*

* **figi**? : *undefined | string*

* **id**: *string*

* **instrumentType**? : *[InstrumentType](globals.md#instrumenttype)*

* **isMarginCall**: *boolean*

* **operationType**? : *[OperationTypeWithCommission](globals.md#operationtypewithcommission)*

* **payment**: *number*

* **price**? : *undefined | number*

* **quantity**? : *undefined | number*

* **status**: *[OperationStatus](globals.md#operationstatus)*

* **trades**? : *[OperationTrade](globals.md#operationtrade)[]*

___

###  OperationStatus

Ƭ **OperationStatus**: *object*

*Defined in [src/domain.d.ts:184](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L184)*

#### Type declaration:

___

###  OperationTrade

Ƭ **OperationTrade**: *object*

*Defined in [src/domain.d.ts:116](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L116)*

#### Type declaration:

* **date**: *string*

* **price**: *number*

* **quantity**: *number*

* **tradeId**: *string*

___

###  OperationType

Ƭ **OperationType**: *object*

*Defined in [src/domain.d.ts:180](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L180)*

#### Type declaration:

___

###  OperationTypeWithCommission

Ƭ **OperationTypeWithCommission**: *object*

*Defined in [src/domain.d.ts:182](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L182)*

#### Type declaration:

___

###  Operations

Ƭ **Operations**: *object*

*Defined in [src/domain.d.ts:112](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L112)*

#### Type declaration:

* **operations**: *[Operation](globals.md#operation)[]*

___

###  OperationsResponse

Ƭ **OperationsResponse**: *object*

*Defined in [src/domain.d.ts:106](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L106)*

#### Type declaration:

* **payload**: *[Operations](globals.md#operations)*

* **status**: *string*

* **trackingId**: *string*

___

###  Order

Ƭ **Order**: *object*

*Defined in [src/domain.d.ts:145](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L145)*

#### Type declaration:

* **executedLots**: *number*

* **figi**: *string*

* **operation**: *[OperationType](globals.md#operationtype)*

* **orderId**: *string*

* **price**: *number*

* **requestedLots**: *number*

* **status**: *[OrderStatus](globals.md#orderstatus)*

* **type**: *[OrderType](globals.md#ordertype)*

___

###  OrderResponse

Ƭ **OrderResponse**: *object*

*Defined in [src/domain.d.ts:76](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L76)*

#### Type declaration:

* **price**: *number*

* **quantity**: *number*

___

###  OrderStatus

Ƭ **OrderStatus**: *object*

*Defined in [src/domain.d.ts:186](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L186)*

#### Type declaration:

___

###  OrderType

Ƭ **OrderType**: *object*

*Defined in [src/domain.d.ts:188](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L188)*

#### Type declaration:

___

###  Orderbook

Ƭ **Orderbook**: *object*

*Defined in [src/domain.d.ts:63](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L63)*

#### Type declaration:

* **asks**: *[OrderResponse](globals.md#orderresponse)[]*

* **bids**: *[OrderResponse](globals.md#orderresponse)[]*

* **closePrice**? : *undefined | number*

* **depth**: *number*

* **figi**: *string*

* **lastPrice**? : *undefined | number*

* **limitDown**? : *undefined | number*

* **limitUp**? : *undefined | number*

* **minPriceIncrement**: *number*

* **tradeStatus**: *[TradeStatus](globals.md#tradestatus)*

___

###  OrderbookResponse

Ƭ **OrderbookResponse**: *object*

*Defined in [src/domain.d.ts:57](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L57)*

#### Type declaration:

* **payload**: *[Orderbook](globals.md#orderbook)*

* **status**: *string*

* **trackingId**: *string*

___

###  OrderbookStreaming

Ƭ **OrderbookStreaming**: *object*

*Defined in [src/OpenAPI.ts:40](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L40)*

#### Type declaration:

* **bids**: *Array‹[number, number]›*

* **depth**: *[Depth](globals.md#depth)*

* **figi**: *string*

___

###  OrdersResponse

Ƭ **OrdersResponse**: *object*

*Defined in [src/domain.d.ts:139](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L139)*

#### Type declaration:

* **payload**: *[Order](globals.md#order)[]*

* **status**: *string*

* **trackingId**: *string*

___

###  PlacedLimitOrder

Ƭ **PlacedLimitOrder**: *object*

*Defined in [src/domain.d.ts:168](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L168)*

#### Type declaration:

* **commission**? : *[MoneyAmount](globals.md#moneyamount)*

* **executedLots**: *number*

* **operation**: *[OperationType](globals.md#operationtype)*

* **orderId**: *string*

* **rejectReason**? : *undefined | string*

* **requestedLots**: *number*

* **status**: *[OrderStatus](globals.md#orderstatus)*

___

###  Portfolio

Ƭ **Portfolio**: *object*

*Defined in [src/domain.d.ts:19](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L19)*

#### Type declaration:

* **positions**: *[PortfolioPosition](globals.md#portfolioposition)[]*

___

###  PortfolioCurrenciesResponse

Ƭ **PortfolioCurrenciesResponse**: *object*

*Defined in [src/domain.d.ts:23](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L23)*

#### Type declaration:

* **payload**: *[Currencies](globals.md#currencies)*

* **status**: *string*

* **trackingId**: *string*

___

###  PortfolioPosition

Ƭ **PortfolioPosition**: *object*

*Defined in [src/domain.d.ts:39](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L39)*

#### Type declaration:

* **averagePositionPrice**? : *[MoneyAmount](globals.md#moneyamount)*

* **averagePositionPriceNoNkd**? : *[MoneyAmount](globals.md#moneyamount)*

* **balance**: *number*

* **blocked**? : *undefined | number*

* **expectedYield**? : *[MoneyAmount](globals.md#moneyamount)*

* **figi**: *string*

* **instrumentType**: *[InstrumentType](globals.md#instrumenttype)*

* **isin**? : *undefined | string*

* **lots**: *number*

* **ticker**? : *undefined | string*

___

###  PortfolioResponse

Ƭ **PortfolioResponse**: *object*

*Defined in [src/domain.d.ts:13](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L13)*

#### Type declaration:

* **payload**: *[Portfolio](globals.md#portfolio)*

* **status**: *string*

* **trackingId**: *string*

___

###  SandboxCurrency

Ƭ **SandboxCurrency**: *object*

*Defined in [src/domain.d.ts:227](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L227)*

#### Type declaration:

___

###  SandboxSetCurrencyBalanceRequest

Ƭ **SandboxSetCurrencyBalanceRequest**: *object*

*Defined in [src/domain.d.ts:190](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L190)*

#### Type declaration:

* **balance**: *number*

* **currency**: *[SandboxCurrency](globals.md#sandboxcurrency)*

___

###  SandboxSetPositionBalanceRequest

Ƭ **SandboxSetPositionBalanceRequest**: *object*

*Defined in [src/domain.d.ts:195](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L195)*

#### Type declaration:

* **balance**: *number*

* **figi**? : *undefined | string*

___

###  SocketEventType

Ƭ **SocketEventType**: *"orderbook" | "candle" | "instrument_info"*

*Defined in [src/OpenAPI.ts:38](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L38)*

___

###  TradeStatus

Ƭ **TradeStatus**: *object*

*Defined in [src/domain.d.ts:178](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/domain.d.ts#L178)*

#### Type declaration:

## Variables

### `Const` WebSocket

• **WebSocket**: *any* = require('ws')

*Defined in [src/OpenAPI.ts:21](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L21)*

## Functions

###  getQueryString

▸ **getQueryString**(`params`: object): *string*

*Defined in [src/OpenAPI.ts:57](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L57)*

**Parameters:**

Name | Type |
------ | ------ |
`params` | object |

**Returns:** *string*

___

###  once

▸ **once**<**P**, **R**>(`fn`: function): *function*

*Defined in [src/OpenAPI.ts:72](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L72)*

**Type parameters:**

▪ **P**: *Array‹any›*

▪ **R**

**Parameters:**

▪ **fn**: *function*

▸ (...`args`: P): *R*

**Parameters:**

Name | Type |
------ | ------ |
`...args` | P |

**Returns:** *function*

▸ (...`args`: P): *R*

**Parameters:**

Name | Type |
------ | ------ |
`...args` | P |
