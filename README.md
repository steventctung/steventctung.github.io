# Steven T.C. Tung - Academic Portfolio Website

This is a Jekyll-powered academic portfolio website designed for easy maintenance and content updates. The site is built with an academic minimal aesthetic and optimized for GitHub Pages hosting.

## Quick Start

1. **Repository Setup**: Create a new repository named `steventctung.github.io`
2. **Upload Files**: Upload all files from this directory to your repository
3. **Enable GitHub Pages**: Go to Settings → Pages → Source: GitHub Actions
4. **Automatic Deployment**: The GitHub Actions workflow will automatically build and deploy your site
5. **Wait**: Your site will be available at `https://steventctung.github.io` within a few minutes

## Website Structure

```
├── _config.yml          # Site configuration
├── _data/               # Content data files
│   ├── research.yml     # Research projects
│   ├── publications.yml # Publications & presentations
│   └── notes.yml        # Mathematical notes
├── _layouts/            # Page templates
├── assets/              # Static files
│   ├── css/            # Stylesheets
│   ├── pdfs/           # PDF files (notes, CV, papers)
│   └── images/         # Images and photos
├── index.md            # Homepage
├── research.md         # Research page
├── publications.md     # Publications page
├── notes.md           # Notes page
├── cv.md              # CV page
└── contact.md         # Contact page
```

## How to Update Content

### 1. Adding New Research Projects

Edit `_data/research.yml`:

```yaml
- title: "Your Research Project Title"
  advisor: "Prof. Advisor Name"
  period: "Start Date - End Date"
  status: "Ongoing/Completed"
  description: "Brief description of your research..."
  skills:
    - "Skill 1"
    - "Skill 2"
  links:
    - title: "GitHub"
      url: "https://github.com/username/repo"
```

### 2. Adding Publications

Edit `_data/publications.yml`:

```yaml
- type: "journal"  # or "preprint", "presentation", "thesis"
  title: "Paper Title"
  authors: ["Steven T.C. Tung", "Co-author"]
  journal: "Journal Name"
  year: "2024"
  abstract: "Paper abstract..."
  links:
    - title: "DOI"
      url: "https://doi.org/example"
```

### 3. Adding Mathematical Notes

**Step 1**: Upload your PDF to `assets/pdfs/`

**Step 2**: Edit `_data/notes.yml`:

```yaml
- title: "Note Title"
  topic: "Subject Area"
  date: "2024-MM-DD"  # Use YYYY-MM-DD format
  course: "Course Name (optional)"
  description: "Brief description"
  pages: 25
  pdf: "filename.pdf"
```

The notes page will automatically organize them by topic and list chronologically!

### 4. Updating Personal Information

**Homepage** (`index.md`):
- Edit the intro text and recent updates section
- Add your profile photo to `assets/images/profile.jpg` and uncomment the image line

**Contact Page** (`contact.md`):
- Update email, office hours, and contact information
- Update ORCID when available

**CV Page** (`cv.md`):
- Update the CV content directly in the file
- Upload your CV PDF to `assets/pdfs/steven_tung_cv.pdf`

### 5. Site Configuration

Edit `_config.yml` to update:
- Site title and description
- Email address
- GitHub username
- Navigation menu

## Managing PDF Files

1. **Upload Location**: Place all PDFs in `assets/pdfs/`
2. **Naming Convention**: Use descriptive, lowercase names with underscores
   - `real_analysis_notes.pdf`
   - `Notes 1.pdf`
3. **File Sizes**: Keep PDFs under 25MB for faster loading

## Customizing the Design

### Colors
The main colors are defined in `assets/css/main.css`:
- Primary: `#34495e` (dark blue-gray)
- Secondary: `#2c3e50` (darker blue-gray)
- Background: `#f8f9fa` (light gray)

### Fonts
- Headings: Helvetica Neue, Arial (clean, modern)
- Body text: Georgia, Times New Roman (academic, readable)

### Layout
The design is responsive and works on all devices. Maximum content width is 800px for optimal readability.

## Advanced Customization

### Adding New Pages
1. Create a new `.md` file in the root directory
2. Add front matter:
   ```yaml
   ---
   layout: page
   title: "Page Title"
   ---
   ```
3. Add the page to navigation in `_config.yml`

### Creating Individual Note Pages
Instead of just linking to PDFs, you can create dedicated pages:

1. Create a file in `_notes/` directory
2. Use the `note` layout:
   ```yaml
   ---
   layout: note
   title: "Note Title"
   topic: "Subject"
   date: 2024-01-01
   pdf: "filename.pdf"
   ---

   Additional content here...
   ```

## GitHub Pages Deployment

### Automatic Deployment with GitHub Actions
- The site uses GitHub Actions for modern, reliable deployment
- Every time you push changes to the main branch, the workflow automatically:
  1. Sets up Ruby and Jekyll
  2. Installs dependencies
  3. Builds the site
  4. Deploys to GitHub Pages
- Changes typically appear within 2-5 minutes
- You can monitor the build process in the "Actions" tab of your repository

### Custom Domain (Optional)
1. Add a `CNAME` file with your domain name
2. Configure DNS settings with your domain provider
3. Enable HTTPS in repository settings

## Troubleshooting

### Site Not Loading
1. Check that repository is named `steventctung.github.io`
2. Verify GitHub Pages is enabled in repository settings
3. Check for YAML syntax errors in your files

### Content Not Updating
1. Ensure proper YAML formatting (spaces, not tabs)
2. Check that file names match exactly in YAML files
3. Wait 5 minutes for GitHub to rebuild the site

### PDF Links Not Working
1. Verify PDF files are in `assets/pdfs/` directory
2. Check that filenames in YAML match exactly (case-sensitive)
3. Ensure PDF files are committed to the repository

## Mathematical Content Best Practices

### LaTeX to PDF Workflow
1. Write your notes in LaTeX
2. Compile to PDF
3. Name descriptively (e.g., `topology_chapter_3_notes.pdf`)
4. Upload to `assets/pdfs/`
5. Add entry to `_data/notes.yml`

### Note Organization
- Use consistent topic names (e.g., "Real Analysis", not "real analysis" or "Real analysis")
- Include page counts for user reference
- Write clear, concise descriptions
- Use proper date formatting (YYYY-MM-DD)

## Getting Help

If you encounter issues:
1. Check this README first
2. Review the example entries in the YAML files
3. Ensure all syntax is correct (YAML is sensitive to formatting)
4. Contact your friend who set up the site for technical help

## Regular Maintenance

### Monthly Tasks
- [ ] Update CV page with new achievements
- [ ] Add new notes from completed courses
- [ ] Update research project status
- [ ] Check that all PDF links work

### Semester Tasks
- [ ] Upload PDF version of updated CV
- [ ] Add new course notes
- [ ] Update research project descriptions
- [ ] Review and update contact information

---

**Remember**: This website is designed to be easy to maintain. Most updates only require editing simple text files and uploading PDFs. The site will automatically handle the formatting and organization!

**Live Site**: https://steventctung.github.io