# Smile Bone Marketing Website

Smile Bone Marketing is a static HTML marketing website for a marketing consultant with 25+ years of experience. The site consists of a main landing page and a blog section, built with pure HTML/CSS and deployed on Netlify.

Always reference these instructions first and fallback to search or bash commands only when you encounter unexpected information that does not match the info here.

## Working Effectively

### Bootstrap and Run the Website
- `cd /path/to/smilebone-marketing` - Navigate to the repository root
- `python3 -m http.server 8000` - Start local development server (serves instantly, no build required)
- Open `http://localhost:8000` in browser to view the website
- Access blog at `http://localhost:8000/blog/cold-email-vs-funnels.html`

### No Build System Required
- This is a static HTML website with NO build process
- No dependencies to install (no package.json, no npm install needed)
- Changes to HTML/CSS are immediately visible after browser refresh
- No compilation, bundling, or preprocessing steps required

### Testing and Validation
- **ALWAYS** test manually in a browser after making any changes
- Start local server: `python3 -m http.server 8000`
- **MANDATORY USER SCENARIOS** to test after changes:
  1. Navigate to main page (`http://localhost:8000`)
  2. Test navigation between main page and blog
  3. Test form functionality on blog page (fill all fields)
  4. Test responsive design by resizing browser window
  5. Verify all links and CTAs work correctly
  6. Test email links (`mailto:` addresses)

### Manual Validation Requirements
- **CRITICAL**: Always test the complete user journey manually
- Fill out the contact form on the blog page with realistic data
- Test navigation: Main page → Blog → Back to main page
- Verify all sections scroll correctly (Services, Experience, Results, Contact)
- Test mobile responsiveness by resizing browser window
- Ensure all email links (`hello@smilebonemarketing.com`, `gregryjleroux@gmail.com`) work

## Project Structure

### Key Files
```
/
├── index.html              # Main landing page (372 lines)
├── blog/
│   └── cold-email-vs-funnels.html  # Blog post (87 lines)
├── logo.png               # Company logo (738KB)
├── favicon-16x16.png      # 16x16 favicon
├── favicon-32x32.png      # 32x32 favicon
└── README.md              # Basic project description
```

### Main Page Sections (index.html)
- Header with navigation and logo
- Hero section with main value proposition
- "Why Experience Matters" section
- Services grid (5 service offerings)
- "How It Works" 4-step process
- Results statistics section
- Contact CTA section

### Blog Page Features
- Netlify form integration (`data-netlify="true"`)
- Responsive design with mobile breakpoints
- Email contact fallback option
- Clean typography and spacing

## Common Tasks

### Making Content Changes
- Edit HTML files directly - no preprocessing needed
- CSS is embedded in `<style>` tags within each HTML file
- Changes are visible immediately after browser refresh
- Always test in browser after making changes

### Testing Form Functionality
- Blog page has a Netlify contact form
- Form fields: name, email, company, industry, offer description
- Test form by filling all required fields
- Form uses POST method with Netlify handling
- **ALWAYS** test form submission flow manually

### Responsive Design Testing
- Website uses CSS Grid and Flexbox for responsive layouts
- Test breakpoints by resizing browser window
- Mobile breakpoint: max-width: 720px
- Verify grid layouts collapse properly on mobile
- Check navigation and CTAs remain functional on all screen sizes

## Deployment and Hosting

### Netlify Integration
- Site is deployed on Netlify platform
- Forms automatically handled by Netlify (`data-netlify="true"`)
- No custom deployment scripts required
- Static files served directly from repository

### No CI/CD Pipeline
- No GitHub Actions or build workflows
- No automated testing or linting
- Changes deploy directly when pushed to main branch
- Manual testing is the primary validation method

## Validation Checklist

Before completing any changes, ALWAYS verify:
- [ ] Local server starts without errors: `python3 -m http.server 8000`
- [ ] Main page loads correctly at `http://localhost:8000`
- [ ] Blog page loads correctly at `http://localhost:8000/blog/cold-email-vs-funnels.html`
- [ ] Navigation works: Main ↔ Blog
- [ ] All internal links function (Services, Experience, Results, Contact)
- [ ] Contact form can be filled with test data
- [ ] Email links open email client (`mailto:` links)
- [ ] Responsive design works on mobile viewport
- [ ] No broken images or assets
- [ ] Typography and spacing look correct

## Troubleshooting

### Common Issues
- **Forms not working**: Check `data-netlify="true"` attribute is present
- **Images not loading**: Verify image paths are relative to HTML file
- **CSS not applying**: Check for syntax errors in embedded `<style>` tags
- **Links broken**: Ensure relative paths are correct (`../index.html` from blog)

### Development Server Issues
- If port 8000 is busy: Use `python3 -m http.server 8001` (or another port)
- If Python not available: Try `php -S localhost:8000` or install Python
- Server serves files instantly - no build time or delays expected

## Content Guidelines

### Target Audience
- Small business owners seeking marketing help
- Entrepreneurs needing lead generation
- Companies wanting proven marketing strategies

### Key Messages
- 25+ years of marketing experience
- Focus on practical, results-driven approaches
- Specializes in cold email over complex funnels
- Emphasis on ROI and measurable results

### Brand Voice
- Professional but approachable
- Direct and no-nonsense
- Experience-backed confidence
- Results-focused messaging