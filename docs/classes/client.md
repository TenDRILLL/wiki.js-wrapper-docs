# Client
The class which is used to interact with the Wiki.js API.

### Constructor
```js
new Client({options});
```

> Returns a [Client](/classes/client).

|Parameter|Type|Description|Required
---|---|---|---
|baseURL|String|Wiki.js API address, usually ends with /graphql|✅
|token|String|Wiki.js API token|✅

### Properties
- &lt;Client&gt;.pages<br>
> Used to access methods related to Wiki.js pages.<br>
> Created upon login.<br>
> Null if accessed prior to a successful login.<br>
> **Type:** ?[PageManager](/classes/pagemanager)

### Methods
- &lt;Client&gt;.login()
> Used to verify provided Client options and connect to the Wiki.js API.<br>
> Upon successful verification method returns the title of the Wiki.js instance.<br>
> **Returns:** Promise&lt;String&gt;
