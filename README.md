# be-summoned

```html
<div be-summoned='{
    "as": "1afd1865-9f4d-4098-bea7-aab65ecc10e4",
    "match": "some-element",
    "vigilanceLevel": 0, //0 = querySelector once, 1 = querySelectorAll once, 2 = do again after beacon, 3 =  deep mutation observer
    "beVigilant": true,
    "on": null,//optional
    "vft": "~" //weak ref
}'>
    <p>
        <ul>
            <li>
                <some-element></some-element>
                ...
            </li>
        </ul>
    </p>
    <template be-a-beacon></template>
</div>    

...


```

```JavaScript
import {registrar} from 'be-summoned/registrar.js';
registrar.addEventListener('1afd1865-9f4d-4098-bea7-aab65ecc10e4', e => {
    const {value, summoner} = e.detail;
});
```

can be array
