# Installation
react-md is available as an [npm package](https://www.npmjs.com/package/react-md).

You can install with:

```bash
$ npm install -S react \
                 react-dom \
                 react-addons-transition-group \
                 react-addons-css-transition-group \
                 react-md
```

Once installed, the components can be accessed by `react-md` or `react-md/lib` and the styles from `react-md/src/scss/_react-md.scss`.

### Fonts
The [Roboto font](https://www.google.com/fonts/specimen/Roboto) and 
[material-icons](https://design.google.com/icons/) should be included as well
(or some equivalent). These fonts can be included via [WebFontLoader](https://github.com/typekit/webfontloader)
or by locally hosting and using the provided sass mixins to include them. See [host-material-icons](/customization/typography?tab=1#mixin-host-material-icons)
and [host-google-font](/customization/typography?tab=1#mixin-host-google-font) for more details.

### Usage
Please see the list of [examples](https://github.com/mlaursen/react-md/tree/master/examples/) for
how you can get a project started off quickly with React and React MD or view one of the
[boilerplates](/discover-more/boilerplates).

### UMD
react-md is also available as a UMD bundle. This can either be found in the `dist` folder or from [unpkg](https://unpkg.com).

```js
/* index.js */
import { Card, CardTitle, CardText, CardActions, Button } from ReactMD;

class App extends React.Component {
  render() {
    return (
      <div className="md-grid">
        <Card className="md-cell">
          <CardTitle title="Hello, World!"  />
          <CardText>
            Lorem ipsum... pretend more ...
          </CardText>
          <CardActions>
            <Button flat label="Action 1" />
            <Button flat label="Action 2" />
          </CardActions>
        </Card>
      </div>
    );
  }
}

ReactDOM.render(document.getElementById('app'), <App />);
```

```html
<!-- index.html -->
<!DOCTYPE html>
<html>
  <head><link rel="stylesheet" href="https://unpkg.com/react-md/dist/react-md.indigo-pink.min.css"></head>
  <body>
    <script src="https://unpkg.com/react/dist/react.min.js"></script>
    <script src="https://unpkg.com/react-dom/dist/react-dom.min.js"></script>
    <script src="https://unpkg.com/react-addons-css-transition-group/dist/react-addons-css-transition-group.min.js"></script>
    <script src="https://unpkg.com/react-addons-transition-group/dist/react-addons-transition-group.min.js"></script>
    <script src="https://unpkg.com/react-md/dist/react-md.min.js"></script>
    <script src="/bundle.js"></script>
  </body>
</html>
```

> It is recommended to specify the release version for any UMD build
