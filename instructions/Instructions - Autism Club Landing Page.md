# Instructions - מסוגלות: Landing Page for Autism Sports-Social Club

## Goal

Transform the existing Safarov & Sagi fitness landing page into a **Hebrew, RTL landing page** for **מסוגלות** (Mesugalut) - a sports-social club / activity framework designed for autistic teenagers.

The page has **two audiences** that must be balanced:
- **Primary:** Parents - who discover it first, evaluate it, and register their kids. They need trust, clarity, professionalism, and a sense of emotional safety.
- **Secondary:** Teens themselves - who need to feel like this is their kind of place, not a medical program. Cool, energetic, not patronising.

The design should feel **modern and professional but human** - no AI slop aesthetic, no overly clinical feel, no generic disability-charity clichés.

---

## Project Details (Confirmed)

1. **Project name:** מסגרת ספורטיבית וגיבושית לתקשורת ותנועה (מ.ס.וג.ל.ו.ת)
2. **Activities offered:** Gathering in a specific gym (Profit Bat-Yam) for resistance exercise, cardio, and games. Focus on exposure to a commercial gym, learning communication (grabbing attention, sharing machines, boundaries, hand gestures, logging workouts, timing with stopwatches). Also exposure to hobbies (drumming pad, guitar, AI games, art, video games).
3. **Location:** Bat-Yam, Israel (Profit Gym).
4. **Who runs it:** Roman Safarov (רומן ספרוב) - personal trainer, natural bodybuilder, 6 years working with autistic people. Connects training with health/strength. Hobbyist (drummer, gamer).
5. **Registration / CTA goal:** Contact form. Possible WhatsApp group placeholder. May be subsidized by the city administration later.
6. **Social media:** WhatsApp group placeholder for now.
7. **Stats / trust signals:** Removed / hidden for now.
8. **Testimonials:** Removed / hidden for now.
9. **Google Sheet backend URL:** Placeholder needed; the user will create a new sheet for this project.
10. **Color palette direction:** Modern & clean (navy/teal/white) - already implemented.
11. **Fonts:** Rubik + Assistant (already implemented).
12. **Description:** Details are confirmed from `Mesugalut Description.md`.

---

## Files Involved

| File | Action |
|------|--------|
| `index.html` | Full rewrite - all content replaced, structure restructured |
| `assets/styles.css` | Full rewrite - palette, fonts, and branding updated |
| `assets/coach1.jpg` / `coach2.jpg` | Will be replaced with generated images or placeholders |
| `blog.html` / `competition.html` | Will be left untouched (not part of scope) |

---

## Proposed Page Structure

### 1. Navigation
- Logo: **מסוגלות** (or project name)
- Links: אודות | פעילויות | הצוות | הרשמה
- CTA button: **להרשמה** / **צור קשר**

### 2. Hero (Dark section - full viewport)
- Label badge: e.g. `מסגרת ספורט וחברה לנוער אוטיסטי`
- Big headline split across two lines:
  - Line 1: bold, white - e.g. `מגרש לכולם.`
  - Line 2: accent color - e.g. `מקום שנבנה בשבילך.`
- Sub-copy: one punchy line for teens + one reassuring line for parents
- Two CTAs: `להרשמה` (primary) + `מה אנחנו עושים ↓` (ghost)
- Right side: photo cards (activity/teens - generated imagery)

### 3. "About / How It Works" (White section)
- Section title: `איך זה עובד` / `מה זה מסוגלות`
- 3 pillar cards:
  - **ספורט** - פעילות גופנית מובנית ומהנה, מותאמת לכל רמה
  - **חברה** - קבוצה קבועה, חברים אמיתיים, שייכות
  - **ביטחון** - סביבה בטוחה, צוות מיומן, התקדמות בקצב שלך

### 4. Activities (Dark section)
- Replaces "Services"
- Each activity card: sport name tag, title, description, benefits list

### 5. Team (White section)
- Replaces "Coaches"
- Photo + name + role + bio for each team member
- Generated images if no real photos available

### 6. Trust / Stats (Dark section)
- Replaces "Results"
- Trust numbers (e.g. teens served, sessions/week, years running)
- Or parent testimonial quotes if stats not available

### 7. Registration / Contact (Accent color section)
- Form fields adapted for parents: שם ההורה, שם הנוער, גיל הנוער, טלפון
- CTA copy: `רוצים להצטרף? נשמח לשמוע`
- Same Google Sheets backend (no-cors pattern preserved)

### 8. Footer
- Brand name + tagline
- Instagram + WhatsApp social links
- Copyright

---

## Design Direction (Default Proposal)

| Token | Value | Rationale |
|-------|-------|-----------|
| Background (dark sections) | `#0b0f1a` deep navy-black | Warmer than stark black; sporty and modern |
| Background (light sections) | `#f6f5f2` warm off-white | Same warmth as original |
| Accent color | TBD - blue (`#2D9CDB`) or teal | Trustworthy, energetic, distinct from the orange fitness page |
| Heading font | **Rubik** | Excellent Hebrew support, rounded and professional |
| Body font | **Assistant** | Clean, highly readable Hebrew |

> [!NOTE]
> Aesthetic target: **sporty but grounded** - not childlike, not clinical. Think Nike Israel meets a youth social program. No neon, no gradients unless requested.

---

## Risks / Edge Cases

- **Font:** Bebas Neue (used in original) has zero Hebrew support - must switch to Rubik or similar.
- **Images:** Will use AI-generated placeholder images for hero and team sections. Real photos can be swapped in later.
- **Form field names:** Must be updated to match new audience (parent + teen info). If reusing the same Google Sheet, column headers need updating there too.
- **Teen vs. parent tone:** Two registers required in the copy - will be addressed once description content is available.
- **RTL bullet arrows:** `←` arrows on list items should stay correct in RTL, but will be verified after build.

---

## Troubleshooting Log

*(Append here if anything changes during implementation)*
