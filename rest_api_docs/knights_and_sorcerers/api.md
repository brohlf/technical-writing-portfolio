# API Reference for Knights and Sorcerers

## Contents
- [Overview](#overview)
  - [Quickstart Guide](#quickstartGuide)
  - [Categories of Resource Data](#resourceDataCategories)
  - [Region Codes](#regionCodes)
- [Authentication](#authentication)
- [Resources](#resources)
  - [Servers](#serverData)
  - [Characters](#characterData)

## 1. Overview <a name="overview"></a>
With the Knights and Sorcerers (KaS) RESTful API, you can get detailed information about game servers and player characters. Our endpoints respond in JSON format and use standard HTTP response codes.

All requests must use the HTTP secure protocol: ```https```

Our endpoints build on this base url: ``` https://BASEURL```

By using the KaS API, you agree to our [terms of service](#overview).  

### 1.1. Quickstart Guide <a name="quickstartGuide"></a>
If you are just getting started, see our developer [quickstart guide](#overview). It will walk you through authorization and making your first request.

### 1.2. Categories of Resource Data <a name="resourceDataCategories"></a>
Our endpoints respond with data that we classify in three ways. Data can be static, semi-static, or continuous. 

#### 1.2.1. Static
Static data changes infrequently, if at all.

Examples of static data:
- character name
- server name

#### 1.2.2. Semi-Static
Semi-static data could change frequently, but it does not change continuously.

Examples of semi-stataic data:
- server status
- character achievements

#### 1.2.3. Continuous
Continuous data changes frequently. You should expect it to be different every time you request it.

Examples of continuous data:
- server population
- a character's kill count

### 1.3. Region Codes <a name="regionCodes"></a>
At this time, we serve three geographic regions. Each server has one instance per region. You can include region codes with your request to filter your results.

Our servers are deployed in the following regions:
| Region                   | Region Code |
| :----------------------- | ----------- |
| United States of America | USA         |
| Europe                   | EU          |
| China                    | CN          | 

## 2. Authentication <a name="authentication"></a>
To access our data, you will need an API key. If you do not have one, see our developer [quickstart guide](#overview).

We suport the following two methods of authentication.

Authenticating in your request header:
```
curl -H 'Authentication: bearer <your-api-key>' '<baseurl>/<endpoint-path>/'
```

Authenticating in the query string:
```
curl '<baseurl>/<endpoint-path>/?api-key=<your-api-key>'
```  

While we suport both methods, **we recommend** attaching your API key to your request header because this is more secure.

## 3. Resources <a name="resources"></a>

Our endpoints build on this base url:
```
https://BASEURL
```

### 3.1. Servers <a name="serverData"></a>

Server objects contain data about the identity and status of our game servers. The following endpoints provide general and targeted approaches to monitoring this data.

Endpoints:
```
GET  /listservers
GET  /listservers/:id
GET  /listservers/?region-code=regionCode
GET  /listservers/?name=serverName
```

Path parameters:
| Parameter   | Description | Data Type   |
| :---------- | :---------- | :---------- |
| ```id```    | Four digit integer that identifies a single server. | Integer |

Query string parameters:
| Parameter   | Description | Data Type   |
| :---------- | :---------- | :---------- |
| ```name``` <a name="serverName"></a> | Identifies a server by its name. Filters out all servers that do not have the given name. Two servers can only have the same name if they are in different regions. A name will not be longer than 32 characters. | String |
| ```region-code``` | Filters out all servers that are not in the given regions. You may provide one region or a comma-separated list of regions. | String |

Example request:
```
curl -H 'Authentication: bearer <your-api-key>' 'https://BASEURL/listservers'
```
Example response:
```JSON
{
  "servers": [
    {
      "id": 1001,
      "name": "Merlin",
      "region-code": "USA",
      "status": "ONLINE",
      "population": 97573
    },
    {
      "id": 2001,
      "name": "Merlin",
      "region-code": "EU",
      "status": "RESETTING",
      "population": 27699
    },
    {
      "id": 3007,
      "name": "Arthur",
      "region-code": "CN",
      "status": "OFFLINE",
      "population": 76509
    }
  ]
}
```
**Note:** The real response to our example request would be too long to display. This example response shows only a subset of what you would see.

Response variable descriptions:
| Response Item    | Item Description | Data Category | Data Type     |
| :--------------- | :--------------- | :------------ | :------------ |
| ```id```         | Identifies a specific server resource. The first digit indicates the server's region, and the following three digits indicate when that server was created. For example, if a server's first digit is "1", that server is in the USA. "Merlin" was our first server, so its last three digits are "001". So, an ```id``` of "1001" and "2001" identify the USA and EU instances of our first server, respectively. | static | Integer |
| ```name```       | Identifies a server by its name. Refer to the descipription of the [*name*](#serverData) path parameter for details. | static | String |
| ```region-code```| Idenitifies a server's geographic location. Region codes will not be longer than 5 characters. | static | String |
| ```status```     | Possible values are "ONLINE", "OFFLINE", and "RESETTING". A resetting server is offline but is expected to come back online shortly. | semi-static | String |
| ```population``` | Indicates how many active players have characters on this server. An active player is one who has played for at least 10 hours in the past two months. Maximum population per server is 100,000. | continuous | Integer |

### 3.2. Characters <a name="characterData"></a>

Characer objects contain data about the state of player characters, which each exist on exactly one server. The following endpoints provide general and targeted approaches to monitoring this data.

Endpoints:
```
GET /listcharacters/:id
GET /listcharacters/?serverid=serverId
GET /listcharacters/?name=characterName
```

Path parameters:
| Parameter   | Description | Data Type   |
| :---------- | :---------- | :---------- |
| ```id``` | Identifies a specific character object. Each id is unique across all servers. | Integer |

Query string parameters:
| Parameter   | Description | Data Type   |
| :---------- | :---------- | :---------- |
| ```serverid``` | Refer to the server resource description of this value. It identified all characters belonging to the referenced server.  | Integer |
| ```name``` | Identifies a specific character object on one server. Each name is unique on the character's server. Two characters may only have the same name if the characters exist on different servers. | String |

Example request:
```
curl -H 'Authentication: bearer <your-api-key>' 'https://BASEURL/?name=Lushan'
```
Example response:
```JSON
{
    "characters": [
        {
            "id": 34719,
            "name": "Lushan",
            "server": 1001,
            "class": "Sorcerer",
            "level": 60,
            "status": "ALIVE",
            "kills": 73
        },
        {
            "id": 66735,
            "name": "Lushan",
            "server": 3007,
            "class": "Knight",
            "level": 32,
            "status": "DEAD",
            "kills": 13
        }
    ]
}
```

Response variable descriptions:
| Response Item    | Item Description | Data Category | Data Type     |
| :--------------- | :--------------- | :------------ | :------------ |
| ```id``` | Refer to the path parameter description of this value. | static | Integer |
| ```name``` | Refer to the query string parameter description of this value. | static | String |
| ```server``` | Refer to the query string parameter description of this value. | static | Integer |
| ```class``` | Names a character's class. Possible values are "sorcerer" and "knight". | static | String |
| ```status``` | Marks if the character is alive or dead. Possible values are "alive" and "dead". | continuous | String |
| ```level``` | Marks the character's class level. The minimum value is 1, and the maximum value is 60. | semi-static | Integer |
| ```kills``` | Scores how many other player character kills the character has achieved in player vs. player combat. | continuous | Integer |
