# Design Memory - Taste the City

> **Purpose**: This file captures Taste the City's design standards and brand guidelines. The design-and-refine plugin will automatically load these standards to ensure all generated design variants stay on-brand.

---

## Brand Tone

**Adjectives**: Local, Authentic, Welcoming, Character-driven, Living/Breathing
**Voice**: Friendly and trustworthy food guide that brings character to the dining experience
**Avoid**: Corporate, sterile, overly polished, cold, impersonal

The brand should feel like a living, breathing entity that helps people discover the character of food and culture in their city.

---

## Color

### Primary Palette

**Chopped Kale (Primary Dark Green)**
- Hex: `#2D5D4C`
- RGB: 45, 93, 76
- Use: Primary brand color, headers, dark backgrounds, footer sections
- Represents: Fresh, natural, kitchen-inspired
- On dark green: Use cream or white text

**Sage Butter (Secondary Light Green)**
- Hex: `#9CAB88`
- RGB: 156, 171, 136
- Use: Accents, secondary buttons, highlights, tags
- Represents: Fresh herbs, organic, approachable
- Pairs with: Chopped Kale, Heavy Cream

**Golden Hour (Accent Yellow/Gold)**
- Hex: `#D4AF37` (approximate - seen in Login/Signup button and city selector)
- Alternative: `#E6B800` or `#F0C420`
- Use: Primary CTAs, active states, important UI elements, city/location selectors
- Represents: Energy, discovery, premium experience
- High visibility - use for primary actions
- On yellow: Use Charcoal text for best contrast

**Heavy Cream (Neutral Light)**
- Hex: `#F5EFE8`
- RGB: 245, 239, 232
- Use: Backgrounds, cards, light sections
- Represents: Clean, fresh, natural light
- Never use pure white - always use Heavy Cream for warmth

**Tomato Paste (Accent Terra Cotta)**
- Hex: `#BD5C3C`
- RGB: 189, 92, 60
- Use: Secondary CTAs, highlights, featured items (when not using yellow)
- Represents: Warmth, appetite, featured content
- Alternative to Golden Hour for some CTAs

**Charcoal (Near Black)**
- Hex: `#161514`
- RGB: 22, 21, 20
- Use: Body text, dark UI elements
- Not pure black - warmer tone

### Color Shades (Tints & Tones)

**Dark Green Shades** (Chopped Kale variations):
- 100%: #2D5D4C (base)
- 80%: Lighter tint for hover states
- 60%: Subtle backgrounds
- 40%: Very light accents
- 20%: Near-cream tints

**Gray Shades** (Charcoal variations):
- 100%: #161514 (base)
- 80%: Secondary text
- 60%: Disabled states
- 40%: Borders
- 20%: Light borders

**Tomato Paste Shades**:
- 100%: #BD5C3C (base)
- 80%: Hover state
- 60%: Peachy tones
- 40%: Light pink
- 20%: Very subtle backgrounds

### Semantic Colors

