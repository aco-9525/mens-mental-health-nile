# Men's Mental Health Support Website

## Overview
A mental health support website specifically designed for male students, providing crisis resources, emotional support tools, school staff directory, and mental health information. The site uses direct, relatable language that resonates with young men and avoids clinical jargon.

## Purpose
- Provide immediate access to crisis hotlines (988, Kids Help Phone)
- Connect students with school support staff
- Offer practical coping strategies for common emotions (anger, sadness, anxiety, loneliness)
- Address stress from school, sports, family, and relationships
- Provide mental health resources and FAQs

## Technology Stack
- **Frontend**: React + TypeScript, Wouter (routing), TanStack Query (data fetching)
- **Backend**: Express.js, in-memory storage
- **UI**: Shadcn UI components, Tailwind CSS
- **Design**: Clean, professional, masculine restraint - prioritizes trust and clarity

## Project Structure

### Pages
- **Home** (`/`) - Hero message "You're allowed to ask for help" with three navigation cards
- **I Need Help Now** (`/help-now`) - Crisis information, 988 hotline, Kids Help Phone, safety steps
- **How I'm Feeling** (`/how-feeling`) - Four emotional states with coping strategies
- **Stress/School/Life** (`/stress`) - Academic pressure, sports, family, relationships
- **Support at School** (`/support`) - Staff directory with real school contacts
- **Resources** (`/resources`) - Tabbed resources (crisis, apps, school, community)
- **FAQ** (`/faq`) - Common questions about mental health
- **Admin** (`/admin`) - Content management for staff and resources

### Key Features
1. **Crisis Information Always Accessible** - 988 and Kids Help Phone prominently displayed
2. **School Staff Directory** - Editable directory of counselors, teachers, youth workers
3. **Resource Management** - Categorized mental health resources
4. **Privacy Statement** - Clear confidentiality information on Support page
5. **Mobile-First Design** - Students access privately on phones
6. **Admin Panel** - School staff can update contact information and resources

### API Endpoints

#### Staff Members
- `GET /api/staff` - Get all staff members
- `GET /api/staff/:id` - Get single staff member
- `POST /api/staff` - Create new staff member
- `PUT /api/staff/:id` - Update staff member
- `DELETE /api/staff/:id` - Delete staff member

#### Resources
- `GET /api/resources` - Get all resources (optional ?category= filter)
- `GET /api/resources/:id` - Get single resource
- `POST /api/resources` - Create new resource
- `PUT /api/resources/:id` - Update resource
- `DELETE /api/resources/:id` - Delete resource

#### FAQs
- `GET /api/faqs` - Get all FAQs
- `GET /api/faqs/:id` - Get single FAQ
- `POST /api/faqs` - Create new FAQ
- `PUT /api/faqs/:id` - Update FAQ
- `DELETE /api/faqs/:id` - Delete FAQ

### Data Models

**StaffMember**
- name: string
- role: string (e.g., "Mental Health Contact Teacher")
- room: string (e.g., "Room 214")
- hours: string (e.g., "Before school, Lunch, After school")
- description: string (what they help with)

**Resource**
- category: string (crisis, apps, school, community)
- name: string
- contact: string (phone number, URL, or instruction)
- description: string
- availability: string (e.g., "24/7", "Weekdays 9-5")

**FAQ**
- question: string
- answer: string

## Design Philosophy

### Tone & Language
- Direct, no-BS communication ("You're not okay" vs "experiencing distress")
- Avoids clinical/medical terminology unless necessary
- Acknowledges male-specific barriers ("Guys click more if it feels made for them")
- Normalizes asking for help ("You are allowed to ask for help")

### Visual Design
- Professional legitimacy (school branding, staff names)
- Clean typography (Inter font)
- Masculine restraint (no overly soft aesthetics)
- Crisis information uses red accent for urgency
- Mobile-optimized touch targets

### Trust Markers
- Real staff names and locations (not generic)
- Clear privacy policy
- School affiliation in header
- No ads or external tracking
- Crisis disclaimer on every page (footer)

## Customization for Schools

Schools should customize:
1. **Staff Directory** - Add real names, rooms, hours via admin panel
2. **School Name** - Update in Header component and page titles
3. **Local Resources** - Add community-specific resources via admin panel
4. **Colors** - Optional: adjust primary color in `index.css` for school branding

## Important Notes

- Crisis hotlines (988, Kids Help Phone 686868) are Canada-specific
- Site includes disclaimer: "Not monitored 24/7"
- Privacy statement clarifies mandatory reporting for danger situations
- All content designed to reduce stigma around male mental health
- Admin panel accessible at `/admin` for content management

## Future Enhancements
- Anonymous mood check-in tool
- QR code generator for posters
- Analytics dashboard for school administration
- Database persistence (currently in-memory)
- User authentication for admin panel
