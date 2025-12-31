<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1"/>
  <title>The Mental Fit Mom Transformation™</title>
  <meta name="description" content="A 16-week hybrid coaching experience for moms to build muscle, regulate the nervous system, and become confident, capable, and strong—without burnout or scale obsession." />

  <style>
    :root{
      --bg: #f7f7f5;
      --surface: #ffffff;
      --text: #111827;
      --muted: #6b7280;
      --border: rgba(17,24,39,.10);
      --shadow: 0 12px 30px rgba(0,0,0,.06);
      --accent: #111827;
      --accent2: #374151;
      --radius: 14px;
      --max: 1100px;
    }

    *{ box-sizing:border-box; }
    body{
      margin:0;
      font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, "Apple Color Emoji","Segoe UI Emoji";
      color:var(--text);
      background:var(--bg);
      line-height:1.6;
    }

    a{ color:inherit; }

    .container{
      max-width: var(--max);
      margin: 0 auto;
      padding: 72px 20px;
    }

    .nav{
      position: sticky;
      top:0;
      z-index:10;
      backdrop-filter: blur(10px);
      background: rgba(247,247,245,.75);
      border-bottom: 1px solid var(--border);
    }

    .nav-inner{
      max-width: var(--max);
      margin: 0 auto;
      padding: 14px 20px;
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap:16px;
    }

    .brand{
      font-weight: 800;
      letter-spacing: .2px;
      font-size: 15px;
      text-decoration:none;
      white-space:nowrap;
    }

    .nav-links{
      display:flex;
      gap:14px;
      flex-wrap:wrap;
      justify-content:flex-end;
    }

    .nav-links a{
      font-size: 13px;
      color: var(--muted);
      text-decoration:none;
      padding:8px 10px;
      border-radius: 10px;
    }

    .nav-links a:hover{ background: rgba(17,24,39,.06); color: var(--text); }

    h1,h2,h3{ line-height:1.15; margin:0 0 12px; }
    h1{ font-size: clamp(34px, 4vw, 56px); letter-spacing: -0.8px; }
    h2{ font-size: clamp(24px, 3vw, 38px); letter-spacing: -0.4px; }
    h3{ font-size: 18px; letter-spacing: -0.2px; }

    p{ margin: 0 0 14px; font-size: 16px; color: rgba(17,24,39,.92); }
    .muted{ color: var(--muted); }

    .pill{
      display:inline-flex;
      align-items:center;
      gap:8px;
      padding: 10px 14px;
      border-radius: 999px;
      background: rgba(17,24,39,.06);
      color: var(--text);
      font-size: 13px;
      font-weight: 650;
    }

    .hero{
      background: var(--surface);
      border-bottom: 1px solid var(--border);
    }

    .hero-grid{
      display:grid;
      grid-template-columns: 1.15fr .85fr;
      gap: 28px;
      align-items:center;
    }

    .hero-card{
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      padding: 20px;
    }

    .hero .lead{
      font-size: 18px;
      color: rgba(17,24,39,.90);
      margin-top: 10px;
      max-width: 62ch;
    }

    .authority{
      margin-top: 14px;
      font-size: 13px;
      color: var(--muted);
    }

    .cta-row{
      margin-top: 18px;
      display:flex;
      gap:12px;
      flex-wrap:wrap;
      align-items:center;
    }

    .btn{
      display:inline-flex;
      align-items:center;
      justify-content:center;
      gap:10px;
      padding: 14px 18px;
      border-radius: 12px;
      font-weight: 800;
      font-size: 15px;
      text-decoration:none;
      border: 1px solid transparent;
      cursor:pointer;
      transition: transform .08s ease, background .2s ease, border-color .2s ease;
      user-select:none;
    }

    .btn:active{ transform: translateY(1px); }

    .btn-primary{
      background: var(--accent);
      color: #fff;
    }
    .btn-primary:hover{ background: var(--accent2); }

    .btn-secondary{
      background: rgba(17,24,39,.05);
      color: var(--text);
      border-color: var(--border);
    }
    .btn-secondary:hover{ background: rgba(17,24,39,.08); }

    .section{
      padding: 0;
    }

    .surface{
      background: var(--surface);
      border-top: 1px solid var(--border);
      border-bottom: 1px solid var(--border);
    }

    .grid{
      display:grid;
      grid-template-columns: repeat(12, 1fr);
      gap: 18px;
    }

    .card{
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      padding: 22px;
    }

    .span-6{ grid-column: span 6; }
    .span-4{ grid-column: span 4; }
    .span-8{ grid-column: span 8; }
    .span-12{ grid-column: span 12; }

    .list{
      margin: 14px 0 0;
      padding-left: 18px;
      color: rgba(17,24,39,.92);
    }
    .list li{ margin: 8px 0; }

    .kicker{
      font-size: 12px;
      text-transform: uppercase;
      letter-spacing: 1.4px;
      color: var(--muted);
      font-weight: 800;
      margin-bottom: 10px;
    }

    .pricing{
      display:flex;
      flex-direction:column;
      gap:10px;
      padding: 18px;
      border-radius: 16px;
      background: rgba(17,24,39,.04);
      border: 1px solid var(--border);
    }

    .price{
      display:flex;
      align-items:baseline;
      justify-content:space-between;
      gap:14px;
      flex-wrap:wrap;
    }
    .price strong{ font-size: 22px; }
    .price span{ color: var(--muted); font-size: 13px; }

    .note{
      font-size: 13px;
      color: var(--muted);
      margin-top: 10px;
    }

    .divider{
      height:1px;
      background: var(--border);
      margin: 18px 0;
    }

    details{
      border: 1px solid var(--border);
      border-radius: 14px;
      background: var(--surface);
      box-shadow: var(--shadow);
      padding: 14px 16px;
    }
    details + details{ margin-top: 12px; }
    summary{
      cursor:pointer;
      font-weight: 800;
      color: var(--text);
      list-style:none;
    }
    summary::-webkit-details-marker{ display:none; }
    details p{ margin-top: 10px; color: rgba(17,24,39,.90); }

    .cta-band{
      background: var(--accent);
      color:#fff;
    }
    .cta-band p, .cta-band .muted{ color: rgba(255,255,255,.82); }
    .cta-band h2{ color:#fff; }

    footer{
      padding: 36px 20px;
      text-align:center;
      color: var(--muted);
      font-size: 12px;
    }

    @media (max-width: 900px){
      .hero-grid{ grid-template-columns: 1fr; }
      .span-6, .span-4, .span-8{ grid-column: span 12; }
      .nav-links{ display:none; }
    }
  </style>
</head>

<body>

  <header class="nav">
    <div class="nav-inner">
      <a class="brand" href="#top">Mental Fit Mom™</a>
      <nav class="nav-links" aria-label="Page">
        <a href="#for">For You</a>
        <a href="#how">How It Works</a>
        <a href="#details">Program</a>
        <a href="#pricing">Pricing</a>
        <a href="#apply">Apply</a>
        <a href="#faq">FAQ</a>
      </nav>
    </div>
  </header>

  <main id="top">

    <!-- 1) HERO -->
    <section class="hero">
      <div class="container">
        <div class="hero-grid">
          <div>
            <div class="pill">16-Week Hybrid Coaching • Strength + Lifestyle + Mindset</div>
            <h1 style="margin-top:14px;">The Mental Fit Mom Transformation™</h1>

            <p class="lead">
              For moms who are done trying to do it all and burning out.
              Build strength, prioritize your nervous system, and become confident, capable, and strong —
              without obsessing over the scale.
            </p>

            <div class="authority">
              Certified Personal Trainer • Hybrid Coaching & Mentorship • Limited Monthly Enrollment
            </div>

            <div class="cta-row">
              <a class="btn btn-primary" href="#apply">Apply for Coaching</a>
              <a class="btn btn-secondary" href="#how">Learn How It Works</a>
            </div>

            <p class="note">If you’re ready for structure, support, and a plan you can actually sustain, you’re in the right place.</p>
          </div>

          <div class="hero-card">
            <div class="kicker">What you’ll walk away with</div>
            <ul class="list">
              <li>A strength plan built to support your life (not drain it)</li>
              <li>A nervous-system-first approach to consistency</li>
              <li>More muscle, more energy, and better self-trust</li>
              <li>Confidence to lead yourself—using me as a mentor over time</li>
            </ul>
            <div class="divider"></div>
            <div class="kicker">Capacity</div>
            <p class="muted" style="margin:0;">10–15 clients per month so you get real support.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- 2) WHO IT'S FOR -->
    <section class="section" id="for">
      <div class="container">
        <h2>Is this for you?</h2>
        <p class="muted">
          This program is for moms who want to feel strong and athletic again — with coaching that supports your body and your nervous system.
        </p>

        <div class="grid" style="margin-top:18px;">
          <div class="card span-6">
            <h3>This is for you if:</h3>
            <ul class="list">
              <li>You’re tired of “trying to do it all” and burning out</li>
              <li>You want to build muscle and strength (not chase a smaller number)</li>
              <li>You want structure without rigid rules</li>
              <li>You’re ready to be coached — not just handed a generic plan</li>
              <li>You want to feel confident, capable, and strong in your body</li>
            </ul>
          </div>

          <div class="card span-6">
            <h3>This isn’t for you if:</h3>
            <ul class="list">
              <li>You want a quick fix, detox, or “shred” phase</li>
              <li>You’re looking for a one-time PDF with no accountability</li>
              <li>You’re not ready to commit time, energy, and honesty to the process</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- 3) TRANSFORMATION -->
    <section class="surface" id="how">
      <div class="container">
        <div class="kicker">The point isn’t perfection</div>
        <h2>We build a strong body and a steady mind.</h2>
        <p>
          This isn’t “just workouts.” It’s learning how to train, recover, and live in a way that supports your hormones, your stress, and your real life.
          You’ll start with high support, then gradually shift into confidence and independence — with me as your mentor, not your crutch.
        </p>

        <div class="grid" style="margin-top:18px;">
          <div class="card span-4">
            <h3>Confident</h3>
            <p class="muted">You stop second-guessing every decision. You know what to do and why it works.</p>
          </div>
          <div class="card span-4">
            <h3>Capable</h3>
            <p class="muted">You train like an athlete: clear plan, clear progression, and sustainable habits.</p>
          </div>
          <div class="card span-4">
            <h3>Strong</h3>
            <p class="muted">More muscle, better energy, improved posture, and a body you trust again.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- 4) METHOD -->
    <section class="section" id="details">
      <div class="container">
        <div class="kicker">The Mental Fit Mom Method™</div>
        <h2>Equal parts strength, lifestyle, and mindset.</h2>

        <div class="grid" style="margin-top:18px;">
          <div class="card span-4">
            <h3>Strength</h3>
            <p class="muted">Certified programming with progressive overload, form support, and real-life scheduling.</p>
          </div>
          <div class="card span-4">
            <h3>Lifestyle</h3>
            <p class="muted">Cortisol-aware structure: sleep, recovery, steps, fueling, and routines that fit motherhood.</p>
          </div>
          <div class="card span-4">
            <h3>Mindset</h3>
            <p class="muted">We break all-or-nothing patterns and build identity-level consistency.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- 5) APPLICATION (Google Forms) -->
    <section class="surface" id="apply">
      <div class="container">
        <div class="kicker">Apply</div>
        <h2>Application questions</h2>
        <p class="muted">
          This is a high-touch program. Applications help us make sure it’s the right fit for your goals, lifestyle, and readiness.
        </p>

        <div class="grid" style="margin-top:18px;">
          <div class="card span-8">
            <h3>What you’ll answer</h3>
            <ul class="list">
              <li>What made you apply right now?</li>
              <li>What have you tried before that didn’t work (and why)?</li>
              <li>What would “confident, capable, strong” look like for you in 16 weeks?</li>
              <li>What’s your biggest obstacle (time, energy, stress, consistency, mindset)?</li>
              <li>How many days per week can you realistically train?</li>
              <li>What support do you need most from a coach?</li>
              <li>Are you ready for accountability and honest feedback?</li>
              <li>Are you prepared to invest in coaching? (Pay-in-full or payment plan)</li>
            </ul>
            <p class="note">You’ll also be able to share any postpartum considerations, injuries, or preferences.</p>
          </div>

          <div class="card span-4">
            <h3>Submit your application</h3>
            <p class="muted">Google Form application:</p>
            <a class="btn btn-primary" href="https://YOUR-GOOGLE-FORM-LINK" target="_blank" rel="noopener">Open Application</a>
            <p class="note">Replace the link with your actual Google Form URL.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- 6) PRICING (Upfront) -->
    <section class="section" id="pricing">
      <div class="container">
        <div class="kicker">Pricing</div>
        <h2>Upfront, clear, and simple.</h2>
        <p class="muted">
          You said you prefer to be upfront — and I agree. High-ticket doesn’t mean hidden pricing. It means high support and high standards.
        </p>

        <div class="grid" style="margin-top:18px;">
          <div class="card span-6">
            <h3>16-Week Hybrid Coaching</h3>
            <div class="pricing">
              <div class="price">
                <strong>$3,750</strong>
                <span>Pay in full</span>
              </div>
              <div class="price">
                <strong>$4,000</strong>
                <span>Payment plan total</span>
              </div>
            </div>
            <p class="note">Limited monthly enrollment (10–15 clients) to keep support high.</p>
          </div>

          <div class="card span-6">
            <h3>If asking for the sale feels hard…</h3>
            <p class="muted">
              You don’t have to “push.” Your job is to lead.
              The right client wants clarity, confidence, and a plan.
              We use an application so you can enroll with calm authority — not pressure.
            </p>
            <ul class="list">
              <li>Clear expectations → fewer “maybe” clients</li>
              <li>Upfront pricing → better-fit conversations</li>
              <li>Application-based → confident enrollment</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- 7) PROGRAM INCLUDES -->
    <section class="surface">
      <div class="container">
        <div class="kicker">What’s included</div>
        <h2>High support at first. Mentorship over time.</h2>

        <div class="grid" style="margin-top:18px;">
          <div class="card span-6">
            <h3>Coaching & Support</h3>
            <ul class="list">
              <li>Weekly coaching call (group)</li>
              <li>Weekly check-ins + accountability</li>
              <li>Messaging support (high-touch early → tapered later)</li>
              <li>Form feedback + guidance</li>
            </ul>
          </div>
          <div class="card span-6">
            <h3>Training + Lifestyle</h3>
            <ul class="list">
              <li>Personalized strength programming</li>
              <li>Progressive overload + scheduling that fits mom life</li>
              <li>Nervous system + recovery routines</li>
              <li>Fueling guidance focused on muscle-building</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- 8) ABOUT YOU -->
    <section class="section" id="about">
      <div class="container">
        <div class="kicker">About</div>
        <h2>Meet your coach</h2>

        <div class="grid" style="margin-top:18px;">
          <div class="card span-8">
            <p>
              I’m a certified personal trainer who coaches moms to build strength without burning out.
              I prioritize your nervous system, your real-life schedule, and muscle-building over scale obsession.
            </p>
            <p class="muted">
              My goal is to support you deeply at the start — then help you build the confidence and capability to lead yourself.
              You won’t just get results. You’ll learn how to keep them.
            </p>
          </div>

          <div class="card span-4">
            <h3>My coaching style</h3>
            <ul class="list">
              <li>Calm, direct, and supportive</li>
              <li>Strength-first and sustainable</li>
              <li>Accountability with compassion</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- 9) FINAL CTA -->
    <section class="cta-band">
      <div class="container">
        <h2>Ready to feel confident, capable, and strong?</h2>
        <p class="muted">
          If you’re done burning out and ready for a plan that builds muscle, energy, and self-trust — apply below.
        </p>
        <div class="cta-row" style="margin-top:18px;">
          <a class="btn btn-primary" href="https://YOUR-GOOGLE-FORM-LINK" target="_blank" rel="noopener">Apply via Google Form</a>
          <a class="btn btn-secondary" href="#pricing">View Pricing</a>
        </div>
        <p class="note">Applications reviewed weekly. If accepted, you’ll receive next steps by email.</p>
      </div>
    </section>

    <!-- FAQ -->
    <section class="section" id="faq">
      <div class="container">
        <div class="kicker">FAQ</div>
        <h2>Frequently asked questions</h2>

        <details>
          <summary>How does the hybrid coaching work?</summary>
          <p>
            You’ll get a personalized strength plan plus weekly coaching calls, check-ins, and messaging support.
            The support is highest early on, then shifts toward mentorship as your confidence grows.
          </p>
        </details>

        <details>
          <summary>Is this postpartum-friendly?</summary>
          <p>
            Yes. We’ll tailor training based on your postpartum timeline, current capacity, and your goals.
            If you have specific medical restrictions, we work within your provider’s guidance.
          </p>
        </details>

        <details>
          <summary>Do I need a gym?</summary>
          <p>
            Not necessarily. You can train at home or in a gym. We’ll build your plan around your available equipment.
          </p>
        </details>

        <details>
          <summary>What if I’m exhausted and inconsistent right now?</summary>
          <p>
            That’s exactly who this is designed for. We prioritize nervous system support and sustainable structure
            so you can build consistency without burning out.
          </p>
        </details>

        <details>
          <summary>Do you provide meal plans?</summary>
          <p>
            You’ll get fueling guidance and structure that supports muscle-building and recovery.
            We focus on education and sustainable habits rather than rigid dieting.
          </p>
        </details>

        <details>
          <summary>What happens after I apply?</summary>
          <p>
            You’ll submit the application. If it looks like a good fit, you’ll receive next steps.
            Depending on your process, that may include a short call or a direct enrollment link.
          </p>
        </details>

        <details>
          <summary>Why are you upfront about price?</summary>
          <p>
            Because clarity builds trust. High-ticket should feel calm and honest — not confusing.
            Pricing is shared upfront so only serious, aligned clients apply.
          </p>
        </details>

        <p class="note" style="margin-top:14px;">
          Disclaimer: Coaching is not medical advice and does not replace care from your physician or provider.
          Results vary based on consistency, recovery, and individual factors.
        </p>
      </div>
    </section>

  </main>

  <footer>
    © <span id="year"></span> The Mental Fit Mom Transformation™ • All rights reserved
  </footer>

  <script>
    document.getElementById('year').textContent = new Date().getFullYear();
  </script>

</body>
</html>
