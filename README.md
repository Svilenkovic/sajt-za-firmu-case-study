# Sajt za firmu

A website preparation and diagnostic site that turns technical checks into a clear plan for a business owner.

**[sajtzafirmu.com](https://sajtzafirmu.com/)** · [Bata Stanković case study](https://sajtzafirmu.com/en/examples/bata-stankovic-accounting/) · [Srpski](README.sr.md)

> [!NOTE]
> This is an independent project by D. Svilenković. The production source stays in a private repository; this public repository documents the work.

<table>
  <tr><td><b>Type</b></td><td>Website audit and preparation tool</td></tr>
  <tr><td><b>Languages</b></td><td>Serbian and English</td></tr>
  <tr><td><b>Public routes</b></td><td>24 canonical pages</td></tr>
  <tr><td><b>Role</b></td><td>Research, design, development, SEO, hosting and maintenance</td></tr>
  <tr><td><b>Stack</b></td><td>Astro, TypeScript, CSS, PHP 8.3, SQLite, nginx</td></tr>
</table>

## Purpose

Most owners know that a site feels slow or unclear, but they do not have a useful way to describe the problem. This site turns domains, pages, metadata and contact details into a readable diagnostic path before a redesign begins.

## Design direction

The visual language is a graphite diagnostic chamber with orange scan lines. Real page elements enter the scanner one by one, so the main scroll scene also explains the service.

## What I built

- A structured preparation path before design or migration
- Checks presented in language a nontechnical owner can act on
- A working site verification tool with its own isolated API account
- Contact requests stored before they enter the delivery queue
- Accessible keyboard states and an explicit alternative to animated scanning

## Release checks

Every canonical route was checked at 390, 768, 1440 and 1920 px. The release was also tested without JavaScript and with reduced motion. Live checks covered HTTPS, redirects, response headers, structured data, sitemap files, protected paths and invalid contact requests without sending test mail.

These are engineering checks, not claims about search ranking or field performance.

---

<sub>Designed and built by [D. Svilenković](https://svilenkovic.com).</sub>
