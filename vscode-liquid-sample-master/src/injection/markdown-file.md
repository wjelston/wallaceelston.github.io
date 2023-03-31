---
string: 'string'
number: 35
boolean: false # comment
item: {{ object.prop | filter: 'string' }}
array: [
  'string',
  1234,
  false,
  true
]
---


{% if condition == false %}
  {{ object.prop | filter: 'string' }}
{% endif %}


# Hello World

This example file has Liquid syntax highlighting support!


---


```liquid

{{ object.prop | filter: 'string' }}

{% if condition == false %}

{% endif %}

```


```js

const foo = function() {

  console.log('foo')

  const bar = async (param) => {

    await foo().prop

  }
}
```
