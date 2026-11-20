---
layout: default
title: "Quiénes Somos | Gala Bienes Raíces"
permalink: /quienes-somos/
---

<!-- Forzado de Favicon para layouts de Jekyll -->
<link rel="icon" type="image/png" href="/assets/images/gala-bienes-raices-ícono.png">
<link rel="shortcut icon" type="image/png" href="/assets/images/gala-bienes-raices-ícono.png">
  
<!-- Importación de Josefin Sans con todos los pesos -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Josefin+Sans:ital,wght@0,100..700;1,100..700&display=swap" rel="stylesheet">

<style>
  /* Tipografía general y tamaño de letra a 14pt para el cuerpo */
  body, p, li, blockquote {
    font-family: 'Bahnschrift', 'Segoe UI', system-ui, -apple-system, sans-serif;
    font-size: 14pt !important;
  }

  /* Tipografía para títulos y botones */
  h1, h2, h3, h4, h5, h6, .hero-btn, .btn-agendar {
    font-family: 'Josefin Sans', sans-serif !important;
  }

  /* Tamaño de fuente a 13pt para los botones */
  .hero-btn, .btn-agendar {
    font-size: 13pt !important;
  }

  /* Extra Bold (800) específico para el título principal y botones hero */
  .hero-content h2, 
  .hero-buttons .hero-btn {
    font-weight: 800 !important;
  }

  /* Ajuste de hover para botones secundarios */
  .hero-buttons .hero-btn-secondary:hover {
    background-color: rgba(255, 255, 255, 0.25) !important;
    color: #ffffff !important;
    border-color: #ffffff !important;
  }

  /* Botón de agendar */
  .btn-agendar {
    font-weight: 800 !important;
    color: #ffffff !important;
    background-color: #7f1d1d !important;
    border: 1px solid #7f1d1d !important;
    text-decoration: none !important;
    display: inline-flex !important;
    align-items: center !important;
    justify-content: center !important;
    padding: 12px 24px !important;
    border-radius: 4px !important;
    transition: background-color 0.2s ease, border-color 0.2s ease !important;
    cursor: pointer;
  }

  .btn-agendar:hover, 
  .btn-agendar:focus, 
  .btn-agendar:active {
    background-color: #581313 !important;
    border-color: #581313 !important;
    color: #ffffff !important;
  }

  /* --- ESTILOS DE TARJETAS EDITORIALES PARA QUIÉNES SOMOS --- */
  .gbr-grid-3 {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 22px;
    margin: 24px 0 36px 0;
  }

  .gbr-grid-2 {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 24px;
    margin: 24px 0 36px 0;
  }

  .gbr-card {
    background: #ffffff;
    border: 1px solid #e5e7eb;
    border-radius: 14px;
    padding: 24px 22px;
    box-shadow: 0 4px 14px rgba(0, 0, 0, 0.05);
  }

  .gbr-card h3 {
    margin-top: 0 !important;
    margin-bottom: 10px !important;
    color: #7f1d1d !important;
    font-weight: 700 !important;
    font-size: 1.3rem !important;
  }

  .gbr-card p {
    margin-bottom: 0 !important;
    color: #374151;
    line-height: 1.55;
  }

  .gbr-step-num {
    display: inline-block;
    font-family: 'Josefin Sans', sans-serif !important;
    font-weight: 800;
    font-size: 1.6rem;
    color: #BC2424;
    margin-bottom: 6px;
    line-height: 1;
  }

  .gbr-service-tags {
    font-family: 'Josefin Sans', sans-serif !important;
    font-weight: 700;
    font-size: 0.95rem !important;
    color: #7f1d1d;
    margin-bottom: 12px !important;
    padding-bottom: 10px;
    border-bottom: 1px solid #f3f4f6;
  }

  @media (max-width: 900px) {
    .gbr-grid-3 {
      grid-template-columns: 1fr;
    }
  }

  @media (max-width: 720px) {
    .gbr-grid-2 {
      grid-template-columns: 1fr;
    }
  }

  /* --- ESTILOS DEL MODAL Y CORRECCIÓN DE COLORES --- */
  .modal-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    background: rgba(0, 0, 0, 0.65);
    backdrop-filter: blur(4px);
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 20px;
    z-index: 1000;
    opacity: 0;
    visibility: hidden;
    transition: opacity 0.3s ease, visibility 0.3s ease;
  }

  .modal-overlay.active {
    opacity: 1;
    visibility: visible;
  }

  .modal-card {
    background: rgba(90, 12, 16, 0.95);
    border: 1px solid rgba(255, 255, 255, 0.2);
    border-radius: 32px;
    padding: 32px 28px;
    width: 100%;
    max-width: 480px;
    color: #ffffff !important;
    box-shadow: 0 25px 50px rgba(0, 0, 0, 0.5);
    position: relative;
    transform: scale(0.9);
    transition: transform 0.3s ease;
    max-height: 90vh;
    overflow-y: auto;
  }

  .modal-overlay.active .modal-card {
    transform: scale(1);
  }

  .close-btn {
    position: absolute;
    top: 18px;
    right: 22px;
    background: none;
    border: none;
    color: #ffffff !important;
    font-size: 1.8rem;
    cursor: pointer;
    line-height: 1;
    opacity: 0.8;
    transition: opacity 0.2s;
  }

  .close-btn:hover {
    opacity: 1;
  }

  .modal-card h2.modal-title,
  .modal-title {
    font-size: 1.5rem !important;
    font-weight: 700 !important;
    margin-bottom: 18px !important;
    text-align: center !important;
    color: #ffffff !important;
  }

  .gbr-form {
    display: flex;
    flex-direction: column;
    gap: 14px;
    text-align: left;
  }

  .form-group {
    display: flex;
    flex-direction: column;
    gap: 5px;
  }

  .form-group label {
    font-size: 0.95rem;
    font-weight: 600;
    color: #ffffff !important;
  }

  .form-group input,
  .form-group textarea {
    width: 100%;
    padding: 12px 16px;
    border-radius: 14px;
    border: 1px solid rgba(255, 255, 255, 0.3);
    background: rgba(255, 255, 255, 0.12);
    color: #ffffff !important;
    font-family: inherit;
    font-size: 0.95rem;
    outline: none;
    transition: border-color 0.2s ease, background 0.2s ease;
  }

  .form-group input::placeholder,
  .form-group textarea::placeholder {
    color: rgba(255, 255, 255, 0.6) !important;
  }

  .form-group input:focus,
  .form-group textarea:focus {
    border-color: #ffffff;
    background: rgba(255, 255, 255, 0.22);
  }

  .btn-gbr {
    margin-top: 8px;
    width: 100%;
    min-height: 48px;
    border-radius: 24px;
    border: none;
    background-color: #ffffff !important;
    color: #7f1d1d !important;
    font-family: inherit;
    font-weight: 700;
    font-size: 1.05rem;
    cursor: pointer;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
    transition: transform 0.2s ease, background-color 0.2s ease;
  }

  .btn-gbr:hover {
    transform: translateY(-2px);
    background-color: #f3f4f6 !important;
  }

  .modal-privacy-notice {
    margin-top: 16px;
    padding-top: 12px;
    border-top: 1px solid rgba(255, 255, 255, 0.18);
  }

  .modal-privacy-notice p {
    font-size: 0.74rem !important;
    line-height: 1.45 !important;
    color: rgba(255, 255, 255, 0.82) !important;
    text-align: left !important;
    margin: 0 0 6px 0 !important;
  }

  .modal-privacy-notice p:last-child {
    margin-bottom: 0 !important;
  }

  .modal-privacy-notice strong {
    color: #ffffff !important;
  }

  .modal-privacy-notice a {
    color: #ffffff !important;
    text-decoration: underline !important;
    font-weight: 600;
  }

  .success-message {
    display: none;
    background: rgba(34, 197, 94, 0.2);
    border: 1px solid #22c55e;
    color: #ffffff !important;
    padding: 16px;
    border-radius: 16px;
    text-align: center;
    font-size: 1rem;
    font-weight: 600;
    margin-top: 10px;
  }
