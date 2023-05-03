
## Installation

- Install NodeJS https://nodejs.org/en/
- Install Newman and its HTML Reporter by running
```
npm i -g newman
npm i -g newman-reporter-htmlextra
```

## Running tests and generate reports instructions
- Open terminal and navigate to this project directory
- Run
```
newman run postman-collections/uss-api.json -r htmlextra
```

- The tests will be executed and the report will be generated at `./newman/*.html`
