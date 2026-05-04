# 🚀 Portfolio Website

A clean, responsive, and beginner-friendly personal portfolio website built with **pure HTML & CSS** — no frameworks, no libraries. Designed to be deployed on **GitHub Pages** for free.

---

## 📁 Project Structure

```
portfolio-site/
│
├── index.html          ← Home page (hero + projects)
├── about.html          ← About page (bio + skills)
├── contact.html        ← Contact page (form)
│
├── styles/
│   └── main.css        ← All CSS styles for the entire site
│
├── images/             ← Put your photos and project screenshots here
│   └── (empty)         ← e.g. profile.jpg, project1.png
│
└── README.md           ← This file!
```

### What each file does

| File | Purpose |
|---|---|
| `index.html` | The home page — first thing visitors see. Contains hero section and project cards. |
| `about.html` | About page — your story, background, and skill progress bars. |
| `contact.html` | Contact page — info cards and a validated contact form. |
| `styles/main.css` | **One** stylesheet used by all three pages. Organised with numbered comments. |
| `images/` | Folder for your profile photo and project screenshots. |

---

## ✨ Features

- **3-page website** — Home, About, Contact
- **Responsive design** — mobile-first with CSS media queries
- **Hamburger menu** — appears on screens ≤ 767px
- **CSS Grid & Flexbox** — modern layout techniques
- **Project cards** — showcase your work with tech tags
- **Skill progress bars** — animated with CSS `@keyframes`
- **Contact form** — client-side validation with JavaScript
- **Semantic HTML** — uses `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`
- **No external dependencies** — only Google Fonts (for typography)

---

## 🛠️ Setup Instructions (Open Locally)

You don't need to install anything to run this project locally.

### Option 1: Open directly in browser

1. Download or clone this project to your computer
2. Open the `portfolio-site/` folder
3. Double-click `index.html`
4. It opens in your default browser — done! ✅

### Option 2: Use VS Code Live Server (recommended)

This gives you **auto-refresh** when you save changes.

