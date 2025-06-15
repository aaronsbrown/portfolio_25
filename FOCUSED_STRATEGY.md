# Home Page + Blog Priority Strategy

## Phase 1 Focus: Home + Blog
Based on analysis of your current site at aaronsteelebrown.com, maintaining your minimalist aesthetic while adding the requested creative elements.

## Design Evolution
- **Keep**: Clean typography (PP Fraktion Sans Bold + Inter), neutral palette, grid-based structure
- **Add**: Bauhaus modularity, subtle vaporwave textures, generative art elements
- **Enhance**: Dark mode transitions, analog imperfection details

## Core Pages

### 1. Home Page (/)
```
Header: [Logo] [Blog] [Dark Mode Toggle]

Hero Section:
- Interactive generative art background (subtle vector field or particle system)
- Large title: "Aaron Steele Brown"
- Subtitle: "Creative Technologist"
- CRT grain overlay (very subtle)

About Section:
- Brief bio paragraph
- Current focus/availability status
- Link to full information

Featured Work:
- 2-3 latest projects (minimal cards)
- "View All Work" link (future)

Latest Writing:
- 3 most recent blog posts
- "Read More" link to blog

Footer: Minimal contact links
```

### 2. Blog (/blog)
```
Header: [Logo] [Home] [Dark Mode Toggle]

Blog List:
- Chronological post list
- Each post: Date, Title, Excerpt, Read Time
- Clean typography with generous whitespace
- Search/filter (future enhancement)

Post Page:
- Article header: Date, Title, Read Time
- Rich typography with proper hierarchy
- Code syntax highlighting
- Image optimization
- Previous/Next navigation
```

## Technical Implementation

### Project Structure (Simplified)
```
portfolio/
├── src/
│   ├── components/
│   │   ├── Header.astro
│   │   ├── Footer.astro
│   │   ├── BlogCard.astro
│   │   ├── VectorField.astro    # Generative art
│   │   └── ThemeToggle.astro
│   ├── layouts/
│   │   ├── Base.astro
│   │   └── BlogPost.astro
│   ├── pages/
│   │   ├── index.astro          # Home
│   │   ├── blog/
│   │   │   ├── index.astro      # Blog list
│   │   │   └── [...slug].astro  # Blog posts
├── content/
│   └── blog/                    # 5 Markdown posts from Vault
├── public/
│   └── textures/                # CRT grain, noise patterns
└── package.json
```

### Content Schema
```typescript
// Blog posts from your Vault
export const blogCollection = defineCollection({
  type: 'content',
  schema: z.object({
    title: z.string(),
    date: z.date(),
    excerpt: z.string().optional(),
    tags: z.array(z.string()).optional(),
    featured: z.boolean().default(false),
    draft: z.boolean().default(false)
  })
})
```

## Visual Enhancements

### Typography System
- **Headers**: PP Fraktion Sans Bold (maintain current style)
- **Body**: Inter (maintain current choice)
- **Code**: JetBrains Mono (for code blocks)

### Color Palette (Evolution)
```css
/* Light Mode */
--bg: #ffffff
--text: #000000
--accent: #666666
--highlight: #ff0080  /* Subtle vaporwave accent */

/* Dark Mode */
--bg: #000000
--text: #ffffff
--accent: #cccccc
--highlight: #00ffff  /* Cyan accent */
```

### Subtle Effects
- CRT grain texture overlay (5% opacity)
- Smooth dark mode transitions (300ms ease)
- Vector field animation on home hero (very subtle)
- Hover states with slight color shifts

## Development Sprint Plan

### Week 1: Foundation
- [x] Astro + Tailwind setup
- [x] Basic layout components
- [x] Content collection for blog
- [x] Import 5 blog posts from Vault

### Week 2: Core Implementation  
- [x] Home page with generative art
- [x] Blog list and post layouts
- [x] Dark mode implementation
- [x] Basic styling system

### Week 3: Enhancement
- [x] Vector field animation
- [x] CRT/analog texture overlays
- [x] Performance optimization
- [x] Mobile responsiveness

## Success Criteria
1. **Home page** loads in <2s with smooth generative art
2. **Blog** displays 5 posts with excellent typography
3. **Dark mode** transitions smoothly
4. **Mobile-first** responsive design
5. **SEO-ready** with proper meta tags

This focused approach delivers a strong foundation that can be expanded with portfolio, CV, and contact sections later.