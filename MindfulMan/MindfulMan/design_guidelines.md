# Design Guidelines: Men's Mental Health Support Website

## Design Approach

**Selected Framework**: Healthcare-Informed Design System
This platform requires a trust-building, utility-first approach that prioritizes clarity, accessibility, and immediate access to critical information. Drawing from institutional healthcare design patterns with warmth and approachability for young male students.

**Core Principles**:
- Direct and unambiguous: No decorative elements that obscure information
- Professional legitimacy: Institutional feel that students will trust
- Mobile-first: Students access this privately on phones
- Masculine restraint: Clean, structured, no overly soft aesthetics
- Crisis-ready: Emergency information always prominent

---

## Typography

**Font Selection**: 
- Primary: Inter (via Google Fonts CDN) - clean, professional, excellent readability
- Headings: Inter SemiBold (600) and Bold (700)
- Body: Inter Regular (400) and Medium (500)

**Type Scale**:
- Hero/Page Titles: text-4xl md:text-5xl font-bold (48-60px)
- Section Headings: text-2xl md:text-3xl font-semibold (30-36px)
- Subsection Titles: text-xl font-semibold (24px)
- Card Titles: text-lg font-semibold (20px)
- Body Text: text-base leading-relaxed (16px, 1.75 line-height)
- Small/Meta Text: text-sm (14px)
- Crisis Numbers: text-3xl font-bold for maximum visibility

**Hierarchy Rules**:
- Crisis information uses largest, boldest typography
- Headers are concise statements, not flowery prose
- Body text optimized for scanning (short paragraphs, bullet points)

---

## Layout System

**Spacing Primitives**: 
Consistently use Tailwind units: **4, 6, 8, 12, 16, 20** (1rem = 4 units)
- Micro spacing (elements): 4, 6
- Component padding: 8, 12
- Section spacing: 16, 20
- Page margins: 8 (mobile), 12-16 (desktop)

**Grid Structure**:
- Container: max-w-7xl mx-auto px-6 md:px-8
- Content sections: max-w-4xl for optimal reading width
- Card grids: grid-cols-1 md:grid-cols-2 lg:grid-cols-3 with gap-6 md:gap-8

**Viewport Strategy**:
- No forced 100vh sections - natural content flow
- Sections use py-12 md:py-16 lg:py-20 for vertical rhythm
- Mobile: single column, generous touch targets (min 44px height)
- Desktop: max 3-column layouts for feature cards

---

## Component Library

### Navigation
- Sticky header with school name/logo on left
- Horizontal navigation menu (desktop): text-base font-medium links with hover underline
- Mobile: Hamburger menu (Heroicons: Bars3Icon) with slide-in drawer
- Emergency banner (optional): fixed top bar with red background for 988 crisis line - dismissible

### Homepage Hero
- **No large background image** - clean header section with solid background
- Centered layout with max-w-3xl
- Hero title: "You're allowed to ask for help."
- Subtitle: "Support and resources for male students at [School Name]"
- Quote section below hero: Large blockquote styling with subtle border-left accent
- Three-card grid below for primary navigation (Crisis, FAQ, School Support)

### Card Components
**Primary Navigation Cards** (Homepage):
- Border-based cards with hover lift effect (shadow-sm hover:shadow-md)
- Padding: p-8
- Icon at top (Heroicons: PhoneIcon, QuestionMarkCircleIcon, UserGroupIcon)
- Title: text-xl font-semibold
- Description: text-base
- No background images - solid backgrounds with subtle borders

