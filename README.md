# Aaron Steele Brown Portfolio

A creative professional branding website built with Astro, featuring a home page with generative art and a blog system optimized for Obsidian Markdown content.

## Design Philosophy

This site combines:
- **Bauhaus Modularity**: Grid-based layouts and geometric forms
- **Brutalist Clarity**: Bold typography and stark contrasts  
- **Vaporwave Aesthetics**: CRT grain overlays and retro textures
- **Analog Imperfection**: Subtle noise and organic movement
- **Generative Systems**: Interactive vector field animations

## Architecture

Built with modern web technologies for performance and maintainability:
- **Astro 4.x**: Static site generation with islands architecture
- **Tailwind CSS**: Utility-first styling system
- **TypeScript**: Type-safe development
- **Markdown**: Content management compatible with Obsidian

## Project Structure

```text
portfolio/
├── src/
│   ├── components/
│   │   ├── Header.astro          # Navigation with theme toggle
│   │   └── VectorField.astro     # Generative art animation
│   ├── content/
│   │   ├── blog/                 # Markdown blog posts
│   │   └── config.ts             # Content collections
│   ├── layouts/
│   │   ├── Base.astro            # Core HTML structure
│   │   └── BlogPost.astro        # Article layout
│   ├── pages/
│   │   ├── index.astro           # Home page
│   │   └── blog/                 # Blog routes
│   └── styles/
│       └── global.css            # Custom styles
├── public/                       # Static assets
└── FOCUSED_STRATEGY.md           # Design & technical strategy
```

## Development

### Setup
```bash
npm install
npm run dev
```

Visit `http://localhost:4321/` to see the development server.

### Commands
| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |

## Content Management

### Adding Blog Posts
1. Create new `.md` file in `src/content/blog/`
2. Include frontmatter:
```yaml
---
title: "Your Post Title"
date: 2024-06-15
excerpt: "Brief description"
tags: ["tag1", "tag2"]
featured: true
---
```
3. Write content in Markdown below the frontmatter

### Obsidian Integration
- Blog posts are fully compatible with Obsidian
- Use standard Markdown syntax
- Images should be placed in `public/assets/`
- Internal links work with standard `[text](url)` syntax

## Features

### Interactive Elements
- **Vector Field Animation**: Generative art background on home page
- **Dark Mode**: Smooth transitions with system preference detection
- **CRT Overlay**: Subtle analog grain effect throughout site
- **Responsive Design**: Mobile-first approach with Tailwind

### Typography
- **Primary**: Inter for body text (clean, readable)
- **Headers**: JetBrains Mono for monospace aesthetic
- **Code**: Syntax highlighted code blocks
- **Hierarchy**: Consistent scale and spacing

### Performance
- **Static Generation**: Pre-built pages for fast loading
- **Image Optimization**: Automatic WebP/AVIF conversion
- **CSS Optimization**: Purged and minimized styles
- **Font Loading**: Preloaded and swapped fonts

## Deployment

### Build for Production
```bash
npm run build
```

### Hosting Options
- **Netlify**: Connect GitHub repo for automatic deploys
- **Vercel**: Zero-config deployment with domain
- **GitHub Pages**: Free hosting with custom domain support

### Environment Variables
None required for basic functionality.

## Future Enhancements

The architecture supports easy expansion:
- Portfolio section with project filtering
- CV page with PDF export
- Contact form with serverless functions
- Newsletter integration
- E-commerce capabilities
- Custom landing pages

## Technical Details

- **Framework**: Astro v5.9.3
- **Styling**: Tailwind CSS v4.1.10
- **Fonts**: Google Fonts (Inter, JetBrains Mono)
- **Icons**: Heroicons (built-in SVG)
- **Build Time**: ~2-3 seconds
- **Bundle Size**: <100KB (without content)
