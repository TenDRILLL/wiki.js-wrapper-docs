# wiki.js-wrapper

## About
> wiki.js-wrapper is a work-in-progress wrapper for the Wiki.js API (GraphQL)<br>
> written in Typescript.

## Installation
wiki.js-wrapper doesn't have any dependencies, <br>
and is available through the node package manager
```
npm i wiki.js-wrapper
```

## Example usage
Get a token for the API through the admin-panel, and provide the URL for your Wiki.js instance.
```js
const {Client} = require("wiki.js-wrapper");
const client = new Client({
    baseURL: "https://example.com/graphql",
    token: "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhcGkiOjEsImdycCI6MSwiaWF0IjoxNjQ5MjAzMjAwLCJleHAiOjE2ODA3MzkyMDAsImF1ZCI6InVybjp3aWtpLmpzIiwiaXNzIjoidXJuOndpa2kuanMiLCJ0eXBlIjoiZmFrZS1hc3MtdG9rZW4ifQ.FEWmrlsNrmbf9ESIgOhECNB_N9wRofUbM6UYLGpUrlw"
});

client.login()
    .then((title)=>{
        console.log(`Connected to ${title}.`);
        client.pages.get(1)
            .then(page => {
                console.log(page);
            })
            .catch(e => {
                console.error(e);    
            });
    })
    .catch(e => {
        console.error(e);
    });
```

## Links
- [Source Code](https://github.com/TenDRILLL/wiki.js-wrapper)
- [NPM](https://www.npmjs.com/package/wiki.js-wrapper)

## Contributing
Should you wish to contribute to the application,<br>
you may fork this repository and create a pull request.

## Thank You's
- [Ten](https://github.com/TenDRILLL) for creating this package.
- [Discord.js](https://discord.js.org/) for inspiration on package and documentation.
- [Ben Jamming](https://github.com/BenjammingKirby) for help with typings.