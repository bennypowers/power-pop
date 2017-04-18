# \<power-pop\>

`power-pop` provides a brief animation indicating success or error.

### Usage

```js
function pop(style) {
  let url = '../../bower_components/power-pop/power-pop.html';
  this.importHref(this.resolveUrl(url), () => {
    let anim = document.createElement('power-pop');
        anim.target = this;
    document.body.appendChild(anim);
    anim.animate(style);
  });
}

pop('error');
```
### Styling
`<power-pop>` provides the following custom properties and mixins for styling:

Custom property | Description | Default
----------------|-------------|----------
`--icon-color` | The color of the icon |
