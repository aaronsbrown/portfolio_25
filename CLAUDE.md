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
Blog posts are stored in `src/content/blog/` as Markdown files. Each post requires frontmatter:
```yaml
---
title: "Post Title"
date: 2024-06-15
excerpt: "Brief description"
tags: ["tag1", "tag2"]
featured: true  # Shows on homepage
---
```

## Architecture Overview

### Design Philosophy Integration
This portfolio implements a unique aesthetic combining:
- **Bauhaus modularity**: Grid-based layouts with systematic spacing
- **Brutalist clarity**: Bold monospace typography (JetBrains Mono) for headers
- **Vaporwave elements**: CRT grain overlay and pink (#ff0080) accents  
- **Analog imperfection**: Subtle noise textures and organic animations
- **Generative systems**: Mathematical vector field art on homepage

### Component Architecture
- **Base.astro**: Core layout with dark mode, CRT overlay, and font loading
- **BlogPost.astro**: Article layout optimized for reading with typography hierarchy
- **Header.astro**: Fixed navigation with integrated theme toggle
- **VectorField.astro**: Canvas-based generative art using sine/cosine mathematical functions

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