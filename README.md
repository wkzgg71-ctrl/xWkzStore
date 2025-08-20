<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>WKZ Store</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #1a2a6c, #b21f1f, #fdbb2d);
            background-size: 400% 400%;
            animation: gradientBG 15s ease infinite;
            color: white;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }
        
        @keyframes gradientBG {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        
        .container {
            max-width: 1000px;
            width: 100%;
            background: rgba(0, 0, 0, 0.7);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.4);
            padding: 40px;
            text-align: center;
        }
        
        .logo {
            margin-bottom: 25px;
        }
        
        .logo h1 {
            font-size: 3.8rem;
            font-weight: 800;
            letter-spacing: 3px;
            text-transform: uppercase;
            background: linear-gradient(to right, #ff8a00, #da1b60);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
            margin-bottom: 10px;
        }
        
        .logo p {
            font-size: 1.3rem;
            color: #e0e0e0;
        }
        
        .description {
            margin: 30px 0;
            line-height: 1.6;
            font-size: 1.2rem;
        }
        
        .social-container {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: center;
            margin: 30px 0;
        }
        
        .social-card {
            flex: 1;
            min-width: 280px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            padding: 25px;
            transition: transform 0.3s ease;
        }
        
        .social-card:hover {
            transform: translateY(-5px);
        }
        
        .social-card.whatsapp {
            border-top: 5px solid #25D366;
        }
        
        .social-card.tiktok {
            border-top: 5px solid #000000;
        }
        
        .social-card h2 {
            margin-bottom: 20px;
            font-size: 1.8rem;
        }
        
        .social-card p {
            margin-bottom: 20px;
            color: #e0e0e0;
        }
        
        .social-btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            color: white;
            text-decoration: none;
            padding: 15px 30px;
            border-radius: 50px;
            font-size: 1.2rem;
            font-weight: 600;
            transition: all 0.3s ease;
        }
        
        .whatsapp-btn {
            background: #25D366;
            box-shadow: 0 5px 15px rgba(37, 211, 102, 0.4);
        }
        
        .whatsapp-btn:hover {
            background: #20bd5c;
            box-shadow: 0 8px 20px rgba(37, 211, 102, 0.6);
            transform: translateY(-3px);
        }
        
        .tiktok-btn {
            background: #000000;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.4);
        }
        
        .tiktok-btn:hover {
            background: #222222;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.6);
            transform: translateY(-3px);
        }
        
        .social-btn i {
            margin-right: 12px;
            font-size: 1.5rem;
        }
        
        .link-text {
            display: block;
            margin-top: 15px;
            font-size: 0.9rem;
            color: #cccccc;
            word-break: break-all;
        }
        
        .features {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 25px;
            margin: 40px 0;
        }
        
        .feature {
            flex: 1;
            min-width: 220px;
            background: rgba(255, 255, 255, 0.1);
            padding: 25px;
            border-radius: 15px;
            transition: transform 0.3s ease;
        }
        
        .feature:hover {
            transform: translateY(-5px);
        }
        
        .feature i {
            font-size: 2.8rem;
            margin-bottom: 20px;
            color: #fdbb2d;
        }
        
        .feature h3 {
            margin-bottom: 15px;
            font-size: 1.4rem;
        }
        
        .social-icons {
            margin: 30px 0;
        }
        
        .social-icons a {
            display: inline-block;
            width: 50px;
            height: 50px;
            line-height: 50px;
            text-align: center;
            background: rgba(255, 255, 255, 0.1);
            color: white;
            border-radius: 50%;
            margin: 0 10px;
            font-size: 1.5rem;
            transition: all 0.3s ease;
        }
        
        .social-icons a:hover {
            transform: translateY(-5px);
            background: rgba(255, 255, 255, 0.2);
        }
        
        footer {
            margin-top: 40px;
            color: #a0a0a0;
            font-size: 1rem;
        }
        
        @media (max-width: 768px) {
            .logo h1 {
                font-size: 2.8rem;
            }
            
            .container {
                padding: 25px;
            }
            
            .social-card {
                min-width: 100%;
            }
            
            .feature {
                min-width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="logo">
            <h1>WKZ Store</h1>
            <p>Tu destino para los mejores productos</p>
        </div>
        
        <div class="description">
            <p>En WKZ Store nos especializamos en ofrecerte productos de la más alta calidad con el mejor servicio. Síguenos en nuestras redes sociales para conocer novedades, promociones y realizar tus pedidos.</p>
        </div>
        
        <div class="social-container">
            <div class="social-card whatsapp">
                <h2><i class="fab fa-whatsapp"></i> WhatsApp</h2>
                <p>Únete a nuestro grupo para recibir las últimas novedades y promociones exclusivas</p>
                
                <a href="https://chat.whatsapp.com/CQ2vYPJoN9sBiqvwlTUTih?mode=ac_t" class="social-btn whatsapp-btn" target="_blank">
                    <i class="fab fa-whatsapp"></i> Unirse al grupo
                </a>
                
                <span class="link-text">https://chat.whatsapp.com/CQ2vYPJoN9sBiqvwlTUTih?mode=ac_t</span>
            </div>
            
            <div class="social-card tiktok">
                <h2><i class="fab fa-tiktok"></i> TikTok</h2>
                <p>Síguenos en TikTok para ver contenido exclusivo y demostraciones de productos</p>
                
                <a href="https://www.tiktok.com/@fer_cbyt" class="social-btn tiktok-btn" target="_blank">
                    <i class="fab fa-tiktok"></i> Seguir en TikTok
                </a>
                
                <span class="link-text">https://www.tiktok.com/@fer_cbyt</span>
            </div>
        </div>
        
        <div class="features">
            <div class="feature">
                <i class="fas fa-shipping-fast"></i>
                <h3>Envíos Rápidos</h3>
                <p>Recibe tus productos en tiempo récord con nuestro servicio de entrega express</p>
            </div>
            <div class="feature">
                <i class="fas fa-medal"></i>
                <h3>Calidad Premium</h3>
                <p>Productos seleccionados con los más altos estándares de calidad garantizada</p>
            </div>
            <div class="feature">
                <i class="fas fa-headset"></i>
                <h3>Soporte 24/7</h3>
                <p>Atención personalizada cuando la necesites, estamos disponibles a cualquier hora</p>
            </div>
        </div>
        
        <div class="social-icons">
            <a href="#"><i class="fab fa-facebook-f"></i></a>
            <a href="https://www.instagram.com/wkz_gg09?igsh=c2x3bzYyM2x2M3lq"><i class="fab fa-instagram"></i></a>
            <a href="https://www.tiktok.com/@fer_cbyt" target="_blank"><i class="fab fa-tiktok"></i></a>
            <a href="https://chat.whatsapp.com/CQ2vYPJoN9sBiqvwlTUTih?mode=ac_t" target="_blank"><i class="fab fa-whatsapp"></i></a>
        </div>
        
        <footer>
            <p>© 2025 WKZ Store - Todos los derechos reservados</p>
        </footer>
    </div>
</body>
</html>
