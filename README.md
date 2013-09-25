# Handlebars Helper

A collection of Handlebars Helpers for use with Solidus. Not that you can't use it elsewhere, mind you.

## String Helpers

### Lowercase

Converts a string to all lowercase characters.

```handlebars
{{lowercase "LIQUID!"}}

liquid!
```

### Uppercase

Converts a string to all uppercase characters.

```handlebars
{{uppercase "brother!"}}

BROTHER!
```

### Replace

Replaces part of a string with a string.

```handlebars
{{replace "Liquid Snake" "Liquid" "Solid"}}

Solid Snake
```

## Collection Helpers

### Length

Returns the length of the array, string, or object.

```javascript
{
	array: [1,2,3],
	object: {
		one: 1,
		two: 2,
		three: 3
	},
	string: 'Metal Gear'
}
```

```handlebars
Array length: {{length array}}
Object length: {{length object}}
String length: {{length string}}

Array length: 3
Object length: 3
String length: 10
```

### Contains

Render something if the specified value is in the array, else render some other thing.

```javascript
{
	array: [ 'Solid', 'Liquid', 'Solidus' ],
	array2: [ 'Chell', 'GLAdOS', 'Wheatley' ]
}
```

```handlebars
Array contains "Solidus": {{#contains array "Solidus"}}Yup{{else}}Nope{{/contains}}.
Array2 contains "Solidus": {{#contains array2 "Solidus"}}Yup{{else}}Nope{{/contains}}.

Array contains "Solidus": Yup.
Array2 contains "Solidus": Nope.
```