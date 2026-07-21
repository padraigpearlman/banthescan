---
title: New York State Campaign | Ban the Scan
layout: default
nav: state
description: Four bills would ban law enforcement, landlord, public accommodation,
  and school use of facial recognition across New York State. See the bills and sign
  the petition.
hero:
  eyebrow: New York State Campaign
  heading: Four bills. One statewide ban.
  sub: Four bills moving through the New York State Legislature would ban the use
    of facial recognition and biometric surveillance by law enforcement, landlords,
    public accommodations, and schools statewide. Here's what each bill does, and
    how to tell your state legislators to pass them.
bills_section:
  label: The Legislation
  heading: What these four bills actually do.
  intro: All four bills currently have companion versions in the State Senate and
    Assembly.
petition:
  label: Take Action
  heading: Sign the New York State petition.
  intro: Add your name to tell state legislators to pass all four bills this session.
  action_network_slug: ban-the-scan-outlaw-facial-recognition-in-new-york
documents:
  label: Campaign Documents
  heading: Everything your organization needs to help.
  intro: Sign-on letters and memos of support for the state legislative package.
  doc_link_1_label: State Package Sign-On Letter (PDF)
  doc_link_1_url: "#"
  doc_link_2_label: Memo of Support (PDF)
  doc_link_2_url: "#"
  callout_text: Represent an organization? Sign on to our statewide coalition letter.
  callout_cta_label: Sign On Your Organization
contact:
  label: Get Involved
  heading: Contact your state legislators.
  intro: Signing the petition matters, but a direct call or email to your own State
    Senator and Assemblymember carries the most weight in Albany. Here's how in three
    steps.
  steps:
  - num: '01'
    title: Find Your Legislators
    text: Look up your State Senator and Assemblymember. You'll need both, since these
      bills need companion votes in each chamber.
    links:
    - label: Find My State Senator
      url: https://www.nysenate.gov/find-my-senator
      external: true
    - label: Find My Assemblymember
      url: https://www.nyassembly.gov/mem/search/
      external: true
  - num: '02'
    title: Call or Email
    text: 'A short, personal call takes two minutes and is one of the most effective
      things you can do. Use this script, or send the email template:'
    quote: "&ldquo;Hi, my name is ___ and I'm a constituent from [neighborhood/zip].
      I'm calling to ask [Senator/Assemblymember name] to co-sponsor and vote yes
      on S5609/A1045, S8223/A6363, S8004/A6211, and S9643/A6720 to ban discriminatory
      biometric surveillance in New York State.&rdquo;"
    links:
    - label: Get the Email Template
      url: "#"
      external: false
  - num: '03'
    title: Show Up
    text: Attend a hearing or coalition day of action in Albany. We'll email you the
      dates as soon as they're announced.
    links:
    - label: Join Our Action Alerts
      url: "#action"
      external: false
bridge:
  label: Fighting On Two Fronts
  heading: There's a City Campaign too.
  intro: NYC Council bills would ban biometric surveillance in public accommodations,
    residential buildings, and by city government. See the details and sign that petition
    too.
  cta_label: View the City Campaign
