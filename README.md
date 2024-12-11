# Drago
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/yourusername/repository-name.git
git push -u origin master
/my-website
    /assets
        /images
        /css
            style.css
        /js
            script.js
    /pages
        index.html
        articles.html
        about.html
        contact.html
    server.js (if you're using Node.js backend)
    package.json (for Node.js setup, if needed)
    <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Brighu Raina's Articles</title>
    <link rel="stylesheet" href="assets/css/style.css">
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="articles.html">Articles</a></li>
                <li><a href="about.html">About</a></li>
                <li><a href="contact.html">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section id="home">
            <h1>Welcome to Brighu Raina's Article Hub</h1>
            <p>Explore my latest articles on various topics!</p>
        </section>

        <section id="featured-articles">
            <h2>Featured Articles</h2>
            <p><a href="articles.html">Check out all articles</a></p>
        </section>
    </main>

    <footer>
        <p>&copy; 2024 Brighu Raina. All rights reserved.</p>
    </footer>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Articles - Brighu Raina</title>
    <link rel="stylesheet" href="assets/css/style.css">
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="articles.html">Articles</a></li>
                <li><a href="about.html">About</a></li>
                <li><a href="contact.html">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section id="articles">
            <h1>All Articles</h1>
            <input type="text" id="search" placeholder="Search articles" oninput="searchArticles()">
            <div id="article-list">
                <article>
                    <h2>Article 1 Title</h2>
                    <p>Summary of article 1...</p>
                </article>
                <article>
                    <h2>Article 2 Title</h2>
                    <p>Summary of article 2...</p>
                </article>
            </div>
        </section>
    </main>

    <footer>
        <p>&copy; 2024 Brighu Raina. All rights reserved.</p>
    </footer>

    <script src="assets/js/script.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>About - Brighu Raina</title>
    <link rel="stylesheet" href="assets/css/style.css">
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="articles.html">Articles</a></li>
                <li><a href="about.html">About</a></li>
                <li><a href="contact.html">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section id="about">
            <h1>About Brighu Raina</h1>
            <p>Welcome to my personal article hub! Here I share my thoughts and experiences on various topics.</p>
        </section>
    </main>

    <footer>
        <p>&copy; 2024 Brighu Raina. All rights reserved.</p>
    </footer>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Contact - Brighu Raina</title>
    <link rel="stylesheet" href="assets/css/style.css">
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="articles.html">Articles</a></li>
                <li><a href="about.html">About</a></li>
                <li><a href="contact.html">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section id="contact">
            <h1>Contact Me</h1>
            <form action="submit_contact.php" method="POST">
                <input type="text" name="name" placeholder="Your Name" required><br>
                <input type="email" name="email" placeholder="Your Email" required><br>
                <textarea name="message" placeholder="Your Message" required></textarea><br>
                <button type="submit">Send Message</button>
            </form>
        </section>
    </main>

    <footer>
        <p>&copy; 2024 Brighu Raina. All rights reserved.</p>
    </footer>
</body>
</html>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
}

header {
    background: #333;
    color: white;
    padding: 10px 0;
}

nav ul {
    list-style: none;
    text-align: center;
}

nav ul li {
    display: inline;
    margin: 0 20px;
}

nav ul li a {
    color: white;
    text-decoration: none;
    font-size: 18px;
}

main {
    padding: 20px;
}

footer {
    background: #333;
    color: white;
    text-align: center;
    padding: 10px;
    position: fixed;
    width: 100%;
    bottom: 0;
}

#articles {
    max-width: 900px;
    margin: 0 auto;
}

#articles article {
    border-bottom: 1px solid #ddd;
    padding: 20px;
}

#search {
    width: 100%;
    padding: 10px;
    margin-bottom: 20px;
    font-size: 16px;
}
// Simple search functionality for articles
function searchArticles() {
    const query = document.getElementById('search').value.toLowerCase();
    const articles = document.querySelectorAll('#article-list article');
    
    articles.forEach(article => {
        const title = article.querySelector('h2').textContent.toLowerCase();
        if (title.includes(query)) {
            article.style.display = '';
        } else {
            article.style.display = 'none';
        }
    });
}

