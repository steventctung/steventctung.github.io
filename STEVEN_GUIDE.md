# Website Update Guide

This is a simplified guide for updating your website. Your friend has set up everything to be as easy as possible.

## Most Common Tasks

### Adding a New Math Note

**What you need:**
- Your PDF file
- Title of the note
- Subject/topic
- Date you completed it

**Steps:**
1. Go to your repository on GitHub
2. Click on `assets` → `pdfs` → `Add file` → `Upload files`
3. Upload your PDF (name it something like `calculus_chapter_5.pdf`)
4. Go back to the main repository page
5. Click on `_data` → `notes.yml` → Edit (pencil icon)
6. Add your note at the top of the file:

```yaml
- title: "Your Note Title"
  topic: "Subject Name"
  date: "2024-10-17"  # Today's date in YYYY-MM-DD format
  course: "Math 311 - Course Name"
  description: "What the note covers"
  pages: 25  # Number of pages in your PDF
  pdf: "your_filename.pdf"  # Exact name of the file you uploaded
```

7. Click "Commit changes" at the bottom
8. Wait 5 minutes - your note will appear on the website!

### Updating Your About Section

1. Go to `index.md` in your repository
2. Click the edit button (pencil icon)
3. Update the text in the intro section
4. Add new items to "Recent Updates" section
5. Commit changes

### Adding Research Projects

1. Go to `_data` → `research.yml`
2. Click edit
3. Add your project following the example format
4. Commit changes

## Quick Reference

### Your Website Sections

- **About** (`index.md`) - Your introduction and recent updates
- **Research** - Automatically shows projects from `_data/research.yml`
- **Publications** - Shows items from `_data/publications.yml`
- **Notes** - Shows items from `_data/notes.yml`
- **CV** (`cv.md`) - Your curriculum vitae
- **Contact** (`contact.md`) - Your contact information

### File Locations

- **PDFs go here**: `assets/pdfs/`
- **Photos go here**: `assets/images/`
- **Notes data**: `_data/notes.yml`
- **Research data**: `_data/research.yml`
- **Publications data**: `_data/publications.yml`

## Important Rules

1. **File names**: Use lowercase letters, numbers, and underscores only
   - `topology_notes.pdf`
   - `Topology Notes.pdf`

2. **Dates**: Always use YYYY-MM-DD format
   - `2024-10-17`
   - `October 17, 2024`

3. **YAML formatting**: Be very careful with spaces and indentation
   - Use spaces, not tabs
   - Keep the same indentation as examples

4. **Wait time**: After making changes, wait 5 minutes for the website to update

## If Something Breaks

1. **Check your YAML formatting** - make sure spaces and indentation match the examples
2. **Check file names** - make sure they match exactly between your YAML and uploaded files
3. **Wait 5 minutes** - sometimes changes take time to appear
4. **Contact your friend** - they can help fix any technical issues

## Checking Your Website

Your website is live at: **https://steventctung.github.io**

After making changes:
1. Wait 5 minutes
2. Refresh the page
3. Check that your changes appear correctly

## Pro Tips

- **Organize your notes by topic** - use consistent topic names like "Real Analysis", "Partial Differential Equations"
- **Write good descriptions** - help visitors understand what each note covers
- **Keep PDFs under 25MB** - larger files slow down your website
- **Update regularly** - add notes as you complete them, don't wait until the end of the semester

---

**Remember**: The website is designed to be simple. Most of the time, you're just:
1. Uploading a PDF
2. Adding a few lines to a YAML file
3. Waiting for the magic to happen!

Your friend has made it so the website automatically organizes everything beautifully.