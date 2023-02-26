# PrintJS App - Fix for Firefox 110 blank print issue

Providing fix for Firefox 110 blank print issue.

## Initial Setup

Adding dependencies:
```
npm i print-js
```

Adding CSS to the head:
```
<!DOCTYPE html>
<html lang="en">
  <head>
    ...
    <link rel="stylesheet" href="./node_modules/print-js/dist/print.css" />
  </head>
  <body></body>
</html>
```

Adding JS to the body:
```
<!DOCTYPE html>
<html lang="en">
  <head></head>
  <body>
    ...
    <script src="node_modules/print-js/dist/print.js"></script>
  </body>
</html>
```

## Printing PDF

Add button to HTML:
```
<button id="btnDefault">Default</button>
```

Add scripts for button print:
```
<script>
  const btnDefault = document.getElementById('btnDefault');

  btnDefault.onclick = function () {
    printJS({ printable: 'assets/file-lg.pdf' });
  };
</script>
```