1. Install [Visual Studio Code](https://code.visualstudio.com/)
2. Install the **Live Server** extension (search in VS Code Extensions tab)
3. Open the `portfolio-site/` folder in VS Code
4. Right-click `index.html` → **"Open with Live Server"**
5. Your site opens at `http://127.0.0.1:5500` and auto-refreshes on save

---

## 🎨 Customisation Guide

Here's exactly what to change to make this portfolio yours:

### 1. Update your name

Open all three HTML files and replace:
- `Alex<span>.</span>` in the navbar → your name
- `Alex Johnson` in headings and footer → your name

### 2. Update your bio (about.html)

Find the `about-text` section and rewrite the `<p>` paragraphs with your own story.

### 3. Update the stats (about.html)

```html
<span class="stat-number">2+</span>    ← change the number
<span class="stat-label">Years coding</span>  ← change the label
```

### 4. Update skill bars (about.html)

Change the `width` values and percentages:

```html
<div class="skill-bar-fill" style="width: 90%;"></div>
```

Also update the text labels and `aria-valuenow` attributes.

### 5. Add your projects (index.html)

For each project card, update:
- The emoji/background gradient
- The title, description, and tech tags
- The `href` link to point to your project or GitHub repo

```html
<div class="project-card-image" style="background: linear-gradient(135deg, #667eea, #764ba2);">
  🌦️   ← your emoji
</div>
<h3 class="project-card-title">Weather Dashboard</h3>  ← your project name
<p class="project-card-desc">...</p>                    ← your description
<a href="https://github.com/you/project">View Project →</a>  ← your link
```

### 6. Update contact info (contact.html)

Replace the placeholders:

```html
<a href="mailto:alex@example.com">alex@example.com</a>   ← your email
<span>New York City, USA</span>                           ← your location
<a href="https://github.com/yourusername">...</a>         ← your GitHub
<a href="https://linkedin.com/in/yourusername">...</a>    ← your LinkedIn
```

### 7. Add a real profile photo

Place your photo in the `images/` folder (e.g. `profile.jpg`), then in `about.html` replace:

```html
<div class="about-avatar">🙂</div>
```

with:

```html
<img src="images/profile.jpg" alt="Your Name" class="about-avatar" />
```

Add this CSS for a round image:

```css
img.about-avatar {
  border-radius: 50%;
  object-fit: cover;
}
```

### 8. Make the contact form actually send emails

The form currently only shows a success message (no backend). To make it send real emails:

1. Sign up at [Formspree.io](https://formspree.io) (free)
2. Create a form and get your unique endpoint URL
3. Replace the `<form>` tag:

```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

4. Remove the `id="contactForm"` and the JS validation (Formspree handles submission)

### 9. Change colours

In `styles/main.css`, at the top you'll find CSS variables:

```css
:root {
  --color-accent: #e85d26;   /* ← Change this to any colour you like */
  --color-primary: #0d1b4b;  /* ← Change the dark navy colour        */
}
```

Changing `--color-accent` updates **every** button, link, and highlight automatically.

---

## 🌐 Deployment on GitHub Pages

GitHub Pages hosts static websites for **free**. Follow these steps:

### Step 1 — Create a GitHub account

Go to [github.com](https://github.com) and sign up if you haven't already.

### Step 2 — Create a new repository

1. Click the **+** button → **New repository**
2. Name it: `your-username.github.io` (replace with your actual GitHub username)  
   *(e.g. `alexjohnson.github.io`)*
3. Set visibility to **Public**
4. Click **Create repository**

> 💡 Naming it `username.github.io` makes it your "root" GitHub Pages site, accessible at `https://username.github.io`

### Step 3 — Upload your files

**Option A: Using GitHub website (easiest)**

1. Open your new repository on GitHub
2. Click **"uploading an existing file"**
3. Drag and drop ALL your project files and folders
4. Click **Commit changes**

**Option B: Using Git command line**

```bash
# Navigate to your project folder
cd portfolio-site

# Initialize a Git repository
git init

# Add all files to staging
git add .

# Make your first commit
git commit -m "Initial commit: portfolio website"

# Connect to GitHub (replace YOUR-USERNAME)
git remote add origin https://github.com/YOUR-USERNAME/YOUR-USERNAME.github.io.git

# Push your code to GitHub
git push -u origin main
```

### Step 4 — Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** tab
3. Scroll down to **Pages** in the left sidebar
4. Under **Source**, select **Deploy from a branch**
5. Choose branch: **main** | folder: **/ (root)**
6. Click **Save**

### Step 5 — Visit your live site 🎉

After 1–2 minutes, your site will be live at:

```
https://your-username.github.io
```

> ⏳ It can take up to 10 minutes for the first deployment. Refresh the Settings > Pages page to see the live URL.

---

## 🔄 Making Updates

After your site is live, any future changes are simple:

1. Edit your files locally
2. Save the changes
3. Push to GitHub:

```bash
git add .
git commit -m "Update: added new project card"
git push
```

GitHub Pages will automatically redeploy within a minute or two.

---

## 🧠 What You Learned Building This

If you worked through this project, here's what you practised:

- **HTML**: Semantic elements, forms, accessibility attributes
- **CSS**: Custom properties, Flexbox, Grid, media queries, animations
- **Responsive Design**: Mobile-first approach, breakpoints
- **JavaScript**: DOM manipulation, event listeners, form validation
- **Git & GitHub**: Version control and static hosting
- **Web Accessibility**: ARIA labels, semantic markup, focus management

---

## 📚 Resources to Keep Learning

- [MDN Web Docs](https://developer.mozilla.org) — The best HTML/CSS/JS reference
- [CSS Tricks](https://css-tricks.com) — Great guides on Flexbox and Grid
- [The Odin Project](https://www.theodinproject.com) — Free full-stack curriculum
- [freeCodeCamp](https://www.freecodecamp.org) — Free interactive coding lessons
- [Formspree](https://formspree.io) — Add a backend to your contact form for free

---

## 📄 License

This project is open source and free to use. Customise it however you like!

---

*Made with ❤️ and a lot of `<div>` tags*
