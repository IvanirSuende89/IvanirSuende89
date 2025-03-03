<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EduAngola - Cursos Online</title>
    <style>
        :root {
            --primary-color: #0056b3;
            --secondary-color: #4caf50;
            --accent-color: #ff9800;
            --light-color: #f8f9fa;
            --dark-color: #343a40;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f5f5f5;
            color: #333;
            line-height: 1.6;
        }
        
        header {
            background: linear-gradient(135deg, var(--primary-color), #003366);
            color: white;
            padding: 1rem 0;
            text-align: center;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }
        
        .logo {
            font-size: 2rem;
            font-weight: bold;
            margin-bottom: 0.5rem;
        }
        
        .tagline {
            font-size: 1.1rem;
            opacity: 0.9;
        }
        
        nav {
            background-color: white;
            padding: 1rem;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }
        
        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .menu {
            display: flex;
            list-style: none;
        }
        
        .menu li {
            margin-left: 1.5rem;
        }
        
        .menu a {
            text-decoration: none;
            color: var(--dark-color);
            font-weight: 500;
            transition: color 0.3s;
        }
        
        .menu a:hover {
            color: var(--primary-color);
        }
        
        .container {
            max-width: 1200px;
            margin: 2rem auto;
            padding: 0 1rem;
        }
        
        .hero {
            background-color: white;
            padding: 2rem;
            border-radius: 8px;
            text-align: center;
            margin-bottom: 2rem;
            box-shadow: 0 2px 15px rgba(0, 0, 0, 0.1);
        }
        
        .hero h1 {
            font-size: 2.5rem;
            color: var(--dark-color);
            margin-bottom: 1rem;
        }
        
        .hero p {
            font-size: 1.1rem;
            color: #666;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .btn {
            display: inline-block;
            padding: 0.8rem 1.5rem;
            background-color: var(--primary-color);
            color: white;
            text-decoration: none;
            border-radius: 5px;
            font-weight: 500;
            transition: all 0.3s;
            margin-top: 1rem;
        }
        
        .btn:hover {
            background-color: #004080;
            transform: translateY(-2px);
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.15);
        }
        
        .btn-secondary {
            background-color: var(--secondary-color);
        }
        
        .btn-secondary:hover {
            background-color: #3e8e41;
        }
        
        .courses-heading {
            text-align: center;
            margin-bottom: 2rem;
        }
        
        .courses-heading h2 {
            font-size: 2rem;
            color: var(--dark-color);
            margin-bottom: 0.5rem;
        }
        
        .courses-heading p {
            color: #666;
        }
        
        .courses-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 1.5rem;
        }
        
        .course-card {
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .course-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        .course-image {
            height: 180px;
            background-color: #ddd;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #666;
            font-size: 0.9rem;
        }
        
        .course-info {
            padding: 1.5rem;
        }
        
        .course-category {
            display: inline-block;
            background-color: #e9f5fe;
            color: var(--primary-color);
            padding: 0.3rem 0.8rem;
            border-radius: 20px;
            font-size: 0.8rem;
            margin-bottom: 0.8rem;
        }
        
        .course-title {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
            color: var(--dark-color);
        }
        
        .course-desc {
            color: #666;
            margin-bottom: 1rem;
            font-size: 0.95rem;
        }
        
        .course-meta {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: 1rem;
            padding-top: 1rem;
            border-top: 1px solid #eee;
        }
        
        .course-price {
            font-weight: bold;
            color: var(--dark-color);
            font-size: 1.1rem;
        }
        
        .course-price span {
            color: #999;
            text-decoration: line-through;
            margin-right: 0.5rem;
            font-size: 0.9rem;
        }
        
        .features {
            background-color: white;
            padding: 3rem 0;
            margin: 3rem 0;
        }
        
        .features-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1rem;
        }
        
        .features-heading {
            text-align: center;
            margin-bottom: 3rem;
        }
        
        .features-heading h2 {
            font-size: 2rem;
            color: var(--dark-color);
            margin-bottom: 0.5rem;
        }
        
        .features-heading p {
            color: #666;
            max-width: 700px;
            margin: 0 auto;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .feature-card {
            text-align: center;
            padding: 1.5rem;
        }
        
        .feature-icon {
            background-color: #e9f5fe;
            width: 80px;
            height: 80px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 1.5rem;
            color: var(--primary-color);
            font-size: 2rem;
        }
        
        .feature-title {
            font-size: 1.3rem;
            margin-bottom: 0.8rem;
            color: var(--dark-color);
        }
        
        .feature-desc {
            color: #666;
            font-size: 0.95rem;
        }
        
        footer {
            background-color: var(--dark-color);
            color: white;
            padding: 3rem 0 1.5rem;
        }
        
        .footer-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1rem;
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 2rem;
        }
        
        .footer-col h3 {
            font-size: 1.2rem;
            margin-bottom: 1.5rem;
            position: relative;
            padding-bottom: 0.5rem;
        }
        
        .footer-col h3::after {
            content: '';
            position: absolute;
            left: 0;
            bottom: 0;
            width: 50px;
            height: 2px;
            background-color: var(--primary-color);
        }
        
        .footer-col p {
            margin-bottom: 1rem;
            opacity: 0.8;
            font-size: 0.95rem;
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 0.8rem;
        }
        
        .footer-links a {
            color: white;
            opacity: 0.8;
            text-decoration: none;
            transition: opacity 0.3s;
            font-size: 0.95rem;
        }
        
        .footer-links a:hover {
            opacity: 1;
        }
        
        .copyright {
            text-align: center;
            padding-top: 2rem;
            margin-top: 2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: rgba(255, 255, 255, 0.6);
            font-size: 0.9rem;
        }
        
        @media (max-width: 768px) {
            .menu {
                display: none;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .courses-grid, .features-grid, .footer-container {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="logo">EduAngola</div>
        <div class="tagline">Desenvolvimento Profissional ao Seu Alcance</div>
    </header>
    
    <nav>
        <div class="nav-container">
            <div class="brand">EduAngola</div>
            <ul class="menu">
                <li><a href="#">Início</a></li>
                <li><a href="#">Cursos</a></li>
                <li><a href="#">Categorias</a></li>
                <li><a href="#">Sobre Nós</a></li>
                <li><a href="#">Contacto</a></li>
            </ul>
        </div>
    </nav>
    
    <div class="container">
        <div class="hero">
            <h1>Aprenda habilidades para o seu futuro</h1>
            <p>Todos os cursos a apenas 1.000 kwanzas - Invista no seu desenvolvimento profissional com os melhores cursos online disponíveis em Angola.</p>
            <a href="#" class="btn">Ver Todos os Cursos</a>
            <a href="#" class="btn btn-secondary">Cadastre-se Grátis</a>
        </div>
        
        <div class="courses-heading">
            <h2>Cursos Em Destaque</h2>
            <p>Explore nossos cursos mais populares a apenas 1.000 Kwanzas cada</p>
        </div>
        
        <div class="courses-grid">
            <div class="course-card">
                <div class="course-image">Desenvolvimento Web</div>
                <div class="course-info">
                    <div class="course-category">Programação</div>
                    <h3 class="course-title">HTML, CSS e JavaScript para Iniciantes</h3>
                    <p class="course-desc">Aprenda a criar websites responsivos do zero utilizando as tecnologias mais populares da web.</p>
                    <div class="course-meta">
                        <div class="course-price"><span>2.500 KZ</span>1.000 KZ</div>
                        <a href="#" class="btn">Comprar</a>
                    </div>
                </div>
            </div>
            
            <div class="course-card">
                <div class="course-image">Marketing Digital</div>
                <div class="course-info">
                    <div class="course-category">Marketing</div>
                    <h3 class="course-title">Marketing Digital Completo</h3>
                    <p class="course-desc">Aprenda estratégias de marketing digital para promover seu negócio e aumentar suas vendas.</p>
                    <div class="course-meta">
                        <div class="course-price"><span>2.500 KZ</span>1.000 KZ</div>
                        <a href="#" class="btn">Comprar</a>
                    </div>
                </div>
            </div>
            
            <div class="course-card">
                <div class="course-image">Excel Avançado</div>
                <div class="course-info">
                    <div class="course-category">Produtividade</div>
                    <h3 class="course-title">Excel Avançado para Negócios</h3>
                    <p class="course-desc">Domine fórmulas avançadas, tabelas dinâmicas, macros e VBA para análise de dados empresariais.</p>
                    <div class="course-meta">
                        <div class="course-price"><span>2.500 KZ</span>1.000 KZ</div>
                        <a href="#" class="btn">Comprar</a>
                    </div>
                </div>
            </div>
            
            <div class="course-card">
                <div class="course-image">Design Gráfico</div>
                <div class="course-info">
                    <div class="course-category">Design</div>
                    <h3 class="course-title">Adobe Photoshop para Iniciantes</h3>
                    <p class="course-desc">Aprenda a editar imagens, criar composições e designs profissionais com o Adobe Photoshop.</p>
                    <div class="course-meta">
                        <div class="course-price"><span>2.500 KZ</span>1.000 KZ</div>
                        <a href="#" class="btn">Comprar</a>
                    </div>
                </div>
            </div>
            
            <div class="course-card">
                <div class="course-image">Inglês Comercial</div>
                <div class="course-info">
                    <div class="course-category">Idiomas</div>
                    <h3 class="course-title">Inglês para Negócios</h3>
                    <p class="course-desc">Desenvolva habilidades em inglês para comunicação empresarial, reuniões e negociações internacionais.</p>
                    <div class="course-meta">
                        <div class="course-price"><span>2.500 KZ</span>1.000 KZ</div>
                        <a href="#" class="btn">Comprar</a>
                    </div>
                </div>
            </div>
            
            <div class="course-card">
                <div class="course-image">Gestão de Projetos</div>
                <div class="course-info">
                    <div class="course-category">Negócios</div>
                    <h3 class="course-title">Fundamentos de Gestão de Projetos</h3>
                    <p class="course-desc">Aprenda metodologias ágeis, ferramentas e técnicas para gerenciar projetos com sucesso.</p>
                    <div class="course-meta">
                        <div class="course-price"><span>2.500 KZ</span>1.000 KZ</div>
                        <a href="#" class="btn">Comprar</a>
                    </div>
                </div>
            </div>
        </div>
    </div>
    
    <section class="features">
        <div class="features-container">
            <div class="features-heading">
                <h2>Por que escolher a EduAngola?</h2>
                <p>Oferecemos uma experiência de aprendizado única focada em resultados práticos</p>
            </div>
            
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">$</div>
                    <h3 class="feature-title">Preço Acessível</h3>
                    <p class="feature-desc">Todos os cursos por apenas 1.000 Kwanzas, democratizando o acesso ao conhecimento.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">✓</div>
                    <h3 class="feature-title">Certificados Reconhecidos</h3>
                    <p class="feature-desc">Receba certificados que valorizam seu currículo e são reconhecidos pelo mercado.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">↻</div>
                    <h3 class="feature-title">Acesso Vitalício</h3>
                    <p class="feature-desc">Estude no seu próprio ritmo com acesso ilimitado aos materiais do curso.</p>
                </div>
            </div>
        </div>
    </section>
    
    <footer>
        <div class="footer-container">
            <div class="footer-col">
                <h3>Sobre a EduAngola</h3>
                <p>A EduAngola é uma plataforma de educação online dedicada a oferecer cursos de qualidade a preços acessíveis para todos os angolanos.</p>
                <p>Nossa missão é democratizar o acesso à educação profissional de qualidade.</p>
            </div>
            
            <div class="footer-col">
                <h3>Links Rápidos</h3>
                <ul class="footer-links">
                    <li><a href="#">Todos os Cursos</a></li>
                    <li><a href="#">Categorias</a></li>
                    <li><a href="#">Instrutores</a></li>
                    <li><a href="#">Blog Educativo</a></li>
                    <li><a href="#">FAQ</a></li>
                </ul>
            </div>
            
            <div class="footer-col">
                <h3>Suporte</h3>
                <ul class="footer-links">
                    <li><a href="#">Central de Ajuda</a></li>
                    <li><a href="#">Política de Privacidade</a></li>
                    <li><a href="#">Termos de Uso</a></li>
                    <li><a href="#">Política de Reembolso</a></li>
                    <li><a href="#">Contacte-nos</a></li>
                </ul>
            </div>
            
            <div class="footer-col">
                <h3>Contacto</h3>
                <p>Email: info@eduangola.co.ao</p>
                <p>Tel: +244 923 456 789</p>
                <p>Endereço: Luanda, Angola</p>
            </div>
        </div>
        
        <div class="copyright">
            &copy; 2025 EduAngola. Todos os direitos reservados.
        </div>
    </footer>
</body>
</html>
