# Ananthu K Santhosh | Portfolio Website

A personal portfolio website for **Ananthu K Santhosh**, an aspiring Cloud & DevOps Engineer and Cloud Security enthusiast. It is built with plain HTML, CSS and JavaScript (no framework and no build step) and deployed on Vercel from GitHub.

---

## About Me

I am a final-year **BCA student (Cybersecurity specialization)** at **Marian College Kuttikkanam (Autonomous)**, 2024 to 2027, based in Kerala, India.

My main direction is **Cloud Engineering and DevOps**, with **Cybersecurity** and **IoT security** as additional strengths. I am looking for entry-level Cloud and DevOps opportunities.

### Experience

**Cybersecurity and Cloud Security Intern**, IPSR Solutions Ltd, Kottayam
May 2026 to June 2026 | 8 weeks, 240 hours

- Linux system administration
- AWS and Azure security assessment
- Cloud infrastructure hardening
- Network activity monitoring
- Secure configuration practices

### Education

BCA, Cybersecurity Specialization, Marian College Kuttikkanam (Autonomous), 2024 to 2027.

### Focus Areas

| Area | What I work on |
| --- | --- |
| Cloud | AWS (IAM, EC2, VPC, S3, RDS, CloudTrail, KMS), Microsoft Azure, Google Cloud Platform (learning) |
| DevOps | Docker, Git and GitHub, GitHub Actions, CI/CD fundamentals |
| Operating systems | Linux administration, Windows fundamentals |
| Programming | Python, Java |
| Networking | TCP/IP, subnetting, GNS3, Cisco IOS, ACLs, NAT, DHCP |
| Cybersecurity | Kali Linux, Nmap, Wireshark, Burp Suite, Metasploit (authorized lab environments only) |
| IoT and embedded security | ESP32, MQTT, CoAP, Mosquitto, Binwalk, firmware security |

The website also shows which skills are practical, which are foundational and which are still being learned, so nothing is overstated.

---

## Featured Projects

