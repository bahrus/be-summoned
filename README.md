# be-summoned

```html
<div be-summoned='{
    "as": "1afd1865-9f4d-4098-bea7-aab65ecc10e4",
    "match": "someE"
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
registrar.whenDefined('1afd1865-9f4d-4098-bea7-aab65ecc10e4', weakRef => {

});
```

