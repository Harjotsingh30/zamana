[index.html](https://github.com/user-attachments/files/23202124/index.html)
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>ZAMANA® | WE ARE THE ERA.</title>

  <style>
    :root {
      --bg-main: #0f0f0f;          /* washed black vibe */
      --text-main: #f5f2e9;        /* bone / off-white */
      --text-dim: #9b988f;         /* muted bone */
      --accent-line: #2a2a2a;      /* subtle divider */
      --accent-badge: #1f1f1f;     /* badge bg */
      --accent-border: #3a3a3a;    /* thin borders */
      --btn-bg: #f5f2e9;           /* button light */
      --btn-text: #0f0f0f;         /* button dark text */
      --alt-bg: #f5f2e9;           /* light section bg */
      --alt-text: #0f0f0f;         /* dark text on light */
    }

    * {
      box-sizing: border-box;
      -webkit-font-smoothing: antialiased;
      text-rendering: optimizeLegibility;
      margin: 0;
      padding: 0;
    }

    body {
      background-color: var(--bg-main);
      color: var(--text-main);
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Inter", "Roboto", "Helvetica Neue", Arial, sans-serif;
      line-height: 1.4;
    }

    /* GLOBAL UTILS */
    .wrapper {
      width: 100%;
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 1.25rem;
    }

    h1, h2, h3, .caps {
      text-transform: uppercase;
      font-weight: 700;
      letter-spacing: -0.04em;
      line-height: 1.1;
    }

    .btn {
      background-color: var(--btn-bg);
      color: var(--btn-text);
      text-transform: uppercase;
      font-weight: 600;
      font-size: 0.8rem;
      line-height: 1;
      padding: 0.9rem 1.2rem;
      border: 0;
      cursor: pointer;
      border-radius: 0;
      display: inline-block;
      text-decoration: none;
      letter-spacing: -0.03em;
    }

    .btn-outline {
      background-color: transparent;
      color: var(--text-main);
      border: 1px solid var(--text-main);
    }

    .badge {
      background-color: var(--accent-badge);
      border: 1px solid var(--accent-border);
      color: var(--text-main);
      font-size: 0.6rem;
      font-weight: 600;
      line-height: 1;
      padding: 0.4rem 0.5rem;
      text-transform: uppercase;
      display: inline-block;
      letter-spacing: -0.03em;
    }

    img {
      max-width: 100%;
      display: block;
      object-fit: cover;
    }

    /* NAV */
    header {
      position: sticky;
      top: 0;
      z-index: 1000;
      background-color: rgba(15,15,15,0.9);
      border-bottom: 1px solid var(--accent-border);
      backdrop-filter: blur(4px);
    }

    .nav-bar {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 1rem 1.25rem;
    }

    .brand {
      font-size: 0.8rem;
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: -0.03em;
      line-height: 1.2;
    }

    nav ul {
      list-style: none;
      display: flex;
      gap: 1.25rem;
    }

    nav a {
      text-decoration: none;
      color: var(--text-main);
      font-size: 0.7rem;
      font-weight: 500;
      text-transform: uppercase;
      letter-spacing: -0.03em;
    }

    .cart-link {
      font-size: 0.7rem;
      text-transform: uppercase;
      font-weight: 600;
      letter-spacing: -0.03em;
      color: var(--text-main);
      text-decoration: none;
      border: 1px solid var(--accent-border);
      padding: 0.5rem 0.6rem;
      background-color: var(--accent-badge);
    }

    /* HERO */
    .hero {
      border-bottom: 1px solid var(--accent-border);
      background: radial-gradient(circle at 20% 20%, rgba(255,255,255,0.07) 0%, rgba(0,0,0,0) 70%);
    }

    .hero-inner {
      display: grid;
      grid-template-columns: 1fr;
      gap: 2rem;
      padding: 3rem 0 2rem;
    }

    .hero-copy h1 {
      font-size: clamp(2rem, 2.5vw, 2.8rem);
      font-weight: 700;
      margin-bottom: 1rem;
    }

    .hero-copy .tagline {
      color: var(--text-dim);
      font-size: 0.8rem;
      font-weight: 500;
      text-transform: uppercase;
      letter-spacing: -0.03em;
      margin-bottom: 2rem;
      line-height: 1.4;
    }

    .hero-ctas {
      display: flex;
      flex-wrap: wrap;
      gap: 0.75rem;
    }

    .hero-img {
      position: relative;
      border: 1px solid var(--accent-border);
      background-color: #1a1a1a;
      min-height: 260px;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 1rem;
    }

    .hero-img-note {
      position: absolute;
      bottom: 0.75rem;
      left: 0.75rem;
      font-size: 0.6rem;
      line-height: 1.3;
      color: var(--text-dim);
      background-color: rgba(0,0,0,0.6);
      padding: 0.4rem 0.5rem;
      border: 1px solid var(--accent-border);
    }

    /* DROP SECTION */
    .drop {
      border-bottom: 1px solid var(--accent-border);
      padding: 2.5rem 0;
    }

    .section-head {
      display: flex;
      flex-direction: column;
      gap: 0.5rem;
      margin-bottom: 2rem;
    }

    .section-head h2 {
      font-size: 1rem;
      font-weight: 700;
    }

    .section-head .subtle-line {
      font-size: 0.7rem;
      font-weight: 500;
      color: var(--text-dim);
      line-height: 1.3;
      max-width: 600px;
      letter-spacing: -0.03em;
    }

    .product-grid {
      display: grid;
      grid-template-columns: 1fr;
      gap: 2rem;
    }

    .product-card {
      border: 1px solid var(--accent-border);
      background-color: #1a1a1a;
      padding: 1rem;
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }

    .product-img-frame {
      background-color: #000;
      border: 1px solid var(--accent-border);
      width: 100%;
      aspect-ratio: 4/5;
      position: relative;
      display: flex;
      align-items: center;
      justify-content: center;
      overflow: hidden;
    }

    .badge-wrap {
      position: absolute;
      top: 0.75rem;
      left: 0.75rem;
      display: flex;
      flex-wrap: wrap;
      gap: 0.5rem;
    }

    .product-info-top {
      display: flex;
      align-items: flex-start;
      justify-content: space-between;
      flex-wrap: wrap;
      gap: 0.5rem;
    }

    .product-name {
      font-size: 0.8rem;
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: -0.03em;
      line-height: 1.3;
      max-width: 80%;
    }

    .product-price {
      font-size: 0.8rem;
      font-weight: 600;
      color: var(--text-main);
      line-height: 1.3;
    }

    .product-desc {
      font-size: 0.7rem;
      font-weight: 400;
      color: var(--text-dim);
      line-height: 1.4;
      letter-spacing: -0.03em;
    }

    /* ABOUT / STORY */
    .about {
      border-bottom: 1px solid var(--accent-border);
      padding: 2.5rem 0;
      display: grid;
      grid-template-columns: 1fr;
      gap: 2rem;
    }

    .about-copy h2 {
      font-size: 1rem;
      font-weight: 700;
      margin-bottom: 1rem;
    }

    .about-copy p {
      font-size: 0.8rem;
      line-height: 1.5;
      color: var(--text-main);
      font-weight: 500;
      white-space: pre-line; /* keeps intentional line breaks */
      letter-spacing: -0.03em;
    }

    .about-img {
      border: 1px solid var(--accent-border);
      background-color: #1a1a1a;
      min-height: 260px;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 1rem;
      position: relative;
    }

    .about-img-note {
      position: absolute;
      bottom: 0.75rem;
      left: 0.75rem;
      font-size: 0.6rem;
      line-height: 1.3;
      color: var(--text-dim);
      background-color: rgba(0,0,0,0.6);
      padding: 0.4rem 0.5rem;
      border: 1px solid var(--accent-border);
    }

    /* EMAIL / SIGNUP */
    .signup {
      background-color: var(--alt-bg);
      color: var(--alt-text);
      padding: 2.5rem 0;
    }

    .signup-inner {
      display: grid;
      grid-template-columns: 1fr;
      gap: 1rem;
    }

    .signup-copy h2 {
      color: var(--alt-text);
      font-size: 1rem;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: -0.03em;
      margin-bottom: 0.5rem;
    }

    .signup-copy p {
      color: var(--alt-text);
      font-size: 0.75rem;
      line-height: 1.4;
      font-weight: 500;
      letter-spacing: -0.03em;
    }

    .signup-form {
      display: flex;
      flex-wrap: wrap;
      gap: 0.75rem;
    }

    .signup-form input[type="email"] {
      flex: 1 1 220px;
      min-width: 0;
      border: 1px solid #000;
      background-color: transparent;
      color: #000;
      font-size: 0.8rem;
      padding: 0.9rem 1rem;
      font-family: inherit;
      letter-spacing: -0.03em;
      outline: none;
    }

    .signup-form input::placeholder {
      color: #4a4a4a;
    }

    .btn-alt {
      background-color: #000;
      color: #fff;
      border: 1px solid #000;
      text-transform: uppercase;
      font-weight: 600;
      font-size: 0.8rem;
      line-height: 1;
      padding: 0.9rem 1.2rem;
      border-radius: 0;
      cursor: pointer;
      letter-spacing: -0.03em;
    }

    /* FOOTER */
    footer {
      border-top: 1px solid var(--accent-border);
      padding: 2rem 0 4rem;
      background-color: var(--bg-main);
      color: var(--text-main);
    }

    .footer-grid {
      display: grid;
      grid-template-columns: 1fr;
      gap: 2rem;
      margin-bottom: 2rem;
    }

    .footer-brand {
      font-size: 0.75rem;
      font-weight: 500;
      line-height: 1.5;
      letter-spacing: -0.03em;
      white-space: pre-line;
    }

    .footer-links h3 {
      font-size: 0.7rem;
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: -0.03em;
      margin-bottom: 0.75rem;
    }

    .footer-links ul {
      list-style: none;
      display: grid;
      gap: 0.5rem;
    }

    .footer-links a {
      font-size: 0.7rem;
      color: var(--text-main);
      text-decoration: none;
      font-weight: 400;
      letter-spacing: -0.03em;
    }

    .footer-bottom {
      border-top: 1px solid var(--accent-line);
      padding-top: 1rem;
      font-size: 0.6rem;
      color: var(--text-dim);
      letter-spacing: -0.03em;
    }

    /* RESPONSIVE */
    @media (min-width: 640px) {
      .hero-inner {
        grid-template-columns: 1fr 1fr;
        align-items: center;
      }
      .about {
        grid-template-columns: 1fr 1fr;
        align-items: start;
      }
      .signup-inner {
        grid-template-columns: 1fr 1fr;
        align-items: center;
      }
      .footer-grid {
        grid-template-columns: 1fr auto;
      }
    }

    @media (min-width: 768px) {
      .product-grid {
        grid-template-columns: repeat(3, 1fr);
      }
    }
  </style>
</head>

<body>

  <!-- NAV -->
  <header>
    <div class="wrapper nav-bar">
      <div class="brand">
        ZAMANA®<br/>WE ARE THE ERA.
      </div>

      <nav>
        <ul>
          <li><a href="#drop">Shop</a></li>
          <li><a href="#about">About</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>

      <a class="cart-link" href="#">Cart · 0</a>
    </div>
  </header>

  <!-- HERO -->
  <section class="hero">
    <div class="wrapper hero-inner">
      <div class="hero-copy">
        <h1>WE ARE THE ERA.</h1>

        <div class="tagline caps">
          DROP 001 // LIMITED RELEASE  
          CHICAGO · PANJAB · WORLDWIDE
        </div>

        <div class="hero-ctas">
          <a class="btn" href="#drop">SHOP DROP 001</a>
          <a class="btn btn-outline" href="#email">ENTER THE ERA</a>
        </div>
      </div>

      <div class="hero-img">
        <!-- replace this with your own hoodie photo -->
        <img src="https://via.placeholder.com/500x600/1a1a1a/ffffff?text=ZAMANA+HOODIE+BACKPRINT" alt="ZAMANA hoodie mockup">

        <div class="hero-img-note">
          ZAMANA HEAVY HOODIE — WASHED BLACK<br/>
          BACK PRINT: WE ARE THE ERA.
        </div>
      </div>
    </div>
  </section>

  <!-- DROP -->
  <section id="drop" class="drop">
    <div class="wrapper">
      <div class="section-head">
        <h2 class="caps">DROP 001</h2>
        <div class="subtle-line">
          Era uniform. Heavyweight. No restock after this run.
        </div>
      </div>

      <div class="product-grid">
        <!-- PRODUCT 1 -->
        <div class="product-card">
          <div class="product-img-frame">
            <div class="badge-wrap">
              <div class="badge">LOW STOCK</div>
            </div>
            <img src="https://via.placeholder.com/500x600/000000/ffffff?text=WASHED+BLACK+HOODIE" alt="ZAMANA Heavy Hoodie - Washed Black">
          </div>

          <div class="product-info-top">
            <div class="product-name">
              ZAMANA HEAVY HOODIE — WASHED BLACK
            </div>
            <div class="product-price">$70</div>
          </div>

          <div class="product-desc">
            Oversized, heavyweight street cut. Front chest: ZAMANA®. Back: WE ARE THE ERA / CHICAGO · PKLN · DELHI / EST. 2025. One-color bone ink. Unisex. No restock.
          </div>

          <a class="btn" href="#">ADD TO CART</a>
        </div>

        <!-- PRODUCT 2 -->
        <div class="product-card">
          <div class="product-img-frame">
            <div class="badge-wrap">
              <div class="badge">LIMITED</div>
            </div>
            <img src="https://via.placeholder.com/500x600/f5f2e9/0f0f0f?text=BONE+TEE+BACK" alt="ERA Statement Tee — Bone">
          </div>

          <div class="product-info-top">
            <div class="product-name">
              ERA STATEMENT TEE — BONE
            </div>
            <div class="product-price">$40</div>
          </div>

          <div class="product-desc">
            Bone tee. Front micro stamp: ZAMANA / WE ARE THE ERA / EST. 2025. Back print: TIME DOESN’T OWN US. Boxy fit. Unisex. No restock.
          </div>

          <a class="btn" href="#">ADD TO CART</a>
        </div>

        <!-- PRODUCT 3 -->
        <div class="product-card">
          <div class="product-img-frame">
            <div class="badge-wrap">
              <div class="badge">COMING SOON</div>
            </div>
            <img src="https://via.placeholder.com/500x600/2f2f2f/ffffff?text=ARMY+FADE+SWEATS" alt="ZMN Stacked Sweats — Army Fade">
          </div>

          <div class="product-info-top">
            <div class="product-name">
              ZMN STACKED SWEATS — ARMY FADE
            </div>
            <div class="product-price">$65</div>
          </div>

          <div class="product-desc">
            Faded army green. Thigh print: ZMN // EST. 2025. Down-leg vertical ZAMANA. Tapered ankle. Unisex layer piece with hoodie.
          </div>

          <a class="btn btn-outline" href="#">NOTIFY ME</a>
        </div>
      </div>
    </div>
  </section>

  <!-- ABOUT -->
  <section id="about" class="about wrapper">
    <div class="about-copy">
      <h2 class="caps">THIS IS OUR ERA.</h2>
      <p>
ZAMANA is built for the kids who were “too much” where they came from
and “not enough” where they ended up.

We make uniforms for people who don’t ask to belong.

Chicago raised.
Panjabi blood.
Global timeline.

EST. 2025
      </p>
    </div>

    <div class="about-img">
      <img src="https://via.placeholder.com/500x600/1a1a1a/ffffff?text=FLASH+PHOTO+ON+BODY" alt="On-body street shot">
      <div class="about-img-note">
        SEE IT ON BODY<br/>
        TAG @ZAMANA.WORLD
      </div>
    </div>
  </section>

  <!-- SIGNUP / EMAIL -->
  <section id="email" class="signup">
    <div class="wrapper signup-inner">
      <div class="signup-copy">
        <h2>GET IN EARLY.</h2>
        <p>No spam. Just drop times.</p>
      </div>

      <form class="signup-form">
        <input type="email" placeholder="enter email to get drop codes" />
        <button class="btn-alt" type="submit">ENTER THE ERA</button>
      </form>
    </div>
  </section>

  <!-- FOOTER -->
  <footer id="contact">
    <div class="wrapper">
      <div class="footer-grid">
        <div class="footer-brand">
          ZAMANA®
          WE ARE THE ERA.
          Chicago, IL
          EST. 2025
        </div>

        <div class="footer-links">
          <h3>Info</h3>
          <ul>
            <li><a href="#drop">Shop</a></li>
            <li><a href="#">Sizing</a></li>
            <li><a href="#">Returns</a></li>
            <li><a href="mailto:contact@zamana.world">Contact</a></li>
          </ul>
        </div>
      </div>

      <div class="footer-bottom">
        © 2025 ZAMANA. ALL RIGHTS RESERVED.
      </div>
    </div>
  </footer>

</body>
</html>
