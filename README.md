[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/bennypowers/power-pop)

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

<!--
```
<custom-element-demo>
  <template>
    <base href="https://user-content-dot-custom-elements.appspot.com/bennypowers/power-pop/ac4b78af94f8268f04e210ecf11cb88fd0f96237/power-pop/">
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="power-pop.html">
    <link rel="import" href="../paper-button/paper-button.html">
    <link rel="import" href="../paper-styles/color.html">
    <style>
      #pop {
        display: flex;
        align-items: center;
        justify-content: center;
        border: 1px dashed grey;
        width:200px;
        height:200px;
        margin: 16px;
      }
      #success {
        background: green;
        color: white;
      }
      #error {
        background: red;
        color: white;
      }
    </style>
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
```html
<div id="pop">
  <paper-button id="success" onclick="powerPop('success')" raised>Success!</paper-button>
  <paper-button id="error" onclick="powerPop('error')" raised>Error!</paper-button>
</div>
<script>
  var powerPop = function(type) {
  console.log('pop')
    let anim = document.createElement('power-pop');
        anim.target = document.getElementById('pop');
    document.body.appendChild(anim);
    anim.animate(type);
  };
</script>
```
