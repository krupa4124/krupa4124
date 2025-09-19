# Krupa Yatin Jain - Animated Portfolio Code

## Complete HTML File

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Krupa Yatin Jain - Frontend Developer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            overflow-x: hidden;
        }

        .animated-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        }

        .floating-shapes {
            position: absolute;
            width: 100%;
            height: 100%;
        }

        .shape {
            position: absolute;
            opacity: 0.1;
            animation: float 6s ease-in-out infinite;
        }

        .shape:nth-child(1) {
            top: 20%;
            left: 20%;
            animation-delay: 0s;
        }

        .shape:nth-child(2) {
            top: 60%;
            left: 80%;
            animation-delay: -2s;
        }

        .shape:nth-child(3) {
            top: 80%;
            left: 40%;
            animation-delay: -4s;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(180deg); }
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            position: relative;
            z-index: 1;
        }

        .header {
            text-align: center;
            margin-bottom: 50px;
            animation: slideDown 1s ease-out;
        }

        .profile-image {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4, #45b7d1, #96ceb4);
            background-size: 400% 400%;
            animation: gradientShift 4s ease infinite, pulse 2s ease-in-out infinite alternate;
            margin: 0 auto 30px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
            color: white;
            font-weight: bold;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            transition: transform 0.3s ease;
        }

        .profile-image:hover {
            transform: scale(1.1);
        }

        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(255, 255, 255, 0.7); }
            100% { box-shadow: 0 0 0 20px rgba(255, 255, 255, 0); }
        }

        .name {
            font-size: 3.5rem;
            color: white;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            margin-bottom: 10px;
            animation: typewriter 2s steps(20) 1s both;
        }

        .tagline {
            font-size: 1.5rem;
            color: #e0e0e0;
            margin-bottom: 30px;
            animation: fadeInUp 1s ease-out 1.5s both;
        }

        @keyframes slideDown {
            from { opacity: 0; transform: translateY(-50px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes typewriter {
            from { width: 0; }
            to { width: 100%; }
        }

        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-bottom: 50px;
        }

        .stat-card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 20px;
            padding: 30px;
            text-align: center;
            transition: all 0.3s ease;
            animation: fadeInUp 0.8s ease-out;
        }

        .stat-card:nth-child(1) { animation-delay: 0.2s; }
        .stat-card:nth-child(2) { animation-delay: 0.4s; }
        .stat-card:nth-child(3) { animation-delay: 0.6s; }
        .stat-card:nth-child(4) { animation-delay: 0.8s; }

        .stat-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.2);
            background: rgba(255, 255, 255, 0.2);
        }

        .stat-icon {
            font-size: 2.5rem;
            margin-bottom: 15px;
            animation: bounce 2s ease-in-out infinite;
        }

        .stat-card:nth-child(1) .stat-icon { animation-delay: 0s; }
        .stat-card:nth-child(2) .stat-icon { animation-delay: 0.5s; }
        .stat-card:nth-child(3) .stat-icon { animation-delay: 1s; }
        .stat-card:nth-child(4) .stat-icon { animation-delay: 1.5s; }

        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
            40% { transform: translateY(-10px); }
            60% { transform: translateY(-5px); }
        }

        .stat-title {
            font-size: 1.2rem;
            color: white;
            margin-bottom: 10px;
            font-weight: bold;
        }

        .stat-desc {
            color: #e0e0e0;
            font-size: 0.9rem;
        }

        .about-section {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 20px;
            padding: 40px;
            margin-bottom: 50px;
            animation: fadeInUp 1s ease-out 1s both;
        }

        .section-title {
            font-size: 2.5rem;
            color: white;
            text-align: center;
            margin-bottom: 30px;
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 3px;
            background: linear-gradient(90deg, #ff6b6b, #4ecdc4);
            border-radius: 2px;
            animation: expandLine 1s ease-out 1.5s both;
        }

        @keyframes expandLine {
            from { width: 0; }
            to { width: 100px; }
        }

        .about-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .about-item {
            display: flex;
            align-items: center;
            padding: 20px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            transition: all 0.3s ease;
            animation: slideInLeft 0.8s ease-out;
        }

        .about-item:nth-child(even) {
            animation: slideInRight 0.8s ease-out;
        }

        .about-item:hover {
            background: rgba(255, 255, 255, 0.1);
            transform: translateX(10px);
        }

        @keyframes slideInLeft {
            from { opacity: 0; transform: translateX(-50px); }
            to { opacity: 1; transform: translateX(0); }
        }

        @keyframes slideInRight {
            from { opacity: 0; transform: translateX(50px); }
            to { opacity: 1; transform: translateX(0); }
        }

        .about-icon {
            font-size: 2rem;
            margin-right: 20px;
            min-width: 50px;
        }

        .about-text {
            color: white;
            font-size: 1.1rem;
        }

        .about-label {
            font-weight: bold;
            margin-bottom: 5px;
        }

        .skills-section {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 20px;
            padding: 40px;
            margin-bottom: 50px;
            animation: fadeInUp 1s ease-out 1.2s both;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(80px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .skill-item {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            padding: 20px;
            text-align: center;
            transition: all 0.3s ease;
            animation: fadeInUp 0.6s ease-out;
            cursor: pointer;
        }

        .skill-item:nth-child(1) { animation-delay: 0.1s; }
        .skill-item:nth-child(2) { animation-delay: 0.2s; }
        .skill-item:nth-child(3) { animation-delay: 0.3s; }
        .skill-item:nth-child(4) { animation-delay: 0.4s; }
        .skill-item:nth-child(5) { animation-delay: 0.5s; }
        .skill-item:nth-child(6) { animation-delay: 0.6s; }

        .skill-item:hover {
            transform: translateY(-10px) scale(1.1);
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            box-shadow: 0 15px 30px rgba(0,0,0,0.3);
        }

        .skill-icon {
            width: 40px;
            height: 40px;
            margin: 0 auto 10px;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            color: white;
        }

        .skill-name {
            color: white;
            font-size: 0.9rem;
            font-weight: bold;
        }

        .contact-section {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 20px;
            padding: 40px;
            text-align: center;
            animation: fadeInUp 1s ease-out 1.4s both;
        }

        .contact-btn {
            display: inline-block;
            padding: 15px 40px;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            color: white;
            text-decoration: none;
            border-radius: 30px;
            font-size: 1.2rem;
            font-weight: bold;
            margin: 20px 10px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .contact-btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
            transition: left 0.5s ease;
        }

        .contact-btn:hover::before {
            left: 100%;
        }

        .contact-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.3);
        }

        .fun-fact {
            margin-top: 30px;
            padding: 20px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            animation: wiggle 3s ease-in-out infinite;
        }

        @keyframes wiggle {
            0%, 100% { transform: rotate(0deg); }
            25% { transform: rotate(1deg); }
            75% { transform: rotate(-1deg); }
        }

        .fun-fact-title {
            color: #ff6b6b;
            font-size: 1.3rem;
            font-weight: bold;
            margin-bottom: 10px;
        }

        .fun-fact-text {
            color: white;
            font-size: 1.1rem;
        }

        @media (max-width: 768px) {
            .name { font-size: 2.5rem; }
            .tagline { font-size: 1.2rem; }
            .section-title { font-size: 2rem; }
            .stats { grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); }
            .skills-grid { grid-template-columns: repeat(auto-fill, minmax(60px, 1fr)); }
        }
    </style>
