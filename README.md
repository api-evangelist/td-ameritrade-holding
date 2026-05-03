# TD Ameritrade Holding

TD Ameritrade Holding Corporation was a brokerage firm that provided online brokerage and related services for individual investors. The company was acquired by Charles Schwab in 2020 and the TD Ameritrade platform was fully migrated to Charles Schwab in May 2024. TD Ameritrade offered a developer API for programmatic access to trading, account management, market data, and order management capabilities.

> **Note:** The TD Ameritrade API is deprecated. The successor API is the [Charles Schwab Trader API](https://developer.schwab.com).

**Website:** [https://www.tdameritrade.com](https://www.tdameritrade.com)  
**Successor:** [https://developer.schwab.com](https://developer.schwab.com)

## APIs

### TD Ameritrade Accounts and Trading API (Deprecated)

Programmatic access to brokerage account information, order management, market data, instruments, watchlists, and trading operations. Deprecated May 2024.

- **Base URL:** `https://api.tdameritrade.com/v1`
- **Authentication:** OAuth 2.0
- **OpenAPI:** [openapi/td-ameritrade-accounts-trading-openapi.yml](openapi/td-ameritrade-accounts-trading-openapi.yml)

#### Key Endpoints

| Method | Path | Summary |
|--------|------|---------|
| GET | `/accounts` | Get All Accounts |
| POST | `/accounts/{accountId}/orders` | Place Order |
| GET | `/marketdata/quotes` | Get Quotes |
| GET | `/marketdata/{symbol}/pricehistory` | Get Price History |
| GET | `/marketdata/chains` | Get Option Chain |
| GET | `/instruments` | Search Instruments |
| GET | `/accounts/{accountId}/transactions` | Get Transactions |
| GET | `/accounts/{accountId}/watchlists` | Get Watchlists |
| GET | `/userprincipals` | Get User Principals |

## Features

- **Account Management** - Access balances, positions, and account information
- **Order Management** - Place, modify, cancel, and retrieve trade orders
- **Watchlist Management** - Create and manage security watchlists
- **Real-Time Quotes** - Access real-time market quotes for securities
- **Price History** - Historical OHLCV data at various frequencies
- **Options Chain** - Option chain data for optionable symbols
- **Instrument Search** - Search securities by symbol, CUSIP, or description
- **Transaction History** - Account transaction history and activity
- **OAuth 2.0** - Secure authentication with refresh token support

## Artifacts

### OpenAPI Specifications

| File | Description |
|------|-------------|
| [openapi/td-ameritrade-accounts-trading-openapi.yml](openapi/td-ameritrade-accounts-trading-openapi.yml) | Accounts and Trading API |

### Naftiko Capabilities

| File | Description |
|------|-------------|
| [capabilities/trading-and-portfolio.yaml](capabilities/trading-and-portfolio.yaml) | Trading and portfolio management workflow |
| [capabilities/shared/accounts-trading.yaml](capabilities/shared/accounts-trading.yaml) | Shared accounts and trading API definition |

### Spectral Rules

| File | Description |
|------|-------------|
| [rules/td-ameritrade-rules.yml](rules/td-ameritrade-rules.yml) | Spectral ruleset for TD Ameritrade API conventions |

### JSON Schemas

| File | Description |
|------|-------------|
| [json-schema/td-ameritrade-order-schema.json](json-schema/td-ameritrade-order-schema.json) | Trade order schema |

### JSON Structures

| File | Description |
|------|-------------|
| [json-structure/td-ameritrade-order-structure.json](json-structure/td-ameritrade-order-structure.json) | Order field documentation |

### JSON-LD Context

| File | Description |
|------|-------------|
| [json-ld/td-ameritrade-context.jsonld](json-ld/td-ameritrade-context.jsonld) | Linked data context for brokerage vocabulary |

### Examples

| File | Description |
|------|-------------|
| [examples/td-ameritrade-place-order-example.json](examples/td-ameritrade-place-order-example.json) | Limit order placement example |
| [examples/td-ameritrade-get-quotes-example.json](examples/td-ameritrade-get-quotes-example.json) | Multi-symbol quote retrieval example |

### Vocabulary

| File | Description |
|------|-------------|
| [vocabulary/td-ameritrade-vocabulary.yml](vocabulary/td-ameritrade-vocabulary.yml) | Brokerage and trading domain terminology |

## Maintainers

**FN:** Kin Lane  
**Email:** info@apievangelist.com
