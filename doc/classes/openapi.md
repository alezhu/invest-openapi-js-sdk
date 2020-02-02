[@tinkoff/invest-openapi-js-sdk](../README.md) › [Globals](../globals.md) › [OpenAPI](openapi.md)

# Class: OpenAPI

## Hierarchy

* EventEmitter

  ↳ **OpenAPI**

## Index

### Constructors

* [constructor](openapi.md#constructor)

### Methods

* [bonds](openapi.md#bonds)
* [cancelOrder](openapi.md#cancelorder)
* [candle](openapi.md#candle)
* [candlesGet](openapi.md#candlesget)
* [currencies](openapi.md#currencies)
* [etfs](openapi.md#etfs)
* [instrumentInfo](openapi.md#instrumentinfo)
* [instrumentPortfolio](openapi.md#instrumentportfolio)
* [limitOrder](openapi.md#limitorder)
* [operations](openapi.md#operations)
* [orderbook](openapi.md#orderbook)
* [orderbookGet](openapi.md#orderbookget)
* [orders](openapi.md#orders)
* [portfolio](openapi.md#portfolio)
* [sandboxClear](openapi.md#sandboxclear)
* [search](openapi.md#search)
* [searchOne](openapi.md#searchone)
* [setCurrenciesBalance](openapi.md#setcurrenciesbalance)
* [setPositionBalance](openapi.md#setpositionbalance)
* [stocks](openapi.md#stocks)
* [userAccounts](openapi.md#useraccounts)

## Constructors

###  constructor

\+ **new OpenAPI**(`__namedParameters`: object): *[OpenAPI](openapi.md)*

*Overrides void*

*Defined in [src/OpenAPI.ts:90](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L90)*

**Parameters:**

▪ **__namedParameters**: *object*

Name | Type | Description |
------ | ------ | ------ |
`apiURL` | string | REST api url см [документацию](https://tinkoffcreditsystems.github.io/invest-openapi/env/) |
`secretToken` | string | токен доступа см [получение токена доступа](https://tinkoffcreditsystems.github.io/invest-openapi/auth/)   |
`socketURL` | string | Streaming api url см [документацию](https://tinkoffcreditsystems.github.io/invest-openapi/env/) |

**Returns:** *[OpenAPI](openapi.md)*

## Methods

###  bonds

▸ **bonds**(): *Promise‹[MarketInstrumentList](../globals.md#marketinstrumentlist)›*

*Defined in [src/OpenAPI.ts:311](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L311)*

Метод для получения всех доступных облигаций

**Returns:** *Promise‹[MarketInstrumentList](../globals.md#marketinstrumentlist)›*

___

###  cancelOrder

▸ **cancelOrder**(`__namedParameters`: object): *Promise‹void›*

*Defined in [src/OpenAPI.ts:283](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L283)*

Метод для отмены активных заявок

**Parameters:**

▪ **__namedParameters**: *object*

Name | Type | Description |
------ | ------ | ------ |
`orderId` | string | идентифткатор заявки  |

**Returns:** *Promise‹void›*

___

###  candle

▸ **candle**(`__namedParameters`: object, `cb`: function): *unsubscribe*

*Defined in [src/OpenAPI.ts:422](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L422)*

Метод для подписки на данные по свечному графику инструмента

**`example`** см. метод [orderbook](openapi.md#orderbook)

**Parameters:**

▪ **__namedParameters**: *object*

Name | Type | Default | Description |
------ | ------ | ------ | ------ |
`figi` | string | - | идентификатор инструмента |
`interval` | "1min" &#124; "2min" &#124; "3min" &#124; "5min" &#124; "10min" &#124; "15min" &#124; "30min" &#124; "hour" &#124; "2hour" &#124; "4hour" &#124; "day" &#124; "week" &#124; "month" | "1min" | интервал для свечи |

▪`Default value`  **cb**: *function*= console.log

функция для обработки новых данных по свечи

▸ (`x`: [CandleStreaming](../globals.md#candlestreaming)): *any*

**Parameters:**

Name | Type |
------ | ------ |
`x` | [CandleStreaming](../globals.md#candlestreaming) |

**Returns:** *unsubscribe*

функция для отмены подписки

___

###  candlesGet

▸ **candlesGet**(`__namedParameters`: object): *Promise‹[Candles](../globals.md#candles)›*

*Defined in [src/OpenAPI.ts:341](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L341)*

Метод для получения исторических свечей по FIGI

**Parameters:**

▪ **__namedParameters**: *object*

Name | Type | Default | Description |
------ | ------ | ------ | ------ |
`figi` | string | - | Figi-идентификатор инструмента |
`from` | string | - | Начало временного промежутка в формате ISO 8601 |
`interval` | "1min" &#124; "2min" &#124; "3min" &#124; "5min" &#124; "10min" &#124; "15min" &#124; "30min" &#124; "hour" &#124; "2hour" &#124; "4hour" &#124; "day" &#124; "week" &#124; "month" | "1min" | интервал для свечи  |
`to` | string | - | Конец временного промежутка в формате ISO 8601 |

**Returns:** *Promise‹[Candles](../globals.md#candles)›*

___

###  currencies

▸ **currencies**(): *Promise‹[MarketInstrumentList](../globals.md#marketinstrumentlist)›*

*Defined in [src/OpenAPI.ts:297](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L297)*

Метод для получения всех доступных валютных инструментов

**Returns:** *Promise‹[MarketInstrumentList](../globals.md#marketinstrumentlist)›*

___

###  etfs

▸ **etfs**(): *Promise‹[MarketInstrumentList](../globals.md#marketinstrumentlist)›*

*Defined in [src/OpenAPI.ts:304](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L304)*

Метод для получения всех доступных валютных ETF

**Returns:** *Promise‹[MarketInstrumentList](../globals.md#marketinstrumentlist)›*

___

###  instrumentInfo

▸ **instrumentInfo**(`__namedParameters`: object, `cb`: log): *unsubscribe*

*Defined in [src/OpenAPI.ts:436](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L436)*

Метод для подписки на данные по инструменту

**`example`** см. метод [orderbook](openapi.md#orderbook)

**Parameters:**

▪ **__namedParameters**: *object*

Name | Type | Description |
------ | ------ | ------ |
`figi` | string | идентификатор инструмента |

▪`Default value`  **cb**: *log*= console.log

функция для обработки новых данных по инструменту

**Returns:** *unsubscribe*

функция для отмены подписки

___

###  instrumentPortfolio

▸ **instrumentPortfolio**(`params`: [InstrumentId](../globals.md#instrumentid)): *Promise‹[PortfolioPosition](../globals.md#portfolioposition) | null›*

*Defined in [src/OpenAPI.ts:245](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L245)*

Метод для получение данных по инструменту в портфеле

**Parameters:**

Name | Type |
------ | ------ |
`params` | [InstrumentId](../globals.md#instrumentid) |

**Returns:** *Promise‹[PortfolioPosition](../globals.md#portfolioposition) | null›*

___

###  limitOrder

▸ **limitOrder**(`__namedParameters`: object): *Promise‹[PlacedLimitOrder](../globals.md#placedlimitorder)›*

*Defined in [src/OpenAPI.ts:267](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L267)*

Метод для выставления заявки

**Parameters:**

▪ **__namedParameters**: *object*

Name | Type | Description |
------ | ------ | ------ |
`figi` | string | идентификатор инструмента |
`lots` | number | количество лотов для заявки |
`operation` | object | тип заявки |
`price` | number | цена лимитной заявки  |

**Returns:** *Promise‹[PlacedLimitOrder](../globals.md#placedlimitorder)›*

___

###  operations

▸ **operations**(`__namedParameters`: object): *Promise‹[Operations](../globals.md#operations)›*

*Defined in [src/OpenAPI.ts:328](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L328)*

Метод для получения операций по цб по инструменту

**Parameters:**

▪ **__namedParameters**: *object*

Name | Type | Description |
------ | ------ | ------ |
`figi` | string | Figi-идентификатор инструмента  |
`from` | string | Начало временного промежутка в формате ISO 8601 |
`to` | string | Конец временного промежутка в формате ISO 8601 |

**Returns:** *Promise‹[Operations](../globals.md#operations)›*

___

###  orderbook

▸ **orderbook**(`__namedParameters`: object, `cb`: function): *unsubscribe*

*Defined in [src/OpenAPI.ts:407](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L407)*

Метод для подписки на данные по стакану инструмента

**`example`** 
```typescript
const { figi } = await api.searchOne({ ticker: 'AAPL' });
const unsubFromAAPL = api.orderbook({ figi }, (ob) => { console.log(ob.bids) });
// ... подписка больше не нужна
unsubFromAAPL();
```

**Parameters:**

▪ **__namedParameters**: *object*

Name | Type | Default | Description |
------ | ------ | ------ | ------ |
`depth` | 1 &#124; 2 &#124; 3 &#124; 4 &#124; 5 &#124; 6 &#124; 7 &#124; 8 &#124; 9 &#124; 10 | 3 | - |
`figi` | string | - | идентификатор инструмента |

▪`Default value`  **cb**: *function*= console.log

функция для обработки новых данных по стакану

▸ (`x`: [OrderbookStreaming](../globals.md#orderbookstreaming)): *any*

**Parameters:**

Name | Type |
------ | ------ |
`x` | [OrderbookStreaming](../globals.md#orderbookstreaming) |

**Returns:** *unsubscribe*

функция для отмены подписки

___

###  orderbookGet

▸ **orderbookGet**(`__namedParameters`: object): *Promise‹[Orderbook](../globals.md#orderbook)›*

*Defined in [src/OpenAPI.ts:362](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L362)*

Метод для получение стакана

**Parameters:**

▪ **__namedParameters**: *object*

Name | Type | Default | Description |
------ | ------ | ------ | ------ |
`depth` | 1 &#124; 2 &#124; 3 &#124; 4 &#124; 5 &#124; 6 &#124; 7 &#124; 8 &#124; 9 &#124; 10 | 3 |   |
`figi` | string | - | Figi-идентификатор инструмента |

**Returns:** *Promise‹[Orderbook](../globals.md#orderbook)›*

___

###  orders

▸ **orders**(): *Promise‹[Order](../globals.md#order)[]›*

*Defined in [src/OpenAPI.ts:290](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L290)*

Метод для получения всех активных заявок

**Returns:** *Promise‹[Order](../globals.md#order)[]›*

___

###  portfolio

▸ **portfolio**(): *Promise‹[Portfolio](../globals.md#portfolio)›*

*Defined in [src/OpenAPI.ts:238](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L238)*

Метод для получение портфеля цб

**Returns:** *Promise‹[Portfolio](../globals.md#portfolio)›*

___

###  sandboxClear

▸ **sandboxClear**(): *Promise‹any›*

*Defined in [src/OpenAPI.ts:212](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L212)*

Метод для очистки песочницы

**Returns:** *Promise‹any›*

___

###  search

▸ **search**(`params`: [InstrumentId](../globals.md#instrumentid)): *Promise‹[MarketInstrumentList](../globals.md#marketinstrumentlist)›*

*Defined in [src/OpenAPI.ts:371](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L371)*

Метод для поиска инструментов по figi или ticker

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`params` | [InstrumentId](../globals.md#instrumentid) |   |

**Returns:** *Promise‹[MarketInstrumentList](../globals.md#marketinstrumentlist)›*

___

###  searchOne

▸ **searchOne**(`params`: [InstrumentId](../globals.md#instrumentid)): *Promise‹[MarketInstrument](../globals.md#marketinstrument) | null›*

*Defined in [src/OpenAPI.ts:389](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L389)*

Метод для поиска инструмента по figi или ticker

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`params` | [InstrumentId](../globals.md#instrumentid) |   |

**Returns:** *Promise‹[MarketInstrument](../globals.md#marketinstrument) | null›*

___

###  setCurrenciesBalance

▸ **setCurrenciesBalance**(`params`: [SandboxSetCurrencyBalanceRequest](../globals.md#sandboxsetcurrencybalancerequest)): *Promise‹void›*

*Defined in [src/OpenAPI.ts:230](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L230)*

Метод для задания баланса по валютам

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`params` | [SandboxSetCurrencyBalanceRequest](../globals.md#sandboxsetcurrencybalancerequest) | см. описание типа  |

**Returns:** *Promise‹void›*

___

###  setPositionBalance

▸ **setPositionBalance**(`params`: [SandboxSetPositionBalanceRequest](../globals.md#sandboxsetpositionbalancerequest)): *Promise‹void›*

*Defined in [src/OpenAPI.ts:221](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L221)*

Метод для задания баланса по бумагам

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`params` | [SandboxSetPositionBalanceRequest](../globals.md#sandboxsetpositionbalancerequest) | см. описание типа  |

**Returns:** *Promise‹void›*

___

###  stocks

▸ **stocks**(): *Promise‹[MarketInstrumentList](../globals.md#marketinstrumentlist)›*

*Defined in [src/OpenAPI.ts:318](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L318)*

Метод для получения всех доступных акций

**Returns:** *Promise‹[MarketInstrumentList](../globals.md#marketinstrumentlist)›*

___

###  userAccounts

▸ **userAccounts**(): *Promise‹[UserAccounts](../interfaces/useraccounts.md)›*

*Defined in [src/OpenAPI.ts:440](https://github.com/alezhu/invest-openapi-js-sdk/blob/d881cc4/src/OpenAPI.ts#L440)*

**Returns:** *Promise‹[UserAccounts](../interfaces/useraccounts.md)›*
