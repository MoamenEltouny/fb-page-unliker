#### Facebook [Pages Unliker]
###### Date : 23 Feb 2022
###### Author : Raggi
-----
##### STEPS
- https://www.facebook.com/pages/?category=liked
- Open the browser console - example: Chrome `CTRL + SHIFT + J`.
- Copy the code below and past it there then press enter and keep the page opened.
-----
```js
let tries = 0;

function unlike() {
    let item = document.querySelector('[aria-label="More actions"]')

    if (item) {
        item.click();

        setTimeout(() => {
            let menu = document.querySelector('[role="menuitem"]');
            if (menu.innerText == 'Liked') {
                menu.click();
            } else {
                item.click();
            }

            item.parentNode.parentNode.parentNode.parentNode.parentNode.remove();
        }, 2000);

        setTimeout(() => unlike(), 5000);
    } else {
        if (tries < 3) {
            tries++;
            setTimeout(() => unlike(), 2000);
        } else {
            console.log('DONE :: RaggiTech')
        }
    }
}

unlike();
```
