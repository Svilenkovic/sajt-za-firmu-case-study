<a href="https://sajtzafirmu.com/"><img src="media/cover.jpg" alt="Sajt za firmu, home page on a laptop and a phone" width="100%"></a>

# Sajt za firmu

Tools for owners who are about to order or fix a website: a site check, a brief, a privacy policy generator and sample texts.

**[sajtzafirmu.com](https://sajtzafirmu.com/)** · [Case study (in Serbian)](https://svilenkovic.rs/radovi/sajt-za-firmu) · [Srpski](README.sr.md)

> [!NOTE]
> My own project, not client work. The source code is private. This page describes what the site does and how it is built.

<table>
  <tr><td><b>Client</b></td><td>Own project</td></tr>
  <tr><td><b>Industry</b></td><td>Website checks and preparation for business owners</td></tr>
  <tr><td><b>Location</b></td><td>Serbia</td></tr>
  <tr><td><b>Type</b></td><td>Website with tools and a site checker</td></tr>
  <tr><td><b>My role</b></td><td>Research, design, development, SEO and hosting</td></tr>
  <tr><td><b>Stack</b></td><td>Astro 7, GSAP DrawSVG, PHP 8.3, SQLite, nginx</td></tr>
</table>

## About the project

Before a business orders a new site or fixes the old one, it usually needs three answers: what is wrong with the current site, what exactly it is ordering and which legal texts have to be on the page. Sajt za firmu has a tool for each, with no account and no email address required. The brief and the privacy policy generator run only in the browser and send nothing.

The site check is the one part that needs a server. A PHP 8.3 service opens the home page and one contact page and returns a report of 36 items in six groups, from the certificate and redirects to the company details required by the e-commerce law. A service that fetches any address a visitor types has to be careful, so before each request it resolves the name and refuses local and private addresses, and it runs in its own PHP-FPM pool without functions for starting programs.

## What I built

- A site check with 36 items in six groups, each with what to do about it
- At most twelve requests to the checked site, results cached for ten minutes in SQLite and a rate limit keyed on a hash of the IP address
- A report that also works without JavaScript: a plain form gets the same report as an HTML page
- A brief that downloads for Word or prints, and a privacy policy generator that follows Article 23 of the data protection law
- Ticks drawn with GSAP DrawSVG, loaded only when a visitor starts a check

## Results

| | Performance | Accessibility | Best practices | SEO |
| :-- | :-: | :-: | :-: | :-: |
| Mobile | 100 | 100 | 100 | 100 |
| Desktop | 100 | 100 | 100 | 100 |

PageSpeed Insights, lab test of the live site, October 2026. Security headers: 6 of 6. axe accessibility check: no violations. Structured data: `FAQPage`, `Organization`, `Person`.

## Screenshots

<table>
  <tr>
    <td width="68%" valign="top"><img src="media/desktop.webp" alt="Sajt za firmu, home page on a 1440 px screen"></td>
    <td width="32%" valign="top"><img src="media/mobile.webp" alt="Sajt za firmu, home page on a phone"></td>
  </tr>
</table>

<img src="media/inner-1.webp" alt="Site check: type an address and get a report">
<sub>Site check: type an address and get a report</sub>

---

<sub>Built by [D. Svilenković](https://svilenkovic.com).</sub>
