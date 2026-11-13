---
layout: default
title: "Aquí comienza tu hogar | Gala Bienes Raíces"
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

  /* --- SECCIÓN PROPIEDADES RECIENTES (2 HILERAS DE 3) --- */
  .recent-properties-section {
    margin: 45px 0 55px 0;
  }

  .recent-properties-header {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
    flex-wrap: wrap;
    gap: 12px;
    margin-bottom: 24px;
    border-bottom: 2px solid rgba(188, 36, 36, 0.2);
    padding-bottom: 10px;
  }

  .recent-properties-header h2 {
    margin: 0 !important;
    font-size: 1.8rem !important;
    font-weight: 800 !important;
    color: #BC2424 !important;
    border: none !important;
    padding: 0 !important;
  }

  .recent-grid-3x2 {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 24px;
  }

  .recent-card-link {
    text-decoration: none !important;
    color: inherit !important;
    display: block;
  }

  .recent-card {
    background: #ffffff;
    border: 1px solid #e5e7eb;
    border-radius: 16px;
    overflow: hidden;
    box-shadow: 0 4px 14px rgba(0, 0, 0, 0.06);
    transition: transform 0.25s ease, box-shadow 0.25s ease;
    height: 100%;
    display: flex;
    flex-direction: column;
  }

  .recent-card-link:hover .recent-card {
    transform: translateY(-5px);
    box-shadow: 0 12px 24px rgba(0, 0, 0, 0.12);
  }

  .recent-card-img-wrap {
    position: relative;
    width: 100%;
    height: 200px;
    background: #f3f4f6;
    overflow: hidden;
  }

  .recent-card-img-wrap img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: transform 0.35s ease;
  }

  .recent-card-link:hover .recent-card-img-wrap img {
    transform: scale(1.04);
  }

  .recent-badge {
    position: absolute;
    top: 12px;
    left: 12px;
    background: rgba(127, 29, 29, 0.92);
    color: #ffffff;
    font-family: 'Josefin Sans', sans-serif !important;
    font-size: 0.78rem !important;
    font-weight: 700 !important;
    padding: 5px 12px;
    border-radius: 20px;
    text-transform: uppercase;
    letter-spacing: 0.5px;
  }

  .recent-card-body {
    padding: 18px 20px;
    display: flex;
    flex-direction: column;
    flex-grow: 1;
    justify-content: space-between;
  }

  .recent-price {
    font-family: 'Josefin Sans', sans-serif !important;
    font-weight: 800;
    font-size: 1.25rem;
    color: #111827;
    margin-bottom: 6px;
    line-height: 1.25;
  }

  .recent-title {
    font-weight: 700;
    font-size: 1.05rem;
    color: #374151;
    margin-bottom: 4px;
  }

  .recent-location {
    font-size: 0.92rem !important;
    color: #6b7280;
    margin-bottom: 14px;
  }

  .recent-footer {
    border-top: 1px solid #f3f4f6;
    padding-top: 12px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 0.88rem !important;
    color: #4b5563;
  }

  .recent-cta {
    font-family: 'Josefin Sans', sans-serif !important;
    font-weight: 700;
    color: #BC2424;
  }

  @media (max-width: 960px) {
    .recent-grid-3x2 {
      grid-template-columns: repeat(2, 1fr);
    }
  }

  @media (max-width: 640px) {
    .recent-grid-3x2 {
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

  /* FORZADO BLANCO PARA EL TÍTULO DEL MODAL (Evita sobreescritura de h2 del layout) */
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

<div class="hero-container">
  <video autoplay loop muted playsinline class="hero-video">
    <source src="/assets/videos/cdmx-loop.mp4" type="video/mp4">
  </video>
  <div class="hero-overlay"></div>
  <div class="hero-content">
    <h2>Aquí comienza tu hogar</h2>
    <div class="hero-buttons">
      <!-- Directo al WhatsApp configurado -->
      <a href="https://wa.me/5533313132?text=Hola,%20quisiera%20m%C3%A1s%20informaci%C3%B3n%20sobre%20una%20propiedad" target="_blank" rel="noopener" class="hero-btn hero-btn-primary">Hablar con un asesor</a>
      
      <!-- Botones adicionales -->
      <a href="/catalogo-habitacional.html" class="hero-btn hero-btn-secondary">Propiedades habitacionales</a>
      <a href="/catalogo-comercial/" class="hero-btn hero-btn-secondary">Propiedades comerciales</a>
      
      <a href="/404.html/" class="hero-btn hero-btn-secondary">¿Quiénes Somos?</a>
    </div>
  </div>
</div>

<!-- SECCIÓN DINÁMICA DE PROPIEDADES RECIENTES (MÁXIMO 6 EN 2x3) -->
{% assign todas_propiedades = site.documents | where: "layout", "propiedad" | reverse %}
{% if todas_propiedades.size > 0 %}
<section class="recent-properties-section">
  <div class="recent-properties-header">
    <h2>Propiedades Recientes</h2>
  </div>

  <div class="recent-grid-3x2">
    {% for prop in todas_propiedades limit: 6 %}
      <a href="{{ prop.url | relative_url }}" class="recent-card-link">
        <article class="recent-card">
          <div class="recent-card-img-wrap">
            <img src="{{ prop.foto_principal | relative_url }}" alt="{{ prop.titulo }}">
            {% if prop.estado %}
              <span class="recent-badge">{{ prop.estado }}</span>
            {% endif %}
          </div>
          <div class="recent-card-body">
            <div>
              <div class="recent-price">{{ prop.precio }}</div>
              <div class="recent-title">{{ prop.titulo }}</div>
              <div class="recent-location">📍 {{ prop.ubicacion }}</div>
            </div>
            <div class="recent-footer">
              <span>{{ prop.superficie | default: prop.tipo }}</span>
              <span class="recent-cta">Ver ficha →</span>
            </div>
          </div>
        </article>
      </a>
    {% endfor %}
  </div>
</section>
{% endif %}

# Detrás de cada espacio hay una historia, nosotros acompañamos la tuya.

Despacho jurídico-inmobiliario en la zona centro de la CDMX. Fusionamos la máxima certeza legal con un acompañamiento cercano, transparente y humano.

---

> **Creemos que un hogar no es una métrica ni un código postal: es donde puedes respirar, donde puedas construir tus sueños.**

---

## El Binomio Gala: Certeza Legal + Sensibilidad Humana

### ⚖️ Respaldo Jurídico Especializado
Blindamos tu patrimonio con contratos rigurosos y acompañamiento notarial completo para que inviertas o vendas con absoluta tranquilidad.

### 🤝 Acompañamiento De Persona a Persona
Sin contestadoras automáticas ni filtros deshumanizados. Escuchamos activamente tus necesidades reales para encontrar el espacio o al habitante ideal para tu propiedad.

---

## Zonas de Enfoque Boutique

**Especialistas en la zona centro de la Ciudad de México.**  
Conocimiento profundo del mercado inmobiliario en **Roma · Condesa · Nápoles · Del Valle**.

---

## Servicios

- **Venta de Inmuebles**  

  Auditoría legal previa, comercialización estratégica y acompañamiento integral hasta la firma de escrituras ante notario.

- **Renta de Inmuebles**  

  Selección ética de arrendatarios mediante empatía activa, investigación exhaustiva y contratos blindados jurídicamente.

- **Consultoría Jurídico-Inmobiliaria**  

  Dictaminación de antecedentes, resolución de gravámenes y certezas para propietarios e inversionistas.

---

## Abramos las puertas a tu próximo hogar

Cuéntanos tus planes y encontremos tu espacio ideal.

<!-- Botón que activa la ventana modal -->
<button type="button" class="hero-btn hero-btn-primary btn-agendar" id="openFormBtn">Agendar una llamada</button>

<!-- VENTANA MODAL DEL FORMULARIO -->
<div class="modal-overlay" id="formModal">
  <div class="modal-card">
    <button type="button" class="close-btn" id="closeFormBtn">&times;</button>
    <h2 class="modal-title">Deja tus datos y te contactaremos :)</h2>

    <form id="gbrContactForm" class="gbr-form">
      <input type="hidden" name="propiedad" value="General">
      <input type="hidden" name="origen" value="Landing-Principal">

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
    </form>

    <div class="success-message" id="successMsg">
      ¡Gracias por contactarnos! Nos comunicaremos contigo muy pronto.
    </div>
  </div>
</div>

<script>
  const openBtn = document.getElementById('openFormBtn');
  const closeBtn = document.getElementById('closeFormBtn');
  const modal = document.getElementById('formModal');
  const form = document.getElementById('gbrContactForm');
  const successMsg = document.getElementById('successMsg');
  const submitBtn = document.getElementById('submitBtn');

  const SCRIPT_URL = 'https://script.google.com/macros/s/AKfycbzDfLWwiBHcF_tp69hLcpA7TsnVum7ni_zWZKgS8pJRjeSQh-0sn5W-5uSdaWX0Legv/exec';

  openBtn.addEventListener('click', () => modal.classList.add('active'));
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
