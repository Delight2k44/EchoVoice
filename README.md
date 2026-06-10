# EchoSafe — Protect. Connect. Empower.
> Community-powered safety infrastructure for South Africa

---

## What Is EchoSafe?

EchoSafe is a mobile safety platform built specifically to address Gender-Based Violence (GBV) in South Africa. It combines real-time crisis response, child protection, verified community alerts, and GBV education into a single, accessible platform — designed to work on low-end Android devices, in areas with no internet, and in the most dangerous moments when every second counts.

**This is not another panic button. This is safety infrastructure.**

---

## The Four Pillars

### 1. Crisis SOS
- Triple power-button press triggers silent SOS — screen off, no app interaction needed
- AI confirms real emergency vs accidental press (motion + audio + press pattern)
- Auto-records audio and video, encrypted and timestamped
- Broadcasts via Bluetooth mesh to EchoSafe users within 60–100 metres — **no internet required**
- Pushes evidence to encrypted cloud in real time — phone destroyed = evidence still exists
- Responders see distance, direction, and live audio feed
- Every responder confirmation logged as a timestamped witness in the evidence file

### 2. Guardian Zone (Child Safety)
- Parents define safe zones on a map (home, school, church, after-care)
- Child's phone exits zone → parent and school instantly alerted
- School confirms child is safe but without phone → stolen/lost flag raised automatically + SAPS notified
- Runs on basic Android smartphones with minimal data

### 3. Community Awareness & Missing Persons
- Only verified community leaders can push alerts (ward councillors, principals, neighbourhood watch)
- Missing persons reports require photo + description + last known location before publishing
- Duplicate reports auto-detected and merged
- Resolved alerts officially closed — ends cycle of outdated unverified social media posts

### 4. GBV Learning Platform
- GBV awareness, legal rights, survivor support — validated by GBV organisations
- 100% offline accessible
- Gamified modules with shareable certificates
- Corporate and government sponsors can fund branded content modules

---

## Files in This Package

```
EchoSafe/
│
├── EchoSafe_Website.html          # Static website — open in any browser
│
├── EchoSafe_Pitch_Document.pdf    # Full investor pitch & business plan (PDF)
│
├── SafeNet_SA_Business_Plan.docx  # Full business plan (Word document)
│
└── README.md                      # This file
```

---

## Website — How to Use

### Opening the Website
1. Download `EchoSafe_Website.html`
2. Open it in any web browser (Chrome, Firefox, Edge, Safari)
3. No server needed — it runs entirely as a static file

### Replacing the Placeholder Images
The website currently uses temporary Unsplash images. To replace them with your own:

**Hero Background (full-page image behind the headline):**
```html
<!-- Find this line in the CSS section (~line 91): -->
background-image: url('https://images.unsplash.com/photo-...');

<!-- Replace with your own photo: -->
background-image: url('your-hero-photo.jpg');
```

**Community Impact Cards (3 photos):**
```html
<!-- Schools photo — find: -->
<img src="https://images.unsplash.com/photo-1497486751825..." .../>
<!-- Replace src with: "your-schools-photo.jpg" -->

<!-- Community photo — find: -->
<img src="https://images.unsplash.com/photo-1582213782179..." .../>
<!-- Replace src with: "your-community-photo.jpg" -->

<!-- Campaign photo — find: -->
<img src="https://images.unsplash.com/photo-1559027615-cd4628..." .../>
<!-- Replace src with: "your-campaign-photo.jpg" -->
```

**Team Photos (3 portraits):**
```html
<!-- Find the 3 team <img> tags and replace each src with your photo filenames -->
<img src="https://images.unsplash.com/photo-1531123897727..." .../>
<img src="https://images.unsplash.com/photo-1507003211169..." .../>
<img src="https://images.unsplash.com/photo-1573497019940..." .../>
```

> **Important:** Put your image files in the **same folder** as `EchoSafe_Website.html`  
> **Supported formats:** `.jpg` `.jpeg` `.png` `.webp`  
> **Recommended sizes:**
> - Hero: 1920 × 1080px (landscape)
> - Impact cards: 800 × 440px (landscape)
> - Team portraits: 400 × 520px (portrait, face near the top)

### Updating Team Names and Roles
Search the HTML file for `"Your Name Here"` and replace with actual names, roles, and bios.

### Updating Impact Numbers
Search for the `impact-num` class values (12, 38, 6) and update as your real numbers grow.

---

## Website Sections (in order)

