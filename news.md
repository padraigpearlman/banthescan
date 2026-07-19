---
title: Media Coverage | Ban the Scan
layout: default
nav: media
description: News coverage of facial recognition and biometric surveillance harms
  in New York, from wrongful arrests to corporate overreach to the Ban the Scan campaign.
hero:
  eyebrow: Media Coverage
  heading: Reporters have been paying attention.
  sub: From corporate overreach to the bills themselves, facial recognition in New
    York has drawn sustained national and local coverage since 2019. Here's a closer
    look at what's been reported, and why it matters.
  stat_1_label: Media Mentions
  stat_2_value: 2019&ndash;2026
  stat_2_label: Coverage Span
  stat_3_value: 15+
  stat_3_label: National &amp; Local Outlets
real_stories_pointer:
  label: Real Stories
  heading: Looking for the human stories?
  intro: Robert Williams, Nijeer Parks, Porcha Woodruff, and others were wrongfully
    arrested because of facial recognition misidentification. Their stories are on
    our About page.
  cta_label: Read Their Stories
coverage:
  label: Full Coverage
  heading: Browse coverage by topic.
  corporate_heading: Corporate &amp; Retail Surveillance
  policy_heading: Policy &amp; Legislation
  research_heading: Research &amp; Data
  read_label: Read
press:
  label: Press
  heading: Working on a story?
  intro: Reporters can reach our press team directly for data, interviews, and documentation
    of specific cases.
  cta_label: Contact Our Press Team
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

            <div class="stat-strip">
                <div class="stat-chip">
                    <div class="num">{{ site.news | size }}+</div>
                    <div class="label">{{ page.hero.stat_1_label }}</div>
                </div>
                <div class="stat-chip">
                    <div class="num">{{ page.hero.stat_2_value }}</div>
                    <div class="label">{{ page.hero.stat_2_label }}</div>
                </div>
                <div class="stat-chip">
                    <div class="num">{{ page.hero.stat_3_value }}</div>
                    <div class="label">{{ page.hero.stat_3_label }}</div>
                </div>
            </div>
        </div>
    </section>

    <div class="tape-divider" aria-hidden="true"></div>

    <!-- REAL STORIES POINTER -->
    <section class="bridge-cta" id="real-stories-pointer">
        <div class="wrap">
            <p class="section-label">{{ page.real_stories_pointer.label }}</p>
            <h2 class="section-heading">{{ page.real_stories_pointer.heading }}</h2>
            <p class="section-intro">{{ page.real_stories_pointer.intro }}</p>
            <div class="bridge-actions">
                <a class="btn btn-yellow" href="{{ '/about.html' | relative_url }}#real-stories"
                    >{{ page.real_stories_pointer.cta_label }}</a
                >
            </div>
        </div>
    </section>

    <!-- FULL COVERAGE -->
    <section class="news" id="coverage">
        <div class="wrap">
            <p class="section-label">{{ page.coverage.label }}</p>
            <h2 class="section-heading">{{ page.coverage.heading }}</h2>

            <div class="coverage-category" id="corporate-surveillance">
                <h3>{{ page.coverage.corporate_heading }}</h3>
                <div class="news-grid">
                    {% assign corporate_news = site.news | where_exp: "n", "n.categories contains 'corporate-surveillance'" | sort: "date" | reverse %}
                    {% for item in corporate_news %}
                    <article class="news-card">
                        <div class="outlet">{{ item.outlet }}</div>
                        <h3>{{ item.headline }}</h3>
                        <div class="news-card-foot">
                            <div class="date">{{ item.display_date }}</div>
                            <a class="card-link" href="{{ item.url }}" target="_blank" rel="noopener">{{ page.coverage.read_label }}</a>
                        </div>
                    </article>
                    {% endfor %}
                </div>
            </div>

            <div class="coverage-category" id="policy-legislation">
                <h3>{{ page.coverage.policy_heading }}</h3>
                <div class="news-grid">
                    {% assign policy_news = site.news | where_exp: "n", "n.categories contains 'policy-legislation'" | sort: "date" | reverse %}
                    {% for item in policy_news %}
                    <article class="news-card">
                        <div class="outlet">{{ item.outlet }}</div>
                        <h3>{{ item.headline }}</h3>
                        <div class="news-card-foot">
                            <div class="date">{{ item.display_date }}</div>
                            <a class="card-link" href="{{ item.url }}" target="_blank" rel="noopener">{{ page.coverage.read_label }}</a>
                        </div>
                    </article>
                    {% endfor %}
                </div>
            </div>

            <div class="coverage-category" id="research-data">
                <h3>{{ page.coverage.research_heading }}</h3>
                <div class="news-grid">
                    {% assign research_news = site.news | where_exp: "n", "n.categories contains 'research-data'" | sort: "date" | reverse %}
                    {% for item in research_news %}
                    <article class="news-card">
                        <div class="outlet">{{ item.outlet }}</div>
                        <h3>{{ item.headline }}</h3>
                        <div class="news-card-foot">
                            <div class="date">{{ item.display_date }}</div>
                            <a class="card-link" href="{{ item.url }}" target="_blank" rel="noopener">{{ page.coverage.read_label }}</a>
                        </div>
                    </article>
                    {% endfor %}
                </div>
            </div>
        </div>
    </section>

    <!-- PRESS CONTACT -->
    <section class="bridge-cta" id="press">
        <div class="wrap">
            <p class="section-label">{{ page.press.label }}</p>
            <h2 class="section-heading">{{ page.press.heading }}</h2>
            <p class="section-intro">{{ page.press.intro }}</p>
            <div class="bridge-actions">
                <a
                    class="btn btn-yellow"
                    href="mailto:info@banthescan.org"
                    >{{ page.press.cta_label }}</a
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
