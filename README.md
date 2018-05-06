# Vue Money

**Disclaimer:** I did this as my first vue plugin to allow have elements that autoformat any
given number to a comma separated values. It may lack some stuff, or have serious bugs.

## How to use

```md
# Install

yarn add vue-money # OR dddnstall vue-money
```

Then:

```javascript
import Vue from 'vue'
import Money from 'vue-money'

Vue.use(Money, config)
```

Where `config` can be: 
```javascript
const config = {
  places: 2,
  symbol: '$',
  format: /%money%/,
  directive: 'money-format',
  global: 'moneyFormat'
}
```

This will make the plugin available via the directive `v-money-format` or the global method
`this.$moneyFormat`.

## Usage:

**Directive mode**:

```html
<p v-money-format="value"></p>

<!-- or -->

<p v-money-format="value">Price is %money%</p>
```

This would result in the following:

```html
<p>$123.45</p>

<!-- or -->

<p>Price is $123.45</p>
```