| Project | Summary | Repository |
| --- | --- | --- |
| **SecureOTA** (in progress) | Cloud-based OTA firmware security framework for IoT devices: secure firmware distribution, SHA-256 integrity checks, digital signatures, blocking unauthorized updates. | Not published yet |
| **SYN RECON** | Modular Python and Scapy tool for TCP SYN port discovery and service enumeration, tested in a Kali Linux and Metasploitable 2 lab. | [synrecon](https://github.com/ananthuksanthosh/synrecon) |
| **MEDOX** | Cloud-based multi-hospital management system (React, Node.js, Express, MySQL) deployed on AWS with JWT authentication, Helmet, rate limiting and Fail2Ban. | [medox-healthcare-platform](https://github.com/ananthuksanthosh/medox-healthcare-platform) |
| **Enterprise Network Simulation** | GNS3 enterprise network with routing between segments, NAT, DHCP and an ACL-based firewall on a Cisco 7200 router. | [enterprise-office-network-gns3](https://github.com/ananthuksanthosh/enterprise-office-network-gns3) |
| **Dockerized Python To-Do App** | Flask task manager containerized with a Dockerfile and Docker Compose. | [python-todo-docker](https://github.com/ananthuksanthosh/python-todo-docker) |
| **IoT Environmental Monitoring and Remote Control** | ESP32, DHT22 and Blynk IoT Cloud project for temperature and humidity monitoring with remote LED control. Built as a simulation in Wokwi, with no physical hardware. | LinkedIn project page |

---

## Portfolio Features

- **Editorial hero** with an oversized animated name, a floating pill navigation and rotating keywords.
- **About section** with biography and a custom illustration.
- **Expertise and Tools cards**: every technology category opens a detail panel showing practical, foundational and learning levels.
- **Featured Projects**: six project cards that open detailed project panels (overview, objective, features, technologies, implementation, what I learned, links).
- **Experience and education timeline** with the internship details.
- **FAQ accordion** with smooth open and close animation.
- **Contact form** that sends messages through Formspree.
- **CLI mode**: a Linux-style terminal opened with the floating `>_ CLI` button.
- **Fully responsive** from phones to large desktops, with a scroll progress bar, back-to-top button and mobile menu.

---

## Techniques Used

### Front end

- **Semantic HTML5** structure with landmarks (`nav`, `header`, `section`, `footer`) and labelled controls.
- **CSS custom properties** for the colour system (cream, pale yellow, black, white, grey) and shared easing.
- **Fluid sizing with `clamp()`**, so headings, body text, spacing and the hero name scale smoothly without many breakpoints.
- **CSS Grid and Flexbox** for the card grids, the About layout and the contact form.
- **Content width control**: sections share one max content width (about 1280px) with responsive side padding, while backgrounds stay full width.
- **Mobile-first details**: 16px form inputs to prevent zoom on phones, safe-area insets for notched devices, touch-friendly buttons.

### Animation

- **Staggered hero name reveal** with CSS keyframes.
- **Scroll reveals** using `IntersectionObserver` (fade-up with staggered delays), so no animation library is needed.
- **Hover interactions**: lifting cards, zooming thumbnails, moving arrows.
- **Animated accents**: moving gradient, dashed lines and a rotating keyword ticker built with CSS only.
- **`prefers-reduced-motion` support** disables animations for visitors who ask for less motion.

### JavaScript (vanilla, no dependencies)

- **Data-driven rendering**: skills, projects and project details live in small JavaScript data arrays and are rendered into cards and panels, so adding a project means adding one object.
- **Accessible modal dialogs**: `role="dialog"`, focus moved into the dialog and restored on close, Tab key trapped inside, Escape and backdrop click to close, background scroll locked.
- **Accessible accordion** with `aria-expanded` and animated height using CSS grid rows.
- **Active navigation highlighting** with a second `IntersectionObserver`.
- **Scroll progress bar** and **back-to-top** button.

### CLI terminal (built from scratch)

- A small **terminal emulator** with a virtual file system (`ls`, `cd`, `cat`, `pwd`).
- Commands: `help`, `whoami`, `about`, `skills`, `projects`, `project <n>`, `experience`, `education`, `certs`, `achievements`, `contact`, `links`, `resume`, `neofetch`, `echo`, `date`, `history`, `clear`, `exit`.
- **Tab autocomplete**, **arrow-key history** and **Ctrl+L** to clear.
- Reads the same data as the rest of the site, so content stays in sync.
- **Safe output**: anything a visitor types is escaped before it is shown.

### Contact form

- Sends data with `fetch` as `application/x-www-form-urlencoded` to a **Formspree** endpoint, with a normal HTML `POST` as the fallback.
- **Client-side validation** with inline error messages and `aria-invalid`.
- Submit button is **disabled while sending** to stop duplicate submissions.
- **Success and error messages** are announced with `aria-live`, and the form clears after success.
- A hidden **honeypot field** helps filter bots. No `mailto:` and no API keys are used in the page.

### Performance and SEO

- No frameworks, no build step and no JavaScript libraries.
- A single external dependency: **Google Fonts** (Space Grotesk).
- Images are sized for the layout, and the large About image is cached through `vercel.json`.
- Page title, meta description and Open Graph tags are set for search and link previews.

---

## Project Structure

```
portfolio-site/
├── index.html                    # the whole website (HTML, CSS and JavaScript)
├── assets/
│   └── about-infographic.png     # About section illustration
├── Resume.pdf                    # add your resume here (Download Resume button)
├── vercel.json                   # Vercel settings (clean URLs, asset caching)
├── .github/
│   ├── workflows/
│   │   └── ci.yml                # GitHub Actions workflow (CI checks)
│   └── scripts/
│       └── check_site.py         # checks run by the workflow
├── .gitignore
└── README.md
```

---

## CI/CD Pipeline

This project uses a Git-based CI/CD flow with **GitHub Actions** (CI) and **Vercel** (CD).

### Continuous Integration: `.github/workflows/ci.yml`

The workflow is a YAML file that GitHub Actions runs automatically on every push to `main` and on every pull request.

```yaml
name: CI

on:
  push:
    branches: [main]
  pull_request:

jobs:
  validate:
    name: Validate website
    runs-on: ubuntu-latest
    steps:
      - name: Check out code
        uses: actions/checkout@v4

      - name: Set up Node.js
        uses: actions/setup-node@v4
        with:
          node-version: 20

      - name: Run site checks
        run: python3 .github/scripts/check_site.py
```

The script `.github/scripts/check_site.py` checks that:

- the required files exist (`index.html`, `vercel.json`, the About image)
- `vercel.json` is valid JSON
- the page has a title, language, viewport and description tags, and the Formspree form action
- every local asset the page references exists
- all inline JavaScript has valid syntax (`node --check`)
- `Resume.pdf` is present (shown as a warning, not a failure)

If a check fails, the commit or pull request shows a red cross in GitHub, so the problem is visible before the change is merged.

### Continuous Deployment: Vercel

Vercel is connected to the GitHub repository. Every push to `main` is deployed to production automatically, and pull requests or other branches get their own preview link. Earlier deployments are kept, so a rollback takes one click in the Vercel dashboard.

```
git push  ->  GitHub Actions (checks)  ->  Vercel (deploy)  ->  live site
```

Vercel deploys through its own GitHub integration, separate from the workflow above.

---

## Run Locally

No installation is needed. Open `index.html` in a browser.

For a local server instead, run `python3 -m http.server 8000` in this folder and visit `http://localhost:8000`.

## Deploy (GitHub + Vercel)

1. Push this folder to a GitHub repository.
2. On [vercel.com](https://vercel.com) choose **Add New, then Project**, and import the repository.
3. Set **Framework Preset** to **Other**. Leave Build Command and Output Directory empty.
4. Click **Deploy**.

Every `git push` to `main` redeploys the live site automatically, and pushes to other branches or pull requests get a preview link. Vercel also keeps every earlier deployment, so you can roll back in one click.

## Customize

- **Add a project:** add an entry to the `pj` array (card) and the `D` array (detail panel) in `index.html`.
- **Add a skill category:** edit the `T` array.
- **Contact form:** the Formspree endpoint is in the `action` attribute of the `#cf` form. Submissions go to the recipient set in your Formspree dashboard.
- **Resume:** place `Resume.pdf` next to `index.html`.

---

## Contact

- Email: ananthuksanthosh2006@gmail.com
- GitHub: [github.com/ananthuksanthosh](https://github.com/ananthuksanthosh)
- LinkedIn: [linkedin.com/in/ananthu-k-santhosh](https://www.linkedin.com/in/ananthu-k-santhosh)
- Location: Kerala, India

Thank you for visiting my portfolio.
