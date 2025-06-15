# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Development Commands

### Core Development
- `npm run dev` - Start development server at localhost:4321
- `npm run build` - Build production site to ./dist/
- `npm run preview` - Preview production build locally
- `astro check` - Run TypeScript and content validation
- `astro add <integration>` - Add Astro integrations

### Content Management
Journal posts are stored in `src/content/journal/` as Markdown files. Each post requires frontmatter:
```yaml
---
title: "Post Title"
date: 2024-06-15
excerpt: "Brief description"
tags: ["leadership", "strategy", "design"]
featured: true  # Shows on homepage
audience: ["creative executives", "design leaders"]  # Target audience
---
```

## Architecture Overview

### Design Philosophy Integration
This creative leadership journal implements a tech-brutalist aesthetic combining:
- **Horizontal Editorial Layout**: Full-screen tiles with smooth scroll navigation
- **Brutalist Typography**: Space Grotesk (Pangram Fraktion ready) with geometric precision  
- **Neutral Chromatic Palette**: Low-saturation greys with subtle accent colors
- **Analog Texture Effects**: Enhanced CRT grain overlay with scan lines
- **Tech-Brutalist Elements**: Sharp edges, geometric layouts, systematic spacing

### Component Architecture
- **Base.astro**: Core layout with dark mode, enhanced CRT overlay, and font loading
- **HorizontalJournal.astro**: Main horizontal scroll container with full-screen tiles
- **JournalTile.astro**: Individual editorial tiles for longform content display
- **Header.astro**: Fixed navigation with Journal/About/Contact links
- **BlogPost.astro**: Individual article layout for detailed reading

### Horizontal Scroll System
The site uses a custom horizontal scroll architecture:
- **Full-screen tiles** for each journal post with editorial spacing
- **Smooth scroll behavior** with keyboard navigation (arrow keys)
- **Mobile-adaptive** with touch/swipe support and proximity scroll snap
- **Visual variety** through subtle background patterns (dots, lines, grid)
- **Progressive disclosure** with intro tile, content tiles, and contact tile

### Content Collections System
Uses Astro's type-safe content collections in `src/content/config.ts`. Blog posts are fully compatible with Obsidian and support featured posts, tags, and draft states.

### Styling Approach
- **Typography**: Inter for body text, JetBrains Mono for headers/code
- **Dark Mode**: System preference detection with localStorage persistence and 300ms transitions  
- **Effects**: Animated CRT grain overlay using CSS radial-gradient patterns
- **Colors**: Minimalist black/white/gray palette with strategic pink accents

### Generative Art Implementation
The VectorField component creates organic mathematical animations:
- Canvas-based with device pixel ratio handling
- RequestAnimationFrame loop with proper cleanup
- Theme-responsive vector colors
- Performance optimized for mobile devices

## Key Patterns

### Content-First Architecture
The entire site prioritizes content consumption with excellent typography, reading time estimation, and semantic HTML structure.

### Systematic Design Thinking  
Every component serves a clear purpose in the overall design system. Spacing, colors, and interactions follow consistent patterns throughout.

### Performance Optimization
- Static site generation for fast loading
- Font preloading with display swap
- Minimal JavaScript (only for theme toggle and vector field)
- CSS optimization through Tailwind purging

### Future Extensibility
The architecture supports planned expansions:
- Portfolio section with project filtering
- CV page with PDF export capability  
- Contact forms with serverless integration
- Newsletter and e-commerce features

## Content Editing Workflow

Blog posts are designed for Obsidian compatibility. Place images in `public/assets/` and reference with standard Markdown syntax. The build process automatically generates clean URLs and optimizes content for performance.