Derived from the brand palette:
- **Success**: Sage Butter (#9CAB88) or slightly more saturated green
- **Error**: Tomato Paste (#BD5C3C) - already has urgency/attention
- **Warning**: Golden Hour (#D4AF37) or lighter Tomato Paste shade
- **Info**: Chopped Kale (#2D5D4C)
- **Highlight/Active**: Golden Hour (#D4AF37) - for selected cities, active tabs, etc.

### Color Usage Rules

1. **Backgrounds**: Always prefer Heavy Cream (#F5EFE8) over pure white
2. **Primary Actions**: Chopped Kale (#2D5D4C) or Tomato Paste (#BD5C3C)
3. **Text on Dark Green**: Heavy Cream or white
4. **Text on Light**: Charcoal (#161514), never pure black
5. **Avoid**: Blue grays, cool neutrals - keep everything warm-toned

---

## Typography

### Typefaces

**Instrument Serif** (Headlines & Display)
- Use: H1, H2, H3, hero text, restaurant names, section headings
- Purpose: Gives character and distinction
- Weights: Regular, Bold
- Note: Creates the "living, breathing" brand personality

**Lato** (Body Text)
- Use: Body copy, descriptions, paragraphs, UI labels
- Purpose: Easy readability
- Weights: Regular (400), Bold (700)
- Note: Clean, approachable, highly readable

**IBM Plex Mono** (Technical/Data)
- Use: Prices, addresses, hours, technical details, monospaced data
- Purpose: Highlights technical information
- Weights: Regular (400)
- Note: Use sparingly for data that needs precision

### Type Scale

Recommended hierarchy based on brand guidelines:

```
Display (Hero): Instrument Serif, 48-64px, Bold
H1: Instrument Serif, 36-48px, Bold
H2: Instrument Serif, 28-36px, Bold
H3: Instrument Serif, 24-28px, Regular/Bold
H4: Instrument Serif, 20-24px, Regular

Body Large: Lato, 18-20px, Regular
Body: Lato, 16px, Regular
Body Small: Lato, 14px, Regular
Caption: Lato, 12px, Regular

Data/Technical: IBM Plex Mono, 14-16px, Regular
```

### Typography Rules

1. **Restaurant names**: Always use Instrument Serif (brand character)
2. **Headings**: Instrument Serif, creates distinction
3. **Descriptions**: Lato for readability
4. **Pricing**: IBM Plex Mono ($, $$, $$$)
5. **Addresses/Hours**: IBM Plex Mono
6. **UI buttons**: Lato Bold or Instrument Serif for primary CTAs
7. **Line height**: 1.5-1.7 for body text (Lato), 1.2-1.3 for headings

---

## Layout & Spacing

**Density**: Comfortable
- Food and restaurant content needs room to breathe
- Images should be prominent
- Avoid cramped layouts

**Spacing Scale**: 8px grid system
- Base unit: 8px
- Scale: 4px, 8px, 12px, 16px, 24px, 32px, 48px, 64px
- Use 4px for tight spacing (icon + label)
- Use 16-24px for card padding
- Use 32-48px for section spacing

**Corner Radius**: Rounded, friendly
- Small elements (tags, pills): 4px
- Buttons: 8px
- Cards: 12px or 16px
- Large containers: 16px
- Avoid sharp corners - conflicts with friendly brand tone

**Shadows**: Medium elevation
- Cards should feel elevated but not floating
- Subtle: `0 1px 3px rgba(22, 21, 20, 0.1)`
- Medium: `0 4px 6px rgba(22, 21, 20, 0.1)`
- Strong: `0 10px 15px rgba(22, 21, 20, 0.15)`
- Use warm shadow colors (Charcoal-based, not cool grays)

**Grid System**:
- Mobile-first
- Responsive breakpoints: 640px, 768px, 1024px, 1280px
- Content max-width: 1280px
- Comfortable padding on mobile (16px minimum)

---

## Component Conventions

### Restaurant Cards

**Must Include**:
- Food/restaurant imagery (prominent, above the fold)
- Restaurant name (Instrument Serif)
- Cuisine type (Lato, secondary text)
- Rating (stars or score)
- Distance/location
- Pricing tier ($, $$, $$$) - IBM Plex Mono

**Layout**:
- Image: 16:9 or 4:3 aspect ratio
- Padding: 16-24px
- Border radius: 12px
- Shadow: Medium elevation
- Background: Heavy Cream or white

**Example Structure**:
```
┌─────────────────────────┐
│ [Food Image - 16:9]     │
├─────────────────────────┤
│ Restaurant Name         │ ← Instrument Serif
│ Italian • $$$ • 2.3 km  │ ← Lato + IBM Plex Mono
│ ★★★★☆ 4.5 (120)        │
│ [Book Now Button]       │
└─────────────────────────┘
```

### Buttons

**Primary CTA** (High emphasis):
- Background: Golden Hour (#D4AF37) - highest visibility
- Text: Charcoal (#161514) for best contrast
- Font: Lato Bold or Instrument Serif
- Padding: 12px 24px
- Border radius: 8px
- Use action words: "Login/Signup", "Book Now", "Explore", "Discover"
- Examples: Login/Signup button, Book a Tasting, primary form submits

**Secondary** (Medium emphasis):
- Option 1: Chopped Kale (#2D5D4C) fill + Heavy Cream text
- Option 2: 2px border (Chopped Kale or Charcoal) + transparent/Heavy Cream background
- Text: Chopped Kale or Charcoal
- Same padding/radius as primary
- Examples: "back to browse" links, secondary actions

**Tertiary** (Low emphasis):
- Text-only: Chopped Kale, Tomato Paste, or Charcoal
- Underline on hover
- No background
- Examples: Navigation links, in-text links

**States**:
- Hover: Darken by 10-15%
- Active: Darken by 20%
- Disabled: 40% opacity + cursor not-allowed

### Forms

**Input Fields**:
- Border: 1px solid gray-40% (Charcoal-based)
- Border radius: 8px
- Padding: 12px 16px
- Focus: 2px ring in Chopped Kale
- Font: Lato, 16px

**Labels**:
- Font: Lato, 14px
- Color: Charcoal (#161514)
- Position: Above input with 8px spacing
- Required: Use asterisk or "Required" label

**Validation**:
- Success: Sage Butter border/icon
- Error: Tomato Paste border/icon
- Inline messages below field (12px Lato)

### Navigation

**Logo**: "TASTE the CITY" - hand-lettered logotype
- Primary: Dark green background (#2D5D4C) with white text
- Can use black logotype on light backgrounds
- Never distort or stretch

**Nav Links**:
- Font: Lato Regular or Instrument Serif for emphasis
- Color: Charcoal on light, Heavy Cream on dark
- Active state: Tomato Paste underline or highlight
- Mobile: Hamburger menu with smooth transitions

### Tags/Pills

- Background: Sage Butter (#9CAB88) or light shades
- Text: Charcoal or Chopped Kale
- Border radius: 4px
- Padding: 4px 12px
- Font: Lato, 12-14px
- Use for: Cuisine types, dietary restrictions, features

### Images

**Food Photography**:
- Always prominent and high quality
- Aspect ratios: 16:9 (landscape), 4:3 (standard), 1:1 (square)
- Border radius: 8-12px
- Alt text required (accessibility)
- Loading: Skeleton with Heavy Cream background

**Image Treatment**:
- Subtle overlay on hover (0-10% Charcoal)
- Never apply heavy filters
- Keep colors natural (food should look appetizing)

---

## Interaction Patterns

### Feedback

**Toasts/Notifications**:
- Position: Top-right or bottom-center
- Background: Chopped Kale (success), Tomato Paste (error)
- Text: Heavy Cream
- Duration: 3-5 seconds
- Border radius: 8px
- Shadow: Strong elevation

**Loading States**:
- Skeleton screens with Heavy Cream (#F5EFE8) base
- Pulse animation (subtle, not distracting)
- Spinner color: Chopped Kale or Tomato Paste
- Text: "Loading restaurants..." (Lato)

**Empty States**:
- Icon + message centered
- Illustration in brand colors
- CTA: "Explore nearby" or similar

### Hover/Focus States

**Interactive Elements**:
- Transition: 150-250ms ease-out
- Hover: Darken/lighten by 10-15%
- Focus: 2px ring in Chopped Kale with 2px offset
- Active: Scale 0.98 or darken 20%

**Cards**:
- Hover: Lift with stronger shadow
- Transform: translateY(-4px)
- Shadow transition: 200ms ease-out

---

## Accessibility

**WCAG Level**: AA minimum (AAA for critical flows)

**Color Contrast**:
- Text on Chopped Kale (#2D5D4C): Use Heavy Cream or white (meets AA)
- Text on Heavy Cream (#F5EFE8): Use Charcoal (#161514) (meets AAA)
- Text on Tomato Paste (#BD5C3C): Use white or Heavy Cream
- Small text: 4.5:1 minimum
- Large text (18px+): 3:1 minimum
- UI components: 3:1 minimum

**Focus Management**:
- Visible focus ring: 2px solid Chopped Kale, 2px offset
- Never remove focus styles
- Logical tab order
- Skip links for navigation

**Touch Targets**:
- Minimum: 44x44px (mobile-first app)
- Preferred: 48x48px for primary actions
- Spacing: 8px minimum between targets

**Labels & ARIA**:
- All form inputs labeled
- Alt text for food imagery (describe the dish)
- ARIA labels for icon buttons
- Landmark roles for navigation

**Motion**:
- Respect `prefers-reduced-motion`
- No auto-playing videos
- Smooth scroll: Optional, disable for reduced motion

---

## Design Patterns & Best Practices

### Restaurant Listings

**Card View** (Default):
- Grid: 1 column (mobile), 2 columns (tablet), 3 columns (desktop)
- Image prominent
- Vertical card layout
- Gap: 24px

**List View** (Alternative):
- Horizontal layout
- Image on left (square or 4:3)
- Info on right
- Compact for scanning

**Filtering**:
- Sticky filter bar
- Tags for cuisine, price, distance
- Clear active filters
- "Clear all" option

### Discovery Flow

**Homepage**:
- Hero with search or featured restaurants
- Category tiles (Cuisine types)
- "Near you" section
- "Trending" or "Popular" sections

**Search/Browse**:
- Search bar: Large, prominent (Instrument Serif placeholder)
- Autocomplete with restaurant names and cuisines
- Recent searches
- Filters: Cuisine, price, distance, rating

**Restaurant Detail**:
- Hero image gallery
- Name (Instrument Serif, large)
- Cuisine, price, hours, address (IBM Plex Mono)
- Rating and reviews
- "Book" or "Get Directions" CTAs (Tomato Paste)
- Menu/photos tabs

### Mobile-First Considerations

- Touch targets: 48x48px
- Bottom navigation for key actions
- Swipeable cards/galleries
- Fixed "Book" button at bottom
- Generous padding (16px minimum)
- Font sizes: 16px minimum for body (no browser zoom)

---

## Dark Mode (Future Consideration)

Not defined in current brand guide, but if needed:
- Background: Charcoal (#161514) or darker
- Text: Heavy Cream (#F5EFE8)
- Cards: Lighter Charcoal (gray-80%)
- Chopped Kale: Lighten slightly for better contrast
- Tomato Paste: Lighten slightly
- Food images: Reduce brightness slightly (5-10%)

---

## Repo Conventions

**Component Structure**:
- Prefer functional components (React)
- Use TypeScript for type safety
- Colocate styles (CSS modules or Tailwind)

**Styling Approach**:
- Tailwind CSS preferred (configure with brand colors)
- CSS Modules acceptable
- Avoid inline styles unless dynamic

**Existing Primitives** (Assumed):
- `Button` (Primary, Secondary, Tertiary variants)
- `RestaurantCard` (Card, List variants)
- `Input`, `Select`, `Checkbox`
- `Tag` / `Badge`
- `Rating` component
- `Navbar`, `Footer`
- `Modal`, `Drawer`

**File Organization**:
- Components: `/components` or `/src/components`
- Pages: `/pages` or `/app` (Next.js)
- Styles: `/styles` or colocated
- Assets: `/public` or `/assets`

---

## Do / Don't

### ✅ Do

- Use Instrument Serif for restaurant names and headings
- Use Heavy Cream (#F5EFE8) instead of pure white
- Make food imagery prominent and appetizing
- Use warm tones from the brand palette
- Show pricing tier with $ symbols (IBM Plex Mono)
- Use rounded corners (8-16px)
- Keep layouts comfortable, not cramped
- Use action-oriented CTAs ("Explore", "Discover", "Book")
- Maintain 48x48px touch targets on mobile
- Use Chopped Kale or Tomato Paste for CTAs
- Include distance/location in restaurant cards
- Use medium elevation shadows
- Keep the brand feeling friendly and welcoming

### ❌ Don't

- Use pure white backgrounds (use Heavy Cream)
- Use pure black text (use Charcoal #161514)
- Use cool grays or blue tones
- Overcrowd food imagery
- Use sharp corners (conflicts with friendly tone)
- Hide pricing information
- Use generic CTAs like "Click here" or "Submit"
- Apply heavy filters to food photos
- Use small touch targets (<44px on mobile)
- Make layouts feel cramped or dense
- Use corporate or sterile design patterns
- Ignore the brand's "living, breathing" personality
- Mix in off-brand fonts (stick to Instrument Serif, Lato, IBM Plex Mono)

---

## Links & Resources

**Brand Guidelines**: Taste the City Brand Guide (internal)
**Web App**: https://tastings.tastethecity.ca/
**Marketing Site**: https://www.tastethecity.ca/
**Design System** (if exists): [Link to Storybook or Figma]

---

## Notes

- This design memory is a living document
- Update as brand evolves
- Reference this file before starting any design work
- The design-and-refine plugin will automatically load these standards
- For questions, consult the full brand guide or design lead

---

**Last Updated**: 2026-01-18
**Version**: 1.0
**Maintained By**: Design Team
