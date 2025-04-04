
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fabes - Ahorros y Préstamos para Maestros</title>
    <style>
        /* Reseteo básico */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        /* Variables de colores */
        :root {
            --naranja: #FF7A00;
            --naranja-claro: #FF9A40;
            --negro: #212121;
            --blanco: #FFFFFF;
            --gris-claro: #F5F5F5;
        }
        
        body {
            background-color: var(--blanco);
            color: var(--negro);
            line-height: 1.6;
        }
        
        /* Navegación */
        header {
            background-color: var(--blanco);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: fixed;
            width: 100%;
            z-index: 1000;
        }
        
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 5%;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--naranja);
        }
        
        .logo span {
            color: var(--negro);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 2rem;
        }
        
        .nav-links a {
            text-decoration: none;
            color: var(--negro);
            font-weight: 500;
            transition: color 0.3s ease;
        }
        
        .nav-links a:hover {
            color: var(--naranja);
        }
        
        .btn {
            background-color: var(--naranja);
            color: var(--blanco);
            border: none;
            padding: 0.8rem 1.5rem;
            border-radius: 50px;
            font-weight: 600;
            cursor: pointer;
            transition: background-color 0.3s ease;
            text-decoration: none;
        }
        
        .btn:hover {
            background-color: var(--naranja-claro);
        }
        
        /* Sección Hero */
        .hero {
            background: linear-gradient(135deg, rgba(255, 122, 0, 0.9) 0%, rgba(255, 154, 64, 0.8) 100%), url('/api/placeholder/1200/800') center/cover;
            color: var(--blanco);
            padding: 10rem 5% 8rem;
            text-align: center;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1.5rem;
            line-height: 1.2;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }
        
        .hero-buttons {
            display: flex;
            justify-content: center;
            gap: 1rem;
        }
        
        .btn-secondary {
            background-color: var(--blanco);
            color: var(--naranja);
        }
        
        .btn-secondary:hover {
            background-color: var(--negro);
            color: var(--blanco);
        }
        
        /* Sección características */
        .features {
            padding: 5rem 5%;
            background-color: var(--gris-claro);
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            color: var(--negro);
        }
        
        .section-title p {
            color: #666;
            max-width: 600px;
            margin: 0 auto;
        }
        
        .features-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .feature-card {
            background-color: var(--blanco);
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            padding: 2rem;
            flex: 1 1 300px;
            text-align: center;
            transition: transform 0.3s ease;
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
        }
        
        .feature-icon {
            background-color: var(--naranja);
            color: var(--blanco);
            width: 70px;
            height: 70px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 1.5rem;
            font-size: 1.8rem;
        }
        
        .feature-card h3 {
            margin-bottom: 1rem;
            color: var(--negro);
        }
        
        /* Sección CTA */
        .cta {
            background-color: var(--negro);
            color: var(--blanco);
            padding: 5rem 5%;
            text-align: center;
        }
        
        .cta-content {
            max-width: 700px;
            margin: 0 auto;
        }
        
        .cta h2 {
            font-size: 2.5rem;
            margin-bottom: 1.5rem;
        }
        
        .cta p {
            margin-bottom: 2rem;
            opacity: 0.9;
        }
        
        /* Sección testimonios */
        .testimonials {
            padding: 5rem 5%;
            background-color: var(--blanco);
        }
        
        .testimonials-container {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .testimonial-card {
            background-color: var(--gris-claro);
            border-radius: 10px;
            padding: 2rem;
            flex: 1 1 350px;
            position: relative;
        }
        
        .testimonial-text {
            margin-bottom: 1.5rem;
            font-style: italic;
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
        }
        
        .author-image {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            margin-right: 1rem;
            background-color: #ddd;
        }
        
        .author-info h4 {
            margin-bottom: 0.2rem;
        }
        
        .author-info p {
            color: #666;
            font-size: 0.9rem;
        }
        
        /* Sección calculadora */
        .calculator {
            padding: 5rem 5%;
            background-color: var(--gris-claro);
        }
        
        .calculator-container {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 3rem;
            max-width: 1100px;
            margin: 0 auto;
        }
        
        .calculator-text {
            flex: 1 1 400px;
        }
        
        .calculator-text h2 {
            font-size: 2.5rem;
            margin-bottom: 1.5rem;
            color: var(--negro);
        }
        
        .calculator-form {
            flex: 1 1 500px;
            background-color: var(--blanco);
            border-radius: 10px;
            padding: 2.5rem;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }
        
        .form-control {
            width: 100%;
            padding: 0.8rem 1rem;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
        }
        
        .calculator-result {
            background-color: var(--naranja);
            color: var(--blanco);
            padding: 1.5rem;
            border-radius: 5px;
            margin-top: 1.5rem;
            text-align: center;
        }
        
        .result-amount {
            font-size: 2rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
        }
        
        /* Footer */
        footer {
            background-color: var(--negro);
            color: var(--blanco);
            padding: 4rem 5% 2rem;
        }
        
        .footer-container {
            display: flex;
            flex-wrap: wrap;
            gap: 3rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .footer-column {
            flex: 1 1 250px;
        }
        
        .footer-column h3 {
            color: var(--naranja);
            margin-bottom: 1.5rem;
            font-size: 1.2rem;
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 0.8rem;
        }
        
        .footer-links a {
            color: var(--blanco);
            text-decoration: none;
            opacity: 0.8;
            transition: opacity 0.3s ease;
        }
        
        .footer-links a:hover {
            opacity: 1;
        }
        
        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1.5rem;
        }
        
        .social-icon {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background-color: rgba(255, 255, 255, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            transition: background-color 0.3s ease;
        }
        
        .social-icon:hover {
            background-color: var(--naranja);
        }
        
        .copyright {
            text-align: center;
            margin-top: 3rem;
            padding-top: 2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            opacity: 0.7;
            font-size: 0.9rem;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .navbar {
                flex-direction: column;
                padding: 1rem;
            }
            
            .nav-links {
                margin-top: 1rem;
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .nav-links li {
                margin: 0.5rem;
            }
            
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
            
            .hero-buttons {
                flex-direction: column;
                align-items: center;
            }
            
            .section-title h2, 
            .calculator-text h2,
            .cta h2 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Navegación -->
    <header>
        <nav class="navbar">
            <div class="logo">Fa<span>bes</span></div>
            <ul class="nav-links">
                <li><a href="#features">Beneficios</a></li>
                <li><a href="#calculator">Calculadora</a></li>
                <li><a href="#testimonials">Testimonios</a></li>
                <li><a href="#" class="btn">Iniciar Sesión</a></li>
            </ul>
        </nav>
    </header>

    <!-- Sección Hero -->
    <section class="hero">
        <div class="hero-content">
            <h1>Soluciones financieras diseñadas para maestros</h1>
            <p>En Fabes entendemos las necesidades únicas de los profesionales de la educación. Ofrecemos préstamos personalizados y planes de ahorro exclusivos para ti.</p>
            <div class="hero-buttons">
                <a href="#calculator" class="btn">Calcular mi préstamo</a>
                <a href="#" class="btn btn-secondary">Conocer más</a>
            </div>
        </div>
    </section>

    <!-- Sección características -->
    <section class="features" id="features">
        <div class="section-title">
            <h2>Beneficios exclusivos para maestros</h2>
            <p>Nuestra misión es ayudarte a alcanzar tus metas financieras con soluciones diseñadas especialmente para ti.</p>
        </div>
        <div class="features-container">
            <div class="feature-card">
                <div class="feature-icon">$</div>
                <h3>Tasas preferenciales</h3>
                <p>Ofrecemos tasas de interés especiales para maestros, significativamente más bajas que las del mercado tradicional.</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">⏱</div>
                <h3>Aprobación rápida</h3>
                <p>Nuestro proceso simplificado permite que recibas respuesta en menos de 24 horas.</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">💰</div>
                <h3>Planes de ahorro flexibles</h3>
                <p>Diseñados para adaptarse a los ciclos escolares y tus necesidades específicas como docente.</p>
            </div>
        </div>
    </section>

    <!-- Sección CTA -->
    <section class="cta">
        <div class="cta-content">
            <h2>¿Listo para dar el siguiente paso?</h2>
            <p>Únete a miles de maestros que ya confían en Fabes para sus necesidades financieras. Regístrate hoy y comienza a disfrutar de todos nuestros beneficios.</p>
            <a href="#" class="btn">Crear mi cuenta</a>
        </div>
    </section>

    <!-- Sección testimonios -->
    <section class="testimonials" id="testimonials">
        <div class="section-title">
            <h2>Lo que dicen nuestros usuarios</h2>
            <p>Maestros como tú comparten sus experiencias con Fabes.</p>
        </div>
        <div class="testimonials-container">
            <div class="testimonial-card">
                <p class="testimonial-text">"Gracias a Fabes pude financiar un curso de especialización que transformó mi carrera. El proceso fue sencillo y las tasas realmente accesibles."</p>
                <div class="testimonial-author">
                    <div class="author-image"></div>
                    <div class="author-info">
                        <h4>Laura Méndez</h4>
                        <p>Maestra de primaria, 8 años de experiencia</p>
                    </div>
                </div>
            </div>
            <div class="testimonial-card">
                <p class="testimonial-text">"El plan de ahorro que me recomendaron se adaptó perfectamente a mi calendario laboral. Ahora puedo planificar mis vacaciones con tranquilidad."</p>
                <div class="testimonial-author">
                    <div class="author-image"></div>
                    <div class="author-info">
                        <h4>Carlos Jiménez</h4>
                        <p>Profesor de secundaria, 12 años de experiencia</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Sección calculadora -->
    <section class="calculator" id="calculator">
        <div class="calculator-container">
            <div class="calculator-text">
                <h2>Calcula tu préstamo ideal</h2>
                <p>Nuestra calculadora te ayudará a determinar la cantidad y plazo que mejor se adapta a tus necesidades.</p>
                <p>Los maestros con más de 5 años de servicio pueden acceder a beneficios adicionales. ¡Descúbrelo ahora!</p>
            </div>
            <div class="calculator-form">
                <div class="form-group">
                    <label for="loan-amount">Monto deseado (MXN)</label>
                    <input type="number" id="loan-amount" class="form-control" placeholder="Ej. 50000">
                </div>
                <div class="form-group">
                    <label for="loan-term">Plazo (meses)</label>
                    <input type="number" id="loan-term" class="form-control" placeholder="Ej. 24">
                </div>
                <div class="form-group">
                    <label for="experience">Años de experiencia docente</label>
                    <input type="number" id="experience" class="form-control" placeholder="Ej. 8">
                </div>
                <button class="btn" style="width: 100%;">Calcular</button>
                <div class="calculator-result">
                    <p>Tu pago mensual estimado:</p>
                    <div class="result-amount">$2,350</div>
                    <p>Tasa anual: 12.5%</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-container">
            <div class="footer-column">
                <div class="logo" style="margin-bottom: 1rem;">Fa<span>bes</span></div>
                <p>Transformando las finanzas de los profesionales de la educación desde 2010.</p>
                <div class="social-links">
                    <a href="#" class="social-icon">f</a>
                    <a href="#" class="social-icon">t</a>
                    <a href="#" class="social-icon">in</a>
                </div>
            </div>
            <div class="footer-column">
                <h3>Enlaces rápidos</h3>
                <ul class="footer-links">
                    <li><a href="#">Inicio</a></li>
                    <li><a href="#features">Beneficios</a></li>
                    <li><a href="#calculator">Calculadora</a></li>
                    <li><a href="#testimonials">Testimonios</a></li>
                </ul>
            </div>
            <div class="footer-column">
                <h3>Productos</h3>
                <ul class="footer-links">
                    <li><a href="#">Préstamos personales</a></li>
                    <li><a href="#">Préstamos para capacitación</a></li>
                    <li><a href="#">Planes de ahorro</a></li>
                    <li><a href="#">Seguros</a></li>
                </ul>
            </div>
            <div class="footer-column">
                <h3>Contacto</h3>
                <ul class="footer-links">
                    <li>contacto@fabes.com</li>
                    <li>01-800-FABES (32237)</li>
                    <li>Av. Educación 123, Col. Centro</li>
                </ul>
            </div>
        </div>
        <div class="copyright">
            &copy; 2025 Fabes - Todos los derechos reservados
        </div>
    </footer>
    <div>
        
    </div>
</body>
</html>
