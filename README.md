<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>CyberCore Tech | Hardware & Computadoras Premium</title>
  
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

  <style>
    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
      font-family:'Poppins',sans-serif;
    }

    body{
      background:#0a0a12;
      color:white;
      overflow-x:hidden;
    }

    html{
      scroll-behavior:smooth;
    }

    nav{
      position:fixed;
      width:100%;
      top:0;
      left:0;
      display:flex;
      justify-content:space-between;
      align-items:center;
      padding:20px 8%;
      background:rgba(10,10,18,0.7);
      backdrop-filter:blur(15px);
      z-index:999;
      border-bottom:1px solid rgba(255,255,255,0.05);
    }

    .logo{
      font-size:1.8rem;
      font-weight:900;
      color:#00f0ff;
      text-decoration: none;
    }

    nav ul{
      display:flex;
      gap:30px;
      list-style:none;
      align-items: center;
    }

    nav ul li a{
      color:white;
      text-decoration:none;
      font-weight:500;
      transition:0.3s;
      font-size: 0.95rem;
    }

    nav ul li a:hover{
      color:#00f0ff;
    }

    .menu-toggle {
      display: none;
      color: white;
      font-size: 1.5rem;
      cursor: pointer;
    }

    .btn{
      padding:12px 28px;
      background:#00f0ff;
      border:none;
      border-radius:50px;
      color:#0a0a12;
      font-weight:700;
      cursor:pointer;
      transition:0.4s;
      text-decoration:none;
      display:inline-block;
      box-shadow:0 10px 25px rgba(0,240,255,0.25);
      text-align: center;
    }

    .btn:hover{
      transform:translateY(-3px);
      background:#70f7ff;
      box-shadow:0 15px 30px rgba(0,240,255,0.45);
    }

    .hero{
      min-height:100vh;
      display:flex;
      align-items:center;
      justify-content:center;
      padding:140px 8% 80px 8%;
      gap:50px;
      position:relative;
    }

    .hero::before{
      content:'';
      position:absolute;
      width:400px;
      height:400px;
      background:#00f0ff;
      filter:blur(150px);
      opacity:0.15;
      border-radius:50%;
      top:15%;
      left:10%;
      animation:pulse 6s infinite;
    }

    @keyframes pulse{
      0%{transform:scale(1)}
      50%{transform:scale(1.15)}
      100%{transform:scale(1)}
    }

    .hero-text{
      flex:1;
      z-index:2;
    }

    .hero-text h1{
      font-size:4.5rem;
      line-height:1.1;
      margin-bottom:20px;
      font-weight:900;
    }

    .hero-text span{
      background: linear-gradient(45deg, #00f0ff, #70f7ff);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    .hero-text p{
      color:#b3b3b3;
      font-size:1.1rem;
      margin-bottom:35px;
      max-width:550px;
      line-height: 1.6;
    }

    .hero-img{
      flex:1;
      display:flex;
      justify-content:center;
      z-index:2;
    }

    .hero-img img{
      width:100%;
      max-width:450px;
      border-radius:30px;
      box-shadow:0 20px 50px rgba(0,0,0,0.8);
      animation:float 4s ease-in-out infinite;
    }

    @keyframes float{
      0%{transform:translateY(0)}
      50%{transform:translateY(-15px)}
      100%{transform:translateY(0)}
    }

    section{
      padding:90px 8%;
    }

    .title{
      text-align:center;
      margin-bottom:60px;
    }

    .title h2{
      font-size:2.8rem;
      font-weight:900;
      letter-spacing: -0.5px;
    }

    .title p{
      color:#888;
      margin-top:10px;
      font-size: 1.05rem;
    }

    .products{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
      gap:30px;
    }

    .card{
      background:rgba(255,255,255,0.02);
      border:1px solid rgba(255,255,255,0.05);
      border-radius:24px;
      overflow:hidden;
      transition:0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
      backdrop-filter:blur(10px);
    }

    .card:hover{
      transform:translateY(-10px);
      border-color: rgba(0,240,255,0.3);
      box-shadow:0 15px 35px rgba(0,240,255,0.15);
    }

    .card img{
      width:100%;
      height:250px;
      object-fit:cover;
    }

    .card-content{
      padding:25px;
    }

    .card-content h3{
      font-size:1.5rem;
      margin-bottom:8px;
    }

    .price{
      color:#00f0ff;
      font-size:1.4rem;
      font-weight:800;
      margin-bottom:12px;
    }

    .card-content p{
      color:#aaa;
      margin-bottom:20px;
      font-size: 0.95rem;
      line-height: 1.5;
      min-height: 45px;
    }

    .promo{
      background:linear-gradient(135deg,#0057ff,#002266);
      border-radius:30px;
      text-align:center;
      padding: 60px 40px;
      position:relative;
      overflow:hidden;
      box-shadow: 0 15px 40px rgba(0,87,255,0.2);
    }

    .promo h2{
      font-size:3.5rem;
      font-weight:900;
      margin-bottom:15px;
    }

    .promo p{
      font-size:1.2rem;
      margin-bottom:25px;
      opacity: 0.9;
    }

    .gallery{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
      gap:20px;
    }

    .gallery img{
      width:100%;
      height:280px;
      object-fit:cover;
      border-radius:18px;
      transition:0.4s;
      cursor: pointer;
    }

    .gallery img:hover{
      transform:scale(1.03);
      filter: brightness(1.1);
    }

    .testimonials{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
      gap:30px;
    }

    .review{
      background:rgba(255,255,255,0.01);
      padding:35px;
      border-radius:24px;
      border:1px solid rgba(255,255,255,0.05);
    }

    .stars {
      color: #ffb703;
      margin-bottom: 15px;
      font-size: 0.9rem;
    }

    .review p {
      color: #ccc;
      font-style: italic;
      line-height: 1.6;
    }

    .review h3{
      color:#00f0ff;
      margin-top:20px;
      font-size: 1.1rem;
      font-weight: 600;
    }

    .contact-box{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(320px,1fr));
      gap:50px;
      align-items:center;
    }

    .info-item {
      display: flex;
      align-items: center;
      gap: 15px;
      margin-bottom: 25px;
      color: #ccc;
    }

    .info-item i {
      color: #00f0ff;
      font-size: 1.3rem;
      width: 30px;
    }

    .contact-form{
      background:rgba(255,255,255,0.02);
      padding:40px;
      border-radius:24px;
      border:1px solid rgba(255,255,255,0.05);
    }

    .contact-form input,
    .contact-form textarea{
      width:100%;
      padding:16px;
      margin-bottom:20px;
      background:#0e0e18;
      border:1px solid rgba(255,255,255,0.1);
      border-radius:12px;
      color:white;
      outline:none;
      transition: 0.3s;
    }

    .contact-form input:focus,
    .contact-form textarea:focus {
      border-color: #00f0ff;
      box-shadow: 0 0 10px rgba(0,240,255,0.2);
    }

    footer{
      padding:40px;
      text-align:center;
      border-top:1px solid rgba(255,255,255,0.05);
      color:#555566;
      font-size: 0.9rem;
    }

    .whatsapp{
      position:fixed;
      bottom:25px;
      right:25px;
      width:60px;
      height:60px;
      border-radius:50%;
      background:#25d366;
      display:flex;
      justify-content:center;
      align-items:center;
      font-size:1.8rem;
      text-decoration:none;
      color:white;
      box-shadow:0 10px 30px rgba(37,211,102,0.4);
      z-index:999;
      transition: 0.3s;
    }

    .whatsapp:hover {
      transform: scale(1.1);
      background: #20ba5a;
    }

    /* Responsive */
    @media(max-width:900px){
      nav {
        padding: 15px 5%;
      }
      
      .menu-toggle {
        display: block;
      }

      nav ul {
        position: absolute;
        top: 100%;
        left: 0;
        width: 100%;
        background: rgba(10,10,18,0.95);
        backdrop-filter: blur(10px);
        flex-direction: column;
        padding: 30px;
        gap: 20px;
        box-shadow: 0 10px 20px rgba(0,0,0,0.5);
        display: none;
      }

      nav ul.active {
        display: flex;
      }

      .hero{
        flex-direction:column-reverse;
        text-align:center;
        padding-top: 120px;
      }

      .hero-text h1{
        font-size:3rem;
      }

      .promo h2{
        font-size:2.2rem;
      }
    }
  </style>
</head>
<body>

  <nav>
    <a href="#" class="logo">⚡ CyberCore Tech</a>
    <i class="fa-solid fa-bars menu-toggle" id="menuBtn"></i>
    <ul id="navLinks">
      <li><a href="#inicio">Inicio</a></li>
      <li><a href="#productos">Componentes</a></li>
      <li><a href="#galeria">Setup Galería</a></li>
      <li><a href="#clientes">Opiniones</a></li>
      <li><a href="#contacto">Contacto</a></li>
      <li><a href="#contacto" class="btn" style="color: #0a0a12;">Cotizar</a></li>
    </ul>
  </nav>

  <section class="hero" id="inicio">
    <div class="hero-text">
      <h1>HARDWARE <br><span>AL MÁXIMO NIVEL</span></h1>
      <p>
        Lleva tu experiencia gamer y profesional al siguiente nivel. Equipos de alta gama, monitores de última generación y los periféricos más precisos del mercado con garantía oficial.
      </p>
      <a href="#productos" class="btn" style="color: #0a0a12;">Ver Catálogo</a>
    </div>

    <div class="hero-img">
      <img src="https://images.unsplash.com/photo-1587202372775-e229f172b9d7?q=80&w=1200&auto=format&fit=crop" alt="PC Gaming Setup">
    </div>
  </section>

  <section id="productos">
    <div class="title">
      <h2>Componentes Destacados</h2>
      <p>Equipamiento premium seleccionado para un rendimiento sin límites.</p>
    </div>

    <div class="products">
      <div class="card">
        <img src="https://images.unsplash.com/photo-1527443224154-c4a3942d3acf?q=80&w=1200&auto=format&fit=crop" alt="Monitor Gaming">
        <div class="card-content">
          <h3>Monitor UltraWide 144Hz</h3>
          <div class="price">$349.99</div>
          <p>Pantalla curva de 34 pulgadas, resolución QHD y 1ms de respuesta para una inmersión total.</p>
          <button class="btn add-to-cart" data-product="Monitor UltraWide 34 144Hz" style="color: #0a0a12;">Agregar 🛒</button>
        </div>
      </div>

      <div class="card">
        <img src="https://images.unsplash.com/photo-1615663245857-ac93bb7c39e7?q=80&w=1200&auto=format&fit=crop" alt="Mouse Gamer">
        <div class="card-content">
          <h3>Mouse Pro Wireless</h3>
          <div class="price">$89.99</div>
          <p>Sensor óptico de 26K DPI, estructura ultraligera de 60g y batería de hasta 90 horas continuas.</p>
          <button class="btn add-to-cart" data-product="Mouse Pro Wireless" style="color: #0a0a12;">Agregar 🛒</button>
        </div>
      </div>

      <div class="card">
        <img src="https://images.unsplash.com/photo-1595225476474-87563907a212?q=80&w=1200&auto=format&fit=crop" alt="Teclado Mecánico">
        <div class="card-content">
          <h3>Teclado Mecánico RGB</h3>
          <div class="price">$124.99</div>
          <p>Switches ópticos lineales, distribución del 75%, teclas PBT de doble inyección e iluminación RGB.</p>
          <button class="btn add-to-cart" data-product="Teclado Mecánico RGB 75%" style="color: #0a0a12;">Agregar 🛒</button>
        </div>
      </div>
    </div>
  </section>

  <section>
    <div class="promo">
      <h2>🔥 ENVÍO GRATIS ESTE FIN DE SEMANA 🔥</h2>
      <p>Mejora tu setup hoy mismo. Envío express sin costo en compras mayores a $150.</p>
      <a href="#contacto" class="btn" style="background: #0a0a12; color: white; box-shadow: none;">Reclamar Beneficio</a>
    </div>
  </section>

  <section id="galeria">
    <div class="title">
      <h2>Inspiración de Setups</h2>
      <p>Mira cómo lucen nuestros componentes en las estaciones de batalla de la comunidad.</p>
    </div>

    <div class="gallery">
      <img src="https://images.unsplash.com/photo-1547082299-de196ea013d6?q=80&w=1200&auto=format&fit=crop" alt="Setup Gamer 1">
      <img src="https://images.unsplash.com/photo-1603481588273-2f908a9a7a1b?q=80&w=1200&auto=format&fit=crop" alt="Setup Gamer 2">
      <img src="https://images.unsplash.com/photo-1542751371-adc38448a05e?q=80&w=1200&auto=format&fit=crop" alt="Setup Gamer 3">
      <img src="https://images.unsplash.com/photo-1593642632823-8f785ba67e45?q=80&w=1200&auto=format&fit=crop" alt="Setup Gamer 4">
    </div>
  </section>

  <section id="clientes">
    <div class="title">
      <h2>Opiniones de la Comunidad</h2>
      <p>Lo que dicen los profesionales del streaming y desarrollo sobre nosotros.</p>
    </div>

    <div class="testimonials">
      <div class="review">
        <div class="stars"><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i></div>
        <p>"El monitor UltraWide cambió por completo mi flujo de trabajo en edición de video. Recomendados al 100%."</p>
        <h3>Andrés M.</h3>
      </div>

      <div class="review">
        <div class="stars"><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i></div>
        <p>"El Mouse Wireless llegó al día siguiente de pedirlo. El empaque y la atención al cliente fueron excelentes."</p>
        <h3>Kevin R.</h3>
      </div>

      <div class="review">
        <div class="stars"><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i></div>
        <p>"Increíble el teclado mecánico. La respuesta de los switches ópticos se nota muchísimo en juegos competitivos."</p>
        <h3>Camila S.</h3>
      </div>
    </div>
  </section>

  <section id="contacto">
    <div class="contact-box">
      <div>
        <div class="title" style="text-align:left; margin-bottom:30px;">
          <h2>Haz tu Pedido o Cotización</h2>
          <p>Escríbenos directamente y un asesor técnico armará tu presupuesto.</p>
        </div>

        <div class="info-item">
          <i class="fa-solid fa-location-dot"></i>
          <span>📍 Tech Hub Center, Local Tech 101</span>
        </div>

        <div class="info-item">
          <i class="fa-solid fa-phone"></i>
          <span>📞 +503 6076 4838</span>
        </div>

        <div class="info-item">
          <i class="fa-solid fa-clock"></i>
          <span>🕒 Soporte Online · Lunes a Domingo · 9AM - 10PM</span>
        </div>
      </div>

      <div class="contact-form">
        <input type="text" id="clientName" placeholder="Tu Nombre" required>
        <input type="tel" id="clientPhone" placeholder="Tu Teléfono de contacto" required>
        <textarea id="orderDetail" rows="5" placeholder="Selecciona componentes del catálogo o escribe las especificaciones que buscas para tu PC..."></textarea>

        <button type="button" class="btn" id="sendOrderBtn" style="width:100%; color: #0a0a12;">Enviar Pedido vía WhatsApp <i class="fa-brands fa-whatsapp"></i></button>
      </div>
    </div>
  </section>

  <footer>
    &copy; 2026 CyberCore Tech. Todos los derechos reservados.
  </footer>

  <a class="whatsapp" href="https://wa.me/50360764838" target="_blank" aria-label="Chat en WhatsApp">
    <i class="fa-brands fa-whatsapp"></i>
  </a>

  <script>
    // 1. Menú Responsive en Móviles
    const menuBtn = document.getElementById('menuBtn');
    const navLinks = document.getElementById('navLinks');

    menuBtn.addEventListener('click', () => {
      navLinks.classList.toggle('active');
    });

    // Cerrar el menú al hacer clic en un enlace (Móvil)
    document.querySelectorAll('#navLinks a').forEach(link => {
      link.addEventListener('click', () => {
        navLinks.classList.remove('active');
      });
    });

    // 2. Sistema interactivo para agregar al Formulario de Pedido
    const cartButtons = document.querySelectorAll('.add-to-cart');
    const orderTextArea = document.getElementById('orderDetail');

    cartButtons.forEach(button => {
      button.addEventListener('click', () => {
        const productName = button.getAttribute('data-product');
        
        // Redirigir al área de contacto de forma fluida
        document.getElementById('contacto').scrollIntoView({ behavior: 'smooth' });
        
        // Añadir el producto al área de texto de la orden de forma limpia
        if (orderTextArea.value.trim() === "" || orderTextArea.value.includes("Selecciona componentes")) {
          orderTextArea.value = `Hola, me gustaría cotizar:\n- 1x ${productName}\n`;
        } else {
          orderTextArea.value += `- 1x ${productName}\n`;
        }
      });
    });

    // 3. Envío Profesional y Automatizado a WhatsApp
    const sendBtn = document.getElementById('sendOrderBtn');

    sendBtn.addEventListener('click', () => {
      const name = document.getElementById('clientName').value.trim();
      const phone = document.getElementById('clientPhone').value.trim();
      const details = document.getElementById('orderDetail').value.trim();

      // Validación simple
      if (name === "" || phone === "") {
        alert("Por favor rellena tu Nombre y Teléfono para procesar la cotización.");
        return;
      }

      // Estructuración del mensaje para WhatsApp
      const baseNumber = "50360764838"; 
      const message = `*NUEVA COTIZACIÓN - CYBERCORE TECH* ⚡\n\n` +
                      `👤 *Cliente:* ${name}\n` +
                      `📞 *Teléfono:* ${phone}\n\n` +
                      `🛒 *Componentes Solicitados:*\n${details || 'No se especificaron detalles.'}`;

      // Codificar el texto para la URL
      const whatsappURL = `https://wa.me/${baseNumber}?text=${encodeURIComponent(message)}`;
      
      // Abrir en una pestaña nueva de forma limpia
      window.open(whatsappURL, '_blank');
    });
  </script>
</body>
</html>
