# update()

Force root Vue component to re-render. 

If called on a Vue component wrapper array, it will force each Vue component to re-render.

### Example

```js
import Foo from './Foo.vue';

const wrapper = mount(Foo);
const divArray = wrapper.findAll('div')
expect(divArray.at(0).vm.bar).to.equal('bar')
divArray.at(0).vm.bar = 'new value';
divArray.update();
expect(divArray.at(0).vm.bar).to.equal('new value');
```