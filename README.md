# Style Guide
## Naming Conventions
**snake_case**: all words are lowercase and are seperated by '_'.  
**html-snake-case**: all words are lowercase and are seperated by '-'.  
**lowerCamelCase**: starts with a lowercase letter and following words start with uppercase letters with no spaces between words.  
**UpperCamelCase**: all words start with capital letters with no spaces between words.  
**lower spaced out**: all words are lowercase and normally spaced.  
**Upper Spaced Out**: all words start with an uppercase letters and are normally spaced.  

**Variables: snake_case**  
example: 
```js
var this_is_a_long_variable_name = 0;
```

**Functions: lowerCamelCase**  
example:
```js
function thisIsALongFunctionName(param_1, param_2, ...)
```

**HTML Attributes: html-snake-case**  
example:
```html
<div this-is-a-long-attribute-name="foo">...</div>
```

**Tables: Upper Spaced Out**  
It's also important to note tables should be singular.  So a table contianing fruits should be called 'Fruit' not 'Fruits'  
example:  
\* Label &nbsp; <input type=text value="Table Name" disabled />

**Table Fields: Upper Spaced Out**  
It's important to note that when accessing a field via GlideRecord table names will be snake_case.  
example:  
\* Column Label &nbsp; <input type=text value="Field Name" disabled />

**Script Includes: UpperCamelCase**
example:  
Name &nbsp; <input type=text value="ScriptIncludeName" disabled />
> **Quick Tip**  
> Declaring static Script Include functions:  
> You can declare a static Script Include function by adding ScriptIncludeName.functionName = function() after createing the prototye.  
> 
> example:   
> declare static function foo on FooUtils  
> ```js
> var FooUtils = class.create();
> FooUtils.prototype = {
>   initialize: function() {...},
> 
>   type: 'FooUtils'
> };
>
> FooUtils.foo = function(foo_1) {...};
> ```


## Comments
**Functions**:  
All functions should be commented.  They should be formatted in the following way. replacing | | with whats descibed inside them.   
```js
/**
 * |Describe functionality|
 * @param {|parameter type|} |parameter name| |what the parameter should be|
 * ...
 * @return {|return type|} |what should be returned|
 */
function foo(param_1){...}
```
example:  
```js
/**
 * Fooifys the two parameters.
 * @param {String} param_1 The first item to fooify
 * @param {String} param_2 The second item to fooify
 * @return {Object} param_1 and param_2 fooified together
 */
function fooify(param_1, param_2) {
	var rv = {};
	// Do Something...
	return rv;
}
```
> **Quick Tip**  
> This function commenting format will allow vscode to display the function information when hovering over it.  

## IPC Colors
<img width="100%" src="ColorPalleteHex.png" />
