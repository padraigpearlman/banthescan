---
title: The Coalition | Ban the Scan
layout: default
nav: coalition
description: Ban the Scan is led by a steering committee of civil rights organizations
  and backed by dozens of coalition members across New York. Join us.
hero:
  eyebrow: The Coalition
  heading: One campaign, dozens of organizations.
  sub: Ban the Scan is led by a steering committee of civil rights and civil liberties
    organizations, and backed by a growing coalition of community groups, legal organizations,
    and advocates across New York.
steering:
  label: Steering Committee
  heading: Who leads this campaign.
  intro: These organizations set the strategy and direction for the Ban the Scan campaign.
members:
  label: Coalition Members
  heading_suffix: organizations, standing together.
  intro: Legal defenders, immigrant justice groups, digital rights advocates, and
    community organizations across New York have all signed on.
join:
  label: Get Involved
  heading: Join the coalition.
  intro: Represent an organization that wants to help ban biometric surveillance in
    New York? Tell us about your organization below.
  form_action: "#"
  form_heading: Join the Coalition
  form_intro: We'll follow up by email to confirm your organization and add you to
    our sign-on letters.
  label_org_name: Organization Name
  label_contact_name: Contact Name
  label_contact_email: Email Address
  label_org_website: Organization Website (optional)
  label_message: Anything else we should know? (optional)
  submit_label: Submit
final_cta:
  label: Take Action
  heading: Your legislators need to hear from you.
  intro: Sign the petition, contact your representatives, and stay in the loop as
    these bills move through the City Council and State Legislature.
  cta_primary_label: Sign the Petition
  cta_primary_url: "/get-involved.html"
  cta_secondary_label: Contact Your Legislators
  cta_secondary_url: "/contact-legislators.html"
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

    <!-- STEERING COMMITTEE -->
    <section class="definitions" id="steering-committee">
        <div class="wrap">
            <p class="section-label">{{ page.steering.label }}</p>
            <h2 class="section-heading">{{ page.steering.heading }}</h2>
            <p class="section-intro">{{ page.steering.intro }}</p>

            <div class="logo-grid">
                {% assign steering_orgs = site.coalition_orgs | where_exp: "o", "o.tags contains 'steering'" | sort: "steering_order" %}
                {% for org in steering_orgs %}
                <div class="logo-tile">
                    <span>{{ org.name }}</span>
                </div>
                {% endfor %}
            </div>
        </div>
    </section>

    <!-- COALITION MEMBERS -->
    <section class="precedent" id="members">
        <div class="wrap">
            <p class="section-label">{{ page.members.label }}</p>
            <h2 class="section-heading">
                {{ site.coalition_orgs | where_exp: "o", "o.tags contains 'member'" | size }} {{ page.members.heading_suffix }}
            </h2>
            <p class="section-intro">{{ page.members.intro }}</p>

            <div class="logo-grid">
                {% assign member_orgs = site.coalition_orgs | where_exp: "o", "o.tags contains 'member'" | sort: "member_order" %}
                {% for org in member_orgs %}
                <div class="logo-tile">
                    <span>{{ org.name }}</span>
                </div>
                {% endfor %}
            </div>
        </div>
    </section>

    <!-- JOIN THE COALITION -->
    <section class="petition" id="join">
        <div class="wrap">
            <p class="section-label">{{ page.join.label }}</p>
            <h2 class="section-heading">{{ page.join.heading }}</h2>
            <p class="section-intro">{{ page.join.intro }}</p>

            <form class="join-form" action="{{ page.join.form_action }}" method="post">
                <h3>{{ page.join.form_heading }}</h3>
                <p>{{ page.join.form_intro }}</p>

                <div class="form-row">
                    <label for="org-name">{{ page.join.label_org_name }}</label>
                    <input
                        type="text"
                        id="org-name"
                        name="org-name"
                        required
                    />
                </div>
                <div class="form-row">
                    <label for="contact-name">{{ page.join.label_contact_name }}</label>
                    <input
                        type="text"
                        id="contact-name"
                        name="contact-name"
                        required
                    />
                </div>
                <div class="form-row">
                    <label for="contact-email">{{ page.join.label_contact_email }}</label>
                    <input
                        type="email"
                        id="contact-email"
                        name="contact-email"
                        required
                    />
                </div>
                <div class="form-row">
                    <label for="org-website"
                        >{{ page.join.label_org_website }}</label
                    >
                    <input
                        type="url"
                        id="org-website"
                        name="org-website"
                    />
                </div>
                <div class="form-row">
                    <label for="message"
                        >{{ page.join.label_message }}</label
                    >
                    <textarea
                        id="message"
                        name="message"
                    ></textarea>
                </div>

                <button class="btn btn-primary" type="submit">
                    {{ page.join.submit_label }}
                </button>
            </form>
        </div>
    </section>

    <!-- FINAL CTA -->
    <section class="final-cta" id="action">
        <div class="wrap">
            <p class="section-label">{{ page.final_cta.label }}</p>
            <h2 class="section-heading">{{ page.final_cta.heading }}</h2>
            <p class="section-intro">{{ page.final_cta.intro }}</p>

            <div class="cta-actions">
                <a class="btn btn-black" href="{{ page.final_cta.cta_primary_url | relative_url }}"
                    >{{ page.final_cta.cta_primary_label }}</a
                >
                <a
                    class="btn btn-primary"
                    href="{{ page.final_cta.cta_secondary_url | relative_url }}"
                    >{{ page.final_cta.cta_secondary_label }}</a
                >
            </div>

            {% include signup-form.html %}
        </div>
    </section>
</main>
