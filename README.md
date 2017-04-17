# vue-bootstrap-modal

Bootstrap style modal component for vue.

<img src="https://github.com/Coffcer/vue-bootstrap-modal/blob/master/modal.gif">

# Usage

import Bootstrap.css
```
<link href="bootstrap.css"></link>
```
**NOTE:**  By default, the modal style is pure bootstrap style, you can use any 3rd party bootstrap framework, like above GIF.


simple options:
``` html
<!--text content-->
<modal title="Modal Title" :show.sync="show" @ok="ok" @cancel="cancel">
    Modal Text
</modal>

<!--custom content-->
<modal title="Modal Title" :show.sync="show" @ok="ok" @cancel="cancel">
    <div>Modal Body</div>
    
    <div slot="header">Modal Header</div>
    <div slot="title">Modal Title</div>
    <div slot="footer">Modal Footer</div>
</modal>

```

# Props
``` javascript
props: {
    show: {
        type: Boolean,
        twoWay: true,
        default: false
    },
    title: {
        type: String,
        default: 'Modal'
    },
    // Bootstrap small style modal
    small: {
        type: Boolean,
        default: false
    },
    // Bootstrap large style modal
    large: {
        type: Boolean,
        default: false
    },
    // Bootstrap full style modal    
    full: {
        type: Boolean,
        default: false
    },
    // if it set false, click background will close modal 
    force: {
        type: Boolean,
        default: false
    },
    // vue transition name
    transition: {
        type: String,
        default: 'modal'
    },
    // [OK button] text
    okText: {
        type: String,
        default: 'OK'
    },
    // [Cancel button] text
    cancelText: {
        type: String,
        default: 'Cancel'
    },
    // [OK button] className
    okClass: {
        type: String,
        default: 'btn blue'
    },
    // [Cancel button] className
    cancelClass: {
        type: String,
        default: 'btn red btn-outline'
    },
    // automatically close when click [OK button]
    closeWhenOK: {
        type: Boolean,
        default: false
    }
}
```

# License
MIT