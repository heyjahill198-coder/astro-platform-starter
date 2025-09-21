# Astro on Netlify Platform Starter

[Live Demo](https://astro-platform-starter.netlify.app/)

A modern starter based on Astro.js, Tailwind, and [Netlify Core Primitives](https://docs.netlify.com/core/overview/#develop) (Edge Functions, Image CDN, Blob Store).

## Astro Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help` | Get help using the Astro CLI                     |

## Deploying to Netlify

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/netlify-templates/astro-platform-starter)

## Developing Locally

| Prerequisites                                                                |
| :--------------------------------------------------------------------------- |
| [Node.js](https://nodejs.org/) v18.14+.                                      |
| (optional) [nvm](https://github.com/nvm-sh/nvm) for Node version management. |

1. Clone this repository, then run `npm install` in its root directory.

2. For the starter to have full functionality locally (e.g. edge functions, blob store), please ensure you have an up-to-date version of Netlify CLI. Run:

```
npm install netlify-cli@latest -g
```

3. Link your local repository to the deployed Netlify site. This will ensure you're using the same runtime version for both local development and your deployed site.

```
netlify link
```

4. Then, run the Astro.js development server via Netlify CLI:

```
netlify dev
```

If your browser doesn't navigate to the site automatically, visit [localhost:8888](http://localhost:8888).
<!doctype html>
<html lang="ur">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />

  <!-- ---------- SEO / Google ---------- -->
  <title>REPLACE_ME - Aapka Business Naam</title>
  <meta name="description" content="REPLACE_ME — Chhota business ki short description yahan." />
  <!-- Google Search Console verification (paste the code from Search Console) -->
  <meta name="google-site-verification" content="REPLACE_ME_SEARCH_CONSOLE_CODE" />

  <!-- Canonical -->
  <link rel="canonical" href="https://www.example.com/" />

  <!-- Robots -->
  <meta name="robots" content="index, follow" />

  <!-- Open Graph (Facebook, WhatsApp previews) -->
  <meta property="og:type" content="website" />
  <meta property="og:title" content="REPLACE_ME - Aapka Business Naam" />
  <meta property="og:description" content="REPLACE_ME — short description." />
  <meta property="og:url" content="https://www.example.com/" />
  <meta property="og:image" content="https://www.example.com/og-image.jpg" />

  <!-- Twitter Card -->
  <meta name="twitter:card" content="summary_large_image" />
  <meta name="twitter:title" content="REPLACE_ME - Aapka Business Naam" />
  <meta name="twitter:description" content="REPLACE_ME — short description." />
  <meta name="twitter:image" content="https://www.example.com/og-image.jpg" />

  <!-- Favicon -->
  <link rel="icon" href="/favicon.ico" />

  <!-- ---------- Google Analytics (GA4) ---------- -->
  <!-- Replace G-XXXXXXXXXX with your Measurement ID -->
  <script async src="https://www.googletagmanager.com/gtag/js?id=G-REPLACE_ME"></script>
  <script>
    window.dataLayer = window.dataLayer || [];
    function gtag(){dataLayer.push(arguments);}
    gtag('js', new Date());
    gtag('config', 'G-REPLACE_ME'); // <-- put your GA4 ID
  </script>

  <!-- ---------- LocalBusiness structured data (JSON-LD) ---------- -->
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "LocalBusiness",
    "name": "REPLACE_ME - Aapka Business Naam",
    "image": "https://www.example.com/logo.png",
    "@id": "https://www.example.com/",
    "url": "https://www.example.com/",
    "telephone": "+965-1234-5678",
    "address": {
      "@type": "PostalAddress",
      "streetAddress": "REPLACE_ME Street",
      "addressLocality": "REPLACE_ME City",
      "addressRegion": "REPLACE_ME Region",
      "postalCode": "REPLACE_ME",
      "addressCountry": "KW"
    },
    "openingHoursSpecification": [{
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Monday","Tuesday","Wednesday","Thursday","Friday"],
      "opens": "09:00",
      "closes": "18:00"
    }],
    "priceRange": "$"
  }
  </script>

  <style>
    /* Simple, clean styles */
    body { font-family: system-ui, -apple-system, "Segoe UI", Roboto, "Noto Sans", sans-serif; margin:0; color:#111; }
    header{padding:24px; background:#f7f7f7}
    .container{max-width:900px;margin:24px auto;padding:0 16px}
    .hero{display:flex;gap:18px;align-items:center}
    .hero img{width:120px;height:120px;object-fit:cover;border-radius:12px}
    form{display:grid;gap:8px;max-width:480px}
    input,textarea{padding:10px;border:1px solid #ddd;border-radius:6px;font-size:14px}
    button{padding:10px 14px;border:0;border-radius:8px;cursor:pointer}
    footer{padding:18px;text-align:center;color:#666}
  </style>
</head>
<body>
  <header>
    <div class="container">
      <h1>REPLACE_ME - Aapka Business Naam</h1>
      <p>Short tagline ya business summary.</p>
    </div>
  </header>

  <main class="container">
    <section class="hero">
      <img src="/logo.png" alt="Business Logo">
      <div>
        <h2>Services</h2>
        <p>Yahan apni services/offerings likhein — ek do line mein.</p>
        <p><strong>Address:</strong> REPLACE_ME Street, City</p>
        <p><strong>Phone:</strong> +965-1234-5678</p>
      </div>
    </section>

    <section style="margin-top:20px">
      <h3>Contact karen</h3>
      <form id="contactForm">
        <input type="text" name="name" placeholder="Naam" required/>
        <input type="email" name="email" placeholder="Email" required/>
        <input type="text" name="phone" placeholder="Phone (optional)"/>
        <textarea name="message" rows="5" placeholder="Aapka message" required></textarea>
        <button type="submit">Send</button>
      </form>
      <div id="status" style="margin-top:8px;color:green"></div>
    </section>
  </main>

  <footer>
    © <span id="year"></span> REPLACE_ME. All rights reserved.
  </footer>

  <script>
    // small footer year
    document.getElementById('year').textContent = new Date().getFullYear();

    // contact form: posts to /api/contact (see server example)
    document.getElementById('contactForm').addEventListener('submit', async function(e){
      e.preventDefault();
      const f = e.target;
      const data = { name: f.name.value, email: f.email.value, phone: f.phone.value, message: f.message.value};
      document.getElementById('status').textContent = 'Sending...';
      try {
        const res = await fetch('/api/contact', {
          method:'POST',
          headers:{'Content-Type':'application/json'},
          body: JSON.stringify(data)
        });
        if(res.ok){
          document.getElementById('status').textContent = 'Message sent — shukriya!';
          f.reset();
        } else {
          const txt = await res.text();
          document.getElementById('status').textContent = 'Error: ' + txt;
        }
      } catch(err){
        document.getElementById('status').textContent = 'Network error';
      }
    });
  </script>
</body>
</html>
