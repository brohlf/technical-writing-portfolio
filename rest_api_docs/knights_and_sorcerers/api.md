# API Reference for Knights and Sorcerers
<!-- TODO: client, or you tone?? , how should I handle localization?? -->
## Contents
- [Overview](#overview)
  - [Quickstart Guide](#quickstartGuide)
  - [Categories of Resource Data](#resourceDataCategories)
  - [Region Codes](#regionCodes)
- [Authentication](#authentication)
- [Rate Limiting](#rateLimiting)
- [Pagination](#pagination)
- [Localization](#localization)
- [Resources](#resources)
  - [Servers](#servers)
  - [Characters](#characters)

## 1. Overview <a name="overview"></a>
The Knights and Sorcerers (KS) API is RESTful. It provides static, semi-static, and continuous game data related to servers and characters.

### 1.1. Quickstart Guide <a name="quickstartGuide"></a>
If you are just getting started, see our developer [quickstart guide](#overview). It will walk you through authorization and help you make your first request using cURL.

### 1.2. Categories of Resource Data <a name="resourceDataCategories"></a>

#### 1.2.1. static data
Static data changes infrequently, if at all.

The following are examples of static data:
- character name
- server name

#### 1.2.2. Semi-static data
Semi-static data could change frequently, but it does not change continuously.

The following are examples of semi-stataic data:
- server status
- character achievements

#### 1.2.3. Continuous data
Continuous data changes frequently. Clients should expect it to be different every time they request it.

The following are examples of continuous data:
- server population
- a character's PVP kills

### 1.3.1. Region Codes <a name="regionCodes"></a>
All of our servers have one instance per region. When requesting data about an character or server, you must include the region code.

Our server run in the following regions:
| Region                   | Region Code |
| :----------------------- | ----------- |
| United States of America | USA         |
| Europe                   | EU          |
| China                    | CN          |

By using the KS API, you agree to our [terms of service](#overview).  
&nbsp;
## 2. Authentication <a name="authentication"></a>
The KS API requires clients to authenticate using an OAuth 2.0 access token. To acquire an acess token, see our developer [quickstart guide](#authentication).

In every request's header, include a valid OAuth access token. <!-- TODO: list 2.0? , cap "access token"? -->

```
example of OAuth access token attachment ???
```  
&nbsp;
## 3. Rate Limiting <a name="rateLimiting"></a>
Clients are rate limited based on their memebrship tier.

Free tier clients: 100 calls per minute  
Paid tier clients: 2500 calls per mintue

Fore more information about membership tiers and their benefits, see our [Membership Tier Guide](#rateLimiting).  
&nbsp;
## 4. Pagination <a name="pagination"></a>  
&nbsp;
## 5. Localization <a name="localization"></a>
The KS API Does not provide localization at this time, but we are working on it!  
&nbsp;
## 6. Resources <a name="resources"></a>

Base URL:
```
https://knightsandsorcerers.com
```

### 6.1. Servers <a name="servers"></a>

#### 6.1.1. Servers
List all servers for all regions or for a given region.

path
```
/listservers
```

Path Parameters
| Parameter   | Description |
| :---------- | :---------- |

Query String Parameters
| Parameter   | Description |
| :---------- | :---------- |

Example request using cURL:
```
curl https://knightsandsorcerers.com/listservers
```
Example response:
```JSON
{
  "servers": [
    {
      "id": 1001,
      "name": "Merlin",
      "region": "USA",
      "status": "UP",
      "population": 97573
    },
    {
      "id": 2001,
      "name": "Merlin",
      "region": "EU",
      "status": "UP",
      "population": 127699
    },
    {
      "id": 3007,
      "name": "Arthur",
      "region": "CN",
      "status": "DOWN",
      "population": 76509
    }
  ]
}
```
**Note:** The real response would be prohibitively long, so we've shown only a subset.

Response Description
| Response Item    | Item Description | Data Type    |
| :--------------- | :--------------- | :------------|

#### 6.1.1. Server status

### 6.2. Characters <a name="characters"></a>
