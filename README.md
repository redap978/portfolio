
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mon Portfolio</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
        }

        header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 2rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        nav a {
            color: white;
            text-decoration: none;
            transition: opacity 0.3s;
        }

        nav a:hover {
            opacity: 0.8;
        }

        section {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        #accueil {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            margin-top: 0;
        }

        .hero-content h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            animation: fadeInUp 1s ease;
        }

        .hero-content p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            animation: fadeInUp 1s ease 0.2s;
            animation-fill-mode: both;
        }

        .btn {
            display: inline-block;
            padding: 1rem 2rem;
            background: white;
            color: #667eea;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            transition: transform 0.3s, box-shadow 0.3s;
            animation: fadeInUp 1s ease 0.4s;
            animation-fill-mode: both;
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
        }

        h2 {
            font-size: 2.5rem;
            margin-bottom: 3rem;
            text-align: center;
            color: #667eea;
        }

        .about-content {
            display: flex;
            gap: 3rem;
            align-items: center;
        }

        .about-text {
            flex: 1;
        }

        .about-image {
            width: 300px;
            height: 300px;
            border-radius: 50%;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 5rem;
            color: white;
        }

        .competences-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .competence-card {
            padding: 2rem;
            background: #f8f9fa;
            border-radius: 10px;
            text-align: center;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .competence-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        .competence-card h3 {
            color: #667eea;
            margin-bottom: 1rem;
        }

        .projets-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .projet-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }

        .projet-card:hover {
            transform: translateY(-10px);
        }

        .projet-image {
            width: 100%;
            height: 200px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3rem;
        }

        .projet-content {
            padding: 1.5rem;
        }

        .projet-content h3 {
            color: #667eea;
            margin-bottom: 1rem;
        }

        .contact-form {
            max-width: 600px;
            margin: 0 auto;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            color: #667eea;
            font-weight: bold;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 1rem;
            border: 2px solid #e0e0e0;
            border-radius: 5px;
            font-family: inherit;
            transition: border-color 0.3s;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: #667eea;
        }

        .form-group textarea {
            resize: vertical;
            min-height: 150px;
        }

        footer {
            background: #333;
            color: white;
            text-align: center;
            padding: 2rem;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @media (max-width: 768px) {
            .hero-content h1 {
                font-size: 2rem;
            }

            .about-content {
                flex-direction: column;
                text-align: center;
            }

            nav ul {
                gap: 1rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <nav>
            <div class="logo">Mon Portfolio</div>
            <ul>
                <li><a href="#accueil">Accueil</a></li>
                <li><a href="#a-propos">À propos</a></li>
                <li><a href="#competences">Compétences</a></li>
                <li><a href="#projets">Projets</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="accueil">
        <div class="hero-content">
            <h1>Bonjour, je suis Chami Réda</h1>
            <p>Alternant en Maintenance Informatique Systèmes & Réseaux</p>
            <a href="#contact" class="btn">Me Contacter</a>
        </div>
    </section>

    <section id="a-propos">
        <h2>À Propos de Moi</h2>
        <div class="about-content">
            <div class="about-text">
                <p>Passionné d'informatique depuis mon plus jeune âge, j'ai commencé par créer des mini jeux avec des amis. Par la suite, j'ai suivi une filière STI2D où j'ai développé mes compétences en développement web (HTML/CSS), en programmation (C++, Python) et en graphisme.</p>
                <br>
                <p>Aujourd'hui, je suis en formation de Maintenicien Informatique Systèmes & Réseaux, où je continue d'élargir mes compétences techniques et pratiques dans le domaine de l'informatique.</p>
            </div>
            <div class="about-image">👨‍💻</div>
        </div>
    </section>

    <section id="competences">
        <h2>Mes Compétences</h2>
        <div class="competences-grid">
            <div class="competence-card">
                <h3>Cisco Packet Tracer</h3>
                <p>Simulation et configuration de réseaux informatiques</p>
            </div>
            <div class="competence-card">
                <h3>HTML/CSS</h3>
                <p>Développement de sites web responsive et modernes</p>
            </div>
            <div class="competence-card">
                <h3>C++ & Python</h3>
                <p>Programmation orientée objet et développement d'applications</p>
            </div>
            <div class="competence-card">
                <h3>Graphisme</h3>
                <p>Création de contenus visuels et design graphique</p>
            </div>
            <div class="competence-card">
                <h3>React</h3>
                <p>Création d'applications web interactives avec React</p>
            </div>
        </div>
    </section>

    <section id="projets">
        <h2>Mes Projets</h2>
        <div class="projets-grid">
            <div class="projet-card">
                <div class="projet-image">🐾</div>
                <div class="projet-content">
                    <h3>Application Bien-être Animal</h3>
                    <p>Application mobile proposant des conseils pour animaux et un carnet de santé numérique personnalisé</p>
                </div>
            </div>
            <div class="projet-card">
                <div class="projet-image">🏡</div>
                <div class="projet-content">
                    <h3>Rénovation Éco-gîte Domotique</h3>
                    <p>Installation et configuration d'un système domotique complet pour un éco-gîte</p>
                </div>
            </div>
            <div class="projet-card">
                <div class="projet-image">🤖</div>
                <div class="projet-content">
                    <h3>Trash IA - Classification de déchets</h3>
                    <p>Intelligence artificielle utilisant un CNN pour identifier et classifier les déchets, avec base de données intégrée</p>
                </div>
            </div>
        </div>
    </section>

    <section id="contact">
        <h2>Contactez-moi</h2>
        <div class="contact-content">
            <p style="text-align: center; margin-bottom: 2rem; font-size: 1.1rem;">
                N'hésitez pas à me contacter pour toute opportunité ou question !
            </p>
            <div style="text-align: center; display: flex; flex-direction: column; gap: 1.5rem; align-items: center;">
                <a href="mailto:chamireda42@gmail.com" class="btn">📧 M'envoyer un email</a>
                <a href="tel:0763982405" class="btn">📞 07 63 98 24 05</a>
   
    <script>
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });


    </script>
</body>
</html>