</style>

# Quiénes Somos

## Despacho Jurídico-Inmobiliario

Somos un despacho especializado en la zona centro de la Ciudad de México, con un enfoque boutique en las colonias **Roma, Condesa, Nápoles y Del Valle**.

<div class="gbr-grid-2">
  <div class="gbr-card">
    <h3>Nuestra Misión</h3>
    <p>Ayudamos a las personas a encontrar un hogar que se adapte a sus verdaderas necesidades, con un servicio cálido, empático y humano.</p>
  </div>
  <div class="gbr-card">
    <h3>Nuestra Visión</h3>
    <p>Ser la inmobiliaria de referencia en la zona centro de la CDMX, reconocida por nuestra atención personalizada y por defender lo humano en un mundo cada vez más automatizado.</p>
  </div>
</div>

---

## Los Cimientos de Gala

<div class="gbr-grid-3">
  <div class="gbr-card">
    <h3>Empatía Activa</h3>
    <p>Escuchamos con atención y actuamos con comprensión. Cada cliente tiene una historia y una necesidad única.</p>
  </div>
  <div class="gbr-card">
    <h3>Calidez Humana</h3>
    <p>Nuestro trato es de persona a persona, sin automatismos ni frialdad. La confianza se construye entre humanos.</p>
  </div>
  <div class="gbr-card">
    <h3>Transparencia Profesional</h3>
    <p>Somos claros, éticos y responsables. Porque un hogar no se basa en promesas, sino en cimientos firmes.</p>
  </div>
