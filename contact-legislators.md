---
title: Contact Your Legislators | Ban the Scan
layout: default
description: Find and contact your New York State Senator and Assemblymember, or your
  New York City Council Member, and tell them to ban biometric surveillance.
hero:
  eyebrow: Contact Your Legislators
  heading: A call or email beats a click, every time.
  sub: Signing a petition matters, but a direct call or email from a constituent carries
    the most weight, whether it's your State Senator and Assemblymember in Albany,
    or your City Council Member at City Hall.
choose:
  label: Who Do You Need to Contact?
  heading: Find your legislators.
  intro: Both campaigns matter. If you live, work, or spend time in New York State
    and New York City, contact both sets of legislators.
  state:
    title: New York State
    desc: Four bills need co-sponsors and floor votes in Albany. Look up your State
      Senator and Assemblymember, then use our call script or email template.
    contact_cta_label: Contact Your State Legislators
    view_cta_label: View the State Campaign
  city:
    title: New York City
    desc: Two bills are already in committee, and the government-use ban still needs
      a Council sponsor. Look up your Council Member, then use our call script or
      email template.
    contact_cta_label: Contact Your Council Member
    view_cta_label: View the City Campaign
final_cta:
  label: Stay Involved
  heading: Haven't signed the petition yet?
  intro: Add your name alongside a call or email. Both together move bills faster
    than either alone.
  cta_label: Sign the Petition
---

<main id="main">
    <!-- PAGE HERO -->
    <section class="page-hero">
        <div class="wrap">
            <span class="hero-eyebrow">{{ page.hero.eyebrow }}</span>
            <h1>{{ page.hero.heading }}</h1>
            <p class="hero-sub">{{ page.hero.sub }}</p>
        </div>
    </section>

    <div class="tape-divider" aria-hidden="true"></div>

    <!-- CHOOSE YOUR LEGISLATORS -->
    <section class="definitions" id="choose">
        <div class="wrap">
            <p class="section-label">{{ page.choose.label }}</p>
            <h2 class="section-heading">{{ page.choose.heading }}</h2>
            <p class="section-intro">{{ page.choose.intro }}</p>

            <div class="definitions-grid">
                <div class="definition-card">
                    <h3>{{ page.choose.state.title }}</h3>
                    <p>{{ page.choose.state.desc }}</p>
                    <div class="doc-links" style="margin-top: 20px">
                        <a
                            class="btn btn-primary"
                            href="{{ '/campaign-state.html' | relative_url }}#contact"
                            >{{ page.choose.state.contact_cta_label }}</a
                        >
                        <a
                            class="card-link"
                            href="{{ '/campaign-state.html' | relative_url }}"
                            >{{ page.choose.state.view_cta_label }} &rarr;</a
                        >
                    </div>
                </div>
                <div class="definition-card">
                    <h3>{{ page.choose.city.title }}</h3>
                    <p>{{ page.choose.city.desc }}</p>
                    <div class="doc-links" style="margin-top: 20px">
                        <a
                            class="btn btn-primary"
                            href="{{ '/campaign-city.html' | relative_url }}#contact"
                            >{{ page.choose.city.contact_cta_label }}</a
                        >
                        <a
                            class="card-link"
                            href="{{ '/campaign-city.html' | relative_url }}"
                            >{{ page.choose.city.view_cta_label }} &rarr;</a
                        >
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- FINAL CTA -->
    <section class="final-cta" id="action">
        <div class="wrap">
            <p class="section-label">{{ page.final_cta.label }}</p>
            <h2 class="section-heading">{{ page.final_cta.heading }}</h2>
            <p class="section-intro">{{ page.final_cta.intro }}</p>

            <div class="cta-actions">
                <a class="btn btn-black" href="{{ '/get-involved.html' | relative_url }}"
                    >{{ page.final_cta.cta_label }}</a
                >
            </div>

            {% include signup-form.html %}
        </div>
    </section>
</main>
