# World Language Map - Specification

## Project Overview
- **Project name**: World Language Map
- **Type**: Interactive single-page web application
- **Core functionality**: Visualize world languages by country with interactive exploration
- **Target users**: Language enthusiasts, students, travelers, anyone curious about world languages

## UI/UX Specification

### Layout Structure
- **Header**: Title bar with app name and language filter
- **Main Area**: Full-screen interactive world map
- **Sidebar**: Sliding panel showing country/language details
- **Footer**: Language statistics summary

### Responsive Breakpoints
- Desktop: Full experience with sidebar
- Tablet/Mobile: Bottom sheet for details instead of sidebar

### Visual Design

#### Color Palette
- **Background**: `#0a0f1a` (deep ocean night)
- **Map ocean**: `#0d1929` (dark blue)
- **Map land**: `#1e3a5f` (muted navy)
- **Map hover**: `#2d5a8a` (bright navy)
- **Accent**: `#00d4aa` (teal glow)
- **Secondary accent**: `#ff6b9d` (coral pink)
- **Text primary**: `#e8f0ff` (ice white)
- **Text secondary**: `#7a8fa3` (slate gray)
- **Panel background**: `rgba(15, 25, 45, 0.95)`

#### Language Category Colors (by language family)
- Indo-European: `#4ecdc4` (teal)
- Sino-Tibetan: `#ff6b6b` (coral)
- Afro-Asiatic: `#ffd93d` (golden)
- Niger-Congo: `#6bcb77` (green)
- Austronesian: `#9b59b6` (purple)
- Dravidian: `#e74c3c` (red)
- Turkic: `#3498db` (blue)
- Japonic: `#f39c12` (orange)
- Other: `#95a5a6` (gray)

#### Typography
- **Font family**: "Outfit" (Google Fonts) - modern geometric sans-serif
- **Title**: 28px, weight 700
- **Body**: 14px, weight 400
- **Stats numbers**: 24px, weight 600

#### Visual Effects
- Glowing country borders on hover (box-shadow with accent color)
- Smooth transitions (0.3s ease)
- Subtle grid pattern overlay on ocean
- Particle effect background (subtle floating dots)

### Components

#### World Map (SVG-based)
- Simplified world countries using D3.js and TopoJSON
- Each country colored by primary language family
- Hover: brighten + show tooltip with country name + language
- Click: open detail panel

#### Tooltip
- Country name (bold)
- Primary language
- Language family
- Number of speakers (if available)

#### Detail Side Panel
- Country flag emoji + name
- Official language(s)
- Language family
- Dialects count
- Interesting fact
- Neighboring countries' languages
- Close button

#### Filter Bar
- Search country
- Filter by language family (dropdown)
- Toggle: show language names vs country names

#### Statistics Footer
- Total countries shown
- Most common language family
- Total languages represented

## Functionality Specification

### Core Features
1. **Interactive Map**: Pan and zoom world map
2. **Country Hover**: Quick info tooltip
3. **Country Click**: Detailed side panel
4. **Language Filter**: Filter countries by language family
5. **Country Search**: Search for specific country
6. **Statistics**: Live count of languages displayed

### Data
- Include top 50+ countries with their official languages
- Map language to language family
- Include country ISO codes for map matching

### User Interactions
- Hover country → show tooltip
- Click country → open detail panel
- Click outside panel → close panel
- Type in search → filter countries
- Select language family → highlight those countries

## Acceptance Criteria
1. Map renders with all major countries visible
2. Countries are colored by language family
3. Hovering shows tooltip with language info
4. Clicking opens detailed panel
5. Filter works correctly
6. Search finds countries
7. Responsive on mobile
8. No console errors
9. Smooth animations throughout
