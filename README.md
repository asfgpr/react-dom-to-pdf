# dom-to-pdf

dom-to-pdf generates a printable PDF from DOM node using HTML5 canvas and svg.

## Install

```
npm install --save react-dom-to-pdf
```

## Usage
```javascript
var domToPdf = require('react-dom-to-pdf');

var element = document.getElementById('test');
var options = {
  filename: 'test.pdf'
};
domToPdf(element, options, function() {
  console.log('done');
});
```

## Options
* `filename` - string, name of resulted PDF file, default name is `generated.pdf`
* `excludeClassNames` - array of strings, list of class names of elements to exclude from PDF, e.g. `['Loading', 'ExcludeMeFromPdf']`
* `excludeTagNames` - array of strings, list of html tags to exclude from PDF, e.g. `['button', 'input', 'select']`
* `overrideWidth` - number, overrides a width of a container DOM element 
* `proxyUrl` - string, e.g. `/api/proxyImage?url=`, a route in your app which renders images on your domain in order to avoid problems with CORS with the images on a DOM
* `compression` - string, compression of the generated image, can have the values 'NONE', 'FAST', 'MEDIUM' and 'SLOW'. (default is 'NONE')