</div>

---

## Defensa de lo Humano

Mientras la industria apuesta por la automatización total, nosotros apostamos por el compromiso con el bienestar: **no buscamos cerrar operaciones, buscamos abrir hogares**.

> **Nuestro Compromiso:** En Gala, el hogar se encuentra en el tacto humano. No vendemos espacios, acompañamos decisiones de vida.

### Creemos en la Conversación Humana

- **Más que un Dato**  
  Un hogar no es una métrica ni un código postal. Es donde puedes respirar, donde caben tus recuerdos, donde todo empieza de nuevo.

- **Acompañamos Decisiones**  
  No automatizamos el contacto, estrechamos manos, miramos a los ojos y escuchamos. Porque nadie conoce mejor tus necesidades que tú mismo.

- **Con Empatía y Tacto**  
  En Gala, el hogar no se encuentra por algoritmo: se encuentra con empatía, con tacto, con humanidad.

- **Lo Humano, Primero**  
  Cada día, las máquinas intentan predecirlo todo. Nosotros seguimos creyendo en algo más simple, más profundo: una conversación humana.

---

## Especialización y Trayectoria

### Un Acompañamiento Absoluto en Cada Etapa

<div class="gbr-grid-3">
  <div class="gbr-card">
    <span class="gbr-step-num">01</span>
    <h3>Análisis y Captación Estratégica</h3>
    <p>Contamos con 28 años de trayectoria en la representación, defensa y gestión de operaciones inmobiliarias. No solo buscamos cerrar tratos, buscamos abrir hogares bajo cimientos firmes de legalidad y ética.</p>
  </div>
  <div class="gbr-card">
    <span class="gbr-step-num">02</span>
    <h3>Gestión Integral del Proceso</h3>
    <p>Brindamos acompañamiento absoluto desde la captación estratégica hasta la firma definitiva ante notario, asegurando que cada etapa sea transparente y profesional.</p>
  </div>
  <div class="gbr-card">
    <span class="gbr-step-num">03</span>
    <h3>Compromiso Humano Permanente</h3>
    <p>Mientras la industria se automatiza, nosotros estrechamos manos y miramos a los ojos. Aplicamos empatía activa para escuchar tus necesidades reales y proteger cada decisión de vida.</p>
  </div>
</div>

---

## El Modelo Gala: Precisión Legal y Sensibilidad Humana

- **Binomio Jurídico-Comercial**  
  Integramos estrategias de marketing de alto nivel con una sólida estructura legal para garantizar el éxito de cada operación.

- **Seguridad Jurídica en Cada Etapa**  
  Protegemos tu patrimonio mediante vigilancia legal exhaustiva: desde la revisión de documentos hasta la firma final, asegurando decisiones éticas y responsables.

- **Procesos Transparentes y Trazables**  
  Metodología profesional, clara y transparente que brinda certidumbre absoluta sobre el estatus de cada gestión a compradores y vendedores.

---

## Consultoría Integral Jurídico-Inmobiliaria

<div class="gbr-grid-2">
  <div class="gbr-card">
    <h3>Venta de Inmuebles</h3>
    <p class="gbr-service-tags">Análisis Jurídico Previo · Estrategia de Comercialización · Gestión de Interesados · Negociación y Cierre ante Notario</p>
    <p>Transformamos la transacción en una experiencia segura y exitosa. Diseñamos planes de marketing a la medida para Roma, Condesa y Del Valle, y te acompañamos físicamente hasta la firma de la escritura.</p>
  </div>
  <div class="gbr-card">
    <h3>Renta de Inmuebles</h3>
    <p class="gbr-service-tags">Selección de Arrendatarios · Investigación y Referencias · Contratos Blindados · Entrega–Recepción Formal</p>
    <p>Protegemos tu inversión y buscamos al habitante ideal para tu propiedad. Utilizamos nuestra Empatía Activa para encontrar inquilinos que respeten y cuiden tu hogar.</p>
  </div>
</div>

---

## Tus Beneficios con Gala Bienes Raíces

- **Protección Legal en Todo Momento**  
  Actuamos con transparencia profesional y ética. Blindamos tu patrimonio ante fraudes, incumplimientos u ocupaciones.

- **Optimización de tu Tiempo y Mayor Exposición**  
  Nos encargamos de la gestión total para que disfrutes de soluciones reales. Posicionamos tu propiedad como referencia en la zona centro de la CDMX: Roma, Condesa, Nápoles y Del Valle.

