# Taste the City - Custom Design Plugin Setup

This guide explains how to use the design-and-refine plugin with Taste the City's brand standards baked in.

---

## What Changed?

The plugin has been customized for Taste the City with:

1. **Brand Memory** (`DESIGN_MEMORY.md`) - Your complete design system
2. **Brand Principles** (`design-and-refine/skills/design-lab/DESIGN_PRINCIPLES.md`) - TTC overrides in Part 0
3. **Brand Compliance** (`design-and-refine/templates/DESIGN_PLAN.template.md`) - TTC checklist in output
4. **Brand Locks** (`design-and-refine/skills/design-lab/SKILL.md`) - Automatic brand enforcement

---

## Quick Start

### 1. Install the Plugin

Copy the entire `design-and-refine/` directory to your Taste the City project:

```bash
# From this repo, copy to your project
cp -r design-and-refine /path/to/taste-the-city-project/

# Or if this IS your project, the plugin is already here
```

### 2. Ensure DESIGN_MEMORY.md is in Your Project Root

The `DESIGN_MEMORY.md` file should be at the root of your project (same level as `package.json`).

**Already done!** ✅ The file is in this repo at `/DESIGN_MEMORY.md`

### 3. Run the Plugin

```bash
# Make sure you're in your project directory
cd /path/to/taste-the-city-project

# Start the design lab for a component
/design-and-refine:start RestaurantCard

# Or for a page
/design-and-refine:start BrowseTastingsPage
```

---

## How It Works

### Phase 1: Interview (Shortened for TTC)

The plugin will ask you questions about your design goal. **Many questions are auto-skipped** because your brand is already defined in `DESIGN_MEMORY.md`:

**Questions you'll still see:**
- What are you designing? (component, page, feature)
- Is this a redesign or new design?
- What are the pain points with the current design?
- What are the top 3 user tasks?

**Questions auto-filled from DESIGN_MEMORY.md:**
- ✅ Brand adjectives: Living, breathing, character-driven, friendly, welcoming
- ✅ Density: Comfortable (food needs room to breathe)
- ✅ Color palette: Chopped Kale, Sage Butter, Golden Hour, Heavy Cream, Tomato Paste, Charcoal
- ✅ Typography: Instrument Serif (headings), Lato (body), IBM Plex Mono (data)
- ✅ Spacing: 8px grid (4, 8, 12, 16, 24, 32, 48, 64px)
- ✅ Touch targets: 48x48px (mobile-first)

### Phase 2: Brand Locks Applied

When generating 5 design variants, the plugin will **lock** these elements across all variants:

**LOCKED (same in all 5 variants):**
- ✅ Colors: Golden Hour for primary CTAs, Chopped Kale for secondary, etc.
- ✅ Typography: Instrument Serif for restaurant names and headings, Lato for body
- ✅ Component structure: Restaurant cards must include image, name, cuisine, price, rating, distance
- ✅ CTA language: "Explore", "Discover", "Book Now" (not "Click here", "Submit")
- ✅ Spacing scale: 8px grid multiples only
- ✅ Border radius: 8px buttons, 12-16px cards
- ✅ Shadows: Warm Charcoal-based, medium elevation

**FREE TO VARY (different across variants):**
- ✨ Information hierarchy: What gets emphasized first
- ✨ Layout model: Card vs list vs table, column count, arrangement
- ✨ Density: How spacing tokens are applied (tighter or more spacious within brand grid)
- ✨ Interaction patterns: Hover effects, loading states, validation approaches
- ✨ Component composition: Which components to use where

### Phase 3: Review and Choose

The plugin creates 5 variants at `http://localhost:3000/__design_lab` (or your dev server).

**All 5 variants will:**
- Use TTC brand colors
- Use Instrument Serif for restaurant names
- Use Golden Hour for primary CTAs
- Follow the 8px spacing grid
- Feel "on-brand"

