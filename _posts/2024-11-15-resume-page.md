---
layout: post
--- 
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Theme Change</title>
    <style>
        .transition {
            transition: all 1s ease;
        }
    </style>
</head>
<body>
    <script>
        window.addEventListener('load', themeChange);
        const currentTheme = localStorage.getItem('theme') ? localStorage.getItem('theme') : null;
        if (currentTheme) {
            document.documentElement.setAttribute('data-theme', currentTheme);
        }

        function themeChange() {
            let currentTheme = document.documentElement.getAttribute('data-theme');
            let img = document.querySelector('img');
            if (currentTheme === 'dark') {
                transition();
                img.src = "images/shields_res_dark.png";
                img.alt = "resume";
            } else {
                transition();
                img.src = "images/shields_res.png";
                img.alt = "resume";
            }
        }

        function transition() {
            document.documentElement.classList.add('transition');
            window.setTimeout(() => {
                document.documentElement.classList.remove('transition');
            }, 1000);
        }
    </script>
    <img src="images/shields_res.png" alt="resume">
</body>
</html>