| Section | Description |
|---|---|
| **Navigation** | Fixed top bar with smooth scroll links |
| **Hero** | Full-screen background image with headline and CTA buttons |
| **Problem Stats** | 4 animated stat cards with real GBV data from Stats SA |
| **Mission & Vision** | Spinning SDG globe + mission, vision, values cards |
| **Services** | 6 service cards covering all four pillars + enterprise + schools |
| **Community Impact** | 4 cards with photos showing real-world work done |
| **Team** | 3 portrait cards for team members |
| **Donation** | Animated progress ring (goal: 50 schools) + donation amounts |
| **Footer** | Links, SDG badges, contact info |

---

## Replacing Donation Amounts

Find the `.donate-amounts` section in the HTML and update the labels and logic:

```html
<div class="amount-btn active" onclick="selectAmount(this)">R 85 — One Learner</div>
<div class="amount-btn" onclick="selectAmount(this)">R 500 — One Responder</div>
<div class="amount-btn" onclick="selectAmount(this)">R 2 000 — One Session</div>
<div class="amount-btn" onclick="selectAmount(this)">R 10 000 — One School Term</div>
```

To connect real payments, replace the `handleDonate()` function in the `<script>` section with your payment gateway integration (PayFast, Peach Payments, PayGate, etc.).

---

## Updating the Donation Progress Ring

The ring currently shows 12 of 50 schools (24%). To update it, find this line in the JavaScript:

```javascript
// Current: 12/50 = 24%
const target = Math.round(754 * 12/50);
```

Change `12` to your current number of schools, and `50` to your goal.

Also update the label:
```html
<p class="ring-label">Help us reach <strong>50 schools</strong> ... Currently at 12 schools.</p>
```

---

## Revenue Model Summary

| Stream | Year 1 Target | Model |
|---|---|---|
| Freemium App | R 600 000 | Free core + R49/month premium |
| Guardian Zone — Schools | R 1 000 000 | R85/learner/year |
| Enterprise GBV Packages | R 1 000 000 | R85K corporate / R45K municipal |
| Government Data (Y2+) | R 480 000 | POPIA-compliant anonymised reports |
| Grants | R 400 000 | GBVF Fund, NLC, SEDA, EU |
| **Total Year 1** | **R 3 000 000** | |

---

## Funding Ask

**R 4 500 000 Seed Round — 18-month runway**

| Allocation | Amount | % |
|---|---|---|
| Product Development | R 1 800 000 | 40% |
| Sales & Partnerships | R 900 000 | 20% |
| Marketing & Community | R 675 000 | 15% |
| Operations & Legal | R 450 000 | 10% |
| Team (Founders + Core) | R 675 000 | 15% |

**Series A target:** R 18 million at month 18 — anchored by 200 000 active users and 60 school contracts.

---

## Key Statistics (Stats SA / SAPS 2024)

- **5 578** women killed between April 2023 – March 2024 (33.8% increase in femicide)
- **Every 3 hours** a woman is killed by an intimate partner in South Africa
- **95%** of rape cases never reach a police station
- **26 000+** child abuse cases reported in 2024/25 financial year
- South Africa's femicide rate is **5× the global average**

---

## Contact

| | |
|---|---|
| **Email** | info@echosafe.co.za |
| **Website** | www.echosafe.co.za |
| **Location** | Johannesburg, South Africa |
| **Registration** | NPO Registration pending · Section 18A approval pending |

---

## Competitive Advantage

EchoSafe is the **only** solution in South Africa that combines:

-  Works without internet (Bluetooth mesh)
-  Discreet trigger (screen-off power button)
-  Community mesh broadcast (60–100m radius)
-  Auto tamper-proof evidence recording
-  Child safe-zone protection (Guardian Zone)
-  AI false alert detection
-  Verified missing persons alerts
-  GBV learning platform

No existing competitor — Namola, GRIT, Kwanele, or the Gauteng e-Panic Button — offers more than two of these features.

---

## SDGs Addressed

| SDG | Goal | How EchoSafe Contributes |
|---|---|---|
| **SDG 5** | Gender Equality | Direct GBV crisis response and evidence tools |
| **SDG 16** | Peace, Justice & Strong Institutions | Community safety infrastructure and legal-grade evidence |
| **SDG 4** | Quality Education | Offline GBV learning platform |
| **SDG 3** | Good Health & Wellbeing | Survivor support and mental health awareness content |
| **SDG 11** | Sustainable Cities & Communities | Community-powered neighbourhood safety networks |

---

*EchoSafe — Protect. Connect. Empower.*  
*Built with purpose in South Africa 🇿🇦*