- **Procesos Transparentes y Reportes Humanos**  
  Te brindamos información constante y clara. La confianza se construye en equipo.

---

## No Dejes tu Patrimonio en Manos de un Algoritmo

En Gala tomamos el tiempo de entenderte para acompañar tu decisión de vida.

Permítenos estrechar tu mano y conocer tus necesidades de viva voz. **El primer paso es una conversación humana.**

<!-- Botón que activa la ventana modal -->
<button type="button" class="hero-btn hero-btn-primary btn-agendar" id="openFormBtn">Agenda una Visita</button>

<!-- VENTANA MODAL DEL FORMULARIO -->
<div class="modal-overlay" id="formModal">
  <div class="modal-card">
    <button type="button" class="close-btn" id="closeFormBtn">&times;</button>
    <h2 class="modal-title">Deja tus datos y te contactaremos :)</h2>

    <form id="gbrContactForm" class="gbr-form">
      <input type="hidden" name="propiedad" value="General">
      <input type="hidden" name="origen" value="Quienes-Somos">

      <div class="form-group">
        <label for="nombre">Tu nombre:</label>
        <input type="text" id="nombre" name="nombre" placeholder="Ej. Ana Martínez" required>
      </div>

      <div class="form-group">
        <label for="telefono">Teléfono de contacto:</label>
        <input type="tel" id="telefono" name="telefono" placeholder="Ej. 55 1234 5678" required>
      </div>

      <div class="form-group">
        <label for="correo">Correo electrónico:</label>
        <input type="email" id="correo" name="correo" placeholder="ejemplo@correo.com" required>
      </div>

      <div class="form-group">
        <label for="duda">¿En qué podemos ayudarte?</label>
        <textarea id="duda" name="duda" rows="3" placeholder="Escribe tu mensaje..."></textarea>
      </div>

      <button type="submit" class="btn-gbr" id="submitBtn">Solicitar Informes</button>

      <div class="modal-privacy-notice">
        <p>
          <strong>Gala Bienes Raíces</strong>, responsable del tratamiento de sus datos personales, utilizará la información proporcionada para atender su solicitud y ofrecer servicios inmobiliarios. También podrá utilizarla para enviarle información sobre propiedades y oportunidades inmobiliarias; usted puede oponerse a esta finalidad escribiendo a <strong>contacto@galabienesraices.com</strong>.
        </p>
        <p>
          Consulte nuestro <a href="https://galabienesraices.com/aviso-de-privacidad/" target="_blank" rel="noopener">Aviso de Privacidad Integral</a>.
        </p>
      </div>
    </form>

    <div class="success-message" id="successMsg">
      ¡Gracias por contactarnos! Nos comunicaremos contigo muy pronto.
    </div>
  </div>
</div>

<script>
  const openBtn = document.getElementById('openFormBtn');
  const openBtnHero = document.getElementById('openFormBtnHero');
  const closeBtn = document.getElementById('closeFormBtn');
  const modal = document.getElementById('formModal');
  const form = document.getElementById('gbrContactForm');
  const successMsg = document.getElementById('successMsg');
  const submitBtn = document.getElementById('submitBtn');

  const SCRIPT_URL = 'https://script.google.com/macros/s/AKfycbzDfLWwiBHcF_tp69hLcpA7TsnVum7ni_zWZKgS8pJRjeSQh-0sn5W-5uSdaWX0Legv/exec';

  openBtn.addEventListener('click', () => modal.classList.add('active'));
  if (openBtnHero) {
    openBtnHero.addEventListener('click', () => modal.classList.add('active'));
  }
  closeBtn.addEventListener('click', () => modal.classList.remove('active'));
  modal.addEventListener('click', (e) => { if (e.target === modal) modal.classList.remove('active'); });

  form.addEventListener('submit', (e) => {
    e.preventDefault();

    submitBtn.disabled = true;
    submitBtn.textContent = 'Enviando...';

    const formData = new FormData(form);

    fetch(SCRIPT_URL, {
      method: 'POST',
      body: formData
    })
    .then(() => {
      form.style.display = 'none';
      successMsg.style.display = 'block';

      setTimeout(() => {
        modal.classList.remove('active');
        form.reset();
        form.style.display = 'flex';
        successMsg.style.display = 'none';
        submitBtn.disabled = false;
        submitBtn.textContent = 'Solicitar Informes';
      }, 2500);
    })
    .catch((err) => {
      console.error('Error:', err);
      alert('Ocurrió un error al enviar. Intenta de nuevo.');
      submitBtn.disabled = false;
      submitBtn.textContent = 'Solicitar Informes';
    });
  });
</script>
