Create a bookmarklet with the following URL:

```javascript
javascript: (function() {var WPM=300; var text = ""; if (window.getSelection) { text = window.getSelection().toString(); } else if (document.selection && document.selection.type != "Control") { text = document.selection.createRange().text; } var words = text.split(/[ .,!;:]/).filter(function(n) { return n != "" }); var minutes = words.length / WPM; var seconds = parseInt((minutes - parseInt(minutes)) * 60); alert("This will take " + parseInt(minutes) + ":" + seconds + " to read.");}());
```