</head>
<body>
    <div class="animated-bg">
        <div class="floating-shapes">
            <div class="shape" style="width: 100px; height: 100px; background: rgba(255,255,255,0.1); border-radius: 50%;"></div>
            <div class="shape" style="width: 150px; height: 150px; background: rgba(255,255,255,0.1); transform: rotate(45deg);"></div>
            <div class="shape" style="width: 80px; height: 80px; background: rgba(255,255,255,0.1); clip-path: polygon(50% 0%, 0% 100%, 100% 100%);"></div>
        </div>
    </div>

    <div class="container">
        <header class="header">
            <div class="profile-image">KJ</div>
            <h1 class="name">Krupa Yatin Jain</h1>
            <p class="tagline">A passionate frontend developer from India</p>
        </header>

        <div class="stats">
            <div class="stat-card">
                <div class="stat-icon">🔭</div>
                <div class="stat-title">Currently Working On</div>
                <div class="stat-desc">pro1 - An exciting new project</div>
            </div>
            <div class="stat-card">
                <div class="stat-icon">🌱</div>
                <div class="stat-title">Currently Learning</div>
                <div class="stat-desc">GitHub & Advanced Git Operations</div>
            </div>
            <div class="stat-card">
                <div class="stat-icon">💬</div>
                <div class="stat-title">Ask Me About</div>
                <div class="stat-desc">GitHub & GitOps Implementation</div>
            </div>
            <div class="stat-card">
                <div class="stat-icon">📫</div>
                <div class="stat-title">Get In Touch</div>
                <div class="stat-desc">jainkrupa1210@gmail.com</div>
            </div>
        </div>

        <section class="about-section">
            <h2 class="section-title">About Me</h2>
            <div class="about-grid">
                <div class="about-item">
                    <div class="about-icon">💻</div>
                    <div class="about-text">
                        <div class="about-label">Frontend Developer</div>
                        Passionate about creating beautiful, responsive web experiences
                    </div>
                </div>
                <div class="about-item">
                    <div class="about-icon">🚀</div>
                    <div class="about-text">
                        <div class="about-label">Tech Enthusiast</div>
                        Always exploring new technologies and best practices
                    </div>
                </div>
                <div class="about-item">
                    <div class="about-icon">🏆</div>
                    <div class="about-text">
                        <div class="about-label">Problem Solver</div>
                        Love tackling complex challenges with elegant solutions
                    </div>
                </div>
                <div class="about-item">
                    <div class="about-icon">🌏</div>
                    <div class="about-text">
                        <div class="about-label">Location</div>
                        Based in India, working with global teams
                    </div>
                </div>
            </div>
        </section>

        <section class="skills-section">
            <h2 class="section-title">Technologies & Tools</h2>
            <div class="skills-grid">
                <div class="skill-item">
                    <div class="skill-icon">📱</div>
                    <div class="skill-name">Android</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon">☁️</div>
                    <div class="skill-name">AWS</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon">🎨</div>
                    <div class="skill-name">CSS3</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon">🧪</div>
                    <div class="skill-name">Cypress</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon">🐍</div>
                    <div class="skill-name">Django</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon">🔥</div>
                    <div class="skill-name">Firebase</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon">⚡</div>
                    <div class="skill-name">Gatsby</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon">🌿</div>
                    <div class="skill-name">Git</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon">🌐</div>
                    <div class="skill-name">HTML5</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon">🎯</div>
                    <div class="skill-name">JavaScript</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon">📊</div>
                    <div class="skill-name">Kibana</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon">⚙️</div>
                    <div class="skill-name">Kubernetes</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon">🗄️</div>
                    <div class="skill-name">MySQL</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon">💚</div>
                    <div class="skill-name">Node.js</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon">🐼</div>
                    <div class="skill-name">Pandas</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon">🎮</div>
                    <div class="skill-name">Unity</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon">🔗</div>
                    <div class="skill-name">Zapier</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon">🛡️</div>
                    <div class="skill-name">Realm</div>
                </div>
            </div>
        </section>

        <section class="contact-section">
            <h2 class="section-title">Let's Connect!</h2>
            <p style="color: white; font-size: 1.2rem; margin-bottom: 20px;">
                Ready to collaborate on amazing projects? Let's chat!
            </p>
            <a href="mailto:jainkrupa1210@gmail.com" class="contact-btn">📧 Email Me</a>
            <a href="#" class="contact-btn">🔗 LinkedIn</a>
            <a href="#" class="contact-btn">🐙 GitHub</a>
            
            <div class="fun-fact">
                <div class="fun-fact-title">⚡ Fun Fact</div>
                <div class="fun-fact-text">I believe in the power of clean code and beautiful design!</div>
            </div>
        </section>
    </div>

    <script>
        // Add smooth scrolling and interactive effects
        document.addEventListener('DOMContentLoaded', function() {
            // Add tilt effect to skill items
            const skillItems = document.querySelectorAll('.skill-item');
            skillItems.forEach(item => {
                item.addEventListener('mouseenter', function() {
                    this.style.transform = 'translateY(-10px) scale(1.1) rotateY(10deg)';
                });
                item.addEventListener('mouseleave', function() {
                    this.style.transform = 'translateY(0) scale(1) rotateY(0deg)';
                });
            });

            // Add parallax effect to floating shapes
            const shapes = document.querySelectorAll('.shape');
            let mouseX = 0, mouseY = 0;

            document.addEventListener('mousemove', function(e) {
                mouseX = e.clientX / window.innerWidth;
                mouseY = e.clientY / window.innerHeight;
                
                shapes.forEach((shape, index) => {
                    const speed = (index + 1) * 0.02;
                    const x = (mouseX - 0.5) * 100 * speed;
                    const y = (mouseY - 0.5) * 100 * speed;
                    shape.style.transform = `translate(${x}px, ${y}px) rotate(${x}deg)`;
                });
            });

            // Add typing effect to contact section
            const contactTitle = document.querySelector('.contact-section .section-title');
            const originalText = contactTitle.textContent;
            contactTitle.textContent = '';
            
            setTimeout(() => {
                let i = 0;
                const typeInterval = setInterval(() => {
                    contactTitle.textContent = originalText.slice(0, i + 1);
                    i++;
                    if (i >= originalText.length) {
                        clearInterval(typeInterval);
                    }
                }, 100);
            }, 2000);

            // Add click effect to stat cards
            const statCards = document.querySelectorAll('.stat-card');
            statCards.forEach(card => {
                card.addEventListener('click', function() {
                    this.style.animation = 'none';
                    setTimeout(() => {
                        this.style.animation = 'pulse 0.6s ease-in-out';
                    }, 10);
                });
            });
        });
    </script>
</body>
</html>
```

## Features Included:

### 🎨 Animations
- **Typewriter effect** for the name
- **Floating shapes** with parallax mouse tracking
- **Gradient shifting** profile image
- **Bounce animations** for icons
- **Slide-in effects** for sections
- **Hover transformations** for interactive elements

### 📱 Responsive Design
- Grid layouts that adapt to screen sizes
- Mobile-optimized font sizes
- Flexible card layouts
- Touch-friendly interactions

### 🎯 Interactive Elements
- Hover effects on all cards
- 3D tilt effects on skill items
- Shimmer effects on buttons
- Click animations on stat cards
- Mouse-following background shapes

### 🌈 Modern Styling
- Glass morphism effects
- Gradient backgrounds
- Backdrop blur filters
- Modern color schemes
- Professional typography

## Usage Instructions:
1. Copy the entire code above
2. Save it as an HTML file (e.g., `portfolio.html`)
3. Open in any modern web browser
4. Customize colors, content, or animations as needed

The code is fully self-contained with no external dependencies!
