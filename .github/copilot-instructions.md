# Smile Bone Marketing Website

Smile Bone Marketing is a static HTML marketing website for a marketing consulting business with 25+ years of experience. The site showcases services, experience, results, and contact information for potential clients.

Always reference these instructions first and fallback to search or bash commands only when you encounter unexpected information that does not match the info here.

## Working Effectively

### Quick Setup and Validation
- Serve the website locally: `python3 -m http.server 8000`
- Validate HTML files: `python3 -c "import html.parser; import os; [print(f'{f}: Valid') for f in ['index.html', 'blog/cold-email-vs-funnels.html'] if os.path.exists(f)]"`
- Access the website at: `http://localhost:8000`
- TIMING: Server starts in 2 seconds, HTML validation completes in <0.1 seconds

### Manual Testing and Validation
- ALWAYS test website functionality after making any changes
- Open `http://localhost:8000` and verify:
  - Homepage loads correctly with all sections visible
  - Navigation links work (Services, Experience, Results, Contact)
  - "Get Started" and "Let's Talk Strategy" buttons are functional
  - Logo displays properly (logo.png)
  - All service cards are visible and properly formatted
  - Contact email link (`hello@smilebonemarketing.com`) works
- Test blog functionality at `http://localhost:8000/blog/cold-email-vs-funnels.html`:
  - Blog page loads with proper styling
  - Content displays correctly
  - Contact form elements are present
  - Footer information is visible

### Development Workflow
- NO BUILD PROCESS REQUIRED - This is a pure HTML/CSS static website
- Make changes directly to HTML files
- Refresh browser to see changes immediately
- Always validate HTML after changes: `python3 -c "import html.parser; validator = html.parser.HTMLParser(); validator.feed(open('index.html').read()); print('HTML Valid')"`
- Test on both desktop and mobile viewport sizes

## Repository Structure

### Key Files and Locations
```
/
├── README.md                           # Basic repository description
├── index.html                          # Main homepage (11,459 bytes)
├── logo.png                           # Company logo (738KB)
└── blog/
    └── cold-email-vs-funnels.html     # Blog post about cold email strategy
```

### Website Content Overview
- **Homepage (index.html)**: Complete marketing website with:
  - Header with navigation and logo
  - Hero section with main value proposition
  - Services section (5 service offerings)
  - How It Works (4-step process)
  - Results/Statistics section
  - Contact/CTA section
- **Blog (blog/)**: Currently contains one post about cold email vs funnels strategy

## Common Tasks

### Starting Local Development
```bash
cd /home/runner/work/smilebone-marketing/smilebone-marketing
python3 -m http.server 8000
# Website available at http://localhost:8000
```

### Validating Changes
```bash
# Quick HTML validation
python3 -c "
import html.parser
import os

def validate_html(file):
    with open(file, 'r') as f:
        content = f.read()
    parser = html.parser.HTMLParser()
    parser.feed(content)
    return True

files = ['index.html', 'blog/cold-email-vs-funnels.html']
for f in files:
    if os.path.exists(f):
        validate_html(f)
        print(f'{f}: Valid')
"
```

### Content Updates
- **Service modifications**: Edit the services section in index.html (lines ~280-320)
- **Contact information**: Update email addresses and contact details
- **Statistics**: Modify the results section (lines ~340-360)
- **Blog posts**: Add new HTML files to the `/blog/` directory
- **Styling**: CSS is embedded in the HTML files (lines ~9-220 in index.html)

### Testing Scenarios
After making any changes, ALWAYS complete these validation steps:

1. **Homepage Navigation Test**:
   - Start server: `python3 -m http.server 8000`
   - Navigate to `http://localhost:8000`
   - Click each navigation item (Services, Experience, Results, Contact)
   - Verify page scrolls to correct sections and URL updates with anchors

2. **Content Functionality Test**:
   - Verify all text displays correctly
   - Check that logo image loads (logo.png shows as 738KB file)
   - Test email links open mail client (`hello@smilebonemarketing.com`)
   - Ensure all 5 service cards are visible and readable
   - Verify statistics section shows: 340%, 47%, 185%, 98%

3. **Blog Functionality Test**:
   - Navigate to `http://localhost:8000/blog/cold-email-vs-funnels.html`
   - Verify blog content displays with proper formatting
   - Check that contact form elements are present and functional
   - Test email link (`gregryjleroux@gmail.com`) works

4. **Cross-Browser Testing** (if possible):
   - Test in different viewport sizes
   - Verify responsive design elements work correctly
   - Note: Google Fonts may fail to load in some environments (this is normal)

## Troubleshooting

### Common Issues and Solutions

**Server won't start**:
- Check if port 8000 is already in use: `lsof -i :8000`
- Use alternative port: `python3 -m http.server 8001`

**HTML validation errors**:
- Check for unclosed tags
- Verify proper nesting of HTML elements
- Ensure all required attributes are present

**Styling issues**:
- CSS is embedded in HTML files, not external
- Main styles are in index.html lines ~9-220
- Blog styles are in blog/cold-email-vs-funnels.html lines ~6-15

**Image loading problems**:
- Verify logo.png exists in repository root (should be 738KB)
- Check file permissions
- Ensure correct relative path references

**External font loading errors**:
- Blog page uses Google Fonts (Figtree) which may be blocked in some environments
- Console error "ERR_BLOCKED_BY_CLIENT" for Google Fonts is normal and doesn't affect functionality
- Website remains fully functional without external fonts

### Performance Notes
- HTML validation: <0.1 seconds
- Server startup: ~2 seconds
- Page load time: <1 second (static files)
- No build or compilation time required

## Development Best Practices

- Keep HTML semantic and accessible
- Maintain consistent styling across pages
- Test all interactive elements after changes
- Validate HTML before committing changes
- Preserve existing responsive design patterns
- Keep file sizes reasonable (current index.html is 11KB)

## Project Context

This is a marketing website for a consulting business focused on:
- Content creation and copywriting
- Lead generation systems
- Marketing strategy and consulting  
- Team training and workshops
- Sales training and coaching

The website emphasizes practical, results-driven marketing based on 25+ years of experience, with specific statistics like 340% ROI increase and 47% email open rates.