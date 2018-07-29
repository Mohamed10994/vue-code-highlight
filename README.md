# vue-code-highlight

> Beautiful code syntax highlighting as Vue.js component.

## Usage

```
npm install vue-code-highlight --save
```

Now, you can use this module in two diferrent ways, as a component or as a directive.

### Component
In any component:

```
// You have to extract the component from the module
import { component as VueCodeHighlight } from 'vue-code-highlight';

components:{
  VueCodeHighlight,
  ...
}
```

```
<vue-code-highlight>
 //Paste your code here
</vue-code-highlight>
```
Window styles are already present in a component mode, but you will need to select and include a theme to properly highlight your code. (See the themes section.)

### Directive
In your main file:
```js
import VueCodeHighlight from 'vue-code-highlight';

Vue.use(VueCodeHighlight) //registers the v-highlight directive

```
And then in any Vue component:

```html
<article v-highlight >
 ...
</article>
```
Every node under the article component having the following structure will be syntax highlighted.

```html
<pre class="language-javascript">
  <code>
    //your code goes here
  </code>
</pre>
```
To give the highlighter a window look in a directive mode, also don't forget to include the `./node_modules/vue-code-highlight/themes/window.css` file somewhere in your app.

### Themes
In order to visually higlight your code, you need to select a theme from `./node_modules/vue-code-highlight/themes/` and import it somewhere into your component/application. These are just regular prism themes, so feel free to improvise.


## Examples:
![screenshot](/src/assets/screenshot.png)
