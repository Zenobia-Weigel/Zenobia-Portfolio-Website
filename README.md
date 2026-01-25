# Zenobia Portfolio Website

A modern, minimal resume and portfolio website template built with Jekyll and integrated with Pages CMS for easy content management. Deploy for free on GitHub Pages and edit your content without touching code.

## Features

- **GitHub Pages Hosting** - Free, reliable hosting with automatic SSL
- **Pages CMS Integration** - Edit your resume content through a user-friendly web interface
- **Modern Minimal Design** - Clean, professional layout that puts your content first
- **Responsive Layout** - Looks great on desktop, tablet, and mobile devices
- **Print-Friendly Stylesheet** - Generates a clean PDF when printed from the browser
- **SEO Optimized** - Proper meta tags, semantic HTML, and structured data for search engines

## Quick Start

1. **Fork or clone this repository**
   ```bash
   git clone https://github.com/Zenobia-Weigel/Zenobia-Portfolio-Website.git
   ```

2. **Enable GitHub Pages**
   - Go to your repository on GitHub
   - Navigate to Settings > Pages
   - Under "Source", select the `main` branch
   - Click Save
   - Your site will be available at `https://Zenobia-Weigel.github.io/Zenobia-Portfolio-Website/`

3. **Edit content via Pages CMS**
   - Visit [pagescms.org](https://pagescms.org)
   - Sign in with your GitHub account
   - Select your repository
   - Start editing your content

## Local Development

### Prerequisites

- Ruby 2.7 or higher
- Bundler gem

### Setup

1. Install dependencies:
   ```bash
   bundle install
   ```

2. Start the development server:
   ```bash
   bundle exec jekyll serve
   ```

3. Open your browser and visit:
   ```
   http://localhost:4000
   ```

The site will automatically rebuild when you make changes to the source files.

## Customizing Content via Pages CMS

Pages CMS provides a visual editor for your resume content without requiring any coding knowledge.

1. Go to [https://pagescms.org](https://pagescms.org)
2. Sign in with your GitHub account
3. Select your Zenobia Portfolio Website repository
4. Edit the following sections:
   - **Profile** - Your name, title, photo, about section, and social links
   - **Experience** - Work history and professional experience
   - **Education** - Academic background and certifications
   - **Skills** - Technical and professional skills by category
   - **Settings** - Theme colors and section display order

Changes are committed directly to your repository and automatically deployed via GitHub Pages.

## Customizing Content Manually

All content is stored in YAML files within the `_data/` folder. Edit these files directly to update your resume:

### `_data/profile.yml`
```yaml
name: "Your Name"
title: "Your Professional Title"
photo: "/images/profile.jpg"
about: "A brief description about yourself and your professional background."
social:
  - platform: linkedin
    url: "https://linkedin.com/in/yourprofile"
  - platform: github
    url: "https://github.com/yourusername"
  - platform: email
    url: "mailto:your.email@example.com"
```

### `_data/experience.yml`
```yaml
- company: "Company Name"
  position: "Job Title"
  start_date: "2020-01"
  end_date: "present"
  description: "Description of your role and accomplishments."
  highlights:
    - "Key achievement or responsibility"
    - "Another notable accomplishment"
```

### `_data/education.yml`
```yaml
- institution: "University Name"
  degree: "Bachelor of Science"
  field: "Computer Science"
  start_date: "2016-09"
  end_date: "2020-05"
  gpa: "3.8"
  honors:
    - "Dean's List"
    - "Magna Cum Laude"
```

### `_data/skills.yml`
```yaml
- category: "Programming Languages"
  items:
    - "Python"
    - "JavaScript"
    - "Ruby"

- category: "Frameworks"
  items:
    - "React"
    - "Rails"
    - "Django"
```

### `_data/settings.yml`
```yaml
primary_color: "#2563eb"
secondary_color: "#1e40af"
section_order:
  - profile
  - experience
  - education
  - skills
show_print_button: true
```

## Customizing Styles

To customize the visual appearance, edit the SCSS variables in `_sass/_variables.scss`:

```scss
// Colors
$primary-color: #2563eb;
$secondary-color: #1e40af;
$text-color: #1f2937;
$background-color: #ffffff;
$accent-color: #f3f4f6;

// Typography
$font-family-base: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
$font-family-heading: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
$font-size-base: 16px;
$line-height-base: 1.6;

// Spacing
$spacing-unit: 1rem;
$container-max-width: 800px;
```

## Adding a Profile Photo

1. Add your image to the `images/` folder:
   ```
   images/profile.jpg
   ```

2. Update the photo path in `_data/profile.yml`:
   ```yaml
   photo: "/images/profile.jpg"
   ```

For best results:
- Use a square image (1:1 aspect ratio)
- Recommended size: 400x400 pixels
- Supported formats: JPG, PNG, WebP

## File Structure

```
Zenobia-Portfolio-Website/
├── _config.yml          # Jekyll configuration
├── _data/               # Content data files
│   ├── profile.yml      # Personal information
│   ├── experience.yml   # Work history
│   ├── education.yml    # Education background
│   ├── skills.yml       # Skills and expertise
│   └── settings.yml     # Theme settings
├── _includes/           # Reusable HTML components
├── _layouts/            # Page templates
├── _sass/               # SCSS stylesheets
│   ├── _variables.scss  # Theme variables
│   ├── _base.scss       # Base styles
│   └── _components.scss # Component styles
├── assets/              # Compiled CSS and JS
├── images/              # Image assets
├── .pages.yml           # Pages CMS configuration
├── Gemfile              # Ruby dependencies
└── index.html           # Homepage
```

## Technologies Used

| Technology | Purpose |
|------------|---------|
| [Jekyll](https://jekyllrb.com/) | Static site generator |
| [GitHub Pages](https://pages.github.com/) | Free hosting platform |
| [Pages CMS](https://pagescms.org/) | Content management system |
| [SCSS](https://sass-lang.com/) | CSS preprocessing |

## Troubleshooting

### Build fails on GitHub Pages
- Ensure all YAML files have valid syntax
- Check the Actions tab for detailed error messages

### Changes not appearing
- GitHub Pages may take a few minutes to rebuild
- Try clearing your browser cache
- Check that changes were committed to the `main` branch

### Local server errors
- Run `bundle update` to update dependencies
- Ensure Ruby version matches the required version

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see below for details.

```
MIT License

Copyright (c) 2024

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
