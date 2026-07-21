---
title: Get Involved | Ban the Scan
description: Sign the New York State or New York City petition to ban facial recognition
  and biometric surveillance, or sign your organization on to the coalition.
hero:
  eyebrow: Get Involved
  heading: Two petitions. One fight.
  sub: Add your name to tell New York State and New York City lawmakers to ban facial
    recognition and biometric surveillance. Pick where you live, or sign both.
choose:
  label: Where Do You Live?
  heading: Choose your campaign.
  intro: 'Both petitions matter: if you or a loved one live or work in NYC or New
    York State, sign both for maximum impact.'
  state:
    title: New York State
    desc: Four bills would ban the use of facial recognition and biometric surveillance
      by law enforcement, landlords, public accommodations, and schools statewide.
    petition_cta_label: Sign the State Petition
    view_cta_label: View the State Campaign
  city:
    title: New York City
    desc: Three bills would ban facial recognition and biometric surveillance in public
      accommodations, residential buildings, and by city government itself.
    petition_cta_label: Sign the City Petition
    view_cta_label: View the City Campaign
organizations:
  label: Represent An Organization?
  heading: Join the coalition.
  intro: Sign your organization on to our sign-on letters and join dozens of legal
    defenders, immigrant justice groups, and digital rights advocates already backing
    this campaign.
  cta_label: Join the Coalition
final_cta:
  label: Stay Involved
  heading: Signed already? Do one more thing.
  intro: Calling or emailing your legislators is by far the best way to effect change.
  cta_label: Contact Your Legislators
layout: default
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

    <!-- CHOOSE YOUR CAMPAIGN -->
    <section class="definitions" id="choose">
        <div class="wrap">
            <p class="section-label">{{ page.choose.label }}</p>
            <h2 class="section-heading">{{ page.choose.heading }}</h2>
            <p class="section-intro">{{ page.choose.intro }}</p>

            <div class="definitions-grid">
                <div class="definition-card">
                    <h3>{{ page.choose.state.title }}</h3>
                    <p>{{ page.choose.state.desc }}</p>
                    <a
                        class="btn btn-primary"
                        href="{{ '/campaign-state.html' | relative_url }}#petition"
                        style="margin-top: 20px"
                        >{{ page.choose.state.petition_cta_label }}</a
                    >
                    <p
                        style="
                            text-align: center;
                            margin: 26px 0 -10px 0;
                        "
                    >
                        <a class="card-link" href="{{ '/campaign-state.html' | relative_url }}"
                            >{{ page.choose.state.view_cta_label }} &rarr;</a
                        >
                    </p>
                </div>
                <div class="definition-card">
                    <h3>{{ page.choose.city.title }}</h3>
                    <p>{{ page.choose.city.desc }}</p>
                    <a
                        class="btn btn-primary"
                        href="{{ '/campaign-city.html' | relative_url }}#petition"
                        style="margin-top: 20px"
                        >{{ page.choose.city.petition_cta_label }}</a
                    >
                    <p
                        style="
                            text-align: center;
                            margin: 26px 0 -10px 0;
                        "
                    >
                        <a class="card-link" href="{{ '/campaign-city.html' | relative_url }}"
                            >{{ page.choose.city.view_cta_label }} &rarr;</a
                        >
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- REPRESENT AN ORG -->
    <section class="bridge-cta" id="organizations">
        <div class="wrap">
            <p class="section-label">{{ page.organizations.label }}</p>
            <h2 class="section-heading">{{ page.organizations.heading }}</h2>
            <p class="section-intro">{{ page.organizations.intro }}</p>
            <div class="bridge-actions">
                <a class="btn btn-yellow" href="{{ '/coalition.html' | relative_url }}#join"
                    >{{ page.organizations.cta_label }}</a
                >
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
                <a class="btn btn-black" href="{{ '/contact-legislators.html' | relative_url }}"
                    >{{ page.final_cta.cta_label }}</a
                >
            </div>

            {% include signup-form.html %}
        </div>
    </section>
</main>
