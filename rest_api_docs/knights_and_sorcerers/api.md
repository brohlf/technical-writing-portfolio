# API Reference for Knights and Sorcerers
<!-- TODO: client, or you tone?? , how should I handle localization?? -->
## Contents
- [Overview](#overview)
  - [Quickstart Guide](#quickstartGuide)
  - [Categories of Resource Data](#resourceDataCategories)
  - [Region Codes](#regionCodes)
- [Authentication](#authentication)
- [Resources](#resources)
  - [Servers](#servers)
  - [Characters](#characters)

## 1. Overview <a name="overview"></a>
With the Knights and Sorcerer's (KaS) RESTful API, you can get detailed information about game servers and player characters.

Our endpoints response in JSON formation and use standard HTTP response codes.

All requests must use the recure protocol: ```https```

### 1.1. Quickstart Guide <a name="quickstartGuide"></a>
If you are just getting started, see our developer [quickstart guide](#overview). It will walk you through authorization and making your first request.

### 1.2. Categories of Resource Data <a name="resourceDataCategories"></a>
Our endpoints respond with data that we classify in 3 ways. 

Data can be static, semi-static, and continuous. 

#### 1.2.1. static data
Static data changes infrequently, if at all.

Examples of static data:
- character name
- server name

#### 1.2.2. Semi-static data
Semi-static data could change frequently, but it does not change continuously.

Examples of semi-stataic data:
- server status
- character achievements

#### 1.2.3. Continuous data
Continuous data changes frequently. You should expect it to be different every time you request it.

Examples of continuous data:
- server population
- a character's PVP kills

### 1.3.1. Region Codes <a name="regionCodes"></a>
At this time, we serve 3 regions. Our servers have one instance per region. You can unclude the region codes below with your request to filter your results.

Our servers are deployed in the following regions:
| Region                   | Region Code |
| :----------------------- | ----------- |
| United States of America | USA         |
| Europe                   | EU          |
| China                    | CN          |

By using the KaS API, you agree to our [terms of service](#overview).  
&nbsp;
## 2. Authentication <a name="authentication"></a>
The KS API requires clients to authenticate using an OAuth 2.0 access token. To acquire an acess token, see our developer [quickstart guide](#authentication).

In every request's header, include a valid OAuth access token. <!-- TODO: list 2.0? , cap "access token"? -->

```
example of OAuth access token attachment ???
```  
&nbsp;
## 6. Resources <a name="resources"></a>

Base URL:
```
https://BASEURL
```

### 6.1. Servers <a name="servers"></a>

List all servers for all regions or for a given region.

paths
```
/listservers
/listservers/?region-code=regionCode
/listservers/?name=serverName
/listservers/:id
```

Query String Parameters
| Parameter   | Description | Data Type   |
| :---------- | :---------- | :---------- |
| name | If you provide the server name, you will get a list os all servers with that name. MAximum of one per region. | String |
| region-code | if you provide a region code, or a list of regioncodes, comman delimited, you will get all servers in each of the provided reagions. | String |

Path Parameters
| Parameter   | Description | Data Type   |
| :---------- | :---------- | :---------- |
| id | If you provide the server id, your response will contain only that server's resource, if it exists. Otherwise, you can expect a 404 error. | Integer |

Example request using cURL:
```
curl https://BASEURL/listservers
```
Example response:
```JSON
{
  "servers": [
    {
      "id": 1001,
      "name": "Merlin",
      "region": "USA",
      "status": "ONLINE",
      "population": 97573
    },
    {
      "id": 2001,
      "name": "Merlin",
      "region": "EU",
      "status": "ONLINE",
      "population": 27699
    },
    {
      "id": 3007,
      "name": "Arthur",
      "region": "CN",
      "status": "OFFLINE",
      "population": 76509
    }
  ]
}
```
**Note:** The real response would be prohibitively long, so we've shown only a subset.

Response Description
| Response Item    | Item Description | Data Type     |
| :--------------- | :--------------- | :------------ |
| id | Identifies a specific server. The first digit indicates the region and the following three indicate when that server was created. Higher means it was created mosre recently. | integer |
| name | Name of the server. A name is used once per region. A name will not be longer than 32 characters. | String |
| region | Inidacte geographic region. Where the server is geographically. Region codes will nto be longer than 5 characters. | String |
| status | Possible values are "ONLINE" and "OFFLINE". | String |
| population | Indicates how many active players are have characters on this server. An active player is one who has played for at least 10 hours in the past 2 months. Maximum population per server is 100,000. | integer |
