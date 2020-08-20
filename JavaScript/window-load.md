# Window Load events
- load
- DOMContentLoaded

## load
css, image, font 등 DOM 뿐만 아니라 모든 리소스가 로드된 후 발생하는 이벤트

## DOMContentLoaded
DOM이 로드된 후 발생하는 이벤트

```html
(...ing)
<html>

</html>
// only document
window.addEventListener('DOMContentLoaded', () => {
    console.log('DOMContentLoaded');
});

// after resources (css, images)
window.addEventListener('load', () => {
    console.log('load');
})
```