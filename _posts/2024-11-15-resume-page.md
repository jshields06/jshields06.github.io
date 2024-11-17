<!DOCTYPE html>
<html>
<script>
    window.addEventListener('load', themeChange);
    const currentTheme = localStorage.getItem('theme') ? localStorage.getItem('theme') : null;
    if (currentTheme)
        document.documentElement.setAttribute('data-theme', currentTheme);

    let currentTheme = document.documentElement.getAttribute('data-theme');
    if (currentTheme === 'dark') {
        transition(); <
        img src = "images\shields_res_dark.png"
        alt = "resume" >
    } else {
        transition(); <
        img src = "images\shields_res.png"
        alt = "resume" >
    });

    let transition = () => {
        document.documentElement.classList.add('transition');
        window.setTimeout(() => {
            document.documentElement.classList.remove('transition');

        }, 1000);
    }
    }
</script>
</html>