# How to print webpage content into the browser

TIL how to print webpage content using browser's printer and i easily did this using https://github.com/jasonday/printThis
to use simply enclosed a div to your print area, add id, then put this button, on your page

```HTML
<button onClick="$('printarea').printThis();">print</button>
```

of course, you should include the script to your header tag, along with jquery. there are other options to see. read the docs
