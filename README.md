<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ishan Sasanka - GitHub Profile</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: #0d1117;
            color: #c9d1d9;
            line-height: 1.6;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        .header {
            text-align: center;
            margin-bottom: 40px;
            padding-top: 30px;
        }
        
        h1 {
            font-size: 3rem;
            margin-bottom: 10px;
            background: linear-gradient(90deg, #4776E6 0%, #8E54E9 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: fadeIn 1s ease-in;
        }
        
        h3 {
            font-size: 1.2rem;
            font-weight: 400;
            max-width: 800px;
            margin: 0 auto 20px;
            color: #8b949e;
            animation: slideUp 1s ease-out;
        }
        
        .views {
            display: inline-block;
            padding: 8px 15px;
            background: rgba(14, 117, 182, 0.1);
            border-radius: 20px;
            color: #0e75b6;
            margin: 10px 0;
            animation: pulse 2s infinite;
        }
        
        .container {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            margin-bottom: 40px;
        }
        
        .info-card {
            flex: 1;
            min-width: 300px;
            background: #161b22;
            border-radius: 10px;
            padding: 25px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.15);
            border: 1px solid #30363d;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .info-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.2);
        }
        
        .avatar-card {
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
        }
        
        .avatar-container {
            position: relative;
            width: 200px;
            height: 200px;
            overflow: hidden;
            border-radius: 50%;
            margin-bottom: 20px;
            border: 4px solid #4776E6;
            animation: morph 8s ease-in-out infinite;
            transition: all 1s ease-in-out;
            box-shadow: 0 0 25px rgba(71, 118, 230, 0.5);
        }
        
        @keyframes morph {
            0% { border-radius: 60% 40% 30% 70% / 60% 30% 70% 40%; }
            50% { border-radius: 30% 60% 70% 40% / 50% 60% 30% 60%; }
            100% { border-radius: 60% 40% 30% 70% / 60% 30% 70% 40%; }
        }
        
        .avatar-img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .placeholder-avatar {
            width: 100%;
            height: 100%;
            display: flex;
            justify-content: center;
            align-items: center;
            background: linear-gradient(45deg, #4776E6, #8E54E9);
            font-size: 4rem;
            color: white;
        }
        
        .info-list {
            list-style: none;
            padding: 0;
        }
        
        .info-list li {
            margin-bottom: 15px;
            display: flex;
            align-items: flex-start;
        }
        
        .info-list li i {
            margin-right: 10px;
            background: linear-gradient(90deg, #4776E6 0%, #8E54E9 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-size: 1.2rem;
            min-width: 24px;
        }
        
        .section-title {
            font-size: 1.8rem;
            margin: 40px 0 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid #30363d;
            color: #e6edf3;
            position: relative;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            left: 0;
            bottom: -2px;
            width: 100px;
            height: 2px;
            background: linear-gradient(90deg, #4776E6 0%, #8E54E9 100%);
            animation: expandWidth 2s ease-out forwards;
        }
        
        @keyframes expandWidth {
            from { width: 0; }
            to { width: 100px; }
        }
        
        .connect-section {
            margin: 30px 0;
        }
        
        .social-icons {
            display: flex;
            gap: 15px;
            margin-top: 15px;
        }
        
        .social-icon {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: #161b22;
            border: 1px solid #30363d;
            transition: all 0.3s ease;
        }
        
        .social-icon:hover {
            transform: translateY(-5px);
            background: linear-gradient(90deg, #4776E6 0%, #8E54E9 100%);
        }
        
        .social-icon img {
            width: 30px;
            height: 30px;
            transition: transform 0.3s ease;
        }
        
        .social-icon:hover img {
            transform: scale(1.1);
        }
        
        .skills-container {
            margin-top: 20px;
        }
        
        .skills-category {
            margin-bottom: 30px;
        }
        
        .skills-category h4 {
            font-size: 1.2rem;
            color: #e6edf3;
            margin-bottom: 15px;
        }
        
        .skills-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
        }
        
        .skill-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            width: 80px;
            height: 80px;
            background: #161b22;
            border-radius: 10px;
            border: 1px solid #30363d;
            padding: 10px;
            transition: all 0.3s ease;
        }
        
        .skill-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            border-color: #4776E6;
        }
        
        .skill-item img {
            width: 40px;
            height: 40px;
            object-fit: contain;
            margin-bottom: 5px;
        }
        
        .skill-item span {
            font-size: 0.8rem;
            text-align: center;
            color: #8b949e;
        }
        
        .stats-container {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 30px;
        }
        
        .stats-card {
            flex: 1;
            min-width: 300px;
            background: #161b22;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.15);
            border: 1px solid #30363d;
            overflow: hidden;
            transition: transform 0.3s ease;
        }
        
        .stats-card:hover {
            transform: translateY(-5px);
        }
        
        .stats-card img {
            width: 100%;
            height: auto;
            border-radius: 5px;
            transition: transform 0.3s ease;
        }
        
        .stats-card:hover img {
            transform: scale(1.02);
        }
        
        footer {
            text-align: center;
            margin-top: 50px;
            padding: 20px;
            color: #8b949e;
            border-top: 1px solid #30363d;
            animation: fadeIn 1s ease-in;
        }
        
        .typing {
            overflow: hidden;
            border-right: 0.15em solid #4776E6;
            white-space: nowrap;
            margin: 0 auto;
            letter-spacing: 0.15em;
            animation: typing 3.5s steps(40, end), blink-caret 0.75s step-end infinite;
        }
        
        @keyframes typing {
            from { width: 0 }
            to { width: 100% }
        }
        
        @keyframes blink-caret {
            from, to { border-color: transparent }
            50% { border-color: #4776E6 }
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        @keyframes slideUp {
            from { 
                opacity: 0;
                transform: translateY(20px); 
            }
            to { 
                opacity: 1;
                transform: translateY(0); 
            }
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        /* Responsive design */
        @media (max-width: 768px) {
            .container {
                flex-direction: column;
            }
            
            .stats-container {
                flex-direction: column;
            }
            
            h1 {
                font-size: 2rem;
            }
            
            h3 {
                font-size: 1rem;
            }
            
            .section-title {
                font-size: 1.5rem;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css">
</head>
<body>
    <div class="header">
        <h1 class="typing">Hi 👋, I'm Ishan Sasanka</h1>
        <h3>Undergraduate mechanical engineering student with a passion for programming and strong skills in Python, Java, and web development. Proven ability in team management and collaboration, evidenced by experience as a batch representative. Eager to leverage technical abilities and leadership experience in contributing to impactful projects.</h3>
        <div class="views">
            <i class="fas fa-eye"></i> Profile views: <span id="viewCount">0</span>
        </div>
    </div>
    
    <div class="container">
        <div class="info-card">
            <ul class="info-list">
                <li>
                    <i class="fas fa-seedling"></i>
                    <span>I'm currently learning <strong>Machine Learning, Deep Learning and Computer Vision</strong></span>
                </li>
                <li>
                    <i class="fas fa-user-graduate"></i>
                    <span>I'm an Undergraduate at <strong>UOM</strong></span>
                </li>
                <li>
                    <i class="fas fa-envelope"></i>
                    <span>How to reach me <strong>dmisasanka@gmail.com</strong></span>
                </li>
            </ul>
        </div>
        
        <div class="info-card avatar-card">
            <div class="avatar-container">
                <div class="placeholder-avatar">IS</div>
            </div>
            <h3>Mechanical Engineer & Developer</h3>
        </div>
    </div>
    
    <div class="connect-section">
        <h2 class="section-title">Connect with me:</h2>
        <div class="social-icons">
            <a href="https://www.hackerrank.com/ishansasankadis1" target="_blank" class="social-icon">
                <img src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/hackerrank.svg" alt="HackerRank">
            </a>
            <a href="https://github.com/dmisasanka2002" target="_blank" class="social-icon">
                <i class="fab fa-github" style="font-size: 30px; color: #c9d1d9;"></i>
            </a>
            <a href="mailto:dmisasanka@gmail.com" class="social-icon">
                <i class="fas fa-envelope" style="font-size: 24px; color: #c9d1d9;"></i>
            </a>
        </div>
    </div>
    
    <h2 class="section-title">Languages and Tools:</h2>
    
    <div class="skills-container">
        <div class="skills-category">
            <h4>Programming Languages</h4>
            <div class="skills-grid">
                <div class="skill-item">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/cplusplus/cplusplus-original.svg" alt="C++">
                    <span>C++</span>
                </div>
                <div class="skill-item">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/csharp/csharp-original.svg" alt="C#">
                    <span>C#</span>
                </div>
                <div class="skill-item">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original.svg" alt="Java">
                    <span>Java</span>
                </div>
                <div class="skill-item">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="JavaScript">
                    <span>JavaScript</span>
                </div>
                <div class="skill-item">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="Python">
                    <span>Python</span>
                </div>
                <div class="skill-item">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/php/php-original.svg" alt="PHP">
                    <span>PHP</span>
                </div>
                <div class="skill-item">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/typescript/typescript-original.svg" alt="TypeScript">
                    <span>TypeScript</span>
                </div>
            </div>
        </div>
        
        <div class="skills-category">
            <h4>Frontend Development</h4>
            <div class="skills-grid">
                <div class="skill-item">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" alt="HTML5">
                    <span>HTML5</span>
                </div>
                <div class="skill-item">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" alt="CSS3">
                    <span>CSS3</span>
                </div>
                <div class="skill-item">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original-wordmark.svg" alt="React">
                    <span>React</span>
                </div>
                <div class="skill-item">
                    <img src="https://cdn.worldvectorlogo.com/logos/nextjs-2.svg" alt="Next.js">
                    <span>Next.js</span>
                </div>
                <div class="skill-item">
                    <img src="https://www.vectorlogo.zone/logos/tailwindcss/tailwindcss-icon.svg" alt="Tailwind CSS">
                    <span>Tailwind</span>
                </div>
            </div>
        </div>
        
        <div class="skills-category">
            <h4>Backend & Database</h4>
            <div class="skills-grid">
                <div class="skill-item">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original-wordmark.svg" alt="Node.js">
                    <span>Node.js</span>
                </div>
                <div class="skill-item">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/express/express-original-wordmark.svg" alt="Express.js">
                    <span>Express</span>
                </div>
                <div class="skill-item">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mongodb/mongodb-original-wordmark.svg" alt="MongoDB">
                    <span>MongoDB</span>
                </div>
                <div class="skill-item">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" alt="MySQL">
                    <span>MySQL</span>
                </div>
            </div>
        </div>
        
        <div class="skills-category">
            <h4>Machine Learning & Data Science</h4>
            <div class="skills-grid">
                <div class="skill-item">
                    <img src="https://www.vectorlogo.zone/logos/opencv/opencv-icon.svg" alt="OpenCV">
                    <span>OpenCV</span>
                </div>
                <div class="skill-item">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/2ae2a900d2f041da66e950e4d48052658d850630/icons/pandas/pandas-original.svg" alt="Pandas">
                    <span>Pandas</span>
                </div>
                <div class="skill-item">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" alt="Scikit-Learn">
                    <span>Scikit-Learn</span>
                </div>
                <div class="skill-item">
                    <img src="https://www.vectorlogo.zone/logos/tensorflow/tensorflow-icon.svg" alt="TensorFlow">
                    <span>TensorFlow</span>
                </div>
            </div>
        </div>
        
        <div class="skills-category">
            <h4>Tools & Others</h4>
            <div class="skills-grid">
                <div class="skill-item">
                    <img src="https://cdn.worldvectorlogo.com/logos/arduino-1.svg" alt="Arduino">
                    <span>Arduino</span>
                </div>
                <div class="skill-item">
                    <img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="Git">
                    <span>Git</span>
                </div>
                <div class="skill-item">
                    <img src="https://www.vectorlogo.zone/logos/getpostman/getpostman-icon.svg" alt="Postman">
                    <span>Postman</span>
                </div>
                <div class="skill-item">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/2/21/Matlab_Logo.png" alt="MATLAB">
                    <span>MATLAB</span>
                </div>
            </div>
        </div>
    </div>
    
    <h2 class="section-title">My Statistics:</h2>
    
    <div class="stats-container">
        <div class="stats-card">
            <img src="https://github-readme-stats.vercel.app/api?username=dmisasanka2002&theme=algolia&show_icons=true&count_private=true" alt="GitHub Stats">
        </div>
        <div class="stats-card">
            <img src="https://github-readme-streak-stats.herokuapp.com/?user=dmisasanka2002&theme=algolia&hide_border=false" alt="GitHub Streak">
        </div>
    </div>
    
    <div class="stats-container">
        <div class="stats-card">
            <img src="https://github-readme-stats.anuraghazra1.vercel.app/api/top-langs/?username=dmisasanka2002&theme=algolia&hide_border=false&no-bg=true&no-frame=true&langs_count=10" alt="Top Languages">
        </div>
    </div>
    
    <footer>
        <p>© 2025 Ishan Sasanka. All Rights Reserved.</p>
    </footer>
    
    <script>
        // Simulating view counter animation
        const viewCount = document.getElementById('viewCount');
        let count = 0;
        const targetCount = 1254;
        const duration = 2000; // 2 seconds
        const interval = 20; // 20ms between updates
        const increment = targetCount / (duration / interval);
        
        const counter = setInterval(() => {
            count += increment;
            if (count >= targetCount) {
                count = targetCount;
                clearInterval(counter);
            }
            viewCount.textContent = Math.floor(count).toLocaleString();
        }, interval);
        
        // Add scroll animation for skill items
        const observer = new IntersectionObserver((entries) => {
            entries.forEach((entry) => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = 1;
                    entry.target.style.transform = "translateY(0)";
                }
            });
        }, { threshold: 0.1 });
        
        document.querySelectorAll('.skill-item').forEach((item, index) => {
            item.style.opacity = 0;
            item.style.transform = "translateY(20px)";
            item.style.transitionDelay = `${index * 50}ms`;
            observer.observe(item);
        });
    </script>
</body>
</html>
