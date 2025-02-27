# css-wireframe
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Wireframe</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>Header</header>
    <nav>Navigation</nav>
    <main>
        <section>Section 1</section>
        <section>Section 2</section>
    </main>
    <aside>Sidebar</aside>
    <footer>Footer</footer>
</body>
</html>
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
}

body {
    display: grid;
    grid-template-areas: 
        "header header"
        "nav nav"
        "main aside"
        "footer footer";
    grid-template-columns: 2fr 1fr;
    grid-template-rows: auto;
    gap: 10px;
    padding: 20px;
}

header, nav, main, section, aside, footer {
    padding: 20px;
    text-align: center;
    font-size: 1.5rem;
    font-weight: bold;
}

header { background: red; grid-area: header; }
nav { background: orange; grid-area: nav; }
main { background: yellow; grid-area: main; }
section { background: green; margin-bottom: 10px; }
aside { background: blue; grid-area: aside; }
footer { background: purple; grid-area: footer; }

/* Mobile responsiveness */
@media (max-width: 768px) {
    body {
        grid-template-areas: 
            "header"
            "nav"
            "main"
            "aside"
            "footer";
        grid-template-columns: 1fr;
    }
}
