# vuejs-toggle-switch
Toggle switch for vue.js

[Live demo](http://softwarefun.no/#/toggleswitch) <i>only image under </i>

[![license][0]][1] 
[![updated][2]][99] 
[![dependecies][3]][99]
[![npm][4]][98]
[![bugs][5]][99]
> Only 1 dependency (vue)

<img src="http://softwarefun.no/static/toggleswitch.png" height="300">

## Setup
install:
```bash
npm install vuejs-toggle-switch --save
```

Import: (in your main.js)
```javascript
import ToggleSwitch from 'vuejs-toggle-switch'
Vue.use(ToggleSwitch)
```
## Usage
Use: (in your local .vue file/component, html section)

```xml

      <toggle-switch
        preSelected="WinPhone" // This is optional     
        :labels="[
        {name: 'Android', color: 'white', backgroundColor: '#61BB46'}, 
        {name: 'iPhone', color: 'white', backgroundColor: '#FDB827'},
        {name: 'WinPhone', color: 'black', backgroundColor: 'yellow'}
        ]" // color and backgroundColor is optional, name is mandatory
        :width="380" // This is optional
        :height="24" // This is optional
        :padding="2" // This is optional
        fontFamily="Lucida Grande" // This is optional
        @change="updateMap($event.value)" // This is optional
        @selected="selectedMethod() // This is optional
        v-model="selectedMapOption" // This is optional 2-way binding (try not to use both 1-way and 2-way)
        :value="selectedMapOption" // This is optional 1-way binding (try not to use both 1-way and 2-way)
       /> 
```

### Properties

| Name      | Type              | Default     | Description                        |
| ---       | ---               | ---         | ---                                |
| width     | Number           | 100       | Width of labels|
| height      | Number           | 34       | Height |
| padding     | Number           | 7       | adjust text location in label with this |
| backgroundColor      | String           | white       | background color (not selected) |
| color     | String           | black       | text color (not selected)|
| borderColor      | String  | #007aff | border color |
| selectedColor     | String           | white     | text color selected label |
| selectedBackgroundColor      | String           | #007aff       | selected label background color |
| fontFamily     | String           | n/a  | font of label text |
| fontSize      | Number           | 14     | text size |
| disabled     | Boolean           | false       | disable switch |
| preSelected     | String           | unknown       | set (pre) selected label |
| labels     | Array       | n/a       | Labels for switch, name property is mandatory|
| value     | String          | n/a       | value, ie:  v-model="selectedMapOption"  |

### Events

| Name   | Description              |
| ---    | ---                      |
| change | Triggered on toggle, user selects switch option, returns current value. @change="vmValueItem = $event.value" |
| selected | Triggered whenever user select switch item |
| input | Triggered on mount if preSelected is set or value is set, and on toggle/change |


[0]: https://img.shields.io/badge/license-MIT-green.svg
[1]: https://github.com/larsmars/vuejs-toggle-switch/blob/master/LICENSE
[2]: https://img.shields.io/badge/updated-february%202018-brightgreen.svg
[3]: https://img.shields.io/badge/dependencies-1-brightgreen.svg
[4]: https://img.shields.io/badge/npm-v1.0.11-blue.svg
[5]: https://img.shields.io/badge/bugs-0-red.svg
[98]: https://www.npmjs.org/package/vuejs-toggle-switch
[99]: https://github.com/larsmars/vuejs-toggle-switch