**Feeling State Cards** (How I'm Feeling page):
- Horizontal layout on desktop: icon/emoji left, content right
- Compact padding: p-6
- Title in bold, symptoms in regular text
- Action steps in bullet list
- "Talk to:" contact at bottom

**Resource Cards**:
- Dense information cards with clear hierarchy
- Service name, contact method (large), hours, description
- Border radius: rounded-lg consistently

### Crisis Information Sections
- Distinct visual treatment with border-l-4 accent
- Red or amber border for urgency signals
- Large, bold phone numbers: text-3xl md:text-4xl font-bold
- Clear "Call" or "Text" labels
- Background: slightly elevated with subtle shadow

### Forms (Admin Panel)
- Input fields: border-2 with focus:ring-2 states
- Labels above inputs: text-sm font-medium
- Generous padding: px-4 py-3
- Full-width on mobile: w-full
- Submit buttons: primary style, full-width mobile, auto desktop

### Buttons
- Primary: px-6 py-3 text-base font-semibold rounded-md
- Large (crisis actions): px-8 py-4 text-lg
- Icon buttons: p-2 rounded-full for mobile menu
- States: solid backgrounds with hover brightness change
- No gradient backgrounds - solid fills only

### Footer
- Comprehensive footer on all pages
- Three-column layout (desktop): Crisis Info | Quick Links | Contact
- Single column (mobile) with clear sections
- Emergency disclaimer in prominent box at top of footer
- Minimal styling: text-sm with clear link hierarchy

---

## Page-Specific Layouts

### I Need Help Now
- Large crisis hotlines at top (988, Kids Help Phone)
- Chunked information: "If you are in danger" / "Talk to someone now" / "Before you act"
- No multi-column - single column for clarity
- Action-oriented bullets with checkmark icons
- Consistent visual weight throughout - all sections equally important

### How I'm Feeling  
- Four emotional state sections (Angry, Sad/Numb, Anxious, Lonely)
- Each section: 2-column on desktop (feeling left, coping right)
- Call-to-action button at bottom: "Talk to someone at school"
- Clean separation between sections with borders

### Support at School
- Staff directory with structured cards
- Each staff card: Name (large), Role (medium), Room/Location, Hours, Brief description
- Privacy notice in highlighted box
- Searchable/filterable if staff count is high (admin feature)

### Resources
- Organized accordion or tabbed sections: Crisis | Apps | School | Community
- Each resource: Name, contact/link, description, availability
- Links open in new tabs with external link icon (Heroicons: ArrowTopRightOnSquareIcon)

### FAQ
- Accordion-style Q&A (open one at a time)
- Question in bold, answer in regular weight
- Generous line-height for readability
- No numbering - questions stand alone

---

## Images

**Hero Section**: No large hero image. Use clean, solid background with focused typography.

**Supporting Imagery** (if needed):
- Small, abstract illustrations for emotional state sections (minimalist line art)
- Icon-based rather than photographic
- Avoid stock photos of smiling students - feels inauthentic
- School logo in header for legitimacy

**Image Specifications**:
- Format: SVG for icons, WebP for any photos
- Loading: lazy loading for below-fold images
- Alt text: descriptive for accessibility

---

## Accessibility & Interaction

- WCAG AA compliance minimum for text contrast
- Focus indicators: ring-2 ring-offset-2 on all interactive elements
- Skip-to-content link for screen readers
- Form labels always visible (not placeholder-only)
- Touch targets: minimum 44px for mobile
- Keyboard navigation: full site navigable without mouse
- No animation on page load - instant content visibility
- Reduced motion support: prefers-reduced-motion respected

---

## Mobile Optimization

- Navigation: Hamburger menu, full-screen drawer
- Crisis numbers: one-tap to call (tel: links)
- Text sizing: 16px minimum to prevent iOS zoom
- Forms: appropriate input types (tel, email)
- Cards stack to single column
- Footer condenses to single column with accordions for link groups

---

## Trust & Professionalism Markers

- School name/logo prominent in header
- Staff photos (optional) with real names and credentials
- Consistent terminology (no slang in UI labels)
- Clear privacy statements
- Professional domain (school-hosted ideal)
- No ads, no external tracking scripts
- Last updated date in footer

This design prioritizes **clarity, trust, and immediate access to help** over visual creativity, appropriate for a life-supporting mental health resource.