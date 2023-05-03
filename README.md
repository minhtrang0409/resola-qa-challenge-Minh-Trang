## Assignment solving Approach

I've selected the USS APIs to prepare the test cases, bug reports and test report.
As I inspected the API specification, I noticed there are several environments available, but as I'm lacking the access to the dev/staging environment, I've been using the Mock server to proceed with the challenge.
Due to this, I wasn't able to execute the API calls and expect the actual result since the mock server only gives me a few ideas about what the response would actually be. Also, usually I'd access staging databases to properly check if the data has been correctly added/updated/removed as expected from the endpoints, so I'm skipping this part in the test cases. 


## Installation
- Install Postman https://www.postman.com/downloads/ 
- Install NodeJS https://nodejs.org/en/
- Install Newman and its HTML Reporter by running
```
npm i -g newman
npm i -g newman-reporter-htmlextra
```

## Executing tests in Postman
- Open Postman
- Select App menu, select File, and Import
- Select `./postman-collections/uss-api.json` file located in this project directory

## Executing tests and generate reports instructions
- Open terminal and navigate to this project directory
- Run
```
newman run postman-collections/uss-api.json -r htmlextra
```

- The tests will be executed and the report will be generated at `./newman/*.html`
