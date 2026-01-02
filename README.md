# AllenFive Website

This repository contains the source for the **AllenFive** marketing website, built with **Jekyll** and the **Minimal Mistakes** theme.  

The site runs locally for development and is deployed automatically to **GitHub Pages** via GitHub Actions.

---

## Tech Stack

- **Jekyll** (static site generator)
- **Minimal Mistakes** (Jekyll theme)
- **Ruby** (via rbenv)
- **Bundler** (dependency management)
- **GitHub Pages** (hosting)
- **GitHub Actions** (build & deploy)

---

## Repository Structure

```
.
├── _config.yml            # Jekyll configuration
├── index.md               # Homepage
├── Gemfile                # Ruby gem dependencies
├── Gemfile.lock           # Locked dependency versions
├── .ruby-version          # Ruby version for local + CI
├── assets/                # Images, favicon, etc.
├── _site/                 # Generated output (build artifact)
└── .github/workflows/
    └── pages.yml          # GitHub Actions build & deploy workflow
```

---

## Prerequisites (Local Development)

- macOS or Linux
- Ruby **3.3.x**
- Bundler
- Git

Recommended setup uses **rbenv** and Homebrew.

---

## Local Setup

### 1. Clone the repository
```bash
git clone https://github.com/<your-username>/allenfive.github.io.git
cd allenfive.github.io
```

### 2. Install Ruby (if needed)
```bash
rbenv install 3.3.6
rbenv global 3.3.6
ruby -v
```

### 3. Install Bundler
```bash
gem install bundler
```

### 4. Install dependencies
```bash
bundle install
```

### 5. Run the site locally
```bash
bundle exec jekyll serve
```

Open in your browser:
```
http://127.0.0.1:4000
```

Jekyll will automatically rebuild when files change.

---

## Deployment

Deployment is handled automatically using **GitHub Actions**.

### How it works
- On every push to `main`, GitHub Actions:
  1. Installs Ruby & dependencies
  2. Builds the Jekyll site
  3. Deploys the generated site to GitHub Pages

### GitHub Pages Settings
Make sure the repository is configured as:
```
Settings → Pages → Source: GitHub Actions
```

No manual deployment steps are required.

---

## Theme

This site uses the **Minimal Mistakes** Jekyll theme.

- Theme documentation: https://mmistakes.github.io/minimal-mistakes/
- Layouts used:
  - `single`
  - `home`

Theme configuration lives in `_config.yml`.

---

## Customization

Common places to customize:

- **Homepage content:** `index.md`
- **Site metadata:** `_config.yml`
- **Images & favicon:** `assets/`
- **Additional pages:** add new `.md` files at the repo root or in folders

---

## Notes

- The `_site/` directory is generated output and should not be edited directly.
- Local builds use the theme gem (`minimal-mistakes-jekyll`) to avoid SSL and remote theme issues.
- GitHub Actions builds from the same Gemfile to ensure parity.

---

## License

Content and configuration in this repository are proprietary unless otherwise stated.  
Third-party dependencies (Jekyll, Minimal Mistakes) are licensed under their respective open-source licenses.
