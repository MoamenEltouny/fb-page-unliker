#### Facebook [Pages Unliker]
###### Date : 23 Feb 2022
###### Author : Raggi
-----
##### STEPS
- https://www.facebook.com/pages/?category=liked
- Open the browser console - example: Chrome `CTRL + SHIFT + J`.
- Copy the code below and past it there then press enter and keep the page open.
-----
```js
let tries = 0;

function unlike() {
    let item = document.querySelector('.l9j0dhe7.du4w35lb.j83agx80.pfnyh3mw.taijpn5t.bp9cbjyn.owycx6da.btwxx1t3.kt9q3ron.ak7q8e6j.isp2s0ed.ri5dt5u2.rt8b4zig.n8ej3o3l.agehan2d.sk4xxmp2.rq0escxv.tdjehn4e.tv7at329.hv4rvrfc.dati1w0a');

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