**Each variant will differ in:**
- Layout (cards in 2 columns vs 3 columns vs list view)
- Information hierarchy (what's emphasized)
- Density (comfortable vs spacious)
- Interaction patterns

### Phase 4: Final Output

After you choose a winner, the plugin generates:

1. **`DESIGN_PLAN.md`** with:
   - **Taste the City Brand Compliance** checklist (✅ Golden Hour CTAs, ✅ Instrument Serif, etc.)
   - Implementation steps
   - Component API
   - Accessibility checklist (48x48px touch targets, WCAG AAA for critical flows)
   - Links to TTC sites (tastings.tastethecity.ca, tastethecity.ca)

2. **Final component code** ready to integrate

3. **Updated `DESIGN_MEMORY.md`** (if new patterns discovered)

---

## Examples

### Example 1: Redesign Restaurant Card

```bash
/design-and-refine:start RestaurantCard
```

**Plugin will:**
1. Detect you're redesigning `src/components/RestaurantCard.tsx`
2. Load TTC brand from `DESIGN_MEMORY.md`
3. Generate 5 variants:
   - **Variant A**: Vertical card, image-first, prominent CTA
   - **Variant B**: Horizontal card, info-dense, smaller images
   - **Variant C**: Minimal card, large images, text overlay
   - **Variant D**: List view, compact, more cards visible
   - **Variant E**: Feature card, spacious, editorial feel

4. **All variants use:**
   - Golden Hour (#D4AF37) "Book Now" button
   - Instrument Serif for restaurant name
   - IBM Plex Mono for pricing ($$$)
   - Lato for cuisine type and description
   - 16px padding, 12px border radius
   - Medium elevation shadow

5. You pick the winner, plugin generates final code + compliance checklist

### Example 2: New Browse Tastings Page

```bash
/design-and-refine:start BrowseTastingsPage
```

**Plugin will:**
1. Ask about pain points and key tasks
2. Auto-fill brand standards from `DESIGN_MEMORY.md`
3. Generate 5 page layout variants:
   - **Variant A**: Grid of cards, filter sidebar, search bar
   - **Variant B**: List view, inline filters, compact
   - **Variant C**: Map + list split view
   - **Variant D**: Hero search + featured tastings + grid
   - **Variant E**: Tabbed categories + infinite scroll

4. **All variants use:**
   - Golden Hour city selector (like "Calgary, AB")
   - Chopped Kale footer section
   - Heavy Cream backgrounds (no pure white)
   - Instrument Serif headings

5. You choose, plugin outputs page code + compliance checklist

---

## Brand Compliance Checklist

Every generated `DESIGN_PLAN.md` includes this checklist:

### Color Palette
- [ ] Uses Golden Hour (#D4AF37) for primary CTAs
- [ ] Uses Chopped Kale (#2D5D4C) for secondary CTAs
- [ ] Uses Heavy Cream (#F5EFE8) instead of pure white for backgrounds
- [ ] Uses Charcoal (#161514) instead of pure black for text
- [ ] Avoids cool grays and blue tones
- [ ] Food imagery uses natural colors

### Typography
- [ ] Restaurant names use Instrument Serif
- [ ] Headings use Instrument Serif
- [ ] Body text uses Lato
- [ ] Pricing tiers ($, $$, $$$) use IBM Plex Mono
- [ ] Addresses/hours use IBM Plex Mono

### Layout & Spacing
- [ ] Uses 8px grid (4, 8, 12, 16, 24, 32, 48, 64px)
- [ ] Comfortable density
- [ ] Border radius: 8px (buttons), 12-16px (cards)
- [ ] Warm Charcoal-based shadows
- [ ] Mobile-first, 16px minimum padding

### Component Standards
- [ ] Restaurant cards include: image, name, cuisine, price, rating, distance, CTA
- [ ] Primary buttons: Golden Hour fill + Charcoal text
- [ ] Secondary buttons: Chopped Kale fill + Heavy Cream text
- [ ] CTAs use action verbs: "Explore", "Discover", "Book Now"
- [ ] Food imagery is prominent
- [ ] Tags use Sage Butter background

### Brand Tone
- [ ] Feels friendly, welcoming, character-driven
- [ ] Enthusiastic but trustworthy voice
- [ ] Avoids overly technical language

---

## File Structure

```
taste-the-city-project/
├── DESIGN_MEMORY.md                     ← TTC brand standards (YOU ARE HERE)
├── design-and-refine/                   ← Plugin directory
│   ├── .claude-plugin/
│   │   └── plugin.json
│   ├── commands/
│   │   └── start.md                     ← Entry point
│   ├── skills/
│   │   └── design-lab/
│   │       ├── SKILL.md                 ← Workflow + brand locks
│   │       └── DESIGN_PRINCIPLES.md     ← Part 0: TTC overrides
│   ├── templates/
│   │   └── DESIGN_PLAN.template.md      ← TTC compliance checklist
│   └── hooks/
│       └── hooks.json
├── .claude-design/                      ← TEMPORARY (created during session)
│   ├── lab/
│   │   ├── variants/
│   │   │   ├── VariantA.tsx
│   │   │   ├── VariantB.tsx
│   │   │   └── ...
│   │   └── data/fixtures.ts
│   ├── design-brief.json
│   └── run-log.md
└── DESIGN_PLAN.md                       ← OUTPUT (after session)
```

**Note**: `.claude-design/` is **temporary** and auto-deleted after you finalize or cancel.

---

## Updating Brand Standards

### To Update Colors

Edit `DESIGN_MEMORY.md`:

```markdown
## Color

### Primary Palette

**Golden Hour (Accent Yellow/Gold)**
- Hex: `#D4AF37` ← Change this
- Use: Primary CTAs, active states
```

The plugin will automatically use the new color in all future sessions.

### To Update Typography

Edit `DESIGN_MEMORY.md`:

```markdown
## Typography

### Typefaces

**Instrument Serif** (Headlines & Display)
- Use: H1, H2, H3, restaurant names ← Edit usage here
```

### To Update Component Patterns

Edit `DESIGN_MEMORY.md`:

```markdown
### Restaurant Cards

**Must Include**:
- Food imagery ← Add or remove required elements
- Restaurant name
- Pricing tier
```

---

## Troubleshooting

### Plugin doesn't load brand standards

**Check:**
1. `DESIGN_MEMORY.md` is in project root (same level as `package.json`)
2. File name is exact: `DESIGN_MEMORY.md` (all caps, with underscore)

**Test:**
```bash
ls -la DESIGN_MEMORY.md
# Should show the file
```

### Variants aren't following brand colors

**Check:**
1. `DESIGN_MEMORY.md` color section has correct hex values
2. Run `/design-and-refine:start` again (plugin reads file at start)

### Plugin generates off-brand CTAs

**Check:**
1. `DESIGN_MEMORY.md` → "Do / Don't" section has CTA examples
2. Brand Tone section specifies language

---

## FAQ

### Do I need to fork the plugin repo?

**No!** The plugin is designed to be customized through configuration files:
- `DESIGN_MEMORY.md` (project-level brand standards)
- `DESIGN_PRINCIPLES.md` Part 0 (plugin-level TTC overrides)

Forking would create maintenance overhead. Instead, you get:
- ✅ TTC brand baked into plugin via config
- ✅ Automatic updates from main plugin repo
- ✅ Easy to switch between generic and TTC mode

### Can I use this for multiple TTC projects?

**Yes!** Just copy `DESIGN_MEMORY.md` to each project. Each project gets the same brand standards, but the plugin will adapt to:
- Each project's framework (Next.js, Vite, etc.)
- Each project's existing components
- Each project's specific Tailwind config or styling system

### What if I want to break brand rules?

**Option 1: Temporary override**
- Rename `DESIGN_MEMORY.md` to `DESIGN_MEMORY.md.backup` before running the plugin
- Plugin will generate variants without brand locks
- Rename back after session

**Option 2: Update DESIGN_MEMORY.md**
- Edit the brand standards to allow the new pattern
- Plugin will use updated standards going forward

**Option 3: Manual override**
- Let plugin generate variants with brand locks
- Manually edit the final component code after output

### How do I share brand updates across the team?

**Commit `DESIGN_MEMORY.md` to version control:**

```bash
git add DESIGN_MEMORY.md
git commit -m "Update TTC brand standards"
git push
```

Now all team members pulling the repo get the latest brand standards.

---

## Links & Resources

- **Web App**: https://tastings.tastethecity.ca/
- **Marketing Site**: https://www.tastethecity.ca/
- **Design Memory**: `DESIGN_MEMORY.md` (this repo)
- **Brand Guidelines**: TTC Brand Guide (Chopped Kale, Sage Butter, Heavy Cream, Tomato Paste, Golden Hour)

---

## Next Steps

1. **Test the setup**: Run `/design-and-refine:start Button` on a simple component
2. **Review output**: Check that `DESIGN_PLAN.md` includes TTC compliance checklist
3. **Verify brand locks**: All 5 variants should use TTC colors and fonts
4. **Customize further**: Update `DESIGN_MEMORY.md` with project-specific patterns as you discover them

---

**Questions?**
- Check `DESIGN_MEMORY.md` for brand standards
- Check `design-and-refine/skills/design-lab/DESIGN_PRINCIPLES.md` Part 0 for TTC overrides
- Check `design-and-refine/skills/design-lab/SKILL.md` for workflow details

---

**Last Updated**: 2026-01-18
**Version**: 1.0 (TTC Custom)
**Maintained By**: Taste the City Design Team
