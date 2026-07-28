# Hello World (Vulnerable)

A minimal Hello World React app used as a **test target** for SBOM / code-connector vulnerability scanning.

> ⚠️ **Do not use in production.** The dependencies in this project are pinned to old versions with well-known published CVEs *on purpose*, so that an SBOM scanner has something to find.

## What's in here

- `package.json` / `package-lock.json` — dependency manifest and lockfile with pinned, vulnerable versions
- `src/` — a tiny React "Hello World" component
- `public/index.html` — HTML entry point

## Intentionally vulnerable dependencies

| Package | Version | Example CVE / advisory |
| --- | --- | --- |
| lodash | 4.17.4 | CVE-2019-10744 (prototype pollution) |
| minimist | 1.2.0 | CVE-2021-44906 (prototype pollution) |
| axios | 0.18.0 | CVE-2020-28168 (SSRF) |
| node-fetch | 2.6.0 | CVE-2020-15168 (DoS) |
| ejs | 2.6.1 | CVE-2022-29078 (RCE) |
| serialize-javascript | 1.4.0 | CVE-2020-7660 (RCE) |
| handlebars | 4.0.11 | CVE-2019-20920 (RCE) |
| marked | 0.3.6 | CVE-2017-16114 (ReDoS) |

## Run it

```bash
npm install
npm start
```
