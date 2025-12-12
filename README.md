<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>TechLine Mobile Distributors</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background: #f4f4f4;
      color: #333;
    }
    header {
      background: #0a2a43;
      color: white;
      padding: 20px;
      text-align: center;
    }
    header img {
      max-width: 120px;
      margin-bottom: 10px;
    }
    section {
      padding: 20px;
      max-width: 900px;
      margin: auto;
      background: white;
      margin-top: 20px;
      border-radius: 10px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }
    h2 {
      color: #0a2a43;
    }
    footer {
      text-align: center;
      padding: 10px;
      margin-top: 30px;
      background: #0a2a43;
      color: white;
    }
    a { color: inherit; text-decoration: none; }
    .contact-item { cursor: pointer; }
  </style>
</head>
<body>
  <header>
    <img id="site-logo" src="logo-placeholder.png" alt="TechLine Logo" />
    <h1 id="site-title">TechLine Mobile Distributors</h1>
    <p>Reliable • Professional • Trusted in Mobile Technology</p>
  </header>

  <section id="about">
    <h2 id="about-title">About Us</h2>
    <p>TechLine Mobile Distributors is a Malawi-based supplier of high-quality mobile accessories, smartphones, chargers, earphones, and digital gadgets. We distribute to over 25 retailers in Blantyre, Limbe, Zomba, and Mulanje.</p>
  </section>

  <section id="services">
    <h2 id="services-title">Our Services</h2>
    <ul id="services-list">
      <li class="service">Wholesale mobile accessories</li>
      <li class="service">Retail distribution</li>
      <li class="service">Product sourcing and logistics</li>
      <li class="service">Marketing and product promotion</li>
    </ul>
  </section>

  <section id="contact">
    <h2 id="contact-title">Contact Us</h2>
    <p><strong>Phone:</strong> <span id="phone" class="contact-item">0885 760 776</span></p>
    <p><strong>Email:</strong> <span id="email" class="contact-item">chisangalalomaganga (at) gmail (dot) com</span></p>
    <p><strong>Location:</strong> <span id="location" class="contact-item">Blantyre, Malawi</span></p>
  </section>

  <footer id="site-footer">
    <p>© 2025 TechLine Mobile Distributors. All rights reserved.</p>
  </footer>

  <script>
    function safeLog(message) {
      if (window && typeof console !== 'undefined' && typeof console.log === 'function') {
        console.log(message);
      }
    }

    document.addEventListener('DOMContentLoaded', function () {
      safeLog('DEBUG: DOMContentLoaded fired');

      var logo = document.getElementById('site-logo');
      if (logo) {
        logo.addEventListener('load', function () { safeLog('DEBUG: Logo image loaded'); });
        logo.addEventListener('error', function () { safeLog('DEBUG: Logo image failed to load'); });
      } else {
        safeLog('DEBUG: Logo element not found');
      }

      var title = document.getElementById('site-title');
      if (title) title.addEventListener('click', function () { safeLog('DEBUG: Header title clicked'); });

      var aboutTitle = document.getElementById('about-title');
      if (aboutTitle) aboutTitle.addEventListener('click', function () { safeLog('DEBUG: About Us section title clicked'); });

      var servicesTitle = document.getElementById('services-title');
      if (servicesTitle) servicesTitle.addEventListener('click', function () { safeLog('DEBUG: Services section title clicked'); });

      var serviceItems = document.querySelectorAll('#services-list .service');
      serviceItems.forEach(function (item) {
        item.addEventListener('click', function () { safeLog('DEBUG: List item clicked – ' + item.textContent); });
      });

      var contactTitle = document.getElementById('contact-title');
      if (contactTitle) contactTitle.addEventListener('click', function () { safeLog('DEBUG: Contact Us section title clicked'); });

      var phone = document.getElementById('phone');
      if (phone) phone.addEventListener('click', function () { safeLog('DEBUG: Phone number clicked'); });

      var email = document.getElementById('email');
      if (email) email.addEventListener('click', function () { safeLog('DEBUG: Email clicked'); });

      var locationEl = document.getElementById('location');
      if (locationEl) locationEl.addEventListener('click', function () { safeLog('DEBUG: Location clicked'); });

      var footer = document.getElementById('site-footer');
      if (footer) footer.addEventListener('click', function () { safeLog('DEBUG: Footer clicked'); });

      safeLog('DEBUG: Script initialized and event listeners attached');
    });
  </script>
</body>
</html>
