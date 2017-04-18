# \<power-pop\>

`power-pop` provides a brief animation indicating success or error.

### Usage

```js
function pop(style) {
  this.importHref(this.resolveUrl('power-pop.html'), () => {
    let anim = document.createElement('power-pop');
        anim.fitInto = this;
        anim.positionTarget = this;
        anim.notifyResize();
    document.body.appendChild(anim);
    anim.center();
    anim.animate(style);
    anim.refit();
  });
}

pop('error');
```
### Styling
`<power-pop>` provides the following custom properties and mixins for styling:

Custom property | Description | Default
----------------|-------------|----------
`--icon-color` | The color of the icon |
