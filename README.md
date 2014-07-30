Autocomplete
============
This is yet another jquery autocomplete plugin with a couple of specific functions. 
Some of them:

- The button to show all results and related callback;
- Translitiration for cyrillyc input;
- Configurable css-classes;

## Usage

Usage is quite simple. You just have to set up lookup data and some options (if you need it).
For example:

```javascript
var lookupDataArray = [
    {"data": "<url of current item>", "value": "<text value, to recognize current search item>"},
    ...
    {"data": "<url of current item>", "value": "<text value, to recognize current search item>"}
];

$("<search field selector>").autocomplete({
    "lookup": lookupDataArray,
    "autoSelectFirst": true,
    "showAll": function (suggestions) {
        // do something
    }
});
```

## Options

#### lookup

|**Parameter**|lookup|
| ------------- | ------- |
|**Type**|`Array`|
|**Default**|`[] (empty array)`|
|**Required**|Yes|
|**Description**|Data for autocomplete|

#### transliteration
|**Parameter**|transliteration|
| ------------- | ------- |
|**Type**|`Boolean`|
|**Default**|`true`|
|**Required**|No|
|**Description**|It defines if we need to transliterate cyrilic symbols (e.g. "лента"-> "lenta", "триггер"->"trigger")|

#### autoSelectFirst

|**Parameter**|autoSelectFirst|
| ------------- | ------- |
|**Type**|`Boolean`|
|**Default**|`true`|
|**Required**|No|
|**Description**|If defined as 'true' first item in search result will be selected |

#### caseSensetive

|**Parameter**|caseSensetive|
| ------------- | ------- |
|**Type**|`Boolean`|
|**Default**|`false`|
|**Required**|No|
|**Description**|If defined as 'false' search will ignore upper case symbols |

#### classes

|**Parameter**|classes|
| ------------- | ------- |
|**Type**|`Object`|
|**Required**|No|
|**Description**|Set of css classes to customize output view.|

Default classes:
```js
"classes": {
    "container": "autocomplete-suggestions",
    "selected": "autocomplete-selected",
    "suggestion": "autocomplete-suggestion",
    "wrapper": "autocomplete-wrapper",
    "showAll": "autocomplete-show-all"
}
```

#### containerParent

|**Parameter**|**containerParent**|
| ------------- | ------- |
|**Type**|`String`|
|**Default**|`"body"`|
|**Required**|No|
|**Description**|It defines element to append suggestions container.|

#### showAll

|**Parameter**|showAll|
| ------------- | ------- |
|**Type**|`function`|
|**Default**|`undefined`|
|**Required**|No|
|**Description**|If defined, there is an ability to use "Show all" button to get all search results.|

Usage example:
```js
"showAll": function (suggestions) {
    console.log(suggestions); // [{"data": "<url>", "value": "<text value>"}, ... {...}]
}
```

#### containerHeight

|**Parameter**|containerHeight|
| ------------- | ------- |
|**Type**|`Number`|
|**Default**|`500`|
|**Required**|No|
|**Description**|It defines suggestions container max-height in pixels. |

#### labels.showAllButtonText

|**Parameter**|labels.showAllButtonText|
| ------------- | ------- |
|**Type**|`String`|
|**Default**|`"Show all"`|
|**Required**|No|
|**Description**|It defines label for "show all" button. |

## Licence

MIT
