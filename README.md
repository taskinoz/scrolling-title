# Scrolling Title

If your page title is too long it will start scrolling like a marquee

```javascript
document.addEventListener("DOMContentLoaded", function () {
  // Get the existing title
  var title = document.querySelector("title").textContent + " ";

  //Check the length of the title, if its greater than 33 then scroll
  if (title.length > 33) {
    setInterval(function () {
      // Slice off the first letter of the title and add it to the extend
      // then repeat after 300ms
      title = title.slice(1, title.length) + title.slice(0, 1);
      document.querySelector("title").textContent = title;
    }, 300);
  }
});
```
