# smackbar
a simple jquery notification library plugin

**DISCLAIMER: this library is still in development**

the name comes from the word snackbar which describes the message style from
Google's material design mixed with the project's only dependency
[smiler](https://github.com/steebchen/smiler) to transpile files

### setup

CDN method (recommended)

```html
<script src="https://cdndoge.xyz/common/js/jquery.js"></script>
<script src="https://cdndoge.xyz/lib/smackbar/smackbar.js"></script>
<link rel="stylesheet" href="https://cdndoge.xyz/lib/smackbar/smackbar.css"/>
```

### usage

#### simple

This simple example shows a toast with a close button. It gets automatically
dismissed after 4 seconds.

```js
$.toast({
    message: 'hi'
})
```

#### all options

```js
$.toast({
    message: 'hi', // this is the only required field
    timeout: 5000, // sepcify time in ms after the toast closes. set to false or 0 to disable
    button: {
        text: 'Undo', // the button text, will be transformed into uppercase automatically
        preventClose: boolean, // TODO
        onclick: function() {
            console.log('clicked the button')
        }
    },
    onclose: function() {
        console.log('this function gets called when the toast gets closed')
    }
})
```
