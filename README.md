# Ex01 Portfolio
## Date:

## AIM
To create a Portfolio using HTML and CSS.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for introduction, about, projects, and contact details.

### STEP 5
Define global styles for fonts, colors, and layout.

### STEP 6
Style the header, navigation bar, and sections.

### STEP 7
Use Flexbox or CSS Grid for layout design.

### STEP 8
Add hover effects and transitions for interactivity.

### STEP 9
Add Images and Media.

### STEP 10
Use optimized images for a professional look.

### STEP 11
Open the HTML file in a browser to check layout and functionality.

### STEP 12
Fix styling issues and refine content placement.

### STEP 13
Deploy the Portfolio.

### STEP 14
Upload to GitHub Pages for free hosting.

## PROGRAM
# Index.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kranthi Kiran | Portfolio</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Navbar -->
    <nav>
        <h2 class="logo">Portfolio</h2>
        <ul>
            <li><a href="#hero">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <!-- Hero Section -->
    <section id="hero" class="hero">
        <div class="hero-content">

            <img src="images/profile.jpeg" alt="Profile Photo" class="profile-pic">

            <h1>Hi, I'm pranav kirthik s s</h1>
            <p>Aspiring AI & Data Science Engineer</p>

            <a href="#projects" class="btn">View Projects</a>
        </div>
    </section>

    <!-- About -->
    <section id="about" class="glass-card">
        <h2>About Me</h2>
        <p>
            Passionate engineering student focused on AI, Data Science,
            Web Development, and building impactful tech products.
        </p>
    </section>

    <!-- Projects -->
    <section id="projects">
        <h2 class="section-title">Projects</h2>

        <div class="project-container">

            <div class="glass-card project-card">
                <h3>Portfolio Website</h3>
                <p>Modern responsive portfolio using HTML & CSS.</p>
            </div>

            <div class="glass-card project-card">
                <h3>Weather App</h3>
                <p>Real-time weather app using APIs.</p>
            </div>

            <div class="glass-card project-card">
                <h3>AI Chatbot</h3>
                <p>Conversational AI assistant project.</p>
            </div>

        </div>
    </section>

    <!-- Contact -->
    <section id="contact" class="glass-card">
        <h2>Contact Me</h2>
        <p>Email: alapatikranthikiran@gmail.com</p>
        <p>LinkedIn: www.linkedin.com/in/alapati-kranthi-kiran-876631379</p>
    </section>

</body>
</html>

# style.css

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    background: linear-gradient(135deg, #0B1120, #1E1B4B);
    color: white;
    scroll-behavior: smooth;
}

/* Navbar */
nav {
    position: sticky;
    top: 0;
    width: 100%;
    padding: 20px 8%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    backdrop-filter: blur(15px);
    background: rgba(30, 41, 59, 0.85);
    z-index: 1000;
    border-bottom: 1px solid rgba(139, 92, 246, 0.2);
}

.logo {
    font-size: 2rem;
    font-weight: bold;
    color: #8B5CF6;
}

nav ul {
    display: flex;
    list-style: none;
    gap: 25px;
}

nav a {
    text-decoration: none;
    color: white;
    transition: 0.3s;
    font-weight: 500;
}

nav a:hover {
    color: #8B5CF6;
}

/* Hero */
.hero {
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 40px 20px;
}

.hero-content h1 {
    font-size: 3.5rem;
    margin-bottom: 15px;
    animation: fadeUp 1s ease;
}

.hero-content p {
    font-size: 1.3rem;
    margin-bottom: 25px;
    color: #CBD5E1;
}

/* Profile Image */
.profile-pic {
    width: 180px;
    height: 180px;
    border-radius: 50%;
    object-fit: cover;
    border: 4px solid #8B5CF6;
    box-shadow: 0 0 30px rgba(139, 92, 246, 0.5);
    margin-bottom: 25px;
    animation: fadeUp 1s ease;
}

/* Button */
.btn {
    display: inline-block;
    padding: 12px 28px;
    background: linear-gradient(90deg, #8B5CF6, #06B6D4);
    color: white;
    border-radius: 30px;
    text-decoration: none;
    font-weight: bold;
    transition: 0.3s;
}

.btn:hover {
    transform: scale(1.08);
    box-shadow: 0 0 20px rgba(139, 92, 246, 0.6);
}

/* Glass Card */
.glass-card {
    width: 85%;
    margin: 40px auto;
    padding: 30px;
    border-radius: 20px;
    background: rgba(30, 41, 59, 0.75);
    backdrop-filter: blur(20px);
    box-shadow: 0 8px 32px rgba(0,0,0,0.35);
    border: 1px solid rgba(139, 92, 246, 0.15);
}

/* Section Title */
.section-title {
    text-align: center;
    font-size: 2rem;
    margin-top: 50px;
    color: #8B5CF6;
}

/* Projects */
.project-container {
    width: 85%;
    margin: 30px auto;
    display: grid;
    grid-template-columns: repeat(auto-fit,minmax(250px,1fr));
    gap: 20px;
}

.project-card {
    transition: 0.4s;
}

.project-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 0 25px rgba(139, 92, 246, 0.4);
}

/* Animation */
@keyframes fadeUp {
    from {
        opacity: 0;
        transform: translateY(40px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

/* Mobile Responsive */
@media(max-width:768px) {
    nav {
        flex-direction: column;
        gap: 15px;
    }

    .hero-content h1 {
        font-size: 2.4rem;
    }

    .profile-pic {
        width: 140px;
        height: 140px;
    }
}

## OUTPUT
<img width="1900" height="929" alt="Screenshot 2026-05-01 122709" src="https://github.com/user-attachments/assets/724b2f81-0329-475d-90aa-f4b8c7cb8fde" />


## RESULT
The program for creating Portfolio using HTML and CSS is executed successfully.
