### m2.4.4 features
- php 8.1 support
- 3rd party dependencies upgrade
- opensearch & analytics suite
- decoupling vendor bundle extensions
- expended grapql coverage

- live search
- seller assitsted shopping
- b2b purchase approval
- payment services

## securities
- PCI compliance
- multiple security enhancement
- security patches are not backported

### performance
- new indexer for gift card
- 8.1 performance
- deferring sales rules calculation for faster cart
- improvment to asynchronous ordering
  - support to 200M eSKU, 60k order per minute & 750 items in cart
 
 ### strategy
 
| Project Kickoff  | Annual planning   | Upgrade Execution  |
|---|---|---|
| Monitor release schedule  | Partner/Merchant coordination  | analysis  |
| setup upgrade expectations  | discuss yearly plaform health,security impact,direction & strategy  | Dev & QA  |
| define when & how to plan for upgrade  | define yearly goals & KPIs   | UAT & Launch Prep  |
|   | Assign budget & release windows  | Launch  |
|  | Post-Launch | 


##### upgrade execution: analysis
- scope of target release
- upgrade compatibility tool results
- upgrading services to support target version
- extensions and third-party modules
- custom modules
- composer packages and dependencies

| Service  | current version   | upgrade version  |
|---|---|---|
| PHP  | 7.2.33  | 7.4  |
| Redis  | 5.05  | 6.0  |
| Rabbitmq  | 3.7  | 3.8  |
| Mariadb  | 10.2.33  | 10.4  |
| composer  | 1.9.2  | 2.0  |
| elasticsearch  |   | 7.9  |

| module name  | composer package   | vendor  | current version | functionality | comaptible with latest AC version? | issues | native in AC | action |Notes |
|--|---|---|---|---|---|---|---|---|---|
|||||||||||

| module name  | functionality | required | native in AC | action |Notes |
|--|---|---|---|---|--|
| | business requirement | | | | |

##### upgrade execution: Development & QA

- Application tesing guide
- 
