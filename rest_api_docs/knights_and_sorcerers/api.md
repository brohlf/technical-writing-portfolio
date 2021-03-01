# API Reference for Knights and Sorcerers

## Contents
- [Overview](#Overview)
  - [Response Data Categories](#ResponseDataCategories)
- [Authentication](#Authentication)
- [Rate Limiting](#RateLimiting)
- [Pagination](#Pagination)
- [Localization](#Localization)
- [Resources](#Resources)
  - [Servers](#Servers)
  - [Characters](#Characters)

## 1. Overview <a name="Overview"></a>
The Knights and Sorcerers API is RESTful. It provides static, semi-static, and continuous game data related to servers and characters. 

### 1.1. Response Data Categories <a name="ResponseDataCategories"></a>

#### 1.1.1. static data
Static data changes infrequently, if at all.

The following are examples of static data:
- character name
- server name

#### 1.1.2. Semi-static data
Semi-static data could change frequently, but it does not change continuously.

The following are examples of semi-stataic data:
- server status
- character achievements

#### 1.1.3. Continuous data
Continuous data changes frequently. Clients should expect it to be different every time they request it.

The following are examples of continuous data:
- server population
- a character's PVP kills


By using the Knights and Sorcerers API, you agree to our [terms of service](#Overview).

## 2. Authentication <a name="Authentication"></a>
The Knights and Sorcerers API requires clients to authenticate using an OAuth 2.0 access token. To acquire an acess token, see our [Authorization Guide](#Authentication).

In every request's header, include a valid OAuth access token. <!-- TODO: list 2.0? , cap "access token"? -->

```
example of OAuth access token attachment ???
```

## 3. Rate Limiting <a name="RateLimiting"></a>
Clients are rate limited based on their memebrship tier.

Free tier clients: 100 calls per minute
Paid tier clients: 2500 calls per mintue

Fore more information about membership tiers and their benefits, see our [Membership Tier Guide](#RateLimiting).

## 4. Pagination <a name="Pagination"></a>

## 5. Localization <a name="Localization"></a>

## 6. Resources <a name="Resources"></a>

### 6.1. Servers <a name="Servers"></a>

### 6.2. Characters <a name="Characters"></a>
