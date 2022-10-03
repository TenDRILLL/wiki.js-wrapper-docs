# PageManager
The class containing Wiki.js page related methods.

### Constructor
```js
new PageManager(Client);
```

> Returns a [PageManager](/classes/pagemanager).

### Methods

- &lt;PageManager&gt;.get(id);

|Parameter|Type|Description|Required|
---|---|---|---
|id|Int|ID of the page to get.|✅|

> Used to get a page by ID from the Wiki.js instance.<br>
> **Returns:** Promise&lt;[PageObject](/structures/pageobject)&gt; 

- &lt;PageManager&gt;.search(query | queryObject);

|Parameter|Type|Description|Required|
---|---|---|---
|query|String|Search string.|✳|
|queryObject|[SearchPageQuery](/structures/searchpagequery)|Object containing options for search.|✳|

> ✳ Either one is required.<br>
> Used to get a page by ID from the Wiki.js instance.<br>
> **Returns:** Promise&lt;[PageObject](/structures/pageobject)&gt;