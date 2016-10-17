# smackbar
a simple jquery notification library plugin

**DISCLAIMER: this library is still in development**

the name comes from the word snackbar which describes the message style from
Google's material design mixed with the project's only dependency
[smiler](https://github.com/steebchen/smiler) to transpile files

### setup

Method 1: CDN (**recommended**)

```html
<script src="https://cdndoge.xyz/common/js/jquery.js"></script>
<script src="https://cdndoge.xyz/lib/smackbar/smackbar.js"></script>
<link rel="stylesheet" href="https://cdndoge.xyz/lib/smackbar/smackbar.css"/>
```

Method 2: compile it by yourself (fully customizable)

```
git clone https://github.com/steebchen/smackbar && cd smackbar
npm i
npm start # compiles all files to the ./public/ directory. edit app.js to customize behavior
```

Method 3: get from npm

```
npm i smackbar
```

### usage

#### simple

This simple example shows a smackbar with a close button. It gets automatically
dismissed after 4 seconds.

```js
$.smackbar({
    message: 'hi'
})
```

#### all options

```js
$.smackbar({
    message: 'hi', // this is the only required field
    timeout: 5000, // sepcify time in ms after the smackbar closes. set to false or 0 to disable
    button: {
        text: 'Undo', // the button text, will be transformed into uppercase automatically
        preventClose: boolean, // TODO
        onclick: function() {
            console.log('clicked the button')
        }
    },
    onclose: function() {
        console.log('this function gets called when the smackbar gets closed')
    }
})
```