final_cta:
  label: Stay Involved
  heading: Don't miss a hearing date.
  intro: 'Get email updates as these four bills move through the State Legislature:
    hearing dates, votes, and moments when your call matters most.'
  cta_label: Why This Matters
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

    <!-- BILLS -->
    <section class="bills" id="bills">
        <div class="wrap">
            <p class="section-label">{{ page.bills_section.label }}</p>
            <h2 class="section-heading">{{ page.bills_section.heading }}</h2>
            <p class="section-intro">{{ page.bills_section.intro }}</p>

            <div class="bills-list">
                {% assign state_bills = site.bills | where: "scope", "state" | sort: "order" %}
                {% for bill in state_bills %}
                <article class="bill-card">
                    <div class="bill-card-head">
                        <span class="bill-number">{{ bill.bill_number }}</span>
                        <span class="status status-{{ bill.status_class }}"
                            >{{ bill.status }}</span
                        >
                    </div>
                    <h3>{{ bill.title }}</h3>
                    <p class="bill-sponsors">{{ bill.sponsors }}</p>
                    <p class="bill-desc">{{ bill.desc }}</p>
                    <div class="bill-links">
                        {% for link in bill.links %}
                        <a class="bill-link" href="{{ link.url }}">{{ link.label }} &rarr;</a>
                        {% endfor %}
                    </div>
                </article>
                {% endfor %}
            </div>
        </div>
    </section>

    <!-- PETITION -->
    <section class="petition" id="petition">
        <div class="wrap">
            <p class="section-label">{{ page.petition.label }}</p>
            <h2 class="section-heading">{{ page.petition.heading }}</h2>
            <p class="section-intro">{{ page.petition.intro }}</p>

            <div class="petition-embed">
                <!--
                  NOTE: this Action Network petition targets both the
                  New York State Legislature and New York City Council,
                  and its letter text cites an older bill number (S79)
                  rather than the current S5609/A1045, S8223/A6363,
                  S8004/A6211, S9643/A6720. Confirm the letter has been
                  updated before publishing.
                -->
                <link
                    href="https://actionnetwork.org/css/style-embed-v3.css"
                    rel="stylesheet"
                    type="text/css"
                />
                <script
                    src="https://actionnetwork.org/widgets/v6/petition/{{ page.petition.action_network_slug }}?format=js&source=widget"
                ></script>
                <div
                    id="can-petition-area-{{ page.petition.action_network_slug }}"
                    style="width: 100%"
                ></div>
            </div>
        </div>
    </section>

    <!-- CAMPAIGN DOCUMENTS -->
    <section class="campaign-docs" id="documents">
        <div class="wrap">
            <p class="section-label">{{ page.documents.label }}</p>
            <h2 class="section-heading">{{ page.documents.heading }}</h2>
            <p class="section-intro">{{ page.documents.intro }}</p>

            <div class="doc-links">
                <a class="btn btn-sm" href="{{ page.documents.doc_link_1_url }}"
                    >{{ page.documents.doc_link_1_label }}</a
                >
                <a class="btn btn-sm" href="{{ page.documents.doc_link_2_url }}"
                    >{{ page.documents.doc_link_2_label }}</a
                >
            </div>

            <div class="org-callout">
                <p>{{ page.documents.callout_text }}</p>
                <a class="btn btn-black" href="mailto:{{ site.footer_contact_email }}"
                    >{{ page.documents.callout_cta_label }}</a
                >
            </div>
        </div>
    </section>

    <!-- CONTACT YOUR LEGISLATORS -->
    <section class="contact-legislators" id="contact">
        <div class="wrap">
            <p class="section-label">{{ page.contact.label }}</p>
            <h2 class="section-heading">{{ page.contact.heading }}</h2>
            <p class="section-intro">{{ page.contact.intro }}</p>

            <div class="contact-grid">
                {% for step in page.contact.steps %}
                <div class="contact-step">
                    <div class="step-num">{{ step.num }}</div>
                    <h3>{{ step.title }}</h3>
                    <p>{{ step.text }}</p>
                    {% if step.quote %}
                    <blockquote>{{ step.quote }}</blockquote>
                    {% endif %}
                    <div class="contact-step-links">
                        {% for link in step.links %}
                        {% if link.external %}
                        <a class="btn btn-sm" href="{{ link.url }}" target="_blank" rel="noopener"
                            >{{ link.label }}</a
                        >
                        {% else %}
                        <a class="btn btn-sm" href="{{ link.url }}"
                            >{{ link.label }}</a
                        >
                        {% endif %}
                        {% endfor %}
                    </div>
                </div>
                {% endfor %}
            </div>
        </div>
    </section>

    <!-- BRIDGE TO CITY CAMPAIGN -->
    <section class="bridge-cta" id="bridge">
        <div class="wrap">
            <p class="section-label">{{ page.bridge.label }}</p>
            <h2 class="section-heading">{{ page.bridge.heading }}</h2>
            <p class="section-intro">{{ page.bridge.intro }}</p>
            <div class="bridge-actions">
                <a class="btn btn-yellow" href="{{ '/campaign-city.html' | relative_url }}"
                    >{{ page.bridge.cta_label }}</a
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
                <a class="btn btn-primary" href="{{ '/about.html' | relative_url }}"
                    >{{ page.final_cta.cta_label }}</a
                >
            </div>

            {% include signup-form.html %}
        </div>
    </section>
</main>
