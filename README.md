# Andrew Jenkins - Portfolio Website

A modern, multi-page static portfolio website showcasing platform engineering expertise, AI systems architecture, and technical leadership. Built for Staff/Principal Platform Engineering roles with emphasis on force multiplication and infrastructure impact.

🌐 **Live Site**: [andrewajenkins.com](https://andrewajenkins.com)

## Overview

This portfolio demonstrates 8 years of remote platform engineering experience through detailed case studies, blog posts, and project showcases. The site emphasizes measurable impact, technical depth, and force-multiplier achievements.

### Key Features

- **Multi-Page Architecture**: Homepage, Projects, About, Blog, and detailed Case Studies
- **Blog with Technical Content**: 3 comprehensive blog posts on platform engineering, RAG systems, and knowledge codification
- **Interactive Diagrams**: Mermaid diagrams converted to SVG with collapsible source code
- **SEO Optimized**: Complete Open Graph tags, Twitter Cards, structured data (JSON-LD), sitemap.xml
- **Responsive Design**: Mobile-first Tailwind CSS implementation
- **Analytics**: Google Analytics integration across all pages
- **Performance**: Static HTML/CSS/JS with CDN-hosted dependencies

## Tech Stack

- **Framework**: Static HTML5 with semantic markup
- **Styling**: Tailwind CSS 3.x (via CDN)
- **Typography**: Inter font family from Google Fonts
- **Diagrams**: Mermaid CLI for architecture visualizations
- **Icons**: Inline SVG with Heroicons patterns
- **Analytics**: Google Analytics 4 (gtag.js)
- **Hosting**: GitHub Pages (via gh-pages branch)
- **Domain**: Custom domain with SSL

### Color Scheme

- **Brand Dark**: `#0f172a` (primary background)
- **Brand Light**: `#1e293b` (secondary background)
- **Brand Accent**: `#38bdf8` (CTAs, highlights, links)
- **Brand Text**: `#e2e8f0` (primary text)
- **Brand Subtext**: `#94a3b8` (secondary text)

## Project Structure

```
ai-portfolio/
├── index.html                  # Homepage with hero, featured projects
├── projects.html               # Full project showcase (15 achievements)
├── about.html                  # Career timeline, leadership, remote work
├── favicon.svg                 # Site favicon (AJ initials)
├── robots.txt                  # SEO: allow all, sitemap reference
├── sitemap.xml                 # SEO: all pages indexed
│
├── blog/
│   ├── index.html                                        # Blog landing page
│   ├── eliminating-40-hours-weekly-toil.html            # Blog post 1
│   ├── building-production-rag-systems.html             # Blog post 2
│   └── troubleshooting-playbook-knowledge-codification.html  # Blog post 3
│
├── case-studies/
│   ├── build-system-stabilization.html      # CTO bonus, DevOps team formation
│   ├── e2e-tracker.html                     # 40+ hrs/week eliminated
│   └── framework-migration.html             # 2-year stall to 2-month completion
│
├── assets/
│   └── diagrams/
│       ├── build-system.mermaid             # Mermaid source files
│       ├── e2e-tracker.mermaid
│       ├── framework-migration.mermaid
│       ├── ai-test-platform.mermaid
│       ├── build-system.svg                 # Generated SVG diagrams
│       ├── e2e-tracker.svg
│       ├── framework-migration.svg
│       └── ai-test-platform.svg
│
└── data/docs/                               # Source materials (not deployed)
    ├── TAP_V2/                              # AI platform documentation
    ├── advancement/                         # Career progression materials
    └── on-the-hunt/                         # Job search resources
```

## Content Overview

### Homepage (`index.html`)
- Hero section with force-multiplier positioning
- Featured case studies (3 highest-impact projects)
- "What I'm Building Next" section with AI platform
- Strategic roadmap initiatives
- Structured data (JSON-LD) for SEO

### Projects Page (`projects.html`)
- 15 achievements organized by category
- Expandable cards with detailed descriptions
- Tags: Platform Engineering, AI, Infrastructure, Testing
- Metrics-driven impact statements

### About Page (`about.html`)
- Career timeline (Coast Guard → Intuit/Home Depot → 4G Clinical)
- 8 years fully remote emphasis
- Technical leadership grid (4 categories)
- Remote work excellence metrics
- "What I'm Building Next" details

### Blog (`blog/`)
Three comprehensive technical posts:

1. **Eliminating 40 Hours of Weekly Toil** (8 min read)
   - E2E Test Tracker platform case study
   - Force multiplication through full-stack analytics
   - Production lessons learned

2. **Building Production RAG Systems** (10 min read)
   - Dual-context architecture (production + branch)
   - Domain-specific knowledge bases
   - Context engine design patterns
   - Lessons from AI platform development

3. **Troubleshooting Playbook: Codifying Knowledge** (9 min read)
   - Multi-tier playbook structure
   - Tribal → institutional knowledge transformation
   - Onboarding acceleration
   - 4 versions of evolution

### Case Studies
Three detailed project deep-dives with:
- Challenge/Approach/Solution/Impact/Lessons structure
- Architecture diagrams with collapsible Mermaid source
- Reading time indicators
- Related projects cross-links
- Measurable outcomes (time-based metrics only)

## Development

### Local Development

1. Clone the repository:
   ```bash
   git clone https://github.com/andrewajenkins/ai-portfolio.git
   cd ai-portfolio
   ```

2. Open in browser:
   ```bash
   # Using Python's built-in server
   python -m http.server 8000

   # Or using Node's http-server
   npx http-server -p 8000
   ```

3. Navigate to `http://localhost:8000`

### Updating Diagrams

Diagrams are created using Mermaid syntax and converted to SVG:

1. Edit `.mermaid` files in `assets/diagrams/`
2. Regenerate SVGs:
   ```bash
   npm install -g @mermaid-js/mermaid-cli

   # Convert all diagrams
   mmdc -i assets/diagrams/build-system.mermaid -o assets/diagrams/build-system.svg -t dark -b transparent
   mmdc -i assets/diagrams/e2e-tracker.mermaid -o assets/diagrams/e2e-tracker.svg -t dark -b transparent
   mmdc -i assets/diagrams/framework-migration.mermaid -o assets/diagrams/framework-migration.svg -t dark -b transparent
   mmdc -i assets/diagrams/ai-test-platform.mermaid -o assets/diagrams/ai-test-platform.svg -t dark -b transparent
   ```

3. Diagrams automatically embedded in HTML with collapsible source

### Adding a New Blog Post

1. Create new HTML file in `blog/` directory
2. Copy structure from existing post (e.g., `eliminating-40-hours-weekly-toil.html`)
3. Update:
   - Title, meta tags, canonical URL
   - Open Graph and Twitter Card metadata
   - Article content
   - Related posts section
   - Reading time estimate

4. Add entry to `blog/index.html`
5. Add URL to `sitemap.xml`

## Deployment

### GitHub Pages

Site deploys automatically to GitHub Pages:

1. Push changes to `master` branch
2. GitHub Pages serves from root directory
3. Custom domain configured via DNS CNAME
4. SSL automatically provisioned

### DNS Configuration

- **Type**: CNAME
- **Host**: www (or @)
- **Value**: andrewajenkins.github.io
- **TTL**: 3600

## SEO & Analytics

### Search Engine Optimization

- **Sitemap**: `sitemap.xml` with all pages, priorities, and update frequencies
- **Robots.txt**: Allow all crawlers, sitemap reference
- **Meta Tags**: Title, description, keywords on every page
- **Open Graph**: Full OG tags for social sharing
- **Twitter Cards**: Summary cards with descriptions
- **Structured Data**: JSON-LD Person schema on homepage
- **Canonical URLs**: Prevent duplicate content indexing
- **Semantic HTML**: Proper heading hierarchy, landmarks

### Analytics

- Google Analytics 4 (gtag.js) on all pages
- Property ID: `G-44TWQEWQP8`
- Tracks: pageviews, events, user flows

## Design Principles

1. **Metrics-Driven**: All impact claims backed by time-based metrics
2. **No Proprietary Info**: Generic terminology, no company-specific names
3. **Force Multiplication**: Emphasis on team enablement, not individual output
4. **Technical Depth**: Detailed case studies with architecture diagrams
5. **Remote-First**: Highlight 8 years remote, async collaboration
6. **Staff+ Positioning**: Strategic leadership, not just IC work

## Performance

- **No JavaScript frameworks**: Vanilla JS for menu interactions only
- **CDN-hosted assets**: Tailwind CSS, Google Fonts via CDN
- **Optimized images**: SVG diagrams (vector, scalable)
- **Minimal dependencies**: Static HTML, no build process
- **Fast load times**: No heavy frameworks, simple architecture

## Content Guidelines

### What to Include
- Time-based metrics (hours saved, time reduced)
- Team impact (people enabled, processes improved)
- Technical architecture details
- Lessons learned, failure modes
- Strategic leadership examples

### What to Avoid
- ROI calculations (indefensible without data)
- Proprietary company names (IP concerns)
- Over-sharing internal details
- Claims without evidence
- Individual hero narratives

## Maintenance

### Regular Updates
- Update "What I'm Building Next" as projects evolve
- Add new blog posts quarterly
- Refresh project metrics if new data available
- Update About page with new accomplishments

### Content Refresh
- Review SEO meta descriptions annually
- Update career timeline with new roles
- Add new case studies for major projects
- Refresh screenshots if design changes

## License

Content and code © 2025 Andrew Jenkins. All rights reserved.

Feel free to use the structure and design as inspiration for your own portfolio, but please don't copy content verbatim.

## Contact

- **Website**: [andrewajenkins.com](https://andrewajenkins.com)
- **LinkedIn**: [linkedin.com/in/andrewajenkins](https://linkedin.com/in/andrewajenkins)
- **GitHub**: [github.com/andrewajenkins](https://github.com/andrewajenkins)
- **Location**: San Diego, CA (Remote)

---

**Built for Staff+ Platform Engineering roles. Targeting $140-150k. 8 years fully remote.**
