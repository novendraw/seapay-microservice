# Seapay

## Prerequisites
+ Make (GNU utility to maintain groups of programs)
+ PostgreSQL (Sophisticated object-relational DBMS)
## Description
Seapay is a fintech app consists of 4 different services
  - API gateway
    - API gateway service routes all requests to other services
  - User account
    - User account service takes care of user management: user creation, get user data, etc
  - Wallet
    - Wallet service handles all wallet functionalities: update balance, get balance, create wallet, etc
  - Transaction
    - Transaction service manage all transaction data

The project itself has 4 modules
 - seapay-api
   - a module that abstracts interface for all services
 - seapay-common
   - a module that groups all common functionalities used by all services
 - seapay-domain
   - the bussiness logic for all services goes here
 - seapay-monolith
   - an entry point of our monolithic app, including all handlers
  
## Installation
##### 1. Clone the repo
```
git clone https://github.com/novendraw/seapay-microservice    
```
##### 2. Run the Makefile
```
make all
```
##### 3. Run all the services
```
make run-monolith run-gateway run-transaction run-user run-wallet
``` 
## Usage
Sending HTTP request to the appropriate address:
```
curl -X GET \
  http://localhost:8080/ping \
  -H 'Accept: */*' \
  -H 'Accept-Encoding: gzip, deflate' \
  -H 'Cache-Control: no-cache' \
  -H 'Connection: keep-alive' \
  -H 'Host: localhost:8080' \
  -H 'Postman-Token: 0fc45346-52c2-43f7-a034-3e2323c34d45,1fbb4925-9661-442d-aa5b-1e2124255511' \
  -H 'User-Agent: PostmanRuntime/7.15.2' \
  -H 'cache-control: no-cache'
```
## License
Copyright 2019, Pangeran Kopi Kenangan.
  



