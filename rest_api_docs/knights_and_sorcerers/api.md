# Knights and Sorcerers API Documentation

## Contents
- [Overview](Overview)

## 1. Overview </a name="Overview">
The Knights and Sorcerers API is RESTful. It provides satic, semi-static, and continuous game data related to servers and characters. 

### 1.1. static data
Static data changes infrequently, if at all.

The following are examples of static data:
- character name
- server name

### 1.2. Semi-static data
Semi-static data could change frequently, but it does not change continuously.

The following are examples of semi-stataic data:
- server status
- character achievements

### 1.3. Continuous data
Continuous data changes frequently. Clients should expect it to be different every time they request it.

The following are examples of continuous data:
- server population
- a character's PVP kills

By using the Knights and Sorcerers API, you agree to our [terms of service](https://github.com/brohlf/technical-writing-portfolio/blob/main/rest_api_docs/knights_and_sorcerers/api.md).

## 2. Authentication
The Knights and Sorcerers API requires clients to authenticate using an OAuth 2.0 access token. To acquire an acess token, see our [Authorization Guide](https://github.com/brohlf/technical-writing-portfolio/blob/main/rest_api_docs/knights_and_sorcerers/api.md).

In every request's header, include a valid OAuth access token. <!-- TODO: list 2.0? , cap "access token"? -->

```
example of OAuth access token attachment ???
```

## 3. Rate Limiting
Clients are rate limited based on their memebrship tier.

Free tier clients: 100 calls per minute
Paid tier clients: 2500 calls per mintue

Fore more information about membership tiers and their benefits, see our [Membership Tier Guide](https://github.com/brohlf/technical-writing-portfolio/blob/main/rest_api_docs/knights_and_sorcerers/api.md).

## 4. Pagination

## 5. Localization

## 6. Resources

### 6.1. Servers

### 6.2. Characters
